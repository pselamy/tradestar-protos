load("@com_github_grpc_grpc//bazel:python_rules.bzl", "py_proto_library")
load("@rules_java//java:defs.bzl", "java_proto_library")
load("@rules_proto//proto:defs.bzl", "proto_library")

proto_library(
    name = "candles_proto",
    srcs = ["candles.proto"],
    deps = [
        "@com_google_protobuf//:timestamp_proto",
        ":instruments_proto",
    ],
)

java_proto_library(
    name = "candles_java_proto",
    visibility = ["//visibility:public"],
    deps = [
        ":candles_proto",
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
    srcs = [
        "exchanges.proto",
    ],
    deps = [
        ":instruments_proto",    
    ],
)

java_proto_library(
    name = "exchanges_java_proto",
    visibility = ["//visibility:public"],
    deps = [
        ":exchanges_proto",
    ],
)


py_proto_library(
    name = "exchanges_py_proto",
    visibility = ["//visibility:public"],
    deps = [
        ":exchanges_proto",
    ],
)

proto_library(
    name = "instruments_proto",
    srcs = [
        "instruments.proto",
    ],
)

java_proto_library(
    name = "instruments_java_proto",
    visibility = ["//visibility:public"],
    deps = [
        ":instruments_proto",
    ],
)

py_proto_library(
    name = "instruments_py_proto",
    visibility = ["//visibility:public"],
    deps = [
        ":instruments_proto",
    ],
)

proto_library(
    name = "strategies_proto",
    srcs = [
        "strategies.proto",
    ],
    deps = [
        "@com_google_protobuf//:timestamp_proto",       
        ":candles_proto",    
    ],    
)

java_proto_library(
    name = "strategies_java_proto",
    visibility = ["//visibility:public"],
    deps = [
        ":strategies_proto",
    ],
)

py_proto_library(
    name = "strategies_py_proto",
    visibility = ["//visibility:public"],
    deps = [
        ":strategies_proto",
    ],
)

proto_library(
    name = "trading_proto",
    srcs = [
        "trading.proto",
    ],
    deps = [
        ":exchanges_proto",    
        ":instruments_proto",    
        ":strategies_proto",
        "@com_google_protobuf//:timestamp_proto",
    ],    
)

java_proto_library(
    name = "trading_java_proto",
    visibility = ["//visibility:public"],
    deps = [
        ":trading_proto",
    ],
)

py_proto_library(
    name = "trading_py_proto",
    visibility = ["//visibility:public"],
    deps = [
        ":trading_proto",
    ],
)
