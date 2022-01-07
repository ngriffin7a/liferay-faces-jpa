# Liferay Faces JPA

This is an OSGi bundle that claims to provide the "JavaJPA" capability via OSGI so that PrimeFaces can, in turn, be deployed as an OSGi module within Liferay Portal.

## Usage

Copy this jar to $LIFERAY_HOME/osgi/modules in order to suppress the following error when primefaces-11.0.0.jar fails to start as an OSGi module do to the following error:

    org.osgi.framework.BundleException: Could not resolve module: org.primefaces [1498]_ Require-Capability: osgi.contract; osgi.contract="JavaJPA"; filter:="(&(osgi.contract=JavaJPA)(version=2.2.0))"_

Alternatively, copy and entire set of OSGi bundles to $LIFERAY_HOME/osgi/modules that support JPA, including a JPA implementation such as OpenJPA, Hibernate, or EclipseLink.

## License

[Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0)

## News

For the latest news and updates, follow [@liferayfaces](https://twitter.com/liferayfaces).

## Building From Source

Using [Maven](https://maven.apache.org/) 3.x:

	mvn clean install