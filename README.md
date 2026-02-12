# Marvin — Project Summary

This application is a platform for managing and running automated end-to-end (E2E) tests with **Playwright**, using **versioned test plans and test cases**, with **results and run artifacts** browsable from a **web interface**.

---

## Key Features

### Test Plans
- Create **test plans** that group multiple **test cases**.
- Define **execution order** and shared configuration, such as:
  - `baseUrl`
  - browser settings
  - timeouts
  - retries
  - and other common options
- Run an entire plan and view:
  - overall (aggregated) plan status
  - per-test-case status and details

### Editable Test Cases
- Each test case is a **Playwright script** (TypeScript/JavaScript) editable by the user through a **web editor**.
- Tests follow a **standard template** and can rely on **shared helpers** to improve stability and reusability.

### Versioning and Reproducibility
- Every save creates a **new immutable version** of the test case.
- Every execution (**run**) is linked to:
  - a **specific test version**
  - a configuration **snapshot**
- This makes it possible to re-run *exactly the same test* over time.

### Automated Execution (Playwright Runner)
Users can start:
- a run for a **single test case** (optionally selecting a specific version)
- a run for a **test plan** (sequential execution or configurable behavior)

Each run has a tracked status (e.g.):
- `queued`
- `running`
- `pass`
- `fail`
- `canceled`
- `timeout`

Runs are stored and accessible from the **history**.

### Reports and Artifacts
Each run generates reports and debugging artifacts such as:
- execution logs
- Playwright trace
- screenshots on failure
- video (optional)

The UI lets you quickly inspect:
- outcome
- main error/failure reason
- downloadable artifacts

### Safe Execution (Local and Infrastructure)
Tests run in a controlled and isolatable environment (separate process and/or container),
with timeouts and access policies—so they can run:
- locally for development/debug
- in infrastructure with improved safety and scalability

### AI-Based Assistance (Optional, Extensible)
The platform can optionally include AI-driven features to boost productivity, such as:
- suggestions and diagnostics for failures
- generation of test skeletons from descriptions/steps

---

## In Short
This project combines **test management** and an **E2E runner** into a single experience:
write/manage Playwright tests, version them, run them with one click, and inspect results and artifacts for debugging—both locally and in safer, more scalable infrastructure setups.
