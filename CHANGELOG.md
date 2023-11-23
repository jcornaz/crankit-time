# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).


## [Unreleased]

### Breaking changes

* Remove `playdate-sys-v02` from default feature flags


## [0.1.1] - 2023-11-19

### Documentation

* Add maintenance status in readme
* Fix description for crates.io
* Add more information to the root module documentation

## [0.1.0] - 2023-11-18

* `ElapsedTime` trait defining API to get and reset elapsed time since last reset
* `AbsoluteTime` trait defining API to get the time elasped since epoch
* `playdate-sys-v02` feature flag that implements the above traits for `ffi::playdate_sys` and `ffi::PlaydateAPI` of [playdate-sys](https://docs.rs/playdate-sys) (version `0.2`)


[Unreleased]: https://github.com/jcornaz/beancount_parser_2/compare/v0.1.1...HEAD
[0.1.1]: https://github.com/jcornaz/beancount_parser_2/compare/v0.1.0...v0.1.1
[0.1.0]: https://github.com/jcornaz/beancount_parser_2/compare/...v0.1.0
