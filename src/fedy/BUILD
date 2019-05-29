load( "@bazel_tools//tools/build_defs/pkg:pkg.bzl", "pkg_tar")
load( "@bazel_tools//tools/build_defs/pkg:rpm.bzl", "pkg_rpm")

pkg_tar(
    name ="fedy-tar",
    srcs = [
        ":Makefile",
        ":app.js",
        ":cli.js",
        ":config.json",
        ":fedy-symbolic.svg",
        ":fedy.appdata.xml",
        ":fedy.desktop",
        ":fedy.exec",
        ":fedy.svg",
        ":option.js",
        ":plugins",
        ":repository.js",
        ":run-as-root.policy",
    ]
)
    
pkg_rpm(
    name = "fedy-rpm",
    spec_file = ":fedy.spec",
    architecture = "all",
    version = "0.1.0",
    data = [
        "//src/fedy:fedy-tar",
    ],
    visibility = ["//visibility:public"],
)
