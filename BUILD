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

proto_library(
    name = "indicators_proto",
    srcs = [
        "indicators.proto",
    ],
)

proto_library(
    name = "instruments_proto",
    srcs = [
        "instruments.proto",
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

proto_library(
    name = "strategies_proto",
    srcs = [
        "strategies.proto",
    ],
    deps = [
        ":indicators_proto",    
    ]
)

proto_library(
    name = "time_proto",
    srcs = ["time.proto"],
    deps = [
        "@com_google_protobuf//:timestamp_proto",
    ],
)

proto_library(
    name = "trading_proto",
    srcs = [
        "trading.proto",
    ],
    deps = [
        "@com_google_protobuf//:timestamp_proto",
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
    name = "indicators_java_proto",
    visibility = ["//visibility:public"],
    deps = [
        ":indicators_proto",
    ]
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
    deps = [
        ":strategies_proto",
    ],
)

java_proto_library(
    name = "time_java_proto",
    visibility = ["//visibility:public"],
    deps = [
        ":time_proto",
    ],
)

java_proto_library(
    name = "timestamp_java_proto",
    visibility = ["//visibility:public"],
    deps = [
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
