load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "legacy_registry.go",
        "registry.go",
    ],
    importpath = "k8s.io/kubernetes/pkg/scheduler/framework/plugins",
    visibility = ["//visibility:public"],
    deps = [
        "//pkg/features:go_default_library",
        "//pkg/scheduler/apis/config:go_default_library",
        "//pkg/scheduler/framework/plugins/defaultbinder:go_default_library",
        "//pkg/scheduler/framework/plugins/defaultpodtopologyspread:go_default_library",
        "//pkg/scheduler/framework/plugins/imagelocality:go_default_library",
        "//pkg/scheduler/framework/plugins/interpodaffinity:go_default_library",
        "//pkg/scheduler/framework/plugins/nodeaffinity:go_default_library",
        "//pkg/scheduler/framework/plugins/nodelabel:go_default_library",
        "//pkg/scheduler/framework/plugins/nodename:go_default_library",
        "//pkg/scheduler/framework/plugins/nodeports:go_default_library",
        "//pkg/scheduler/framework/plugins/nodepreferavoidpods:go_default_library",
        "//pkg/scheduler/framework/plugins/noderesources:go_default_library",
        "//pkg/scheduler/framework/plugins/nodeunschedulable:go_default_library",
        "//pkg/scheduler/framework/plugins/nodevolumelimits:go_default_library",
        "//pkg/scheduler/framework/plugins/podtopologyspread:go_default_library",
        "//pkg/scheduler/framework/plugins/queuesort:go_default_library",
        "//pkg/scheduler/framework/plugins/serviceaffinity:go_default_library",
        "//pkg/scheduler/framework/plugins/tainttoleration:go_default_library",
        "//pkg/scheduler/framework/plugins/volumebinding:go_default_library",
        "//pkg/scheduler/framework/plugins/volumerestrictions:go_default_library",
        "//pkg/scheduler/framework/plugins/volumezone:go_default_library",
        "//pkg/scheduler/framework/v1alpha1:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/runtime:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/util/sets:go_default_library",
        "//staging/src/k8s.io/apiserver/pkg/util/feature:go_default_library",
        "//staging/src/k8s.io/kube-scheduler/config/v1alpha2:go_default_library",
        "//vendor/k8s.io/klog:go_default_library",
    ],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [
        ":package-srcs",
        "//pkg/scheduler/framework/plugins/defaultbinder:all-srcs",
        "//pkg/scheduler/framework/plugins/defaultpodtopologyspread:all-srcs",
        "//pkg/scheduler/framework/plugins/examples:all-srcs",
        "//pkg/scheduler/framework/plugins/helper:all-srcs",
        "//pkg/scheduler/framework/plugins/imagelocality:all-srcs",
        "//pkg/scheduler/framework/plugins/interpodaffinity:all-srcs",
        "//pkg/scheduler/framework/plugins/nodeaffinity:all-srcs",
        "//pkg/scheduler/framework/plugins/nodelabel:all-srcs",
        "//pkg/scheduler/framework/plugins/nodename:all-srcs",
        "//pkg/scheduler/framework/plugins/nodeports:all-srcs",
        "//pkg/scheduler/framework/plugins/nodepreferavoidpods:all-srcs",
        "//pkg/scheduler/framework/plugins/noderesources:all-srcs",
        "//pkg/scheduler/framework/plugins/nodeunschedulable:all-srcs",
        "//pkg/scheduler/framework/plugins/nodevolumelimits:all-srcs",
        "//pkg/scheduler/framework/plugins/podtopologyspread:all-srcs",
        "//pkg/scheduler/framework/plugins/queuesort:all-srcs",
        "//pkg/scheduler/framework/plugins/serviceaffinity:all-srcs",
        "//pkg/scheduler/framework/plugins/tainttoleration:all-srcs",
        "//pkg/scheduler/framework/plugins/volumebinding:all-srcs",
        "//pkg/scheduler/framework/plugins/volumerestrictions:all-srcs",
        "//pkg/scheduler/framework/plugins/volumezone:all-srcs",
    ],
    tags = ["automanaged"],
    visibility = ["//visibility:public"],
)

go_test(
    name = "go_default_test",
    srcs = ["legacy_registry_test.go"],
    embed = [":go_default_library"],
    deps = [
        "//pkg/scheduler/apis/config:go_default_library",
        "//vendor/github.com/google/go-cmp/cmp:go_default_library",
    ],
)
