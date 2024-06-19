# Reproduction repository

An alias is set for the rand crate from `rand` -> `custom`.
Type completion is still shown for the original crate name, not for the alias set.

### Reproduction steps:
1. `bazel build //...`
2. `@rules_rust//tools/rust_analyzer:gen_rust_project`
3. Restart rust analyzer
