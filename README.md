# bun-pty

[![NPM Version](https://img.shields.io/npm/v/bun-pty.svg)](https://www.npmjs.com/package/bun-pty)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Bun Compatible](https://img.shields.io/badge/Bun-%E2%89%A51.0.0-black)](https://bun.sh)

A cross-platform pseudo-terminal (PTY) implementation for Bun, powered by Rust's portable-pty library and Bun's FFI capabilities.

## 🔧 Fork Improvements

This fork includes critical fixes for argument handling:

- **Fixed Quote Problem**: Properly escapes arguments containing spaces and special characters using POSIX-style single-quote escaping
- **Improved shell_words Compatibility**: Arguments are now correctly tokenized on the Rust side, preventing issues with commands that contain spaces or quotes
- **Preserves Original Behavior**: The fix is transparent and doesn't change the API - your existing code will work better automatically

## 🚀 Features

- **Cross-platform** - Works on macOS, Linux, and Windows
- **Simple API** - Clean Promise-based API similar to node-pty
- **Type-safe** - Complete TypeScript definitions included
- **Efficient** - Rust backend with proper error handling and multithreading
- **Zero dependencies** - No external JavaScript dependencies required
- **Modern** - Built specifically for Bun using its FFI capabilities

## 📦 Installation

```bash
bun add @snomiao/bun-pty
```

## ⚙️ Requirements

- **Bun** 1.0.0 or higher
- **Rust** is only needed if you're building from source (the npm package includes pre-built binaries)

## 📋 Platform Support

| Platform | Status | Notes |
|----------|--------|-------|
| macOS    | ✅     | Fully supported |
| Linux    | ✅     | Fully supported |
| Windows  | ✅     | Fully supported |

## 🚦 Usage

### Basic Example

```typescript
import { spawn } from "@snomiao/bun-pty";

// Create a new terminal
const terminal = spawn("bash", [], {
  name: "xterm-256color",
  cols: 80,
  rows: 24
});

// Handle data from the terminal
terminal.onData((data) => {
  console.log("Received:", data);
});

// Handle terminal exit
terminal.onExit(({ exitCode, signal }) => {
  console.log(`Process exited with code ${exitCode} and signal ${signal}`);
});

// Write to the terminal
terminal.write("echo Hello from Bun PTY\n");

// Resize the terminal
terminal.resize(100, 40);

// Kill the process when done
setTimeout(() => {
  terminal.kill();
}, 5000);
```

### Arguments with Spaces and Special Characters

This fork fixes a critical issue where arguments containing spaces or quotes were incorrectly tokenized. The fix is automatic and transparent:

```typescript
import { spawn } from "@snomiao/bun-pty";

// These commands now work correctly:
const terminal1 = spawn("echo", ["hello world", "with spaces"]);
const terminal2 = spawn("bash", ["-c", "echo 'quoted command'"]);
const terminal3 = spawn("ls", ["/path/with spaces/file.txt"]);

// Previously, arguments with spaces would be split incorrectly
// Now they're properly escaped for the Rust backend
```

The fix uses POSIX-style single-quote escaping internally, so `"hello world"` becomes `'hello world'` when passed to the Rust side, ensuring proper argument boundaries.

### TypeScript Usage

The library includes complete TypeScript definitions. Here's how to use it with full type safety:

```typescript
import { spawn } from "@snomiao/bun-pty";
import type { IPty, IExitEvent, IPtyForkOptions } from "@snomiao/bun-pty";

// Create typed options
const options: IPtyForkOptions = {
  name: "xterm-256color",
  cols: 100,
  rows: 30,
  cwd: process.cwd()
};

// Create a terminal with proper typing
const terminal: IPty = spawn("bash", [], options);

// Typed event handlers
const dataHandler = terminal.onData((data: string) => {
  process.stdout.write(data);
});

const exitHandler = terminal.onExit((event: IExitEvent) => {
  console.log(`Process exited with code: ${event.exitCode}`);
});

// Clean up when done
dataHandler.dispose();
exitHandler.dispose();
```

### Interactive Shell Example

```typescript
import { spawn } from "@snomiao/bun-pty";
import { createInterface } from "node:readline";

// Create a PTY running bash
const pty = spawn("bash", [], {
  name: "xterm-256color",
  cwd: process.cwd()
});

// Forward PTY output to stdout
pty.onData((data) => {
  process.stdout.write(data);
});

// Send user input to the PTY
process.stdin.on("data", (data) => {
  pty.write(data.toString());
});

// Handle PTY exit
pty.onExit(() => {
  console.log("Terminal session ended");
  process.exit(0);
});

// Handle SIGINT (Ctrl+C)
process.on("SIGINT", () => {
  pty.kill();
});
```

## 📖 API Reference

### `spawn(file: string, args: string[], options: IPtyForkOptions): IPty`

Creates and spawns a new pseudoterminal.

- `file`: The executable to launch
- `args`: Arguments to pass to the executable
- `options`: Configuration options
  - `name`: Terminal name (e.g., "xterm-256color")
  - `cols`: Number of columns (default: 80)
  - `rows`: Number of rows (default: 24)
  - `cwd`: Working directory (default: process.cwd())
  - `env`: Environment variables

Returns an `IPty` instance.

### `IPty` Interface

```typescript
interface IPty {
  // Properties
  readonly pid: number;        // Process ID
  readonly cols: number;       // Current columns
  readonly rows: number;       // Current rows
  readonly process: string;    // Process name
  
  // Events
  onData: (listener: (data: string) => void) => IDisposable;
  onExit: (listener: (event: IExitEvent) => void) => IDisposable;
  
  // Methods
  write(data: string): void;   // Write data to terminal
  resize(cols: number, rows: number): void;  // Resize terminal
  kill(signal?: string): void;  // Kill the process
}
```

### Event Types

```typescript
interface IExitEvent {
  exitCode: number;
  signal?: number | string;
}

interface IDisposable {
  dispose(): void;
}
```

## 🔧 Building from Source

If you want to build the package from source:

```bash
# Clone the repository
git clone https://github.com/sursaone/bun-pty.git
cd bun-pty

# Install dependencies
bun install

# Build Rust library and TypeScript
bun run build

# Run tests
bun test
```

## ❓ Troubleshooting

### Prebuilt Binaries

The npm package includes prebuilt binaries for macOS, Linux, and Windows. If you encounter issues with the prebuilt binaries, you can build from source:

```bash
# In your project directory
bun add @snomiao/bun-pty
cd node_modules/@snomiao/bun-pty
bun run build
```

### Common Issues

- **Error: Unable to load shared library**: Make sure you have the necessary system libraries installed.
- **Process spawn fails**: Check if you have the required permissions and paths.

### Quote Problem Fix Details

This fork addresses a critical argument parsing issue in the original bun-pty:

**Problem**: When passing arguments containing spaces or quotes to `spawn()`, the original implementation would incorrectly split them during command line construction. For example:

```typescript
// This would fail in the original version
spawn("echo", ["hello world"]) // "world" would be treated as a separate argument
```

**Solution**: Added a `shQuote()` helper function that properly escapes arguments using POSIX-style single-quote escaping:

- Empty strings become `''`
- Single quotes are escaped as `\'\'\'` (close-quote, escaped single quote, reopen)
- All arguments are wrapped in single quotes for safe parsing

**Technical Implementation**: The fix modifies `src/terminal.ts` to escape arguments before joining them into a command line string, ensuring that when the Rust backend uses `shell_words::split()`, it reconstructs the exact original arguments.

This is purely a compatibility fix for the argument parsing layer - no shell execution is involved.

## 📄 License

This project is licensed under the [MIT License](LICENSE).

## 🙏 Credits

- Built specifically for [Bun](https://bun.sh/)
- Uses [portable-pty](https://github.com/wez/wezterm/tree/main/pty) from WezTerm for cross-platform PTY support
- Inspired by [node-pty](https://github.com/microsoft/node-pty) for the API design
