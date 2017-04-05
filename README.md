# Drupal Build

A default build system for Drupal projects.

This project aims to make building a Drupal project incredibly easy, and to
provide a framework to developers to streamline their workflow.

It will make available and provide sensible defaults for tools such as:

  - Compass
  - PHP_CodeSniffer

## Installation

This project can be checked out with Composer.

```
"require-dev": {
    "doghouse/drupal-build": "*"
}
```

## Quick start guide

To get started, you will need to create a `build.xml` file and extend this
project's build base.

```
<?xml version="1.0" encoding="UTF-8"?>

<project name="PROJECT-NAME" default="help">
  <import file="vendor/doghouse/drupal-build/build.xml" />
</project>
```

## Configuration

This project ships with sensible defaults, however you must override some of its
properties to suit your project.

  1. Copy [build.example.properties](http://stash.dhmedia.com.au/projects/DB/repos/drupal-build/browse/build.example.properties)
     to create a `build.default.properties` file at the root of your project.
  2. Update the necessary build properties and save.

If you need to override properties for your local environment only, you can do
so by creating a `build.local.properties` and placing it in the same directory.

A full list of properties can be found [here](http://stash.dhmedia.com.au/projects/DB/repos/drupal-build/browse/build.default.properties).

### Compass configuration

This project compiles Sass files into CSS using Bundler via Ruby Version Manager
and sets of Ruby gems. But in order to do that it requires the following files
to exist at the root of the project.

  - `.ruby-gemset` - The Ruby gemset name (e.g. `myproject`).
  - `.ruby-version` - The Ruby version (e.g. `2.4.0`).
  - `Gemfile` - The list of Ruby gems the project depends on.

Ensure these are created before attempting to run the build.

## System requirements

This project is designed to run on almost any environment that can run Drupal,
however it is also important to ensure that the following are also installed and
configured:

  - Git
  - Composer
  - Ruby Version Manager
