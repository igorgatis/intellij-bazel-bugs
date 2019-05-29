package(default_visibility = ["//visibility:public"])

java_library(
    name = "java",
    srcs = glob(["src/**/*.java"]),
)

java_test(
    name = "test",
    srcs = glob(["test/**/*.java"]),
    deps = [
        ":java",
    ],
)

