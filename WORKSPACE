workspace(name = "acqio")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")
load("@bazel_tools//tools/build_defs/repo:git.bzl", "git_repository")

# ----------------------------------------------------------------------------
# Scala.

rules_scala_version = "f3113fb6e9e35cb8f441d2305542026d98afc0a2"  # update this as needed

http_archive(
    name = "io_bazel_rules_scala",
    strip_prefix = "rules_scala-%s" % rules_scala_version,
    type = "zip",
    url = "https://github.com/bazelbuild/rules_scala/archive/%s.zip" % rules_scala_version,
)

load("@io_bazel_rules_scala//scala:scala.bzl", "scala_repositories")

scala_repositories()

load("@io_bazel_rules_scala//scala_proto:scala_proto.bzl", "scala_proto_repositories")

scala_proto_repositories()

load("@io_bazel_rules_scala//scala:toolchains.bzl", "scala_register_toolchains")

scala_register_toolchains()

# ----------------------------------------------------------------------------
# Kotlin.

rules_kotlin_version = "f7a3b5fd823c2418fc2c2881c00e27e4d63475d5"

http_archive(
    name = "io_bazel_rules_kotlin",
    strip_prefix = "rules_kotlin-%s" % rules_kotlin_version,
    type = "zip",
    urls = ["https://github.com/bazelbuild/rules_kotlin/archive/%s.zip" % rules_kotlin_version],
)

load("@io_bazel_rules_kotlin//kotlin:kotlin.bzl", "kotlin_repositories", "kt_register_toolchains")

kotlin_repositories()

kt_register_toolchains()

# ----------------------------------------------------------------------------
# Java.

http_archive(
    name = "io_grpc_grpc_java",
    sha256 = "81d1e12bf0f8bd1560eed7c75f24d8bb8e7368dcf07802586e439c85cf89b005",
    strip_prefix = "grpc-java-1.19.0",
    urls = ["https://github.com/grpc/grpc-java/archive/v1.19.0.tar.gz"],
)

load("@io_grpc_grpc_java//:repositories.bzl", "grpc_java_repositories")

grpc_java_repositories()
