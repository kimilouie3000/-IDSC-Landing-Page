# 2. Information Architecture

## 2.1 Shared site structure

The PowerPoint shows a repeated header and footer on the home page and detail-page mockups. Keep these shared elements consistent so visitors can move between sections without having to relearn the site.

### Header
The presentation shows:
- School name: **INFOTECH DEVELOPMENT SYSTEM COLLEGES, INC.**
- Tagline: **Empowering Futures with Dedicated Service**
- Main navigation: **PROGRAMS, STUDENTS, FACILITIES, ABOUT IDSC, ADMISSION, NEWS**
- **Apply Now** button
- Small upward-chevron marks beside or under navigation items in the mockup. Inspect Figma to determine their intended behavior and appearance.

Do not assume every navigation item opens a dropdown. Confirm the behavior in Figma or with the project owner. If dropdowns are used, make them usable by mouse, keyboard, and touch.

### Footer
The PowerPoint shows:
- IDSC, INC branding
- Copyright text: `© 2008-2026 Infotech Development System Colleges, Inc.`
- A note that visitors may visit the school Monday–Friday, 8:00 AM–4:00 PM
- Email: `idscollegensinc@gmail.com`
- Phone: `09178812683`

These are source values from the supplied presentation, not independently verified current details. Confirm the office schedule, email, phone number, and copyright year before release. If appropriate, generate the copyright year dynamically.

## 2.2 Proposed page hierarchy
This hierarchy organizes items named in the presentation. It is a proposal; confirm the final dropdown structure and URLs.

```text
Home
├── Programs
│   ├── College Courses
│   └── Senior High School
├── Students
│   ├── Student Organizations
│   ├── Student Scholarships
│   └── Student Privileges
├── Facilities
│   ├── Laboratories
│   │   ├── CSS Laboratory
│   │   ├── Criminology Laboratory
│   │   └── HM Laboratory
│   ├── Academic Spaces
│   │   ├── Library
│   │   └── G-Hall
│   └── Specialized Spaces
│       ├── Clinic
│       └── Mock Hotel
├── About IDSC
│   ├── About the School
│   ├── Vision, Mission, and Core Values
│   ├── IDSC Hymn
│   └── Career
├── Admission
│   ├── Admission Requirements
│   ├── Estimated Tuition Fee
│   └── Alternative Payment Service
└── News
    ├── Announcements
    └── Advisories
```

The PowerPoint also shows **IDSC Pulse** near the home-page news area. Treat this as the label or identity for the news/announcement section unless the owner confirms it is a separate page.

## 2.3 Suggested URL plan
These are proposed paths, not existing routes verified in the repository.

| Page | Suggested path |
|---|---|
| Home | `/` |
| College courses | `/programs/college-courses` |
| Senior High School | `/programs/senior-high-school` |
| About IDSC | `/about` |
| Vision, Mission, and Core Values | `/about/vision-mission-values` |
| IDSC Hymn | `/about/hymn` |
| Career | `/about/careers` |
| Admission requirements | `/admission/requirements` |
| Estimated tuition fee | `/admission/tuition-fees` |
| Alternative payment service | `/admission/payment-options` |
| Student organizations | `/students/organizations` |
| Student scholarships | `/students/scholarships` |
| Student privileges | `/students/privileges` |
| Laboratories | `/facilities/laboratories` |
| Academic spaces | `/facilities/academic-spaces` |
| Specialized spaces | `/facilities/specialized-spaces` |
| News and announcements | `/news` |

## 2.4 Main visitor journeys

### Prospective student
1. Open the home page.
2. Explore College Courses or Senior High School.
3. Open Admission Requirements.
4. Review Estimated Tuition Fee and Alternative Payment Service.
5. Select Apply Now.
6. Follow the confirmed application instructions or external application link.

### Parent or guardian
1. Open Admission.
2. Review requirements and estimated fees.
3. Read payment information.
4. Use the published contact information to ask about details not covered.

### Current student
1. Open Students.
2. Review organizations, scholarships, and privileges.
3. Open News to check announcements and advisories.

### Visitor interested in facilities
1. Open Facilities.
2. Choose Laboratories, Academic Spaces, or Specialized Spaces.
3. Read each description and view approved photographs.

## 2.5 Navigation rules
- Use the same header and footer on every main page.
- Show a clear page title on each detail page.
- Make the current section understandable without relying on color alone.
- Every navigation item must lead somewhere useful; do not leave `#` links in the finished site.
- If a page is not ready, do not present it as complete. Hide it from primary navigation or show an approved “coming soon” state.
- On small screens, use a mobile navigation control with an accessible name and visible open/closed state.
