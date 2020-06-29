load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

# Current master commit on rules_rust (Fails to build target)
# http_archive(
#     name = "io_bazel_rules_rust",
#     sha256 = "332924e8e0da20220ce47ddf2ad7ac861e30e947edfcb4d6c7a9224f83db8467",
#     strip_prefix = "rules_rust-0b784535a4288637ab70338a06edec8caa2498c5",
#     urls = [
#         "https://github.com/bazelbuild/rules_rust/archive/0b784535a4288637ab70338a06edec8caa2498c5.tar.gz",
#     ],
# )

# My PR (Successfully builds target)
http_archive(
    name = "io_bazel_rules_rust",
    sha256 = "8b1976994cc9301e5817d7cfefdae81c69ed1f5884f85e1b0ded4350eea45bc9",
    strip_prefix = "rules_rust-a4571892e7ecacbab19a145422fe0df5479fd050",
    urls = [
        "https://github.com/Arm1stice/rules_rust/archive/a4571892e7ecacbab19a145422fe0df5479fd050.tar.gz",
    ],
)

http_archive(
    name = "bazel_skylib",
    sha256 = "e5d90f0ec952883d56747b7604e2a15ee36e288bb556c3d0ed33e818a4d971f2",
    strip_prefix = "bazel-skylib-1.0.2",
    urls = ["https://github.com/bazelbuild/bazel-skylib/archive/1.0.2.tar.gz"],
)

load("@io_bazel_rules_rust//rust:repositories.bzl", "rust_repositories")
rust_repositories(version = "nightly", iso_date = "2020-06-23", dev_components = True)

load("@io_bazel_rules_rust//:workspace.bzl", "bazel_version")
bazel_version(name = "bazel_version")
