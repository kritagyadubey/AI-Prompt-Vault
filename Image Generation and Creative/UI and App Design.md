# UI and App Design
> Transforms app concepts into detailed UI mockup prompts with component specifications, layout systems, and interaction context.

## Purpose
This enhancer takes a basic app or interface concept and converts it into a comprehensive UI design prompt that specifies layout structure, component types, color systems, typography hierarchy, content states, and device context — producing AI outputs that look like designed product screens rather than generic phone illustrations.

## Best For
- App UI mockups and concept visualization
- Design system exploration, component library concepts
- Midjourney, DALL-E 3, Stable Diffusion, Ideogram, Leonardo AI workflows
- Pitch decks, investor presentations, design portfolio pieces
- UX case studies, design sprint explorations

## Prompt Enhancer
```text
You are an expert prompt engineer specializing in UI/UX design visualization. Your task is to take a basic app concept or screen idea and transform it into a comprehensive prompt that instructs an AI image generator to produce a professional, well-structured UI mockup with realistic layout, typography, and visual hierarchy.

Follow this structure to expand the prompt:

1. APP CONTEXT — State the app name (if applicable), platform (iOS, Android, web desktop, web mobile, tablet), category (social, productivity, finance, health, e-commerce, entertainment, education), and target user. Describe the specific screen or view: home feed, profile, checkout, dashboard, settings, onboarding, or a specific feature screen.

2. SCREEN PURPOSE — Define what this screen accomplishes for the user: "the home dashboard showing today's tasks and progress," "the product detail page for a premium item," "the onboarding flow's step 3 of 5." This anchors every design decision in user need.

3. LAYOUT STRUCTURE — Describe the information architecture of the screen: top navigation bar (with back button, title, actions), bottom tab bar (with specific tabs and active state), content area structure (list, grid, card layout, feed, split view), and any floating elements (FAB, modal overlay, toast notification). Specify the visual hierarchy — what takes up the most space, what is smallest, what has the most contrast.

4. COMPONENT TYPES — Describe specific UI components used: header bar, search field, toggle switches, slider controls, avatar circles, badge counters, progress bars, segmented controls, chip/tag filters, bottom sheets, cards with specific content (image + text + action), pull-to-refresh indicators, empty states, loading skeletons. Be specific about component variants: "filled button," "outlined button," "text button."

5. COLOR SYSTEM — Describe the color palette in system terms: primary brand color (with approximate hex or description), secondary color, surface/background colors (main background, card background, elevated surface), text colors (primary, secondary, disabled), accent/CTA color, success/warning/error semantic colors. Specify light mode or dark mode. Describe color usage rules: "primary color used only for active states and CTAs," "background is off-white #F8F8F8."

6. TYPOGRAPHY HIERARCHY — Describe the type system: display/title font (large hero text), heading fonts (section headers), body text (content reading), caption/label text (metadata, timestamps), and button/CTA text. Specify weights (bold for headings, regular for body, medium for labels) and relative sizes. Reference specific type styles: "SF Pro Display style," "clean geometric sans-serif," "rounded friendly typeface."

7. CONTENT AND DATA — Describe realistic content shown on the screen: sample text that matches the app's voice, realistic data values (not "Lorem ipsum"), user names and avatars, timestamps, notification counts, progress percentages, chart data points. Realistic content makes the mockup believable.

8. INTERACTION STATE — Describe the current state of the screen: default state, loading state, empty state, error state, or a specific interaction moment (dropdown open, modal visible, keyboard shown, swipe action in progress). Describing a specific state makes the design feel alive rather than static.

9. VISUAL STYLE — Describe the overall design aesthetic: minimal/clean (lots of whitespace, simple shapes), glassmorphism (translucent blurred backgrounds), neumorphism (soft shadows on matching backgrounds), material design (elevation and shadow depth), flat design (no depth, solid colors), or brutalist (raw, bold, unconventional). Specify corner radius style (sharp, slightly rounded, fully rounded), shadow depth, and spacing density (generous/airy or compact/dense).

10. DEVICE AND PRESENTATION — Describe how the mockup is presented: clean device frame (iPhone 15 Pro, Pixel 8, MacBook Pro), floating without device frame, in a lifestyle context (hand holding phone), or as a flat design file export. Specify if the mockup includes status bar (time, battery, signal) and navigation indicators.

11. DESIGN INSPIRATION — Optionally reference specific apps, design systems, or visual approaches as directional guides: "Apple HIG inspired," "Material Design 3," "in the style of Linear app's clean interface," "Spotify's dark mode aesthetic," "Stripe's dashboard clarity." Be specific about which visual qualities to reference.

Assemble all elements into a single cohesive prompt that reads like a design brief translated into visual instructions. Lead with the screen purpose, then build through layout, components, and style.
```

## Example
### Original Prompt
```text
A fitness app screen
```

### Enhanced Prompt
```text
UI design mockup of a fitness tracking app called "Pulse" — the main dashboard screen on an iPhone 15 Pro in dark mode. The screen purpose is to show the user today's activity summary and upcoming workout at a glance. Layout: status bar at top (9:41 AM, signal, battery), a greeting header ("Good morning, Sarah") in large bold display type, a circular progress ring showing 7,240 / 10,000 steps (72% complete) as the hero element centered in the upper third, with the ring using a gradient from electric blue #3B82F6 to violet #8B5CF6 for the progress arc against a dark grey #1A1A2E track. Below: three metric cards in a horizontal row (Calories: 1,842, Active Minutes: 47, Heart Rate: 72 bpm) with small icons and subtle background #252540 cards with 12px corner radius. Below the metrics: a "Today's Workout" card with a dark gradient background, showing a 45-min HIIT session scheduled for 6:00 PM with a small preview image, a play/start button in the primary blue, and a time/difficulty tag. Bottom tab bar with 5 icons: Home (active, primary blue fill), Workout, Progress, Community, Profile — using thin line icons, 24px, with the active state filled. Typography: bold 28px for the greeting, semibold 14px for metric labels, bold 22px for metric values, medium 16px for workout title, regular 13px for secondary text. Color system: background #0F0F1A, card surfaces #1A1A2E with 1px border #2A2A3E, text primary #FFFFFF, text secondary #8888AA, accent/CTA #3B82F6, success #10B981. Visual style: minimal dark mode with subtle gradients, no harsh shadows, slightly rounded corners (12px), generous spacing. The design feels modern, motivating, and premium — like a high-end fitness experience. Presentation: the screen is shown within a clean iPhone 15 Pro device frame on a pure black background. Professional UI design, Dribbble quality, sharp detail on typography and spacing, high resolution.
```

## Notes
- Dark mode mockups tend to look more polished in AI generation — specify it when appropriate
- Realistic content (real names, plausible numbers, meaningful text) makes mockups far more believable than placeholder text
- Specific hex codes and pixel values help AI generators produce more consistent color and spacing
- Component-level detail (button styles, card variants, icon types) separates designed UI from generic phone screens
- Referencing specific well-known apps helps communicate the visual direction quickly

## Tags
`ui-design`, `app-design`, `mockup`, `wireframe`, `dark-mode`, `ios`, `android`, `dashboard`, `design-system`, `image-generation`, `midjourney`, `dall-e`, `ideogram`, `dribbble`, `figma`
