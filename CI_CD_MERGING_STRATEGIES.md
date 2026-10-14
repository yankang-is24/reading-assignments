# Candidate reading exercise: Two ways to release changes

Take about 5 minutes to read this text. Then explain your thoughts in your own words. There is no single right answer.

## The situation

A team builds a web application. It uses React for the frontend and Kotlin / Spring Boot for the backend.

The team has two environments:

- **Sandbox:** A place to test changes and show new features to business stakeholders, such as the product manager.
- **Production:** The live application that customers use.

The team wants feedback on new features quickly. It also wants reliable demos and safe releases for customers.

A deployment puts a version of the application into an environment. A CI/CD pipeline runs checks and deploys changes automatically.

The team is considering two approaches.

## Approach 1: A separate `demo` branch

Developers work on feature branches. These branches hold their changes while they work.

When a change is ready for testing or a demo, it is merged into `demo`. Merging means combining changes into another branch. Only `demo` is deployed to sandbox.

When a change is ready for customers, it is merged into `main`. Only `main` is deployed to production.

## Approach 2: One `main` branch

Developers work on feature branches. When a change is ready, they open a pull request (PR). This asks other developers to review it.

After the review and automated checks pass, the change is merged into `main`.

The pipeline then deploys it to sandbox. If the pipeline checks pass, it also deploys it to production.

There is no separate `demo` branch. Both environments get changes from `main`.

## Your task

1. What problem is the team trying to solve?
2. How does each approach work? What are its main benefits and risks?
3. Which approach would you choose, and why? You can also suggest changes or another approach.
