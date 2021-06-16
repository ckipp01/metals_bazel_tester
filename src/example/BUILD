load("@io_bazel_rules_scala//scala:scala.bzl", "scala_library", "scala_binary")
load("@io_bazel_rules_scala//scala:scala_toolchain.bzl", "scala_toolchain")

scala_binary(
    name = "Example",
    srcs = glob(["*.scala"]),
    main_class = "example.Main"
)

scala_toolchain(
    name = "diagnostics_reporter_toolchain_impl",
    enable_diagnostics_report = True,
    visibility = ["//visibility:public"],
)

toolchain(
    name = "diagnostics_reporter_toolchain",
    toolchain = "diagnostics_reporter_toolchain_impl",
    toolchain_type = "@io_bazel_rules_scala//scala:toolchain_type",
    visibility = ["//visibility:public"],
)
