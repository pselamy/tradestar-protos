load("@com_github_grpc_grpc//bazel:python_rules.bzl", "py_proto_library")
load("@rules_proto//proto:defs.bzl", "proto_library")

proto_library(
    name = "candles_proto",
    srcs = ["candles.proto"],
    deps = [
        "@com_google_protobuf//:timestamp_proto",
        ":instruments_proto",
    ],
)

py_proto_library(
    name = "candles_py_proto",
    visibility = ["//visibility:public"],
    deps = [
        ":candles_proto",
    ],
)

proto_library(
    name = "exchanges_proto",
    srcs = ["exchanges.proto"],
)

py_proto_library(
    name = "exchanges_py_proto",
    visibility = ["//visibility:public"],
    deps = [
        ":exchanges_proto",
    ],
)
