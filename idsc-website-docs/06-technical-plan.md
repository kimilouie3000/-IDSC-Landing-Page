# 6. Technical Implementation Plan

## 6.1 Implementation status
This is an implementation plan, not a verified inventory of the current application. Confirm the repository's actual framework, folder layout, API, and database before treating any recommendation below as existing functionality.

The broader project context identifies React, Node.js/Express, and MongoDB as the intended stack. The website's page content and visual design must still be driven by Figma and the PowerPoint. If the repository or instructor specifies a different stack, follow the confirmed requirements and update this document.

## 6.2 Suggested frontend organization
If the project uses React, organize around reusable layout elements, page-level components, and a dedicated location for API calls. Adapt names to the existing source tree rather than replacing working conventions.

```text
src/
├── components/
│   ├── SiteHeader.jsx
│   ├── SiteFooter.jsx
│   ├── AnnouncementCard.jsx
│   ├── FacilityCard.jsx
│   └── OrganizationCard.jsx
├── layouts/
│   └── MainLayout.jsx
├── pages/
│   ├── HomePage.jsx
│   ├── AboutPage.jsx
│   ├── ProgramsPage.jsx
│   ├── AdmissionRequirementsPage.jsx
│   ├── TuitionFeesPage.jsx
│   ├── PaymentOptionsPage.jsx
│   ├── StudentOrganizationsPage.jsx
│   ├── ScholarshipsPage.jsx
│   ├── FacilitiesPage.jsx
│   └── NewsPage.jsx
├── services/
│   └── api.js
├── styles/
│   └── design-tokens.css
└── assets/
```

This is a suggested structure. Keep the project's established structure unless there is a clear reason to change it.

## 6.3 Shared layout
Build the header and footer once and reuse them on all pages. Keep navigation data in one place if possible so labels and destinations do not drift. Confirm dropdowns and routes before implementation.

## 6.4 Conceptual data models
If a backend is required, these are possible content types, not a finalized schema.

### Announcement
- `id`
- `title`
- `body` or `summary`
- `category` (`announcement` or `advisory`)
- `publishedAt`
- `status`
- Optional `imageUrl` and `slug`

### Program
- `id`
- `name`
- `level` (only values agreed by the project)
- `description`
- Optional `imageUrl`
- `status`

### Facility
- `id`
- `name`
- `group` (laboratory, academic space, or specialized space)
- `description`
- Optional `imageUrl`

### Student organization
- `id`
- `name`
- `description`
- Optional `imageUrl`
- Optional public `contact`, if approved

### Scholarship or privilege
- `id`
- `name`
- `type`
- `description`
- `eligibility`
- `applicationInstructions`
- Optional validity period or dates
- `status`

Admission requirements and tuition figures change over time. If stored as data, include an applicable academic year/effective date and a clear update process. Do not invent amounts or requirements.

## 6.5 API considerations
If a Node.js/Express API is used:
- Keep routes separate from business logic and database access.
- Validate input on the server.
- Return consistent JSON shapes and suitable HTTP status codes.
- Store database connection details in server-side environment variables.
- Do not put database credentials in React environment variables.
- Document the API contract if frontend and backend are developed separately.

Possible read endpoints, subject to approval:
- `GET /api/v1/announcements`
- `GET /api/v1/announcements/:id`
- `GET /api/v1/programs`
- `GET /api/v1/facilities`
- `GET /api/v1/organizations`
- `GET /api/v1/scholarships`

These endpoints are proposals only. A static informational site may not need all of them.

## 6.6 MongoDB considerations
If MongoDB is approved, use it for content that benefits from centralized updates or querying. Avoid duplicating the same shared content across documents.

Safeguards:
- Validate required fields before writing.
- Store dates consistently.
- Add indexes where query patterns justify them.
- Keep credentials in server-side environment variables.
- Use a least-privilege database account.
- Back up important content and define who may edit it.
- Do not store payment card details or sensitive application documents as part of a basic public-information website.

## 6.7 Static content versus database
Static content may be enough if developers handle updates. A database becomes useful when staff need to update announcements, fees, programs, or other content without changing application code. Decide based on the real update workflow and record the decision.

## 6.8 Environment configuration
- Commit a safe `.env.example` if environment variables are used.
- Keep real `.env` files out of version control.
- Never put database credentials, private tokens, or secret keys in frontend variables.
- Document required variables and startup commands in the repository's existing setup instructions.
- Do not alter unrelated configuration files as part of this documentation work.

## 6.9 Error and empty states
For dynamic pages, define:
- **Loading:** request is in progress.
- **Success:** content is displayed.
- **Empty:** no published items are available.
- **Error:** request failed, with a useful retry or contact path.

A failed announcement request should not make the entire home page unusable.
