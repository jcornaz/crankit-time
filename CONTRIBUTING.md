# How to contribute

## Ask for help, propose a feature request a feature or report a bug

Use the [discussions](https://github.com/jcornaz/crankit-time/discussions) to ask questions, share/discuss idea of features and even show-case what cool think you made with this project!

Use the [issues](https://github.com/jcornaz/crankit-time/issues) to report any issue you have (bug or missing feature). Make sure to explain why you need something.


## Work with the sources

1. Make sure you have latest stable rust toolchain installed (https://rustup.rs)
2. Make sure you have [just](https://just.systems/man/en/chapter_4.html) installed
3. Run `just -l` to see the list of available recipes

## Coding standards

### Tests

***This is a test-driven project!*** Every new feature and bug fixes must come with tests.

### Stable API

***Do not break the (stable) public API!***

(See https://doc.rust-lang.org/cargo/reference/semver.html to understand what constitutes a breaking change)

Favor, creating new types/functions, that could be used in place of the old ones.
Eventually we may deprecate the old abstractions and even (potentially) hide them from the doc.

When extending the API, make sure it can last. In particular:
* Think twice for every new public member
* Consider `#[non_exhaustive]` for public enums and structs
* Don't eagerly add api surface (incl. trait implementation) just "because we can". Make sure they are needed and provide value first.
    * In doubt, refrein from adding the new api surface, we can still add it later.
* Don't leak private dependencies in the API
* Public dependencies must be optional
* Gate new/unstable/unfinished api behind a `unstable-*` feature flag until stabilized/finished.

> **Note**
> 
> `unstable-*` features are not considered part of the stable public api and can receive breaking changes.
> 
> Api added in a pre-release version (`-alpha.x`, `-beta.x` or `-rc.x`) is not considered part of the stable public api and can receive breaking changes until published in a stable version.

## Open a pull request

Don't be afraid of small steps. I'd rather review 5 tiny pull-requests than 1 big. It is fine to have a PR that only partilally implement a feature. We can gate the feature behind the `unstable-*` feature flag until it is complete.

But no matter how small the PR is, it must have automated tests for any new feature and fixes!
