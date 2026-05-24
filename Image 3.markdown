---
name: Modern Corporate Precision
colors:
  surface: '#f7f9fb'
  surface-dim: '#d8dadc'
  surface-bright: '#f7f9fb'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#f2f4f6'
  surface-container: '#eceef0'
  surface-container-high: '#e6e8ea'
  surface-container-highest: '#e0e3e5'
  on-surface: '#191c1e'
  on-surface-variant: '#434655'
  inverse-surface: '#2d3133'
  inverse-on-surface: '#eff1f3'
  outline: '#737686'
  outline-variant: '#c3c6d7'
  surface-tint: '#0053db'
  primary: '#004ac6'
  on-primary: '#ffffff'
  primary-container: '#2563eb'
  on-primary-container: '#eeefff'
  inverse-primary: '#b4c5ff'
  secondary: '#565e74'
  on-secondary: '#ffffff'
  secondary-container: '#dae2fd'
  on-secondary-container: '#5c647a'
  tertiary: '#46566c'
  on-tertiary: '#ffffff'
  tertiary-container: '#5e6e85'
  on-tertiary-container: '#e9f0ff'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#dbe1ff'
  primary-fixed-dim: '#b4c5ff'
  on-primary-fixed: '#00174b'
  on-primary-fixed-variant: '#003ea8'
  secondary-fixed: '#dae2fd'
  secondary-fixed-dim: '#bec6e0'
  on-secondary-fixed: '#131b2e'
  on-secondary-fixed-variant: '#3f465c'
  tertiary-fixed: '#d3e4fe'
  tertiary-fixed-dim: '#b7c8e1'
  on-tertiary-fixed: '#0b1c30'
  on-tertiary-fixed-variant: '#38485d'
  background: '#f7f9fb'
  on-background: '#191c1e'
  surface-variant: '#e0e3e5'
typography:
  headline-lg:
    fontFamily: Inter
    fontSize: 48px
    fontWeight: '700'
    lineHeight: 56px
    letterSpacing: -0.02em
  headline-lg-mobile:
    fontFamily: Inter
    fontSize: 32px
    fontWeight: '700'
    lineHeight: 40px
    letterSpacing: -0.02em
  headline-md:
    fontFamily: Inter
    fontSize: 24px
    fontWeight: '600'
    lineHeight: 32px
    letterSpacing: -0.01em
  body-lg:
    fontFamily: Inter
    fontSize: 18px
    fontWeight: '400'
    lineHeight: 28px
  body-md:
    fontFamily: Inter
    fontSize: 16px
    fontWeight: '400'
    lineHeight: 24px
  label-sm:
    fontFamily: Inter
    fontSize: 14px
    fontWeight: '500'
    lineHeight: 20px
    letterSpacing: 0.01em
  label-xs:
    fontFamily: Inter
    fontSize: 12px
    fontWeight: '600'
    lineHeight: 16px
    letterSpacing: 0.05em
rounded:
  sm: 0.125rem
  DEFAULT: 0.25rem
  md: 0.375rem
  lg: 0.5rem
  xl: 0.75rem
  full: 9999px
spacing:
  base: 4px
  xs: 8px
  sm: 16px
  md: 24px
  lg: 40px
  xl: 64px
  gutter: 24px
  margin-mobile: 16px
  container-max: 1280px
---

## Brand & Style
The design system is engineered for high-stakes professional environments where clarity, efficiency, and trust are paramount. It targets enterprise users and decision-makers who require a tool that feels authoritative yet effortless to navigate.

The aesthetic follows a **Modern Corporate** direction, blending minimalist principles with functional density. By prioritizing generous whitespace and a restricted color palette, the interface reduces cognitive load while highlighting critical data and primary actions. The emotional response is one of reliability, precision, and calm control.

## Colors
The palette is rooted in a "Global Blue" foundation, utilizing **#2563EB** as the singular driver for interactive intent and brand presence. 

- **Primary:** Used for call-to-action buttons, active states, and focus indicators.
- **Surface & Background:** The application utilizes a "White-on-Grey" strategy. The main background is **#F8FAFC** (Slate 50), while primary content containers use pure white to create natural separation without heavy borders.
- **Typography:** Headlines utilize **#0F172A** (Deep Navy) for maximum contrast, while secondary information uses **#64748B** (Slate) to establish a clear information hierarchy.

## Typography
This design system utilizes **Inter** exclusively to leverage its exceptional legibility and systematic rhythm. The type scale is built on a modular 8px grid to ensure vertical alignment across all components.

Headlines use semi-bold and bold weights with slight negative letter spacing to feel "locked in" and professional. Body text maintains a standard tracking for optimal readability in data-heavy views. Labels and small utility text use a medium weight to maintain legibility at smaller scales.

## Layout & Spacing
The layout follows a **Fixed Grid** philosophy for desktop environments to ensure a consistent reading experience, centering content within a 1280px container. 

- **Grid:** A 12-column system with 24px gutters.
- **Rhythm:** Spacing follows a strictly linear scale (4, 8, 16, 24, 40, 64). Use `md` (24px) for internal card padding and `lg` (40px) for section vertical margins.
- **Mobile:** The grid becomes fluid with 16px side margins. Elements reflow to a single column, with certain secondary actions moving to bottom sheets or simplified icon-only representations.

## Elevation & Depth
Hierarchy is established through **Ambient Shadows** and **Tonal Layering**. Instead of heavy borders, the design system uses subtle depth cues to separate the interface into three logical planes:

1.  **Level 0 (Background):** Slate 50. The "canvas" of the application.
2.  **Level 1 (Cards/Surfaces):** Pure White. These surfaces use a soft, low-opacity shadow (Color: Slate 900, Alpha: 0.05, Blur: 10px) and a subtle 1px border (#E2E8F0) to ensure crispness on all displays.
3.  **Level 2 (Modals/Popovers):** Pure White. These floating elements use a more pronounced shadow with a wider spread to suggest physical proximity to the user.

Interactions are signaled by elevation shifts; buttons slightly "lift" or darken on hover to provide tactile feedback without breaking the minimalist aesthetic.

## Shapes
The shape language is **Soft** and structured. A 0.25rem (4px) base radius is used for small components like checkboxes and input fields, while larger containers like cards and primary buttons use a 0.5rem (8px) radius. 

This approach balances the "industrial" feel of sharp corners with the modern, approachable feel of rounded corners. Avoid using pill-shapes (fully rounded) except for specific status indicators or badges to maintain the professional, corporate tone.

## Components

### Buttons
- **Primary:** Solid #2563EB with white text. 8px border radius. Use for the single most important action on a page.
- **Secondary:** White background with a #CBD5E1 border. Slate 800 text.
- **Ghost:** No background or border. Used for tertiary actions (e.g., "Cancel" or "Learn More").

### Cards
Cards are the primary organizational unit. They feature a white background, 8px corner radius, and a subtle #E2E8F0 border. Padding is fixed at 24px (`md`) to ensure internal content has room to breathe.

### Input Fields
Inputs use a white background with a 1px border. On focus, the border transitions to Primary Blue with a 3px soft outer glow (the focus ring) to provide clear visual confirmation. Labels are positioned above the field in `label-sm` typography.

### File Upload Zone
The file upload zone is a distinct component. It features a dashed border (2px width, 4px dash) in Slate 300, a light grey background (#F1F5F9), and a centered icon with a "Browse" link in Primary Blue. Upon drag-over, the background shifts to a very pale blue tint.

### Lists & Tables
Rows are separated by thin 1px horizontal lines (#F1F5F9). Zebra-striping is avoided; instead, use a subtle grey hover state on the entire row to assist in data tracking.