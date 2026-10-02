# 7. Testing and Acceptance

## 7.1 Visual review against Figma
Review each page against the supplied Figma design at the same or closest available viewport size.

- [ ] Header height, alignment, school identity, and navigation match the reference.
- [ ] Apply Now appearance and placement match the reference.
- [ ] Hero layout, text placement, and image crop match the reference.
- [ ] Typography, colors, spacing, borders, and corner radii use verified Figma values.
- [ ] Announcement/advisory cards follow the reference's visual hierarchy.
- [ ] Footer layout and contact information are consistent.
- [ ] Detail pages reuse the shared header and footer.
- [ ] Mobile layout remains usable and does not simply shrink the desktop layout.

Do not mark visual review complete until the actual Figma frame has been inspected.

## 7.2 Functional test cases

| ID | Test | Expected result |
|---|---|---|
| TC-01 | Open the home page | Page loads without a blocking error and shows approved school identity. |
| TC-02 | Select each primary navigation item | Correct page or approved submenu opens. |
| TC-03 | Use navigation with a keyboard | Links and menu controls can be reached and activated without a mouse. |
| TC-04 | Select Apply Now | The approved application destination opens. |
| TC-05 | Open an announcement | Full content is readable or its approved destination opens. |
| TC-06 | View an advisory card | Category and publication date are clear. |
| TC-07 | Open Admission Requirements | Latest school-approved list is shown. |
| TC-08 | Open Estimated Tuition Fee | Academic year and confirmed fee information are visible. |
| TC-09 | Open Alternative Payment Service | Only verified methods and instructions are shown. |
| TC-10 | Open student organization details | Names, descriptions, and images are correct. |
| TC-11 | Open scholarship information | Eligibility and application details match approved material. |
| TC-12 | Open a facilities page | Each facility has the correct name, description, and image. |
| TC-13 | Test a page with no news items | A clear empty state appears; no fake placeholder cards are shown. |
| TC-14 | Simulate a failed data request | Useful error state appears and shared layout remains usable. |
| TC-15 | Check footer contact information | Email, phone, office hours, and copyright details are approved/current. |
| TC-16 | Test at 375 px, 768 px, and 1280 px | Content is readable, controls do not overlap, and no horizontal scrolling occurs. |
| TC-17 | Inspect images with a screen reader | Informative images have meaningful alternative text. |
| TC-18 | Check all visible links | No unintended dead links, `#` placeholders, or unrelated destinations remain. |

## 7.3 Content review
Before release, ask an authorized school representative to verify:
- [ ] School name and tagline
- [ ] Vision, mission, and core values
- [ ] Program and Senior High School details
- [ ] Admission requirements and deadlines
- [ ] Tuition estimates and applicable academic year
- [ ] Payment services and instructions
- [ ] Scholarship and student-privilege information
- [ ] Organization names and descriptions
- [ ] Facility names and descriptions
- [ ] Announcement/advisory text and dates
- [ ] Contact details and office hours
- [ ] Photos, logos, hymn media, and permission to publish

## 7.4 Accessibility review
- [ ] Every form field, if any, has a visible label.
- [ ] Keyboard focus is visible.
- [ ] Menus can be opened and closed without a mouse.
- [ ] Heading levels follow a logical order.
- [ ] Color is not the only way to identify categories or status.
- [ ] Text contrast is sufficient.
- [ ] Images have appropriate alt text.
- [ ] Interactive controls have meaningful accessible names.

## 7.5 Definition of done
A page is ready when:
1. Its content is approved or remaining placeholders are withheld from publication.
2. Its layout has been checked against Figma.
3. Its links and controls work.
4. It is usable at desktop and mobile widths.
5. Loading, empty, and error states are handled if it loads data.
6. No unverified fee, admission, scholarship, or payment claim is presented as official.
7. The team knows who is responsible for updating time-sensitive content.
