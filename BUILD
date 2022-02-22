load("@rules_java//java:defs.bzl", "java_binary", "java_lite_proto_library", "java_proto_library")
load("@rules_proto//proto:defs.bzl", "proto_library")

proto_library(
    name = "backtesting_proto",
    srcs = ["backtesting.proto"],
    deps = [
        ":candles_proto",
        ":strategies_proto",
    ],
)

proto_library(
    name = "candles_proto",
    srcs = ["candles.proto"],
    deps = [
        "@com_google_protobuf//:timestamp_proto",
    ],
)

proto_library(
    name = "currencies_proto",
    srcs = ["currencies.proto"],
)

proto_library(
    name = "exchanges_proto",
    srcs = ["exchanges.proto"],
)

proto_library(
    name = "strategies_proto",
    srcs = ["strategies.proto"],
)

java_proto_library(
    name = "backtesting_java_proto",
    visibility = ["//visibility:public"],
    deps = [
        ":backtesting_proto",
    ],
)

java_proto_library(
    name = "candles_java_proto",
    visibility = ["//visibility:public"],
    deps = [
        ":candles_proto",
    ],
)

java_proto_library(
    name = "exchanges_java_proto",
    visibility = ["//visibility:public"],
    deps = [
        ":exchanges_proto",
    ],
)

java_proto_library(
    name = "strategies_java_proto",
    visibility = ["//visibility:public"],
    deps = [":strategies_proto"],
)

java_proto_library(
    name = "timestamp_java_proto",
    visibility = ["//visibility:public"],
    deps = [
        "@com_google_protobuf//:timestamp_proto",
    ],
)
