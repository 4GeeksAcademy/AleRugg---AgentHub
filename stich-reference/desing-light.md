---
name: AgentHub Modern SaaS
colors:
  surface: '#faf8ff'
  surface-dim: '#d2d9f4'
  surface-bright: '#faf8ff'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#f2f3ff'
  surface-container: '#eaedff'
  surface-container-high: '#e2e7ff'
  surface-container-highest: '#dae2fd'
  on-surface: '#131b2e'
  on-surface-variant: '#464555'
  inverse-surface: '#283044'
  inverse-on-surface: '#eef0ff'
  outline: '#777587'
  outline-variant: '#c7c4d8'
  surface-tint: '#4d44e3'
  primary: '#3525cd'
  on-primary: '#ffffff'
  primary-container: '#4f46e5'
  on-primary-container: '#dad7ff'
  inverse-primary: '#c3c0ff'
  secondary: '#4648d4'
  on-secondary: '#ffffff'
  secondary-container: '#6063ee'
  on-secondary-container: '#fffbff'
  tertiary: '#004c76'
  on-tertiary: '#ffffff'
  tertiary-container: '#00659a'
  on-tertiary-container: '#bedfff'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#e2dfff'
  primary-fixed-dim: '#c3c0ff'
  on-primary-fixed: '#0f0069'
  on-primary-fixed-variant: '#3323cc'
  secondary-fixed: '#e1e0ff'
  secondary-fixed-dim: '#c0c1ff'
  on-secondary-fixed: '#07006c'
  on-secondary-fixed-variant: '#2f2ebe'
  tertiary-fixed: '#cce5ff'
  tertiary-fixed-dim: '#93ccff'
  on-tertiary-fixed: '#001d31'
  on-tertiary-fixed-variant: '#004b73'
  background: '#faf8ff'
  on-background: '#131b2e'
  surface-variant: '#dae2fd'
typography:
  headline-xl:
    fontFamily: Geist
    fontSize: 2.25rem
    fontWeight: '700'
    lineHeight: 2.75rem
    letterSpacing: -0.025em
  headline-xl-mobile:
    fontFamily: Geist
    fontSize: 1.75rem
    fontWeight: '700'
    lineHeight: 2.25rem
    letterSpacing: -0.02em
  headline-lg:
    fontFamily: Geist
    fontSize: 1.75rem
    fontWeight: '600'
    lineHeight: 2.25rem
    letterSpacing: -0.02em
  headline-lg-mobile:
    fontFamily: Geist
    fontSize: 1.375rem
    fontWeight: '600'
    lineHeight: 1.875rem
    letterSpacing: -0.015em
  headline-md:
    fontFamily: Geist
    fontSize: 1.25rem
    fontWeight: '600'
    lineHeight: 1.75rem
    letterSpacing: -0.015em
  headline-sm:
    fontFamily: Geist
    fontSize: 1rem
    fontWeight: '600'
    lineHeight: 1.5rem
    letterSpacing: -0.01em
  body-lg:
    fontFamily: Geist
    fontSize: 1rem
    fontWeight: '400'
    lineHeight: 1.625rem
  body-md:
    fontFamily: Geist
    fontSize: 0.875rem
    fontWeight: '400'
    lineHeight: 1.375rem
  body-sm:
    fontFamily: Geist
    fontSize: 0.75rem
    fontWeight: '400'
    lineHeight: 1.125rem
  label-md:
    fontFamily: Geist
    fontSize: 0.875rem
    fontWeight: '500'
    lineHeight: 1.25rem
  label-sm:
    fontFamily: Geist
    fontSize: 0.75rem
    fontWeight: '500'
    lineHeight: 1rem
    letterSpacing: 0.01em
  code-sm:
    fontFamily: JetBrains Mono
    fontSize: 0.75rem
    fontWeight: '400'
    lineHeight: 1.125rem
  code-xs:
    fontFamily: JetBrains Mono
    fontSize: 0.6875rem
    fontWeight: '500'
    lineHeight: 0.875rem
rounded:
  sm: 0.25rem
  DEFAULT: 0.5rem
  md: 0.75rem
  lg: 1rem
  xl: 1.5rem
  full: 9999px
spacing:
  gutter: 1.5rem
  gutter-mobile: 1rem
  margin: 2rem
  margin-mobile: 1rem
  space-xs: 0.25rem
  space-sm: 0.5rem
  space-md: 1rem
  space-lg: 1.5rem
  space-xl: 2rem
---

## Brand & Style

This design system embodies precise, high-velocity orchestration for enterprise AI and automation workstreams. Designed strictly for high-clarity Light Mode, it merges the crispness of modernist information architecture with technical utility.

