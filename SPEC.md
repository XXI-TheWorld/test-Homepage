# Personal Link Page Specification

## Project Overview
- **Project name**: LinkPage
- **Type**: Single-page personal link hub (Terminal/Command-line style)
- **Core functionality**: Display personal profile with social media links
- **Target users**: Personal use / portfolio

## Visual Specification

### Style: Terminal / Command Line
- Pure black background (#000000)
- Neon green text (#00ff41) with glow effect
- Monospace font (JetBrains Mono)
- Dashed borders, no rounded corners

### Layout
- Left-aligned content within centered container, max-width 520px
- Vertical stack: Avatar → Name → Bio → Section Label → Links
- Full viewport height, centered with flexbox
- Responsive padding: 24px mobile, 32px desktop

### Color Palette
- Background: `#000000` (pure black)
- Primary text: `#00ff41` (neon green)
- Dim text: `#00cc33` (darker green)
- Border: `#00cc33`

### Typography
- Font: "JetBrains Mono", monospace
- Name: 1.5rem, font-weight 700, text-shadow glow
- Bio: 0.875rem, dim green, command prompt style ($)
- Links: 0.9375rem, font-weight 500

### Components

**Avatar**
- Size: 80px × 80px
- Circular with green border
- Display initials (2 chars max)
- Green text with glow

**Link Buttons**
- Full width within container
- Height: 44px
- Border: 1px dashed green
- Background: transparent (hover: solid green fill)
- `> ` prefix via CSS ::before
- Hover: invert colors, text blinks

**Icons**
- Size: 20px
- Green fill (inverts to black on hover)

## Interaction Specification
- Hover: background fills green, text turns black, glow effect
- Text blinks on hover via CSS animation
- Active state: slight scale down (0.98)
- Smooth transitions (150ms)

## Acceptance Criteria
- [ ] Terminal aesthetic with green monospace font
- [ ] Pure black background
- [ ] Links have > prefix
- [ ] Text blinks on hover
- [ ] All 5 social links with correct icons
- [ ] Responsive layout works on mobile and desktop
