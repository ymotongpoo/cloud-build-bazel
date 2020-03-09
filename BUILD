load("@io_bazel_rules_docker//container:container.bzl", "container_image")

filegroup(
    name = "hello_files",
    srcs = [
        "hello.txt",
    ],
    visibility = ["//visibility:public"],
)

container_image(
    name = "hello_container",
    base = "@distroless_base_debian10//image",
    directory = "/app",
    files = [
        ":hello_files",
    ],
    cmd = ["cat", "/app/hello.txt"],
)