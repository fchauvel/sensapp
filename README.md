[![Build Status](https://travis-ci.org/fchauvel/sensapp.svg?branch=master)](https://travis-ci.org/fchauvel/sensapp)

# SensApp

A rewriting of the SensApp system, as a microservice architecture.


# Installation

SensApp includes four independent services, which appears in this
repository as submodules. To fetch the all source code, do as follows:

    $> git clone --recursive-submodules https://github.com/fchauvel/sensapp.git 
	
Refer to the documentation of each services for their installation and
configuration.


# Running Integration Tests

The `test/tester` module runs integration tests against the SensApp
architecture. You can run these tests using docker compose as follows:

	$ cd tests
	$ docker-compose rm -f
	$ docker-compose build --no-cache
	$ docker-compose up --no-build -d
	$ docker-compose run tests sensapp-tester -o storage-db -s data/sensors.yml

	
# TODOs

 - Add configuration file in the storage

 - Add configuration file in the registry

 - Add retry mechanism in the receiver, so it does not fail when the queue is not yet ready!

 - Document the REST endpoints of the receiver

 - Document the REST endpoints of the registry

 - Clean up the parameters of the tester
