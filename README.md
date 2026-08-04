# Gradescope (gradescope)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
