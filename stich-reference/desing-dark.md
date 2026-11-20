---
name: AgentHub
colors:
  surface: '#0b1326'
  surface-dim: '#0b1326'
  surface-bright: '#31394d'
  surface-container-lowest: '#060e20'
  surface-container-low: '#131b2e'
  surface-container: '#171f33'
  surface-container-high: '#222a3d'
  surface-container-highest: '#2d3449'
  on-surface: '#dae2fd'
  on-surface-variant: '#c7c4d7'
  inverse-surface: '#dae2fd'
  inverse-on-surface: '#283044'
  outline: '#908fa0'
  outline-variant: '#464554'
  surface-tint: '#c0c1ff'
  primary: '#c0c1ff'
  on-primary: '#1000a9'
  primary-container: '#8083ff'
  on-primary-container: '#0d0096'
  inverse-primary: '#494bd6'
  secondary: '#d0bcff'
  on-secondary: '#3c0091'
  secondary-container: '#571bc1'
  on-secondary-container: '#c4abff'
  tertiary: '#4edea3'
  on-tertiary: '#003824'
  tertiary-container: '#00885d'
  on-tertiary-container: '#000703'
  error: '#ffb4ab'
  on-error: '#690005'
  error-container: '#93000a'
  on-error-container: '#ffdad6'
  primary-fixed: '#e1e0ff'
  primary-fixed-dim: '#c0c1ff'
  on-primary-fixed: '#07006c'
  on-primary-fixed-variant: '#2f2ebe'
  secondary-fixed: '#e9ddff'
  secondary-fixed-dim: '#d0bcff'
  on-secondary-fixed: '#23005c'
  on-secondary-fixed-variant: '#5516be'
  tertiary-fixed: '#6ffbbe'
  tertiary-fixed-dim: '#4edea3'
  on-tertiary-fixed: '#002113'
  on-tertiary-fixed-variant: '#005236'
  background: '#0b1326'
  on-background: '#dae2fd'
  surface-variant: '#2d3449'
typography:
  display:
    fontFamily: Geist
    fontSize: 36px
    fontWeight: '600'
    lineHeight: 44px
    letterSpacing: -0.03em
  headline-lg:
    fontFamily: Geist
    fontSize: 30px
    fontWeight: '600'
    lineHeight: 38px
    letterSpacing: -0.025em
  headline-lg-mobile:
    fontFamily: Geist
    fontSize: 24px
    fontWeight: '600'
    lineHeight: 32px
    letterSpacing: -0.02em
  headline-md:
    fontFamily: Geist
    fontSize: 20px
    fontWeight: '600'
    lineHeight: 28px
    letterSpacing: -0.015em
  headline-sm:
    fontFamily: Geist
    fontSize: 16px
    fontWeight: '600'
    lineHeight: 24px
    letterSpacing: -0.01em
  body-lg:
    fontFamily: Geist
    fontSize: 16px
    fontWeight: '400'
    lineHeight: 24px
    letterSpacing: 0em
  body-md:
    fontFamily: Geist
    fontSize: 14px
    fontWeight: '400'
    lineHeight: 20px
    letterSpacing: -0.005em
  body-sm:
    fontFamily: Geist
    fontSize: 12px
    fontWeight: '400'
    lineHeight: 16px
    letterSpacing: 0em
  label-md:
    fontFamily: JetBrains Mono
    fontSize: 12px
    fontWeight: '500'
    lineHeight: 16px
    letterSpacing: 0.02em
  label-sm:
    fontFamily: JetBrains Mono
    fontSize: 11px
    fontWeight: '500'
    lineHeight: 14px
    letterSpacing: 0.03em
  label-xs:
    fontFamily: JetBrains Mono
    fontSize: 10px
    fontWeight: '600'
    lineHeight: 12px
    letterSpacing: 0.04em
rounded:
  sm: 0.25rem
  DEFAULT: 0.5rem
  md: 0.75rem
  lg: 1rem
  xl: 1.5rem
  full: 9999px
spacing:
  gutter: 1rem
  gutter-md: 1.5rem
  gutter-lg: 1.5rem
  margin: 1rem
  margin-md: 1.5rem
  margin-lg: 2rem
  space-xs: 0.25rem
  space-sm: 0.5rem
  space-md: 1rem
  space-lg: 1.5rem
  space-xl: 2rem
---

## Brand & Style

The design system establishes a high-density, performance-driven administrative environment tailored for technical operators, enterprise teams, and AI fleet managers. It balances utilitarian enterprise command-and-control with modern SaaS refinement. 

The aesthetic is precision-engineered, modern, and structural. It utilizes crisp bounding borders, deep slate/zinc neutral surfaces, and electric violet-indigo accents to evoke a feeling of autonomous intelligence, security, and real-time responsiveness. Interface patterns prioritize instantaneous readability, clear runtime status distinction, and structured analytical density over purely decorative elements.

## Colors

The system uses a calibrated palette designed for deep dark-mode immersion while fully supporting crisp light-mode execution. Neutral values rely on zinc-tinted slates to keep technical data readable and glare-free.

- **Primary (`#6366f1` / Indigo 500):** Anchors primary calls to action, focus rings, active navigation items, and deployed agent badges.
- **Secondary (`#8b5cf6` / Violet 500):** Designates automated orchestration, multi-agent clusters, and telemetry intelligence layers.
- **Functional Semantics:**
  - **Success / Active (`#10b981` / Emerald 500):** Running agent status, healthy inference latency, billable uptime, and positive delta values.
  - **Warning / Degraded (`#f59e0b` / Amber 500):** Token limit approaching, memory starvation, API throttling, and unattended runs.
  - **Critical / Failure (`#f43f5e` / Rose 500):** Disconnected nodes, container exit codes, expired credentials, and budget overrun termination.
