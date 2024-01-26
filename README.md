# ALAB 319.4.1: Aggregations, Indexes, and Validation

Version 1.0, 07/31/23
GitHub Repo.:  [Click here](https://github.com/HichamBenkada/ExpressAPI_MongooseAggregation) to open in a separate window.

## Introduction:

This project expands the Grades REST API application to include additional features for aggregations, indexes, and validation.

## Objectives:
- Adding additional features to an existing MongoDB + Express CRUD API.
- Refactoring existing code for efficiency, organization, and/or performance.

### Part 1: Exploring Existing Operations
Taking a few minutes to explore the existing code is important to make sure we are familiar with the structure and functionality of what we will be working with. Whenever we are given somebody else's code to work on, it is crucial to take the appropriate time to understand it before attempting modifications and improvements.

### Part 2: Adding Additional Features
Our task is to add the following additional features, and any code necessary to make them work as described. The pre-existing code should remain functional! Assume that we have clients actively using the existing code, so maintaining it is necessary for the health of the application.

*Creating the following features, using good organizational and coding practices:*
- Create a GET route at /grades/stats
Within this route, create an aggregation pipeline that returns the following information:
The number of learners with a weighted average (as calculated by the existing routes) higher than 70%.
The total number of learners.
The percentage of learners with an average above 70% (a ratio of the above two outputs).

- Create a GET route at /grades/stats/:id
Within this route, mimic the above aggregation pipeline, but only for learners within a class that has a class_id equal to the specified :id.
- Create a single-field index on class_id.
- Create a single-field index on learner_id.
- Create a compound index on learner_id and class_id, in that order, both ascending.

*Create the following validation rules on the grades collection:*
Each document must have a class_id field, which must be an integer between 0 and 300, inclusive.
Each document must have a learner_id field, which must be an integer greater than or equal to 0.
Change the validation action to "warn."

### Part 3: Testing
Testing features and Making sure that everything works as expected.

### Part 4: Completion
the completted github repo. of the project is submitted to Canvas.

_Thank you for your time! looking forward to hear your comments and feedback to develop and make this project better_