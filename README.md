# WalmartLabs POM

A Apache Maven parent POM to allow us some standardization across our Maven projects 
to reduce boilerplate as well as enable releases to the Central Repository easily.

## Usage

Just add a parent segment with the latest version to your project

```
  <parent>
    <groupId>com.walmartlabs</groupId>
    <artifactId>walmartlabs-pom</artifactId>
    <version>1</version>
  </parent>
```

To release your project you can use the usual Maven release process.

```
mvn release:prepare release:perform
```

This deploys the project to the
[Central Repository via OSSRH](http://central.sonatype.org/) and hence the
binaries are available whereever Central is available. Prior to that the staging
repository needs to be closed and released on OSSRH. Also person performing
the release has to have correct access. To gain access contact opensource@walmartlabs.com.

The project uses the 
[Takari Lifecycle](http://takari.io/book/40-lifecycle.html) for resources,
compiler, jar, install and deploy replacement. 

## Build

As usual

```
mvn clean install
```

## Release

Same as for usage of the project... 


