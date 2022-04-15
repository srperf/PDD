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
  -  

## Implement/execute


## Loop


WIP...
