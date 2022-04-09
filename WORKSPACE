workspace(name = "tradestar_protos")

load("@bazel_tools//tools/build_defs/repo:git.bzl", "git_repository")

git_repository(
    name = "rules_jvm_external",
    remote = "https://github.com/bazelbuild/rules_jvm_external",
    tag = "4.2",
)

git_repository(
    name = "io_grpc_grpc_java",
    commit = "ff750a52717be34e7fa0d9a03a99268ccf8d495e",
    remote = "https://github.com/grpc/grpc-java",
    shallow_since = "1648566129 -0700"
)

load("@io_grpc_grpc_java//:repositories.bzl", "IO_GRPC_GRPC_JAVA_ARTIFACTS")
load("@io_grpc_grpc_java//:repositories.bzl", "grpc_java_repositories")

grpc_java_repositories()

git_repository(
    name = "com_google_protobuf",
    commit = "498de9f761bef56a032815ee44b6e6dbe0892cc4",
    remote = "https://github.com/protocolbuffers/protobuf",
    shallow_since = "1580681072 -0800",
)

load("@com_google_protobuf//:protobuf_deps.bzl", "protobuf_deps")

protobuf_deps()

load("@rules_jvm_external//:defs.bzl", "maven_install")

maven_install(
    artifacts = [] + IO_GRPC_GRPC_JAVA_ARTIFACTS,
    repositories = [
        "https://repo.maven.apache.org/maven2/",
    ],
)
