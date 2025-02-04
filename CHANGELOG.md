# Changelog

All notable changes to this project will be documented in this file.
This project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## 4.2.1

### Fixed

- Fixed `zlib: unexpected end of file` error for version Node 18. Thanks to [stixx200](https://github.com/stixx200).

## 4.2.0

### Fixed

- Support for Nx version 16.6.0+ by removing the machine id from stored artifacts. Thanks to [MikeFear](https://github.com/MikeFear).
- `read` and `write` flags now prioritize environment variables over the `nx.json`. Thanks to [John98Zakaria](https://github.com/John98Zakaria).

## 4.1.0

### Added

- Options `read` and `write` now allow to disable reading and writing from / to the remote cache separately. Thanks to [rv2673](https://github.com/rv2673).

## 4.0.0

### Breaking Changes

- Nx support now starts at 16.0.0 thanks to [gmfun](https://github.com/gmfun)
- Note: packages consuming this package might need to set `declaration: false` in their TSConfig

## 3.0.0

### Breaking Changes

- Environment variables now start with `NXCACHE_` instead of `NX_CACHE_` to prevent leaking credentials

## 2.0.0

### Breaking Changes

- Implementation & API is now stream based to reduce memory overhead.
- All file system writes are now fully asynchronous.
- Filenames are now suffixed to prevent incorrect cache hits with older versions.

## 1.1.0

### Added

- Added `name` task runner option and `NXCACHE_NAME` env variable to set a custom cache name

## 1.0.0

### Added

- Added `initEnv(options)` function for reading environment variables from `.env`

## 0.0.6

### Fixed

- File copying from `.cache` to `dist` works again

### Fixed

- `fs/promises` import broken in Node 12 and below

## 0.0.5

### Fixed

- `fs/promises` import broken in Node 12 and below

## 0.0.4

### Fixed

- `silent` option now correctly mutes all info and success logs

## 0.0.3

### Added

- `silent` option to mute info and success logs

## 0.0.2

### Added

- Initial implementation of `createCustomRunner`
