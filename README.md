# Progress / Status
In development. This isn't ready for use yet.

# Formulate Overview
A form builder for Umbraco.

![Formulate](assets/images/formulate.png?raw=true "Formulate")

# Contributing
Requires:
* Visual Studio 2015
* Node.js
* npm
* grunt-cli (installed globally)

# Building
To build the source code, you can use the simple building technique or the advanced building technique. Both versions are described below.

## Simple Building Technique
Double click the file "build/build.bat". The Umbraco package will be created in the "dist" folder. You can then install this Umbraco package into your website.

If you would like to use the built-in sample website, refer to the advanced building technique below.

## Advanced Building Technique
These are the steps you can take to build and test Formulate:
* Build the solution.
* Run `npm install` (this only needs to be done once).
* Run `grunt`.
  * Pro-tip: Running `grunt frontend` is faster
* Run the sample website.
* Run `grunt package` to create an Umbraco installer package (in the "dist" folder).

There are a few nuances to building you may want to consider:
* Most grunt tasks will use whichever build configuration is most recent, but will otherwise default to "Release".
* The `grunt package-full` task always defaults to "Release".
* You can specify a particular build configuration like this: `grunt package-full --buildConfiguration=Debug`.