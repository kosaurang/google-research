# Top level intent recognition packages.

load("@mediapipe//mediapipe/framework/port:build_config.bzl", "mediapipe_proto_library")

licenses(["notice"])

package(default_visibility = ["//visibility:public"])

proto_library(
    name = "annotated_recording_collection_proto",
    srcs = ["annotated_recording_collection.proto"],
    deps = [
        "@com_google_protobuf//:duration_proto",
    ],
)

cc_proto_library(
    name = "annotated_recording_collection_cc_proto",
    deps = [":annotated_recording_collection_proto"],
)

mediapipe_proto_library(
    name = "annotated_recording_collection_sensor_options_proto",
    srcs = ["annotated_recording_collection_sensor_options.proto"],
    def_java_lite_proto = False,
    def_options_lib = False,
    def_portable_proto = False,
)

cc_library(
    name = "annotated_recording_collection_utils",
    srcs = ["annotated_recording_collection_utils.cc"],
    hdrs = ["annotated_recording_collection_utils.h"],
    deps = [
        ":annotated_recording_collection_cc_proto",
        "@com_google_absl//absl/status",
        "@com_google_absl//absl/status:statusor",
        "@com_google_absl//absl/strings",
        "@com_google_absl//absl/time",
        "@com_google_absl//absl/types:optional",
        "@com_google_protobuf//:protobuf",
    ],
)
