load("@rules_java//java:defs.bzl", "java_proto_library")
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
    name = "candle_service_proto",
    srcs = ["candle_service.proto"],
    deps = [
        ":candles_proto",
        ":instruments_proto",
        "@com_google_protobuf//:timestamp_proto",
    ],
)

proto_library(
    name = "candles_proto",
    visibility = ["//visibility:public"],
    srcs = ["candles.proto"],
    deps = [
        "@com_google_protobuf//:timestamp_proto",
    ],
)

proto_library(
    name = "instruments_proto",
    srcs = ["instruments.proto"],
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
    name = "candle_service_java_proto",
    visibility = ["//visibility:public"],
    deps = [
        ":candle_service_proto",
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
    name = "instruments_java_proto",
    visibility = ["//visibility:public"],
    deps = [
        ":instruments_proto",
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
