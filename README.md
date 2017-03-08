## Smolder Testing Framework for Cloud Foundry

The *Smolder* testing framework is for application developers who are pushing code to the platform and cloud foundry operators who are constantly updating the platform. 

The application developers would like to see if their code is not broken - either through unit/integration/load testing. 
The cloud foundry operators would like to see that the updates to the platform in not breaking any application development focused tests -- e.g. buildpack test, uaa test, connectivity to services tests. 

The assumption is that each test in the testing harness has few rest endpoints /health, /metrics , /info which will provide the details on if the test is working or if the test is broken. The test harness draws inspiration from Spring Actuator Project (http://docs.spring.io/spring-boot/docs/current/reference/html/production-ready-endpoints.html) 


### Big Picture


### Components of the Test Framework
--

### CF Test Harness
https://github.com/rjain-pivotal/pcf-test-harness

This test harness has a series of simple buildpacks, connectivity test. Each of the test has a /health, /info and /metrics endpoint. The test case for unit, integration and load test would update the /health, /metrics endpoint after the test is executed. 

For execution of the test, the */ci* folder has a concourse pipeline. The pipeline i

Application developers can clone and make similar test for there application orgs and spaces. The

### Concourse



### Raditor Dashboard

https://github.com/rjain-pivotal/pcf-test-harness

The driver for the test harness

## Getting Started

Here is an example of the test harness written for the Platform Operators, which will use for the getting Started Guide. Application developers can follow the same steps, except their tests might change and they can deploy the Radiator Dashboard and Concourse in their own org/spaces. 


#### Step 1: Get the Test Harness

```
   git clone https://github.com/rjain-pivotal/cf-test-harness.git
   cd cf-test-harness
   deploy-test.sh
```







