load("@rules_foreign_cc//foreign_cc:configure.bzl", "configure_make")

configure_make(
    name = "python399lib",
    args = ["-j"],
    configure_in_place = True,
    configure_command = "configure",
    configure_options = ["--enable-optimizations", "--enable-shared", "--without-tests", "CFLAGS='-Dredacted=\"redacted\"'"],
    lib_source = "@python399//:all_srcs",
    out_lib_dir = "lib",
    out_shared_libs = ["libpython3.9.so", "libpython3.9.so.1.0"]
)
