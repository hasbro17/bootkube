package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_binary",
    "go_library",
    "go_test",
    "cgo_library",
)

go_library(
    name = "go_default_library",
    srcs = [
        "dns.go",
        "doc.go",
        "plugins.go",
    ],
    tags = ["automanaged"],
    deps = [
        "//federation/pkg/dnsprovider/rrstype:go_default_library",
        "//vendor:github.com/golang/glog",
    ],
)

go_test(
    name = "go_default_test",
    srcs = ["dns_test.go"],
    library = "go_default_library",
    tags = ["automanaged"],
    deps = ["//federation/pkg/dnsprovider/rrstype:go_default_library"],
)
