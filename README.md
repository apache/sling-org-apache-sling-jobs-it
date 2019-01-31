[<img src="https://sling.apache.org/res/logos/sling.png"/>](https://sling.apache.org)

 [![Build Status](https://builds.apache.org/buildStatus/icon?job=Sling/sling-org-apache-sling-jobs-it/master)](https://builds.apache.org/job/Sling/job/sling-org-apache-sling-jobs-it/job/master) [![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://www.apache.org/licenses/LICENSE-2.0) [![jobs](https://sling.apache.org/badges/group-jobs.svg)](https://github.com/apache/sling-aggregator/blob/master/docs/groups/jobs.md)

# Apache Sling Jobs Integration Tests

This module is part of the [Apache Sling](https://sling.apache.org) project.

This project runs a test launcher that creates an OSGi instance with only what is required to run Server Side tests.
Unfurtunately, since OSGi is a multi classloader environment its not possible to perform tests in this bundle, except
tests over http as any references made to APIs will get resolved with the wrong classloader and so wont be able to 
interact with OSGi. Hence the tests are in a separate bundle that is loaded by the launchpad.
