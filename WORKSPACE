workspace(name = "tradestar_protos")

load("@bazel_tools//tools/build_defs/repo:git.bzl", "git_repository")

############################
##### PROTOBUF SUPPORT #####
############################
git_repository(
    name = "rules_proto",
    remote = "https://github.com/bazelbuild/rules_proto",
    tag = "4.0.0-3.20.0",
)

load("@rules_proto//proto:repositories.bzl", "rules_proto_dependencies", "rules_proto_toolchains")

rules_proto_dependencies()

rules_proto_toolchains()

git_repository(
    name = "com_github_grpc_grpc",
    remote = "https://github.com/grpc/grpc",
    tag = "v1.50.1",
)

load("@com_github_grpc_grpc//bazel:grpc_deps.bzl", "grpc_deps")

grpc_deps()
