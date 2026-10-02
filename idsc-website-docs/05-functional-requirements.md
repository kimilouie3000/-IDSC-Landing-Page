# 5. Functional and Quality Requirements

## 5.1 Functional requirements
These requirements describe expected behavior based on the PowerPoint and page plan. They are targets for implementation and testing, not a claim that the repository already contains them.

| ID | Requirement | Priority | Acceptance condition |
|---|---|---|---|
| FR-01 | Show IDSC name and tagline in the shared header or approved hero area. | Must | Identity is visible and matches approved wording. |
| FR-02 | Provide Programs, Students, Facilities, About IDSC, Admission, and News navigation. | Must | Each item reaches its intended page or approved submenu. |
| FR-03 | Provide an Apply Now call to action. | Must | It opens the destination approved by the project owner. |
| FR-04 | Present a featured area on the home page. | Must | It follows Figma and uses approved content/assets. |
| FR-05 | Display announcements and advisories with category and date. | Must | Each item has correct content and readable category/date. |
| FR-06 | Provide an About IDSC page. | Must | It contains school-approved description content. |
| FR-07 | Provide admission requirements. | Must | Only the current, approved checklist is shown. |
| FR-08 | Provide estimated tuition information. | Must | Figures have an applicable academic year and are confirmed. |
| FR-09 | Provide alternative payment information. | Must | Instructions and providers are verified by the school. |
| FR-10 | Present student organizations. | Should | Each item has an approved name, description, and image if available. |
| FR-11 | Present scholarship and student-privilege information. | Should | Eligibility and application details are accurate and approved. |
| FR-12 | Present laboratories and other named facilities. | Should | Each facility is correctly named and described. |
| FR-13 | Show consistent footer contact information. | Must | Current contact details and office hours are verified. |
| FR-14 | Support small-screen layouts. | Must | No overlap or horizontal scrolling at agreed test widths. |
| FR-15 | Provide loading, empty, and error feedback for dynamically loaded content. | Should | The page remains understandable when content is unavailable. |

## 5.2 Content management
The PowerPoint does not specify how staff will update news, fees, scholarships, or other information. Choose and document one approach:
1. **Static content:** developers update source files and redeploy.
2. **Data-backed content:** pages read content from a backend/database.
3. **Admin-managed content:** authorized staff use a protected management interface.

Do not build an admin portal or authentication system unless it is within the agreed scope. If dynamic content is required, define who can create, edit, publish, archive, and delete each content type.

## 5.3 Data freshness
The following content can become outdated and needs an identified owner:
- Tuition estimates
- Admission requirements and deadlines
- Payment methods
- Scholarship eligibility and deadlines
- Announcements and advisories
- Office hours, email, and phone number
- Program and facility descriptions

For changing content, store or display a last-updated date where appropriate. The date should reflect the actual update.

## 5.4 Non-functional requirements

### Usability
Visitors should be able to reach admission information from the navigation without guessing where it is located.

### Responsive design
The site should work on desktop, tablet, and phone widths. Test at least 375 px, 768 px, and 1280 px viewport widths.

### Accessibility
Use semantic HTML, keyboard-accessible navigation, visible focus indicators, image alt text, meaningful labels, and sufficient contrast.

### Performance
Optimize image sizes, avoid loading unnecessary large assets, and do not add libraries for functionality already supported by the current stack.

### Reliability
Every visible link and button must have a defined result. Handle missing content and failed data requests with clear feedback.

### Maintainability
Keep shared layout elements reusable and separate page content from repeated presentation where practical.

### Security and privacy
Do not collect personal, application, or payment information without an approved protection process. Never expose database credentials or private API keys in frontend code.

## 5.5 Content rules
- Use official names and exact school-approved statements.
- Do not publish invented fees, deadlines, requirements, scholarship benefits, or payment instructions.
- Remove placeholders such as `EXAMPLE`, `(Description)`, and `(Template)` before public release.
- Verify spelling and capitalization of school and facility names.
- Keep announcement dates and academic years accurate.
