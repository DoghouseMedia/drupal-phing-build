# Drupal Build

A default build system for Drupal projects.

This project aims to make building a Drupal project incredibly easy, and to
provide a framework to developers to streamline their workflow.

It will make available and provide sensible defaults for tools such as:

  - Npm assets compile
  - PHP_CodeSniffer

## Installation

This project can be checked out with Composer.

```
"require-dev": {
    "doghouseagency/drupal-phing-build": "*"
}
```

## Quick start guide

To get started, you will need to create a `build.xml` file and extend this
project's build base.

```
<?xml version="1.0" encoding="UTF-8"?>

<project name="PROJECT-NAME" default="help">
  <import file="vendor/doghouseagency/drupal-phing-build/build.xml" />
</project>
```

## Configuration

This project ships with sensible defaults, however you must override some of its
properties to suit your project.

  1. Copy [build.example.properties](https://github.com/DoghouseMedia/drupal-phing-build/blob/master/build.example.properties)
     to create a `build.default.properties` file at the root of your project.
  2. Update the necessary build properties and save.

If you need to override properties for your local environment only, you can do
so by creating a `build.local.properties` and placing it in the same directory.

A full list of properties can be found [here](https://github.com/DoghouseMedia/drupal-phing-build/blob/master/browse/build.default.properties).

### Npm configuration

This project compiles Sass files into CSS using Bundler via npm package manager.


Ensure these are created before attempting to run the build.

## System requirements

This project is designed to run on almost any environment that can run Drupal,
however it is also important to ensure that the following are also installed and
configured:

  - Git
  - Npm
  - Composer
