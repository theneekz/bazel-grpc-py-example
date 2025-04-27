load("@rules_proto//proto:defs.bzl", "proto_library")
load("@rules_proto_grpc_python//:defs.bzl", "python_grpc_library")
load("@rules_python//python:defs.bzl", "py_binary")

proto_library(
    name = "lobby_service_proto",
    srcs = ["lobby_service.proto"],
)

python_grpc_library(
    name = "lobby_service_python_grpc_lib",
    protos = ["lobby_service_proto"],
)

py_binary(
    name = "server",
    srcs = ["server.py"],
    deps = [":lobby_service_python_grpc_lib"],
)