- **Background & Canvas:**
  - **Dark Mode (Default):** Canvas sits at `#090d16` (slate-950 deep), structural cards at `#0f172a` (slate-900), elevated panels and flyouts at `#1e293b` (slate-800).
  - **Light Mode:** Canvas at `#f8fafc` (slate-50), cards at `#ffffff`, elevated menus at `#ffffff` with slate-200 structural borders.

## Typography

The typographic hierarchy uses **Geist** for natural human readability and rigorous geometric structure across all interfaces, coupled with **JetBrains Mono** for all operational parameters, token consumption metrics, hash IDs, status indicators, and console logs.

- **Numerics & Telemetry:** All table values, hardware specifications, and live cost counters must be formatted with tabular figures (`font-variant-numeric: tabular-nums`) using the `label-*` token set.
- **Micro-copy & Badges:** Status chips and agent health indicators use `label-xs` or `label-sm` in all caps with wide tracking (`0.04em`) to maintain sharp legibility against colored container pills.

## Layout & Spacing

The layout is structured around a fluid, dense enterprise grid capable of presenting extensive analytical data without horizontal scroll or unnecessary whitespace:

- **Desktop (1280px+):** 12-column responsive layout with fixed 260px left sidebar navigation, `margin-lg` outer margins, and `gutter-lg` column gutters. Multi-agent runtime dashboards collapse down to 4-, 3-, or 2-column card configurations.
- **Tablet (768px - 1279px):** 8-column layout. Sidebar collapses to a 64px icon-only rail. Canvas padding drops to `margin-md`.
- **Mobile (< 768px):** 4-column layout with a top header and collapsible drawer. Canvas margins shift to `margin`. Dashboard metrics switch to single-column vertical stacks.

All interior component paddings rely on the strict spacing scale (`space-xs` through `space-xl`) to enforce visual rhythm between card headers, data tables, and input controls.

## Elevation & Depth

Visual hierarchy relies on structural borders paired with restrained, dark-tinted ambient occlusion rather than heavy drop shadows:

- **Card Level (Base):** Subtle 1px solid border (`border-slate-800` in dark, `border-slate-200` in light) combined with an ultra-diffused micro shadow (`box-shadow: 0 1px 3px 0 rgba(0, 0, 0, 0.35)`). Surfaces remain planar to keep dense telemetry crisp.
- **Interactive Hover Level:** Elevates with a 1px border shift to `border-indigo-500/40` and an indigo ambient glow (`box-shadow: 0 4px 20px -2px rgba(99, 102, 241, 0.12)`).
- **Floating Overlays (Modals, Slide-overs, Dropdowns):** Sits on `bg-slate-900/95` with `backdrop-blur-md`, framed by a distinct 1px border (`border-slate-700`), cast with deep elevation (`box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.6), 0 8px 10px -6px rgba(0, 0, 0, 0.5)`).

## Shapes

The design system standardizes on `roundedness: 2` (rounded-xl standard for cards and structural panels, matching Tailwind's `rounded-xl` at `0.75rem` / `12px` default, with elements scaling proportionally):

- **Cards, Panels & Modal Windows:** `rounded-xl` (12px to 16px) creates a balanced, modern frame for technical data.
- **Buttons, Form Inputs & Select Triggers:** `rounded-lg` (8px) ensures interactive controls remain distinct from card boundaries.
- **Status Pills, Runtime Indicators & Metric Tags:** Full-pill (`rounded-full`) to immediately signal categorical and state indicators against rectilinear analytical charts.

## Components

### Buttons
- **Primary:** Solid indigo (`bg-indigo-600 hover:bg-indigo-500`), white text, `rounded-lg`, font weight 500, slight vertical padding (`px-3.5 py-2`), with an inset top-edge highlight (`ring-1 ring-inset ring-white/15`).
- **Secondary:** Ghost/slate surface (`bg-slate-800/80 hover:bg-slate-800`), crisp outline (`border border-slate-700`), text slate-200.
- **Destructive:** Rose boundary with muted background (`bg-rose-500/10 hover:bg-rose-500/20 text-rose-400 border border-rose-500/30`).

### Cards & Container Units
- Structural data containers rendered with `rounded-xl`, `border border-slate-800`, and `bg-slate-900/70`. Headers include a standardized subtle bottom rule (`border-b border-slate-800/80`) with categorical actions aligned right.

### Chips & Badges
- Constructed with `rounded-full`, `px-2.5 py-0.5`, using `label-xs` monospace styling. 
- **Active / Deployed:** `bg-emerald-500/10 text-emerald-400 border border-emerald-500/20` with a pulsating 6px dot indicator.
- **Warning / Degraded:** `bg-amber-500/10 text-amber-400 border border-amber-500/20`.
- **Offline / Terminated:** `bg-rose-500/10 text-rose-400 border border-rose-500/20`.

### Form Fields & Inputs
- Dark slate fill (`bg-slate-950/60`), border (`border-slate-800`), `rounded-lg`, text slate-100, placeholder text slate-500. Focus transition triggers `border-indigo-500` accompanied by a distinct 2px ring (`ring-1 ring-indigo-500/50`).

### Lists & Data Grids
- Tabular row heights set strictly to 48px or 56px. Alternating hovers with `hover:bg-slate-800/40`. Header cells rendered using `label-sm` uppercase with bottom separation (`border-b border-slate-800`). Numeric columns aligned right.

### Additional Domain Components
- **Agent Terminal / Execution Log:** Embedded dark surface (`bg-black/80`) with `JetBrains Mono` typography, status timestamp gutters, and color-coded runtime streams (stdout, stderr).
- **Cluster Load Bar:** Linear segmented resource tracks (vCPU, GPU VRAM, Context Window) using primary indigo, violet, and emerald indicators.