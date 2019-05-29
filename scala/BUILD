package(default_visibility = ["//visibility:public"])

load("@io_bazel_rules_scala//scala:scala.bzl", "scala_library", "scala_test")

scala_library(
    name = "scala",
    srcs = glob(["src/**/*.scala"]),
)

scala_test(
    name = "test",
    srcs = glob(["test/**/*.scala"]),
    deps = [
        ":scala",
    ],
)

