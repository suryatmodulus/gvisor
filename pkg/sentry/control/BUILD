load("//tools:defs.bzl", "go_library", "go_test")

package(licenses = ["notice"])

go_library(
    name = "control",
    srcs = [
        "control.go",
        "logging.go",
        "pprof.go",
        "proc.go",
        "state.go",
    ],
    visibility = [
        "//:sandbox",
    ],
    deps = [
        "//pkg/abi/linux",
        "//pkg/context",
        "//pkg/fd",
        "//pkg/fspath",
        "//pkg/log",
        "//pkg/sentry/fs",
        "//pkg/sentry/fs/host",
        "//pkg/sentry/fsbridge",
        "//pkg/sentry/kernel",
        "//pkg/sentry/kernel/auth",
        "//pkg/sentry/kernel/time",
        "//pkg/sentry/limits",
        "//pkg/sentry/state",
        "//pkg/sentry/strace",
        "//pkg/sentry/usage",
        "//pkg/sentry/vfs",
        "//pkg/sentry/watchdog",
        "//pkg/sync",
        "//pkg/syserror",
        "//pkg/tcpip/link/sniffer",
        "//pkg/urpc",
    ],
)

go_test(
    name = "control_test",
    size = "small",
    srcs = ["proc_test.go"],
    library = ":control",
    deps = [
        "//pkg/log",
        "//pkg/sentry/kernel/time",
        "//pkg/sentry/usage",
    ],
)
