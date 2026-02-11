# api-testing-framework
API Testing Framework — Restful Booker
Project description

This project demonstrates API testing using Postman, Newman and GitHub Actions.
It is a QA automation pet-project created to simulate a real-world API testing workflow.
The project includes smoke and regression test suites for the public Restful Booker API and covers positive, negative, security and contract test scenarios.

## The main goal of this project is to showcase:
- API testing skills
- test design
- automation with Postman
- CI integration
- bug reporting

## Tools & Technologies:
- Postman
- Newman
- JavaScript (Postman test scripts)
- REST API
- Node.js
- Git & GitHub
- GitHub Actions (CI)
- HTML reports (Newman reporter)

## Project structure:
collections/
    smoke.json
    regression.json
environments/
    dev.json
docs/
    checklist.md
.github/workflows/
    api-tests.yml
    
- collections:
  Contains Postman collections for smoke and regression testing.
- environments:
  Stores environment variables such as base URL, token and booking IDs.
- docs:
  Contains QA documentation.
- .github/workflows:
  GitHub Actions CI configuration.

## Test coverage
Smoke tests:
- Basic API functionality:
- API health check
- Auth token generation
- Create booking
- Get booking by ID

Smoke tests run automatically on each push to the main branch.
Regression tests

## Full regression suite includes:
- Booking
- Create booking
- Get booking
- Update booking
- Delete booking
- Negative scenarios
- Missing required fields
- Invalid data types
- Invalid date formats
- Business logic validation
- Security
- Update without token
- Delete without token
- Invalid token usage
- Contract
- Response structure validation
- Field types validation

Regression tests can be triggered manually from GitHub Actions.

## Running tests locally
To run tests locally:
- Install Node.js
- Install Newman globally
- Export Postman collections and environment
- Run smoke or regression collection using Newman
HTML report will be generated in the reports folder

CI — GitHub Actions

## This project uses GitHub Actions for continuous integration.
Smoke tests:
- run automatically on push to main branch
- generate HTML report
- upload report as artifact
Regression tests:
- run manually via GitHub Actions
- generate HTML report
- upload report as artifact
This simulates a real QA automation pipeline.

## Known issues (bugs found during testing)
The following issues were discovered during testing:
- Creating booking without firstname returns 500 instead of 400
- Invalid date format is accepted (should return validation error)
- Checkout date earlier than check-in is accepted (should fail validation)

# Bug reports are documented in GitHub Issues.

## How to run in CI
Smoke tests run automatically on push.
Regression tests can be triggered manually in GitHub Actions:
Actions → API tests → Run workflow


Author:
Karina Lukiyanova
