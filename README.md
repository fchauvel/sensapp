# SensApp

A rewriting of the SensApp system, as a microservice architecture.


# Integration Tests

The `test/tester` module runs integration tests against the SensApp
architecture. You can run these tests using docker compose as follows:

	$> cd tests
	$> docker-compose rm -f
	$> docker-compose build --no-cache
	$> docker-compose up --no-build -d
	$> docker-compose run test sensapp-tester -q task-queue -o storage-db
	Starting tests_task-queue_1 ... 
	Starting tests_storage-db_1 ... 
	Starting tests_storage_1    ... 
	Testing with content from './data/sensor-data.json' ... [ OK ]
	
