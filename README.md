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

## Build

As usual

```
mvn clean install
```

## Release

Same as for usage of the project... 
