# Rundeck Java plugin build template

This directory contains a skeleton project to create a Rundeck Plugin.

View the [Rundeck Development Guide - Java] for more information about developing Rundeck Plugins.

## Customizing

1. Add java code to the `src/main/java` directory, implementing one of the Rundeck plugin interfaces.  Don't forget to *annotate* your plugin class with the `@Plugin` annotation at least, and provide a `service` and `name` value.
2. Modify the `build.gradle` file, and add the class names to those used for your plugin(s) to the `ext.pluginClassNames` value.

## Building

Run:

    gradle clean build


## Maven support

You can generate a `pom.xml`:

1. Modify the `build.gradle` file, and change all of the `ext.mavenPom*` values:

        ext.mavenPomGroupId='com.example'
        ext.mavenPomArtifactId='my-rundeck-plugin'
        ext.mavenPomTitle='My Plugin'

2. Run this to generate a `pom.xml:

        gradle createPom