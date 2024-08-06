# Reproduction repository

Aliases are set for the gstreamer crates. Rust-analyzer correctly identifies these aliases.
Type completion is still shown for the original crate name, not for the alias set.

### Reproduction steps:
1. `bazel build //...`
2. `@rules_rust//tools/rust_analyzer:gen_rust_project`
3. Restart rust analyzer

In App you should have type completion for the gstreamer crate with `gst::`.
While in app-broken it does not take the aliases into account and still shows `gstreamer::`.
