cucumber-jvm-parallel-template
=======================

CucumberJVM template project for running tests in parallel. Two options how to run:
 * One "Runner" class per thread (use profile `parallel`)
 * Using [cucumber-jvm-parallel-plugin](https://github.com/temyers/cucumber-jvm-parallel-plugin) (use profile `parallelPlugin`)


###Command for execution
```
mvn clean verify -P [singleThreaded,nogrid,grid,parallel,parallelPlugin]
```

* *singleThreaded* - execute tests sequentially, omits parallel execution
* *nogrid* - execute tests locally
* *grid* - execute tests on Selenium Grid. Grid Hub can be set in pom in `seleniumGridURL` property

For example, invoking `mvn clean verify -P nogrid,parallelPlugin` will execute tests in parallel on local machine and using *cucumber-jvm-parallel-plugin* plugin.



