# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.4.0] - 2023-03-28

## Added

- **! Added `confz` as a dependency!**
- Added `fail_fast` to config

## Fixed

- **Now supports mylog`>=0.7.0`**

## [0.3.0] - 2023-02-25

## Added

- **! Added _first_ linters, which will be ran _before_ formatters. Enable them with `run_first=true` in the linter's config.**
- Added `Config.get_first_linters(self: Self@Config) -> List[Linter]` and `Config.get_other_linters(self: Self@Config) -> List[Linter]`

## [0.2.0] - 2023-02-18

### Added

- **! Added required first positional argument to cli: `task`. Must be `format` or `check`.**
- Added `Formatter.run_format()` and `Formatter.run_check()`
- Added `config.WhatToQuiet`

### Changed

- **! `FormatterOrLinter` changed to this: `(*, packages: List[str]) -> None`**
- **! `Formatter` changed to this: `(*, packages: List[str], format_command: str, check_command: str | None = None, allow_nonzero_on_format: bool = False) -> None`**
- **! `Linter` changed to this: `(*, packages: List[str], command: str) -> None`**
- **Made Lemming compatible with 3.8, and made type hints better**

### Removed

- Removed `FormatterOrLinter._run()`
- Removed the following replace stuff from `FormatterOrLinter.run_command()`:
  - `{package}` (became `{packages}`),
  - `{args}`,
  - `{also_install}`
- Removed `FormatterOrLinter.get_version()`

## [0.1.3] - 2022-12-17

### Added

- Add log message for `run_command()`

## [0.1.2] - 2022-12-17

### Fixed

- Add `shlex.split()` to `run_command()`

## [0.1.1] - 2022-12-17

### Fixed

- There's no try-except at `__main__.main`

## [0.1.0] - 2022-12-17
