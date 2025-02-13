load("//tensorboard/defs:defs.bzl", "tf_ng_module", "tf_ts_library")

package(default_visibility = ["//tensorboard:internal"])

licenses(["notice"])

tf_ts_library(
    name = "lang",
    srcs = [
        "lang.ts",
    ],
)

tf_ts_library(
    name = "string",
    srcs = [
        "string.ts",
    ],
)

tf_ts_library(
    name = "types",
    srcs = [
        "types.ts",
    ],
)

tf_ts_library(
    name = "ngrx",
    srcs = [
        "ngrx.ts",
    ],
    deps = ["@npm//@ngrx/store"],
)

tf_ts_library(
    name = "value_formatter",
    srcs = [
        "value_formatter.ts",
    ],
)

tf_ts_library(
    name = "colors",
    srcs = [
        "colors.ts",
    ],
)

tf_ts_library(
    name = "dom",
    srcs = [
        "dom.ts",
    ],
)

tf_ts_library(
    name = "ui_selectors",
    srcs = [
        "ui_selectors.ts",
    ],
    deps = [
        "//tensorboard/webapp:app_state",
        "//tensorboard/webapp/app_routing/store",
        "//tensorboard/webapp/runs/store:selectors",
        "@npm//@ngrx/store",
    ],
)

tf_ng_module(
    name = "local_storage",
    srcs = ["local_storage.ts"],
    deps = [
        "@npm//@angular/core",
    ],
)

tf_ng_module(
    name = "local_storage_testing",
    testonly = True,
    srcs = ["local_storage_testing.ts"],
    deps = [
        ":local_storage",
        "@npm//@angular/core",
    ],
)

tf_ts_library(
    name = "util_tests",
    testonly = True,
    srcs = [
        "lang_test.ts",
        "ngrx_test.ts",
        "string_test.ts",
        "ui_selectors_test.ts",
        "value_formatter_test.ts",
    ],
    deps = [
        ":colors",
        ":lang",
        ":ngrx",
        ":string",
        ":ui_selectors",
        ":value_formatter",
        "//tensorboard/webapp:selectors",
        "//tensorboard/webapp/app_routing:testing",
        "//tensorboard/webapp/app_routing:types",
        "//tensorboard/webapp/app_routing/store:testing",
        "//tensorboard/webapp/runs/store:testing",
        "@npm//@ngrx/store",
        "@npm//@types/jasmine",
    ],
)
