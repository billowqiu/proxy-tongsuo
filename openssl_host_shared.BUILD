licenses(["notice"])  # Apache 2

cc_library(
    name = "host-ssl-1-1",
    srcs = [
        "lib/libcrypto.a",
        "lib/libssl.a",
    ],
    hdrs = glob(["include/openssl/*.h"]),
    includes = ["include"],
    linkstatic = True,
    visibility = ["//visibility:public"],
)

alias(
    name = "ssl",
    actual = "host-ssl-1-1",
    visibility = ["//visibility:public"],
)
