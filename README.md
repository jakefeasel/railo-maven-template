railo-maven-template
====================

[![Build Status](https://travis-ci.org/jakefeasel/railo-maven-template.png)](https://travis-ci.org/jakefeasel/railo-maven-template)

Fork this template project to quickly use the [Railo](http://www.getrailo.org) ColdFusion system with [Maven](http://maven.apache.org/) and [Jetty](http://jetty.codehaus.org/jetty/).

##Usage

From the project root, just run this command:

    mvn jetty:run

Once everything downloads and runs, you'll have a CF webserver running on [localhost:8080](http://localhost:8080).  The document root being served is src/main/webapp.

You will want to edit the pom.xml, changing these values:

    <groupId>org.yourorg</groupId>
    <artifactId>railo-maven-template</artifactId>
    <name>railo-maven-template</name>

to something specific to your project.  Also, you'll want to set the Railo Admin password right away.  Here's the link to get there, once you have Jetty running:

[Local Railo Admin](http://localhost:8080/railo-context/admin/web.cfm)


##Selenium Tests

The maven project has been configured to support selenium integration tests, with an included example test.  To run the tests, simply run this:

    mvn integration-test

These tests will also work with Travis-CI, so you can automatically verify that your site passes all tests.  All you have to do is enable your fork of this project to use Travis-CI.  See details for doing that on the [Travis-CI Getting Started Guide](http://about.travis-ci.org/docs/user/getting-started/).  All you will need to do is steps one and two in that guide - the rest is already done for you.
