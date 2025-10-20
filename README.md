# GitHub Advanced Security (GHAS) Proof of Concept Demonstrations

This repository contains demonstration materials for GitHub Advanced Security (GHAS) Proof of Concept (PoC) evaluations conducted with GitHub. 
It includes three sample projects within the `projects` folder, all of which can be built using Bazel.

## Projects Overview

### Go Language
- **go_web**: A simple "Hello, World!" application running on a web server.

## Building Projects on Ubuntu

To build the projects, follow the instructions below:

- Build all projects:
  ```
  bazel build //...
  ```

- Build the Go project:
  ```
  bazel build //projects/go_web:go_web --verbose_failures
  ```

## Running Projects on Ubuntu

To execute the projects, use the following commands:

- Run the Go project:
  ```
  bazel run //projects/go_web:go_web --verbose_failures
  ```

For Go, CodeQL does not support builds with Bazel. Bazel does not utilize the standard Go build tooling (i.e., `go build`). Due to this discrepancy, adding support for Bazel-built Go projects is non-trivial. GitHub monitors the demand for such support and may consider it in the future, though there are no current plans. This issue is documented at: [GitHub Issue #17458](https://github.com/github/codeql/issues/17458).