### Visual Aesthetic & Philosophy
- **Modern Enterprise Precision:** Structured, scannable, and dense without feeling cramped. The interface prioritizes deep data density, high-contrast readability, and immediate affordance.
- **Architectural Clarity:** Layouts rely on structural borders, balanced slate canvas tones, and sharp surface delineations rather than heavy elevations or ornamental styling.
- **Controlled Accents:** A vivid indigo base commands attention only where agency, automation triggers, or primary actions occur; functional states (emerald, amber, rose) communicate operational health with strict contrast rules.

## Colors

The color palette is calibrated for high-contrast accessibility (WCAG AAA for body text, AA for functional interactive states) across light environments.

### Canvas & Surface Hierarchy
- **Base Canvas (`#f8fafc` - Slate 50):** The primary application canvas providing low-glare depth behind white content containers.
- **Surface Elevation 0 (`#ffffff`):** Dedicated to primary cards, active panels, table rows, and interactive canvas boards.
- **Surface Muted / Inset (`#f1f5f9` - Slate 100):** Table headers, inactive card wells, side rail bars, and read-only code/terminal regions.
- **Structural Outlines (`#e2e8f0` - Slate 200):** Crisp divider lines, card boundaries, input strokes, and grid columns.
- **Interactive Hover Borders (`#cbd5e1` - Slate 300):** Elevated boundary state for hovered cards and unfocused active inputs.

### Typography & Content Tokens
- **Text Headings / Crucial (`#0f172a` - Slate 900):** Highest contrast tier for all primary numbers, agent titles, and table metrics.
- **Text Body / Standard (`#334155` - Slate 700):** Core body copy, table text, and form labels.
- **Text Secondary / Utility (`#64748b` - Slate 500):** Captions, breadcrumb separators, metadata, and empty state subtitles.

### Accents & Operational States
- **Primary Brand / Action (`#4f46e5` - Indigo 600):** Primary CTA, active workflow routes, toggled state backgrounds.
- **Primary Hover / Focus (`#4338ca` - Indigo 700 / `#6366f1` - Indigo 500):** Focused rings and interactive states.
- **Operational Success (`#059669` - Emerald 600 / Surface: `#ecfdf5`):** Running agents, validated tests, healthy deployment nodes.
- **Operational Warning (`#d97706` - Amber 600 / Surface: `#fffbeb`):** Pending approvals, rate-limit warnings, degraded performance.
- **Operational Danger (`#e11d48` - Rose 600 / Surface: `#fff1f2`):** Errored traces, stopped agents, decommission alerts.

## Typography

The type hierarchy is powered by **Geist** for crisp UI rendering and data density, supported by **JetBrains Mono** for payload structures, logs, agent keys, and metric values.

### Usage Rules
- **Numerical Regularity:** For metrics and table figures set in Geist, enable tabular figures (`font-variant-numeric: tabular-nums`) to prevent horizontal jitter during live telemetry updates.
- **Hierarchy Enforcement:** Headline levels must always leverage tight negative tracking (`-0.015em` to `-0.025em`) to ensure titles hold structural density against expansive canvas regions.
- **Labels vs. Code:** Use `label-sm` for UI badges, metadata labels, and form titles. Reserve `code-sm` and `code-xs` exclusively for execution runtimes, JSON inspect windows, latency timers, and API endpoints.

## Layout & Spacing

The layout model operates on an 8px base rhythm, pairing a fluid modular dashboard container with structured responsive reflow patterns.

### Breakpoint Architecture
- **Desktop (1280px+):** Collapsible 256px sidebar navigation, dynamic multi-column workbench canvas, fixed 1.5rem (`24px`) grid gutters, 2rem (`32px`) canvas margin.
- **Tablet (768px - 1279px):** Icon-only collapsed rail (64px width), 2-column card reflows, gutters scale down to 1.25rem (`20px`).
- **Mobile (< 768px):** Off-canvas drawer navigation, single-column vertical flow, 1rem (`16px`) margin and gutter.

### Grid & Component Padding
- **Card Containers:** Internal padding scales strictly using `space-md` (`16px`) for standard cards and `space-lg` (`24px`) for primary hero telemetry panels.
- **Data Tables:** Dense horizontal padding of `space-md` with concise vertical cell padding of `space-sm` (`8px`) to ensure optimal scan density.

## Elevation & Depth

This design system favors **structural layering** over dramatic drop shadows. Visual depth is established through micro-borders, surface luminance contrast, and delicate ambient light occlusion.

