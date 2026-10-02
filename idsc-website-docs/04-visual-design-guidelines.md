# 4. Visual Design Guidelines

## 4.1 Source of truth
Use the supplied [Figma landing-page frame](https://www.figma.com/design/FZAJNJ2haU7k7oLjk7dCbd/Web-Design-Landing-Page?node-id=43-14&p=f&t=9zckf8pZxuh0vXXh-0) as the visual source of truth for the landing page. Use `Mockup_Planning.pptx` to understand the intended page set and repeated content areas.

The Figma frame could not be inspected automatically while preparing this document. This guide therefore does not specify guessed hex colors, font families, exact spacing values, image dimensions, or component measurements. Read those values from Figma before implementation.

## 4.2 Record the design tokens
Before styling pages, create a design-token reference from the actual Figma file.

| Token | Value to record from Figma | Use |
|---|---|---|
| Primary color | To be verified | Main brand actions and emphasis |
| Secondary color | To be verified | Supporting UI elements |
| Text color | To be verified | Body text and headings |
| Muted/background color | To be verified | Page backgrounds and secondary surfaces |
| Heading font | To be verified | Page and section headings |
| Body font | To be verified | Paragraphs, labels, and navigation |
| Base spacing unit | To be verified | Consistent margins and gaps |
| Border radius | To be verified | Cards, buttons, and panels |
| Button height/padding | To be verified | Consistent action controls |
| Content max width | To be verified | Readable desktop layout |
| Header behavior | To be verified | Static, sticky, or other behavior |
| Breakpoints | To be verified | Responsive layout changes |

Do not fill these entries from personal preference. Inspect Figma styles/components or ask the design owner.

## 4.3 Shared visual elements
The PowerPoint repeats the school identity, navigation, Apply Now button, and footer on multiple mockups. Implement these as shared components rather than copying separate versions into each page.

Suggested components:
- `SiteHeader`
- `PrimaryNavigation`
- `MobileNavigation`
- `ApplyNowButton`
- `PageTitle`
- `AnnouncementCard`
- `AdvisoryCard` or one reusable card with a category property
- `FacilityCard`
- `OrganizationCard`
- `SiteFooter`

These names are suggestions; follow the application's existing naming conventions.

## 4.4 Layout and spacing
- Follow the layout and content order visible in Figma.
- Keep text blocks readable and avoid overly long line lengths.
- Use a consistent spacing scale across cards, page sections, and navigation.
- Align cards and images consistently.
- Avoid adding decorative elements absent from the approved design unless approved.
- Preserve header/footer alignment across detail pages.

## 4.5 Images and cropping
The PowerPoint includes an admin-office image placeholder, organization images, facility templates, and a large home-page feature area.
- Use actual school-approved photographs where available.
- Do not treat placeholder labels as final image assets.
- Use consistent aspect ratios for cards in the same group.
- Choose image fit and positioning based on the reference composition.
- Provide useful alt text for informative images; use empty alt text for purely decorative images.
- Do not use a photo of one facility to represent another unless confirmed.

## 4.6 Typography and content
- Use font styles defined in Figma.
- Preserve official school wording for the tagline and official statements.
- Use a clear heading hierarchy: one main page heading followed by section headings.
- Avoid all caps for long paragraphs. Navigation can remain uppercase if it matches Figma.
- Check wrapping for long page names, announcements, and the Apply Now label.

## 4.7 Responsive behavior
The design must remain usable at narrow widths, even if the supplied frame focuses on desktop.
- Replace full navigation with an accessible menu on mobile if required.
- Keep Apply Now visible or easy to reach without covering other controls.
- Stack multi-column cards into a suitable narrow layout.
- Prevent horizontal scrolling.
- Avoid overlap between headings, dates, and card actions.
- Make footer contact information wrap cleanly.

## 4.8 Accessibility
- Maintain sufficient text/background contrast.
- Use semantic headings, navigation, main content, and footer landmarks.
- Ensure interactive elements work with a keyboard.
- Provide visible focus states.
- Use descriptive link labels.
- Do not rely on color alone to distinguish announcement categories.
- Respect reduced-motion preferences if animations are added.
