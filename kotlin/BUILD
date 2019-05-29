package(default_visibility = ["//visibility:public"])

load("@io_bazel_rules_kotlin//kotlin:kotlin.bzl", "kt_jvm_library", "kt_jvm_test")

kt_jvm_library(
    name = "kotlin",
    srcs = glob(["src/**/*.kt"]),
)

kt_jvm_test(
    name = "test",
    srcs = glob(["test/**/*.kt"]),
    main_class = "com.foo.HelloKotlinTest",
    deps = [
        ":kotlin",
    ],
)
