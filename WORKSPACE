load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

RULES_JVM_EXTERNAL_TAG = "3.2"

RULES_JVM_EXTERNAL_SHA = "82262ff4223c5fda6fb7ff8bd63db8131b51b413d26eb49e3131037e79e324af"

http_archive(
    name = "rules_jvm_external",
    sha256 = RULES_JVM_EXTERNAL_SHA,
    strip_prefix = "rules_jvm_external-%s" % RULES_JVM_EXTERNAL_TAG,
    url = "https://github.com/bazelbuild/rules_jvm_external/archive/%s.zip" % RULES_JVM_EXTERNAL_TAG,
)

load("@rules_jvm_external//:defs.bzl", "maven_install")

JUNIT_JUPITER_VERSION = "5.6.2"

JUNIT_PLATFORM_CONSOLE_VERSION = "1.6.2"

maven_install(
    artifacts = [
        "com.toedter:jcalendar:1.4",  # https://mvnrepository.com/artifact/com.toedter/jcalendar
        "org.junit.jupiter:junit-jupiter-api:%s" % JUNIT_JUPITER_VERSION,
        "org.junit.jupiter:junit-jupiter-engine:%s" % JUNIT_JUPITER_VERSION,
        "org.junit.jupiter:junit-jupiter-params:%s" % JUNIT_JUPITER_VERSION,
        "org.junit.platform:junit-platform-console:%s" % JUNIT_PLATFORM_CONSOLE_VERSION,

        # "junit:junit:4.12",
        # "androidx.test.espresso:espresso-core:3.1.1",
        # "org.hamcrest:hamcrest-library:1.3",
    ],
    repositories = [
        "https://jcenter.bintray.com/",
        "https://maven.google.com",
        "https://repo1.maven.org/maven2",
    ],
)
