workspace(name = "tradestar_protos")

load("@bazel_tools//tools/build_defs/repo:git.bzl", "git_repository")

############################
##### PROTOBUF SUPPORT #####
############################
git_repository(
    name = "com_google_protobuf",
    remote = "https://github.com/protocolbuffers/protobuf",
    tag = "v3.18.2",
)

load("@com_google_protobuf//protobuf_deps.bzl", "protobuf_deps")

protobuf_deps()

git_repository(
    name = "com_google_grpc_grpc",
    remote = "https://github.com/grpc/grpc",
    tag = "v1.50.1",
)

load("@com_google_grpc_grpc//bazel:grpc_deps.bzl", "grpc_deps")

grpc_deps()
