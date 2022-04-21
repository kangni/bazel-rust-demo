load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

# To find additional information on this release or newer ones visit:
# https://github.com/bazelbuild/rules_rust/releases
http_archive(
    name = "rules_rust",
    sha256 = "39655ab175e3c6b979f362f55f58085528f1647957b0e9b3a07f81d8a9c3ea0a",
    urls = [
        "https://mirror.bazel.build/github.com/bazelbuild/rules_rust/releases/download/0.2.0/rules_rust-v0.2.0.tar.gz",
        "https://github.com/bazelbuild/rules_rust/releases/download/0.2.0/rules_rust-v0.2.0.tar.gz",
    ],
)
load("@rules_rust//rust:repositories.bzl", "rust_repositories", "rules_rust_dependencies", "rust_register_toolchains")
rust_repositories()
rules_rust_dependencies()
rust_register_toolchains()


# Set up blackjack
http_archive(
    name = "blackjack",
    url = "https://github.com/wildarch/blackjack/archive/909b66db4782cf963791aa4a24793244dffdba17.zip",
    strip_prefix = "blackjack-909b66db4782cf963791aa4a24793244dffdba17",
)
load("@blackjack//:workspace.bzl", "blackjack_cargo")
blackjack_cargo()
