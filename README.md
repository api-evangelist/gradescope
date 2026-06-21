# Gradescope (gradescope)

Gradescope, a Turnitin company, is an assessment and grading platform for paper-based, digital, and code assignments used across higher education and K-12. It does not publish a generally available public REST API; programmatic integration is delivered through LTI 1.3 / LTI Advantage (roster and grade sync with Canvas, Blackboard, Brightspace/D2L, Moodle, and Sakai) and a documented autograder framework for code assignments. A first-party public API for courses, assignments, submissions, and grades is a published feature request but is not yet generally available.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/gradescope/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/gradescope/refs/heads/main/apis.yml)

## Tags

- Education
- EdTech
- Grading
- Assessment
- LTI

## Timestamps

- **Created:** 2026-06-21
- **Modified:** 2026-06-21

## APIs

### Gradescope LTI Integration

Gradescope's primary supported integration surface. Implements the 1EdTech LTI 1.3 / LTI Advantage standard, including Names and Role Provisioning Services (NRPS) for roster sync, Assignment and Grade Services (AGS) for gradebook column creation and grade passback, and Deep Linking for creating Gradescope assignments from within an LMS. Endpoints are negotiated per LMS tool deployment rather than exposed as a fixed first-party REST API.

- **Human URL:** [https://guides.gradescope.com/hc/en-us/articles/21746234461197-LTI-1-3-and-Advantage-FAQ](https://guides.gradescope.com/hc/en-us/articles/21746234461197-LTI-1-3-and-Advantage-FAQ)
- **Base URL:** `https://www.gradescope.com`

#### Tags

- LTI
- LTI Advantage
- Roster Sync
- Grade Passback

#### Properties

- [Documentation](https://guides.gradescope.com/hc/en-us/articles/21746234461197-LTI-1-3-and-Advantage-FAQ)
- [OpenAPI](openapi/gradescope-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/gradescope.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/gradescope.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Gradescope Courses API

Course and roster data. Gradescope does not expose a generally available public REST endpoint for listing or managing courses; course roster provisioning happens through LTI 1.3 NRPS during LMS sync. A first-party public API for course access is a documented feature request but is not yet available.

- **Human URL:** [https://guides.gradescope.com/hc/en-us/articles/36028522325901-Gradescope-Public-API](https://guides.gradescope.com/hc/en-us/articles/36028522325901-Gradescope-Public-API)
- **Base URL:** `https://www.gradescope.com`

#### Tags

- Courses
- Roster

#### Properties

- [Documentation](https://guides.gradescope.com/hc/en-us/articles/36028522325901-Gradescope-Public-API)
- [OpenAPI](openapi/gradescope-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/gradescope.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/gradescope.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Gradescope Assignments API

Assignment configuration and the autograder framework for code assignments. The documented programmatic contract is a Docker-based autograder that reads student submissions and emits a results.json file (via the gradescope-utils Python package); there is no generally available public REST endpoint for creating or listing assignments. Assignment creation from an LMS is supported via LTI Deep Linking.

- **Human URL:** [https://gradescope-autograders.readthedocs.io/en/latest/specs/](https://gradescope-autograders.readthedocs.io/en/latest/specs/)
- **Base URL:** `https://www.gradescope.com`

#### Tags

- Assignments
- Autograder

#### Properties

- [Documentation](https://gradescope-autograders.readthedocs.io/en/latest/specs/)
- [OpenAPI](openapi/gradescope-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/gradescope.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/gradescope.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Gradescope Submissions API

Submission handling. Code submissions are processed inside the autograder container, where the submission is mounted and graded according to the autograder specification. Gradescope does not publish a generally available public REST endpoint for downloading or uploading submissions; this capability is part of the published public-API feature request.

- **Human URL:** [https://gradescope-autograders.readthedocs.io/en/latest/specs/](https://gradescope-autograders.readthedocs.io/en/latest/specs/)
- **Base URL:** `https://www.gradescope.com`

#### Tags

- Submissions
- Autograder

#### Properties

- [Documentation](https://gradescope-autograders.readthedocs.io/en/latest/specs/)
- [OpenAPI](openapi/gradescope-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/gradescope.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/gradescope.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Gradescope Grades API

Grade data and gradebook sync. Grades are pushed to an LMS gradebook through LTI 1.3 Assignment and Grade Services (AGS) rather than a first-party public REST API. Programmatic export/import of grades outside of LTI is a documented feature request that is not yet generally available.

- **Human URL:** [https://guides.gradescope.com/hc/en-us/articles/21746234461197-LTI-1-3-and-Advantage-FAQ](https://guides.gradescope.com/hc/en-us/articles/21746234461197-LTI-1-3-and-Advantage-FAQ)
- **Base URL:** `https://www.gradescope.com`

#### Tags

- Grades
- Gradebook
- Grade Passback

#### Properties

- [Documentation](https://guides.gradescope.com/hc/en-us/articles/21746234461197-LTI-1-3-and-Advantage-FAQ)
- [OpenAPI](openapi/gradescope-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/gradescope.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/gradescope.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/gradescope)
- [LinkedIn](https://www.linkedin.com/products/turnitin-gradescope/)
- [Website](https://www.gradescope.com)
- [Documentation](https://guides.gradescope.com/hc/en-us)
- [Plans](plans/gradescope-plans-pricing.yml)
- [Rate Limits](rate-limits/gradescope-rate-limits.yml)
- [Fin Ops](finops/gradescope-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
