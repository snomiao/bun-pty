# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## 1.0.0 (2026-01-10)

### Features

* improve argument handling and add semantic-release automation ([64f3bc3](https://github.com/snomiao/bun-pty/commit/64f3bc35719fb8baff1390bbb2108e3b6966b042))
* pass env from options ([#9](https://github.com/snomiao/bun-pty/issues/9)) ([ea4f0ae](https://github.com/snomiao/bun-pty/commit/ea4f0aeb1f60070db9a6243535e3d1e6e7f20e06))

### Bug Fixes

* build ([2baf111](https://github.com/snomiao/bun-pty/commit/2baf1113b25781eb023b79c85bee059980ba2dfd))
* build ([1251e00](https://github.com/snomiao/bun-pty/commit/1251e00549673a545f946a849c5ee3265888fc53))
* builds ([6ef2965](https://github.com/snomiao/bun-pty/commit/6ef2965d832c659751dd71e7fdd413ecaec4b5f3))
* capture actual exit code from child process ([#10](https://github.com/snomiao/bun-pty/issues/10)) ([7a9a6d2](https://github.com/snomiao/bun-pty/commit/7a9a6d2aec88543615f3eada921f71a55d44aad5))
* ci: update GitHub Actions runner to ubuntu-latest\n\nThis commit updates the GitHub Actions runner to use  instead of specifying  for better compatibility and maintenance. ([7d40141](https://github.com/snomiao/bun-pty/commit/7d401412a1c8b173e23404577dedb8e95ceffbff))
* cross platform ([bf0036a](https://github.com/snomiao/bun-pty/commit/bf0036a2049865a1e9c0158bfe0fc3c55370d7ca))
* enable bun compile support and fix Windows path handling ([#25](https://github.com/snomiao/bun-pty/issues/25)) ([0dbea9b](https://github.com/snomiao/bun-pty/commit/0dbea9bb8ff6c633ebe2767991067d801798f284))
* lib name ([813d94d](https://github.com/snomiao/bun-pty/commit/813d94dee255f9cb414de5bbaff08a0a5ca13160))
* path on docker ([12ba21c](https://github.com/snomiao/bun-pty/commit/12ba21ce0e0171dd4a8d4c40cfff4d97fa205cc2))
* properly quote args to preserve spaces and special characters ([9c8c835](https://github.com/snomiao/bun-pty/commit/9c8c835bbbc2e1e7f9d95bd9218cb7a86dcf6f27)), closes [#12](https://github.com/snomiao/bun-pty/issues/12) [#15](https://github.com/snomiao/bun-pty/issues/15)
* release pipeline ([931a60e](https://github.com/snomiao/bun-pty/commit/931a60eddf828fecaab45ee9e1f0ca66e0bf3682))
* restore .d.ts type declarations for TypeScript compatibility ([#28](https://github.com/snomiao/bun-pty/issues/28)) ([685d24a](https://github.com/snomiao/bun-pty/commit/685d24af4fad051ce00ac3d76932918d086d983c))
* use ubuntu-22.04 for GLIBC 2.35 compatibility ([#23](https://github.com/snomiao/bun-pty/issues/23)) ([db635ae](https://github.com/snomiao/bun-pty/commit/db635ae05545e88991913bb9a299987549e1eb56))

### Code Refactoring

* merge auto-publish into publish.yml and fix glibc compatibility ([dc41691](https://github.com/snomiao/bun-pty/commit/dc4169127e7bf57cad7b8d5ac4b150f504a06a6a))
* remove erroneous console log ([#4](https://github.com/snomiao/bun-pty/issues/4)) ([a3acd79](https://github.com/snomiao/bun-pty/commit/a3acd79e2f636426bbe7863a6b5e0a8dcd12f410))

## 1.0.0 (2026-01-10)

### Features

* improve argument handling and add semantic-release automation ([64f3bc3](https://github.com/snomiao/bun-pty/commit/64f3bc35719fb8baff1390bbb2108e3b6966b042))
* pass env from options ([#9](https://github.com/snomiao/bun-pty/issues/9)) ([ea4f0ae](https://github.com/snomiao/bun-pty/commit/ea4f0aeb1f60070db9a6243535e3d1e6e7f20e06))

### Bug Fixes

* build ([2baf111](https://github.com/snomiao/bun-pty/commit/2baf1113b25781eb023b79c85bee059980ba2dfd))
* build ([1251e00](https://github.com/snomiao/bun-pty/commit/1251e00549673a545f946a849c5ee3265888fc53))
* builds ([6ef2965](https://github.com/snomiao/bun-pty/commit/6ef2965d832c659751dd71e7fdd413ecaec4b5f3))
* capture actual exit code from child process ([#10](https://github.com/snomiao/bun-pty/issues/10)) ([7a9a6d2](https://github.com/snomiao/bun-pty/commit/7a9a6d2aec88543615f3eada921f71a55d44aad5))
* ci: update GitHub Actions runner to ubuntu-latest\n\nThis commit updates the GitHub Actions runner to use  instead of specifying  for better compatibility and maintenance. ([7d40141](https://github.com/snomiao/bun-pty/commit/7d401412a1c8b173e23404577dedb8e95ceffbff))
* cross platform ([bf0036a](https://github.com/snomiao/bun-pty/commit/bf0036a2049865a1e9c0158bfe0fc3c55370d7ca))
* enable bun compile support and fix Windows path handling ([#25](https://github.com/snomiao/bun-pty/issues/25)) ([0dbea9b](https://github.com/snomiao/bun-pty/commit/0dbea9bb8ff6c633ebe2767991067d801798f284))
* lib name ([813d94d](https://github.com/snomiao/bun-pty/commit/813d94dee255f9cb414de5bbaff08a0a5ca13160))
* path on docker ([12ba21c](https://github.com/snomiao/bun-pty/commit/12ba21ce0e0171dd4a8d4c40cfff4d97fa205cc2))
* properly quote args to preserve spaces and special characters ([9c8c835](https://github.com/snomiao/bun-pty/commit/9c8c835bbbc2e1e7f9d95bd9218cb7a86dcf6f27)), closes [#12](https://github.com/snomiao/bun-pty/issues/12) [#15](https://github.com/snomiao/bun-pty/issues/15)
* release pipeline ([931a60e](https://github.com/snomiao/bun-pty/commit/931a60eddf828fecaab45ee9e1f0ca66e0bf3682))
* restore .d.ts type declarations for TypeScript compatibility ([#28](https://github.com/snomiao/bun-pty/issues/28)) ([685d24a](https://github.com/snomiao/bun-pty/commit/685d24af4fad051ce00ac3d76932918d086d983c))
* use ubuntu-22.04 for GLIBC 2.35 compatibility ([#23](https://github.com/snomiao/bun-pty/issues/23)) ([db635ae](https://github.com/snomiao/bun-pty/commit/db635ae05545e88991913bb9a299987549e1eb56))

### Code Refactoring

* remove erroneous console log ([#4](https://github.com/snomiao/bun-pty/issues/4)) ([a3acd79](https://github.com/snomiao/bun-pty/commit/a3acd79e2f636426bbe7863a6b5e0a8dcd12f410))

## 1.0.0 (2026-01-10)

### Features

* improve argument handling and add semantic-release automation ([64f3bc3](https://github.com/snomiao/bun-pty/commit/64f3bc35719fb8baff1390bbb2108e3b6966b042))
* pass env from options ([#9](https://github.com/snomiao/bun-pty/issues/9)) ([ea4f0ae](https://github.com/snomiao/bun-pty/commit/ea4f0aeb1f60070db9a6243535e3d1e6e7f20e06))

### Bug Fixes

* build ([2baf111](https://github.com/snomiao/bun-pty/commit/2baf1113b25781eb023b79c85bee059980ba2dfd))
* build ([1251e00](https://github.com/snomiao/bun-pty/commit/1251e00549673a545f946a849c5ee3265888fc53))
* builds ([6ef2965](https://github.com/snomiao/bun-pty/commit/6ef2965d832c659751dd71e7fdd413ecaec4b5f3))
* capture actual exit code from child process ([#10](https://github.com/snomiao/bun-pty/issues/10)) ([7a9a6d2](https://github.com/snomiao/bun-pty/commit/7a9a6d2aec88543615f3eada921f71a55d44aad5))
* ci: update GitHub Actions runner to ubuntu-latest\n\nThis commit updates the GitHub Actions runner to use  instead of specifying  for better compatibility and maintenance. ([7d40141](https://github.com/snomiao/bun-pty/commit/7d401412a1c8b173e23404577dedb8e95ceffbff))
* cross platform ([bf0036a](https://github.com/snomiao/bun-pty/commit/bf0036a2049865a1e9c0158bfe0fc3c55370d7ca))
* enable bun compile support and fix Windows path handling ([#25](https://github.com/snomiao/bun-pty/issues/25)) ([0dbea9b](https://github.com/snomiao/bun-pty/commit/0dbea9bb8ff6c633ebe2767991067d801798f284))
* lib name ([813d94d](https://github.com/snomiao/bun-pty/commit/813d94dee255f9cb414de5bbaff08a0a5ca13160))
* path on docker ([12ba21c](https://github.com/snomiao/bun-pty/commit/12ba21ce0e0171dd4a8d4c40cfff4d97fa205cc2))
* properly quote args to preserve spaces and special characters ([9c8c835](https://github.com/snomiao/bun-pty/commit/9c8c835bbbc2e1e7f9d95bd9218cb7a86dcf6f27)), closes [#12](https://github.com/snomiao/bun-pty/issues/12) [#15](https://github.com/snomiao/bun-pty/issues/15)
* release pipeline ([931a60e](https://github.com/snomiao/bun-pty/commit/931a60eddf828fecaab45ee9e1f0ca66e0bf3682))
* restore .d.ts type declarations for TypeScript compatibility ([#28](https://github.com/snomiao/bun-pty/issues/28)) ([685d24a](https://github.com/snomiao/bun-pty/commit/685d24af4fad051ce00ac3d76932918d086d983c))
* use ubuntu-22.04 for GLIBC 2.35 compatibility ([#23](https://github.com/snomiao/bun-pty/issues/23)) ([db635ae](https://github.com/snomiao/bun-pty/commit/db635ae05545e88991913bb9a299987549e1eb56))

### Code Refactoring

* remove erroneous console log ([#4](https://github.com/snomiao/bun-pty/issues/4)) ([a3acd79](https://github.com/snomiao/bun-pty/commit/a3acd79e2f636426bbe7863a6b5e0a8dcd12f410))

## 1.0.0 (2026-01-09)

### Features

* improve argument handling and add semantic-release automation ([64f3bc3](https://github.com/snomiao/bun-pty/commit/64f3bc35719fb8baff1390bbb2108e3b6966b042))
* pass env from options ([#9](https://github.com/snomiao/bun-pty/issues/9)) ([ea4f0ae](https://github.com/snomiao/bun-pty/commit/ea4f0aeb1f60070db9a6243535e3d1e6e7f20e06))

### Bug Fixes

* build ([2baf111](https://github.com/snomiao/bun-pty/commit/2baf1113b25781eb023b79c85bee059980ba2dfd))
* build ([1251e00](https://github.com/snomiao/bun-pty/commit/1251e00549673a545f946a849c5ee3265888fc53))
* builds ([6ef2965](https://github.com/snomiao/bun-pty/commit/6ef2965d832c659751dd71e7fdd413ecaec4b5f3))
* capture actual exit code from child process ([#10](https://github.com/snomiao/bun-pty/issues/10)) ([7a9a6d2](https://github.com/snomiao/bun-pty/commit/7a9a6d2aec88543615f3eada921f71a55d44aad5))
* cross platform ([bf0036a](https://github.com/snomiao/bun-pty/commit/bf0036a2049865a1e9c0158bfe0fc3c55370d7ca))
* enable bun compile support and fix Windows path handling ([#25](https://github.com/snomiao/bun-pty/issues/25)) ([0dbea9b](https://github.com/snomiao/bun-pty/commit/0dbea9bb8ff6c633ebe2767991067d801798f284))
* lib name ([813d94d](https://github.com/snomiao/bun-pty/commit/813d94dee255f9cb414de5bbaff08a0a5ca13160))
* path on docker ([12ba21c](https://github.com/snomiao/bun-pty/commit/12ba21ce0e0171dd4a8d4c40cfff4d97fa205cc2))
* properly quote args to preserve spaces and special characters ([9c8c835](https://github.com/snomiao/bun-pty/commit/9c8c835bbbc2e1e7f9d95bd9218cb7a86dcf6f27)), closes [#12](https://github.com/snomiao/bun-pty/issues/12) [#15](https://github.com/snomiao/bun-pty/issues/15)
* release pipeline ([931a60e](https://github.com/snomiao/bun-pty/commit/931a60eddf828fecaab45ee9e1f0ca66e0bf3682))
* restore .d.ts type declarations for TypeScript compatibility ([#28](https://github.com/snomiao/bun-pty/issues/28)) ([685d24a](https://github.com/snomiao/bun-pty/commit/685d24af4fad051ce00ac3d76932918d086d983c))
* use ubuntu-22.04 for GLIBC 2.35 compatibility ([#23](https://github.com/snomiao/bun-pty/issues/23)) ([db635ae](https://github.com/snomiao/bun-pty/commit/db635ae05545e88991913bb9a299987549e1eb56))

### Code Refactoring

* remove erroneous console log ([#4](https://github.com/snomiao/bun-pty/issues/4)) ([a3acd79](https://github.com/snomiao/bun-pty/commit/a3acd79e2f636426bbe7863a6b5e0a8dcd12f410))

## [0.4.6] - 2026-01-05

### Fixed
- Restore .d.ts type declarations for TypeScript compatibility (#28)
  - Added TypeScript declaration file generation to build process
  - Ensures proper type definitions are available for TypeScript users
  - Includes dist directory in published package for type declarations

## [0.4.5] - 2026-01-01

### Fixed
- Fixed build script to skip building when libraries already exist
  - Build script now checks for existing libraries before attempting to build
  - Prevents build failures in CI/CD when pre-built libraries are already present
  - Allows publish workflow to work without requiring Rust installation in publish job
  - Improves build performance by skipping unnecessary rebuilds

## [0.4.4] - 2025-12-31

### Fixed
- Enable bun compile support by shipping TypeScript source (#25)
  - Ship TypeScript source instead of bundled JS for static analysis
  - Add statically analyzable require() for native library embedding
  - Fix Windows library name (no 'lib' prefix)
  - Fix spaces in Windows exe path handling
  - Add Windows-specific tests
  - Add compile test script to verify bun build --compile works
  - Fixes: https://github.com/sursaone/bun-pty/issues/19

## [0.4.3] - 2025-12-30

### Fixed
- Use ubuntu-22.04 for GLIBC 2.35 compatibility (#23)
  - Updated CI/CD pipeline to use ubuntu-22.04 to ensure GLIBC 2.35 compatibility
  - Ensures built binaries work on systems with GLIBC 2.35 and newer

## [0.4.2] - 2025-12-01

### Fixed
- Fixed argument parsing to properly preserve arguments with spaces and special characters (#15)
  - Arguments containing spaces, quotes, or special characters are now correctly quoted
  - Prevents arguments from being incorrectly split into multiple tokens
  - Uses POSIX-style single quotes compatible with shell_words::split
  - Thanks to @snomiao for the initial implementation

## [0.4.1] - 2025-12-02

### Changed
- Updated examples and documentation
- Improved example code with better TypeScript usage patterns

## [0.4.0] - 2025-12-01

### Added
- Support for passing environment variables via options (#9)

### Fixed
- Fixed data loss in PTY read operations (#8)
- Fixed capture of actual exit code from child process (#10)
- Fixed build process and configuration

### Changed
- Removed rust build artifacts and updated .gitignore (#7)

## [0.3.2] - 2025-06-20

### Changed
- Updated package.json version
- Updated example to work with installed bun-pty package

### Fixed
- Removed erroneous console log (#4)

## [0.3.1] - 2025-05-15

### Fixed
- Fixed path resolution on Docker environments

## [0.3.0] - 2025-05-15

### Fixed
- Fixed release pipeline configuration

## [0.2.1] - 2025-05-15

### Fixed
- Fixed encoding issues with binary data from Docker and other applications
- Updated Rust code to properly handle non-UTF8 terminal control sequences
- Improved error handling in PTY read/write operations

## [0.2.0] - 2025-05-14

### Added
- Improved TypeScript support with complete type definitions
- Added TypeScript usage examples
- Enhanced documentation with TypeScript usage instructions

### Changed
- Optimized package size by excluding unnecessary files
- Improved build process for more reliable type generation

## [0.1.0] - 2025-05-13

### Added
- Initial release
- Cross-platform PTY support for macOS, Linux, and Windows
- Basic API for terminal process management
- Core PTY functionality: spawn, read, write, resize, and kill
- Process ID retrieval support
- TypeScript type definitions
- Integration tests
