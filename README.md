# Rundeck Java plugin build templates

This directory contains some skeleton projects to create a Rundeck Plugin.

View the [Rundeck Development Guide - Plugin Development - Java Plugin Development](http://rundeck.org/docs/developer/plugin-development.html#java-plugin-development) for more information about developing Rundeck Plugins in Java.

See also: [Rundeck Development Guide](http://rundeck.org/docs/developer/) for more information about plugin development in general.

## Choose a template

1. `java-no-dependencies` is a java project without the need to embed any third-party jar dependencies
2. `java-with-dependencies` can bundle jar dependencies into the built plugin jar

## Customizing

1. Copy the directory and rename it
2. Add java code to the `src/main/java` directory, implementing one of the Rundeck plugin interfaces.  Don't forget to *annotate* your plugin class with the `@Plugin` annotation at least, and provide a `service` and `name` value.
3. Modify the `build.gradle` file, and add the class names to those used for your plugin(s) to the `ext.pluginClassNames` value.
4. Modify the `build.gradle` to specify any jar dependencies

## Building

Run:

    gradle clean build