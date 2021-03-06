#
# Copyright (C) 2020 Grakn Labs
#
# This program is free software: you can redistribute it and/or modify
# it under the terms of the GNU Affero General Public License as
# published by the Free Software Foundation, either version 3 of the
# License, or (at your option) any later version.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU Affero General Public License for more details.
#
# You should have received a copy of the GNU Affero General Public License
# along with this program.  If not, see <https://www.gnu.org/licenses/>.
#

package(default_visibility = ["//test/behaviour/graql/language/define:__subpackages__"])
load("@graknlabs_build_tools//checkstyle:rules.bzl", "checkstyle_test")

java_library(
    name = "steps",
    srcs = [
        "GraqlSteps.java"
    ],
    deps = [
        # Package dependencies
        "//kb/server",
        "//kb/concept/api",
        "//graql/reasoner",
        "//test/behaviour/connection:steps",
        "//concept/answer",

        # Grakn Labs dependencies
        "@graknlabs_graql//java:graql",

        # External dependencies from Maven
        "//dependencies/maven/artifacts/junit:junit",
        "//dependencies/maven/artifacts/io/cucumber:cucumber-java",
        "//dependencies/maven/artifacts/com/google/guava:guava",
    ],
    visibility = ["//visibility:public"],
)

checkstyle_test(
    name = "checkstyle",
    targets = [
        ":steps",
    ],
)
