# Testing / Quality Control / Documentation Overview

Testing and quality control is a major consideration for all projects. As such, multiple redundant testing/QC processes are built in to our standard process for all code development, as described in the workflow documents provided in this document. All testing is risk-based, so more complex updates are subject to more rigorous testing. 

This page provides a brief overview of our different testing / QC techniques. 

# Standard Documentation

We consider detailed documentation to be a crucial first step in the quality control process. The following are created before a version 1.0 release for all repositories, and maintained throughout the project. 

## API / Configuration Documentation

Detailed documentation of each projects API/configuration is maintained. In most cases, we use a machine-readable `settings-schema.json` file ([example](https://github.com/RhoInc/safety-results-over-time/blob/master/settings-schema.json)) that is then used to human-readable wiki pages ([example](https://github.com/RhoInc/safety-results-over-time/wiki/Configuration)).

## Functional Specifications

We document the expected functionality of our tools as part of the project wiki. As functionality evolves, the wiki page is updated ([example](https://github.com/RhoInc/safety-results-over-time/wiki/Technical-Documentation))

## Data Guidelines 

When appropriate a stand-alone data specification page is maintained in the project wiki ([example](https://github.com/RhoInc/safety-results-over-time/wiki/Data-Guidelines)). 

## Reproducible examples

Whenever possible, our projects have one or more reproducible examples, which are automatically deployed using github pages whenever the repository is updated. ([example code](https://github.com/RhoInc/safety-results-over-time/tree/master/test-page), [hosted page]()http://rhoinc.github.io/safety-results-over-time/test-page/)

## Project overview / README.md

Each file has a README.md file that gives brief example, describes intended use and provides a 'hello world' style example. 

## Vignettes / Blog Posts

Longer write-ups describing the use of the project. 

## Description Files / Package.json

Formal description of project depenencies, version etc. (Details vary by programming language / framework)

# Testing Methods 

We use a variety of testing methods across our projects. 

## User Testing

A user (often called a "tester") will confirm that specific functionality is behaving as expected. Testing instructions (or just "tests") are included as part of an issue. Issues numbers are referenced in both code commits and pull requests to help with tracibility. Testers record the test result in pull requests using the github review functionality.

## Regression Testing

Testing that occurs immediately before a new version is released. Results are regression testing is recorded in "Development PRs" using GitHub's review functionality. We keep a running list of regression tests in the project wiki ([example](https://github.com/RhoInc/safety-results-over-time/wiki/Technical-Documentation#regression-tests)).

## Unit Testing / Automated Testing

Programatic testing that typically occurs whenever code is committed to a project. 

## Code Review

Developers review other developers code (typically in feature brances). Results of code reviews are recorded in Feature PRs using GitHub's review functionality. 

# Tools / Frameworks

## Charting Application Tester Framework (CAT)

[CAT](https://github.com/RhoInc/CAT) is a home-grown testing environment for testing our interactive graphics. 

### Continuous Integration (TravisCI)

We use TravisCI as a continuous integration framework on several projects. 

### Linters / Code formatting / Prettier

We don't like arguing about tabs vs. spaces, so we use linters and code formatters when possible. The [prettier.js](https://prettier.io/) package is worth a special mention; it's great. 

# Software Validation for Regulatory Compliance

Finally, a note on software validation. Much of our work is used in the conduct of clinical trials, so there are several relevant regulations that we are well aware of (but are beyond the scope of this page). All projects undergo a full regulatory review before being approved, and the testing processes and workflows described in this document are designed to be trackable, exportable and archivable to support usage in regulatory documentation when appropriate. 

