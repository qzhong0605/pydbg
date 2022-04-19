workspace_name=("pydbg")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")
load("@bazel_tools//tools/build_defs/repo:git.bzl", "git_repository")

http_archive(
    name = "com_google_googletest",
    sha256 = "cbcbf200277828c80f1488e2215d81147e85142127449ff50b1413415a19e48b",
    strip_prefix = "googletest-80600e56cc9afe7ee02737429f9177aa87025054",
    urls = ["https://github.com/google/googletest/archive/80600e56cc9afe7ee02737429f9177aa87025054.zip"], # 2022-04-15T18:59:48Z
)

_ALL_PYTHON_CONTENTS_ = """
filegroup(
    name = "all_srcs",
    srcs = glob(["**"]),
    visibility = ["//visibility:public"]
)
"""

http_archive(
    name = "python399",
    sha256 = "acbbc47faa61c20e68b49dac7c27de497d293a5c2105ca74c6c77a5d10ec1da4",
    build_file_content = _ALL_PYTHON_CONTENTS_,
    strip_prefix = "cpython-ccb0e6a3452335a4c3e2433934c3c0c5622a34cd",
    urls = ["https://github.com/python/cpython/archive/ccb0e6a3452335a4c3e2433934c3c0c5622a34cd.zip"], # python3.9.0, 2022-04-15T19:34:20Z
)

http_archive(
    name = "rules_foreign_cc",
    sha256 = "99320c0801dd23d62e4364095d6237966358e04a09bad3845827e45469a70c28",
    strip_prefix = "rules_foreign_cc-4aa243d4db416e9e57d9c1e0c815b76d09d8745d",
    urls = ["https://github.com/bazelbuild/rules_foreign_cc/archive/4aa243d4db416e9e57d9c1e0c815b76d09d8745d.zip"], # 2022-04-15T21:07:30Z
)

load("@rules_foreign_cc//foreign_cc:repositories.bzl", "rules_foreign_cc_dependencies")
rules_foreign_cc_dependencies()
