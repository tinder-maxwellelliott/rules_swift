load("@bazel_skylib//:bzl_library.bzl", "bzl_library")
load(":debug_settings_tests.bzl", "debug_settings_test_suite")
load(":coverage_settings_tests.bzl", "coverage_settings_test_suite")
load(":generated_header_tests.bzl", "generated_header_test_suite")
load(":private_deps_tests.bzl", "private_deps_test_suite")
load(":swift_through_non_swift_tests.bzl", "swift_through_non_swift_test_suite")

licenses(["notice"])

debug_settings_test_suite()

coverage_settings_test_suite()

generated_header_test_suite()

private_deps_test_suite()

swift_through_non_swift_test_suite()

test_suite(
    name = "all_tests",
)

bzl_library(
    name = "starlark_tests_bzls",
    srcs = glob(["*.bzl"]),
    deps = [
        "//test/fixtures:starlark_tests_bzls",
        "//test/rules:starlark_tests_bzls",
    ],
)