### Surface Tiers
- **Layer 0 (Canvas Base):** Hex `#f8fafc`. Receded environment for dashboard backdrop and canvas workspaces.
- **Layer 1 (Card & Module Shells):** Hex `#ffffff` bound by a solid `1px` stroke of `#e2e8f0`.
- **Layer 2 (Overlays & Drawers):** Hex `#ffffff` bound by `#cbd5e1`, supported by an ambient drop shadow: `0 10px 15px -3px rgba(15, 23, 42, 0.04), 0 4px 6px -4px rgba(15, 23, 42, 0.02)`.
- **Layer 3 (Modals & Command Palettes):** Hex `#ffffff` surrounded by `0 20px 25px -5px rgba(15, 23, 42, 0.08), 0 8px 10px -6px rgba(15, 23, 42, 0.04)` over a backdrop tint of `rgba(15, 23, 42, 0.4)` with `backdrop-filter: blur(4px)`.

### Border Integrity
Shadows never sit borderless. Every elevated component maintains a defined `1px` solid border (`#e2e8f0` or `#cbd5e1`) to protect perimeter definition against light backgrounds.

## Shapes

The geometric framework balances humanized softness with architectural precision using deliberate radius tiering:

- **Base Radius (`0.5rem` / `8px`):** Used for buttons, inputs, dropdown menus, chips, and segmented controls.
- **Container Radius (`rounded-lg` - `1rem` / `16px`):** Used for metric widgets, run cards, workflow blocks, and code panels.
- **Overlay Radius (`rounded-xl` - `1.5rem` / `24px`):** Reserved for system modals, sliding drawers, and workflow canvas dialogs.
- **Pill (`9999px`):** Strictly reserved for dynamic execution status badges (e.g., "Active", "Queued", "Idle").

## Components

### Buttons
- **Primary:** Background `#4f46e5`, text `#ffffff`, border transparent. Hover: `#4338ca`. Active: scale 0.99 with ring focus `ring-2 ring-indigo-500/20`.
- **Secondary / Outline:** Background `#ffffff`, text `#0f172a`, border `1px solid #e2e8f0`. Hover: background `#f8fafc`, border `#cbd5e1`.
- **Ghost:** Background transparent, text `#334155`. Hover: background `#f1f5f9`, text `#0f172a`.
- **Destructive:** Background `#fff1f2`, text `#e11d48`, border `1px solid #fecdd3`. Hover: background `#ffe4e6`.

### Inputs & Form Elements
- **Text Inputs:** Background `#ffffff`, border `1px solid #e2e8f0`, text `#0f172a`, placeholder `#94a3b8`, height `2.5rem` (`40px`), padding `0 0.75rem`. Focus: border `#4f46e5`, box-shadow `0 0 0 3px rgba(79, 70, 229, 0.12)`.
- **Checkboxes & Radios:** Unchecked: border `1.5px solid #cbd5e1`, background `#ffffff`. Checked: background `#4f46e5`, check icon `#ffffff`. Focus: ring `2px` indigo offset.

### Chips & Status Badges
- **Status Badges (Pill):** Height `1.5rem` (`24px`), font `label-sm`, padding `0 0.625rem`.
  - *Active / Success:* Background `#ecfdf5`, text `#047857`, border `1px solid #a7f3d0`.
  - *Warning:* Background `#fffbeb`, text `#b45309`, border `1px solid #fde68a`.
  - *Error:* Background `#fff1f2`, text `#be123c`, border `1px solid #fecdd3`.
  - *Neutral / Idle:* Background `#f1f5f9`, text `#475569`, border `1px solid #e2e8f0`.

### Cards & Data Panels
- **Standard Card:** Background `#ffffff`, border `1px solid #e2e8f0`, border-radius `rounded-lg` (`16px`), padding `space-md` or `space-lg`.
- **Interactive Card:** Transitions border color to `#cbd5e1` and adds subtle hover lift (`translate-y-[-1px]`) with shadow `0 4px 6px -1px rgba(15, 23, 42, 0.05)`.

### Lists & Tables
- **Table Container:** Outer border `1px solid #e2e8f0`, border-radius `rounded-lg`, overflow hidden.
- **Header Cells:** Background `#f8fafc`, text `#475569`, font `label-sm`, border-bottom `1px solid #e2e8f0`, text-transform uppercase, tracking wide.
- **Row Styling:** Background `#ffffff`, border-bottom `1px solid #f1f5f9`, hover background `#f8fafc`. Alternate row striping is omitted in favor of active row highlighting.

### Specialized AI / Agent Components
- **Agent Node Blocks:** Rounded-lg (`16px`) container with `#ffffff` body, `#f8fafc` header rail, and an operational status dot (8px circle with dynamic ping indicator).
- **Execution Run Log:** Monospace view (`JetBrains Mono`, `code-sm`), background `#f8fafc`, border `1px solid #e2e8f0`, text `#334155` with timestamp tokens highlighted in `#64748b`.