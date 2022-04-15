# How to embrace PDD?

## Day -1
Even before the first HW/digital brick is placed, bring the Performance people.
Get input/recommendations on:
- HW
- SW
- Topology
- Processes
- Habits (Best practices, SW steps, and processes)

## Day 1
There are several tasks that should be implemented on the very first day.
- Implement any SW/HW recommendations done on day -1
- Install the recommended Perf Awareness SW on every recommended component
  - APMs (On dev, test, staging, pre-prod, prod, everywhere. Even get info from developer's machines)
  - Central metric repositories (IE Timebased Databases)
  - Graphing, observability, alerting
  - Integrate and interconnect everything, including CI/CD platform(s)
  - Configure pipelines to measure, validate SLO's and react for performance
- Share with the team the guidelines:
  - Define perf risks per project task
  - Identify SLI's and SLO's for the identified risks
  - Code must include instrumentation, telemetry, and principles
  - Code must be easy to automate
  - New features must have Perf automations triggering and measuring the SLI's and SLO's
  - Perf automations should be modular and easy to put together (for load tests)
  - Must check that after updates, Perf automations did not break and still pass SLO's
  - Cannot check in code without a Perf automation and an integration of it in the pipeline

## Continuous Day1 (or per work item)
On agile teams, every sprint new tasks will be defined, and some recommended steps should be paired with each one and implemented before the task can be marked as completed.
But on waterfall projects, these steps may spread along the project phases.

These steps may sound similar to the recommendations above. But they describe specific implementation of the recommendations.

1. For every new requirement, identify the following elements, to be added as completition criteria on the task.
  - Performance risk(s) related to the requirement
  - Identify relevant SLI's (metrics to pay attention)
  - Define SLO's, when is the metric good for:
    - Check in
    - Moving through pipelines
    - Load tests
  - Define what is needed to count that task as done in terms of performance
2. When the developer starts woking/updating on the software
  - Write the software code
  - Instrument the new software
  - Create relevant unit tests (this is from other project but wanted to add as I think is super important)
  - Create the Performance automation with SLI's and SLO's

## Implement/execute
Once everything is ready to be checked in the developer should complete some critical steps.
1. Before checking in 
  - Run the automation in the dev's machine to make sure it passes SLO's
  - Integrate the automation in the CI/CD pipeline-platform to run upon check in
2. After checking in
  - Make sure the automation is running in the pipeline
  - Configure any recurrent load tests
  - Review results and asses that SLO's and alerts are passing or working
  - Check no impact was caused elsewhere
3. At production
  - Make sure the continuous runs are also working in production (synthetics)
  - Review production behavior and check SLO's
  - Act on detections

## Loop
After software with PDD is released into the world, new requirements, updates and defects will be detected.
This will make the team to go back to the "Continuous Day 1" step.
1. Go to "Continuous Day 1" step.
2. Live, improve, repeat.

## BALTs
BALT is the acronym for Big Ass Load Tests. They are the full-system capacity load tests, spike tests, and those massive loads that cannot/shouldnot be simulated continuously without a dedicated/frozen environment.
In modern solutions, BALTs are not needed often. The solution is already in production and we know what is its performance.
BALTs are done when outstanding events are in the horizon. Those that masively go over production levels.

With PDD these can easily be done.
1. Identify coming load risk(s)
2. Define utlization and scenario caracteristics of the risk assessed
  - With great monitoring this will be easy
  - Focus on the business processes stressed during the risk scenario
4. Grab the automation pieces created and updated by developers using PDD and tweak any needs for the BALT
5. Create the scenario using those automations
6. Get a load test environment
7. Load-test the hell out of that thing


This is a WIP. Contributions and suggestions are very welcome.
-Besos <3

