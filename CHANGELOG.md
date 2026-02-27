# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.2.2] - 2026-02-27

### Changed
- Published under `@mfllp` npm organisation
- Updated repository, bugs and homepage URLs to `mobifiliallp` GitHub org
- Replaced Babel build tooling — Node.js source is now used directly (no transpilation step)
- Added `files` field to `package.json` for precise npm package contents
- Added `prepublishOnly` script to auto-rebuild the JAR before every `npm publish`
- Updated minimum Node.js engine requirement to `>=12.0.0`
- **pom.xml** — updated Maven dependencies:
  - PDFBox `2.0.4` → `2.0.32`
  - JUnit `3.8.1` → `4.13.2`
  - JCommander `1.60` → `1.82`
  - maven-shade-plugin `3.0.0` → `3.6.0`
  - groupId updated to `com.mfllp.pdfmerger`

### Fixed
- Resolved 44 npm audit vulnerabilities (critical, high, moderate, low) by removing legacy Babel 6 toolchain

## [0.2.1] - Prior release

### Changed
- Use mixed memory mode in JVM to prevent OOM errors

### Fixed
- Error handling: capture stderr output instead of killing on any stderr data; check exit code in close handler

## [0.2.0] - Prior release

### Added
- `prepare` script for direct install from GitHub URL
- Java heap size options (`maxHeap`, `minHeap`)

## [0.1.1] - Prior release

### Fixed
- Use `toString()` instead of `String()` for data conversion

## [0.1.0] - Initial release

Initial version of pdfmerger — wraps Apache PDFBox via a Java JAR to merge PDF files from Node.js.
