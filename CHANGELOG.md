# Change Log
All notable changes to this project will be documented in this file.
This project adheres to [Semantic Versioning](http://semver.org/).

## [Unreleased]
### Added
- Added `tests` command, that shows missing test files for given source files.
- Added `--format` option to `bc` command to allow generating BC report in different formats: text, html, json.
- The list of BC checkers now can be configured in new `bc_checkers` array-type setting of `.code-insight.json` file.
- Added `sync` command to sync database with the code.
- Added `--source-project-fork` and `--target-project-fork` options for `bc` command to allow operating on different (forked) version of database for same project.
- Added `--project-fork` options to `report` command to allow operating on different (forked) version of database for same project.
- Added `--project-fork` options to `sync` command to allow operating on different (forked) version of database for same project.
- Added `cache.provider` setting to `~/.code-insight/config.json` file, that can be set to `memcache` to use locally installed Memcache server for caching.

### Changed
- The `refresh` option of `report` command was removed in favor of new `sync` command.
- The `code-insight.sqlite` database is now stored in `~/.code-insight` folder's sub-folder instead of scanned project folder.
- Data processed by `bc` command is now cached for 1 hour for performance reasons. This however results in project code changes not being detected within that hour.

### Fixed
- The `in sync` state of changed files wasn't updated on subsquential code syncs resulting is slower syncing process.

## [0.0.1] - 2016-05-07
### Added
- Initial release.

[Unreleased]: https://github.com/console-helpers/code-insight/compare/v0.0.2...HEAD
[0.0.2]: https://github.com/console-helpers/code-insight/compare/v0.0.1...v0.0.2
