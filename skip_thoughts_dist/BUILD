package(
    default_visibility = [
        "//visibility:public",
    ]
)

licenses(["notice"])  # Apache 2.0

exports_files(["LICENSE"])

py_library(
    name = "configuration",
    srcs = ["configuration.py"],
    srcs_version = "PY2AND3",
)

py_binary(
    name = "train",
    srcs = ["train.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":configuration",
        "//skip_thoughts:skip_thoughts_model",
        "//skip_thoughts_dist/ops:training",
    ],
)

py_binary(
    name = "track_perplexity",
    srcs = ["track_perplexity.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":configuration",
        "//skip_thoughts:skip_thoughts_model",
        "//skip_thoughts_dist/ops:evaluation",
    ],
)
