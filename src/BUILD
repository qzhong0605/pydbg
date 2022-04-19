load("@rules_foreign_cc//foreign_cc:configure.bzl", "configure_make")

configure_make(
    name = "pythonlib",
    args = ["-j"],
    configure_in_place = True,
    configure_command = "configure",
    configure_options = ["--enable-optimizations", "--enable-shared", "--without-tests", "CFLAGS='-Dredacted=\"redacted\"'"],
    lib_source = "@cpython//:all_srcs",
    out_lib_dir = "lib",
    out_shared_libs = ["libpython3.so"]
)
