# Stampy

Stampy is a simple stamp collection tracker app written to demo Gradle integration tests and test containers.

The integration tests are in a separate folder to the unit tests called `integrationTest`. The Gradle related set up can be found in `build.gradle` under `testing`. The integration tests are set up to automatically run as part of the build (after the regular tests) but can separately by running the `ingtegrationTest` task.

# Run the project

### Start Postgres in a Docker container

```
docker run --name stampydb -d -p 5432:5432 -e POSTGRES_PASSWORD=postgres -e POSTGRES_DB=stampydb postgres
```

### Run the bootRun task

```
./gradlew bootRun
```