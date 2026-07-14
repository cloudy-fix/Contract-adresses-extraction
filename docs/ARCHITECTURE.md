# Contract Address Extraction Architecture

## Purpose

Practice project for extracting contract addresses and normalizing them for review.

## Stack

Document processing concept, information extraction

## System Context

```mermaid
flowchart LR
    User["Contract text or document"] --> App["Address extraction workflow"]
    App --> Data["Contract clauses and address fields"]
    App --> Output["Structured address records"]
    Data --> Output
```
## Runtime Workflow

```mermaid
flowchart TD
    S1["Collect contract text"] --> S2["Detect address-like sections"]
    S2["Detect address-like sections"] --> S3["Normalize extracted fields"]
    S3["Normalize extracted fields"] --> S4["Review uncertain matches"]
    S4["Review uncertain matches"] --> S5["Export structured output"]
```
## Production Readiness Notes

- Keep secrets in environment variables and commit only .env.example templates.
- Keep generated files, dependency folders, caches, and local databases out of version control.
- Run the GitHub Actions workflow before presenting or deploying changes.
- Update this document when the source layout, dependencies, or deployment model changes.

## Review Checklist

- Architecture diagram matches current source files.
- Workflow diagram matches the main user or data path.
- README links to this architecture document.
- CI workflow validates the project on every push and pull request.

