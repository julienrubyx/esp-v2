load("@envoy_api//bazel:api_build_system.bzl", "api_cc_py_proto_library")
load("@io_bazel_rules_go//proto:def.bzl", "go_proto_library")

package(default_visibility = ["//visibility:public"])

api_cc_py_proto_library(
    name = "config_proto",
    srcs = [
        "config.proto",
        "requirement.proto",
    ],
    visibility = ["//visibility:public"],
    deps = [
        "//api/envoy/http/common:base_proto",
    ],
)

go_proto_library(
    name = "config_go_proto",
    importpath = "github.com/GoogleCloudPlatform/esp-v2/src/go/proto/api/envoy/http/service_control",
    proto = ":config_proto",
    deps = [
        "//api/envoy/http/common:base_go_proto",
        "@com_envoyproxy_protoc_gen_validate//validate:go_default_library",
    ],
)
