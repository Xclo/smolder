## Smolder Testing Framework for Cloud Foundry

The *Smolder* testing framework is for application developers who are pushing code to the platform and cloud foundry operators who are constantly updating the platform. They application developers would like to see if their code is not broken - either through unit/integration/load testing. The cloud foundry operators would like to see that the updates to the platform in not breaking any application development focused tests -- e.g. buildpack test, uaa test, connectivity to services tests. 

The assumption is that each test in the testing harness has few rest endpoints /health, /metrics , /info which will provide the details on if the test is working or if the test is broken. 

Here is an example of the test harness written for the Platform Operators

### CF Test Harness
https://github.com/rjain-pivotal/pcf-test-harness

This test harness has a series of simple buildpacks, connectivity test. Each of the test has a /health, /info and /metrics endpoint. The test case for unit, integration and load test would update the /health, /metrics endpoint after the test is executed. 

For execution of the test, the */ci* folder has a concourse pipeline. The pipeline i

Application developers can clone and make similar test for there application orgs and spaces. The


### Raditor Dashboard

https://github.com/rjain-pivotal/pcf-test-harness

The driver for the test harness

