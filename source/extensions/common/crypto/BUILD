licenses(["notice"])  # Apache 2

load(
    "@envoy//bazel:envoy_build_system.bzl",
    "envoy_cc_extension",
    "envoy_cc_library",
    "envoy_package",
    "envoy_extension_package",
)

# envoy_package()
envoy_extension_package()

# envoy_cc_library(
#     name = "utility_lib",
#     repository = "@envoy",
#     srcs = [
#         "crypto_impl.cc",
#         "utility_impl.cc",
#     ],
#     hdrs = [
#         "crypto_impl.h",
#         "utility_impl.h",
#     ],
#     external_deps = [
#         "ssl",
#     ],
#     deps = [
#         "@envoy//include/envoy/buffer:buffer_interface",
#         "@envoy//source/common/common:assert_lib",
#         "@envoy//source/common/crypto:utility_lib",
#         "//boringssl_compat:bssl_compat_lib",
#         "//boringssl_compat:bssl_compat_cbs_lib",
#     ],
# )

envoy_cc_extension(
    name = "utility_lib",
    repository = "@envoy",
    security_posture = "unknown",
    category = (    
        "envoy.transport_sockets.downstream",
        "envoy.transport_sockets.upstream"), 
        srcs = [
            "crypto_impl.cc",
            "utility_impl.cc",
        ],
        hdrs = [
            "crypto_impl.h",
            "utility_impl.h",
        ],
        deps = [
            "@envoy//include/envoy/buffer:buffer_interface",
            "@envoy//source/common/common:assert_lib",
            "@envoy//source/common/crypto:utility_lib",
            "//boringssl_compat:bssl_compat_lib",
            "//boringssl_compat:bssl_compat_cbs_lib",
        ],
)
