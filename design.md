# SCHEDSY — Design System & UI Specification
> *A modern scheduling platform that replaces friction with flow.*

---

## 1. Product Vision

Schedsy is a next-generation scheduling and meeting platform. Where Calendly feels utilitarian and transactional, Schedsy feels **calm, intelligent, and beautifully crafted** — like a tool built for people who care about their time and their brand.

**Design Personality:** Refined Editorial Minimalism with Warm Depth  
**Tagline:** *Schedule smarter. Meet better.*

---

## 2. Design Principles

| Principle | Description |
|-----------|-------------|
| **Calm Confidence** | No noise. Every element earns its space. White space is a feature. |
| **Progressive Disclosure** | Show only what's needed, when it's needed. Complexity hides until invited. |
| **Warmth in Precision** | Sharp layouts softened by warm tones, round edges, and human typography. |
| **Speed Feels Good** | Transitions, skeleton loaders, and instant feedback make every action feel snappy. |
| **Branded Flexibility** | Every booking page is as beautiful as the host's identity allows. |

---

## 3. Color System

### Primary Palette (Light Mode)

```
--color-bg-base:        #FAFAF8       /* Warm off-white canvas */
--color-bg-surface:     #FFFFFF       /* Card/panel surfaces */
--color-bg-subtle:      #F4F3EF       /* Subtle section fills */
--color-bg-hover:       #EEECEA       /* Hover states */

--color-border:         #E5E3DE       /* Standard borders */
--color-border-strong:  #D0CEC8       /* Emphasized dividers */

--color-text-primary:   #1A1916       /* Headlines & primary text */
--color-text-secondary: #6B6860       /* Supporting text */
--color-text-tertiary:  #A09E98       /* Placeholders, disabled */
--color-text-inverse:   #FAFAF8       /* Text on dark fills */
```

### Accent Colors

```
--color-accent-primary:   #2D6A4F     /* Forest green — primary CTA */
--color-accent-primary-hover: #245C43
--color-accent-primary-light: #E8F5EE /* Light green tint */

--color-accent-secondary: #C4702A    /* Warm amber — secondary actions */
--color-accent-secondary-light: #FDF0E5

--color-accent-info:      #2563EB    /* Blue — links, info states */
--color-accent-info-light: #EFF4FF

--color-accent-success:   #16A34A    /* Confirmation, booking success */
--color-accent-warning:   #CA8A04    /* Conflict warnings */
--color-accent-danger:    #DC2626    /* Errors, destructive actions */
```

### Accent Gradient

```
--gradient-brand: linear-gradient(135deg, #2D6A4F 0%, #40916C 60%, #52B788 100%);
--gradient-warm:  linear-gradient(135deg, #C4702A 0%, #E88C3D 100%);
--gradient-surface: linear-gradient(180deg, #FFFFFF 0%, #FAFAF8 100%);
```

---

## 4. Typography

### Font Stack

```
--font-display:  'Bricolage Grotesque', 'Helvetica Neue', sans-serif  /* Headlines, page titles, hero text */
--font-body:     'Instrument Sans', 'Helvetica Neue', sans-serif      /* Body, UI labels, buttons, forms */
--font-mono:     'JetBrains Mono', 'Fira Code', monospace             /* Code, time values, URLs */
```

> Import via Google Fonts:
> `Bricolage+Grotesque:opsz,wght@12..96,300;12..96,400;12..96,500;12..96,600`
> `Instrument+Sans:wght@400;500;600`
> `JetBrains+Mono:wght@400;500`

**Why this pairing:**
- **Bricolage Grotesque** — an optical-size variable grotesque with subtle ink-trap details at display sizes. Feels crafted and premium without the genericness of Inter or Space Grotesk. Letter-spacing: `-0.02em` to `-0.03em` at large sizes.
- **Instrument Sans** — geometric but warm, designed for UI. Excellent legibility at 11–15px. Neutral enough to never fight the display font.
- **JetBrains Mono** — used sparingly for time values, booking URLs, and API tokens.

### Type Scale

| Token | Size | Weight | Line Height | Font | Usage |
|-------|------|--------|-------------|------|-------|
| `--text-xs` | 11px | 400 | 1.5 | Instrument Sans | Labels, badges, captions |
| `--text-sm` | 13px | 400 | 1.5 | Instrument Sans | Secondary body, helper text |
| `--text-base` | 15px | 400 | 1.6 | Instrument Sans | Primary body copy |
| `--text-md` | 17px | 500 | 1.5 | Instrument Sans | Card titles, emphasized body |
| `--text-lg` | 20px | 500 | 1.4 | Bricolage Grotesque | Section subheadings |
| `--text-xl` | 24px | 500 | 1.3 | Bricolage Grotesque | Page titles |
| `--text-2xl` | 32px | 500 | 1.2 | Bricolage Grotesque | Hero subheadings |
| `--text-3xl` | 42px | 400 | 1.1 | Bricolage Grotesque | Hero headlines |
| `--text-4xl` | 56px | 300 | 1.0 | Bricolage Grotesque | Landing hero |

### Usage Rules
- All headlines, page titles, stat numbers, and hero text use **Bricolage Grotesque**
- All UI chrome (nav items, labels, buttons, inputs, forms, body copy) uses **Instrument Sans**
- Time values, booking URLs, API keys, and code snippets use **JetBrains Mono**
- Letter-spacing: `-0.02em` on Bricolage at `--text-xl` and above; `0` on Instrument Sans
- No italic usage — both fonts are upright-only in this system

---

## 5. Spacing & Layout

### Spacing Scale (8px base)

```
--space-1:  4px
--space-2:  8px
--space-3:  12px
--space-4:  16px
--space-5:  20px
--space-6:  24px
--space-8:  32px
--space-10: 40px
--space-12: 48px
--space-16: 64px
--space-20: 80px
--space-24: 96px
```

### Layout Grid

- **App Shell:** Fixed 240px left sidebar + fluid content area
- **Content Max Width:** 1200px (centered, with 48px horizontal padding)
- **Card Grid:** 3-column (desktop), 2-column (tablet), 1-column (mobile)
- **Sidebar Width (collapsed):** 64px icon rail
- **Right Panel/Drawer:** 420px fixed width

### Border Radius

```
--radius-sm:   6px    /* Inputs, small chips */
--radius-md:   10px   /* Cards, dropdowns */
--radius-lg:   16px   /* Panels, dialogs */
--radius-xl:   24px   /* Feature cards, hero panels */
--radius-full: 9999px /* Pills, avatars, toggles */
```

---

## 6. Elevation & Shadow

```
--shadow-xs:  0 1px 2px rgba(26,25,22,0.04);
--shadow-sm:  0 2px 6px rgba(26,25,22,0.06), 0 1px 2px rgba(26,25,22,0.04);
--shadow-md:  0 4px 16px rgba(26,25,22,0.08), 0 2px 4px rgba(26,25,22,0.04);
--shadow-lg:  0 8px 32px rgba(26,25,22,0.10), 0 4px 8px rgba(26,25,22,0.06);
--shadow-xl:  0 20px 60px rgba(26,25,22,0.12), 0 8px 16px rgba(26,25,22,0.06);
--shadow-focus: 0 0 0 3px rgba(45,106,79,0.25);  /* Focus ring */
```

---

## 7. Component Library

### 7.1 Navigation — Left Sidebar

**Structure:**
```
[Logo + Brand Name]           ← 56px top bar
─────────────────
[User Avatar + Name]          ← Profile mini-card
─────────────────
Navigation Groups:
  • Scheduling
    - Home
    - Event Types
    - Calendar
    - Availability
  • People
    - Contacts
    - Routing
  • Growth
    - Workflows
    - Analytics
  • Platform
    - Integrations & Apps
    - Admin Center
─────────────────
[Help & Support]              ← bottom pinned
[Upgrade CTA] (free tier)    ← bottom pinned
```

**Visual Spec:**
- Background: `#FFFFFF` (pure white — reads cleanly against the warm `#FAFAF8` page canvas)
- Right edge: `border-right: 1px solid --color-border`
- Active item: `--color-accent-primary-light` fill + `border-left: 2px solid --color-accent-primary`, `border-radius: 0 --radius-sm --radius-sm 0`, offset with `margin-left: -2px`
- Hover: `--color-bg-hover` with 150ms ease transition
- Group labels: `--text-xs`, `--color-text-tertiary`, UPPERCASE, letter-spacing: 0.08em
- Icons: 18px, Lucide icons, stroke-width: 1.5
- Collapsed state: 64px icon rail with tooltips

### 7.2 Top Bar

- Height: 56px
- Background: `--color-bg-surface` with `border-bottom: 1px solid --color-border`
- Contains: Page title (left) + Actions (right: Search, Notifications bell, New Event button)
- "New Event" CTA: Filled forest green, `--radius-full`, icon + label
- Search: Expands inline with `⌘K` shortcut trigger

### 7.3 Buttons

| Variant | Background | Text | Border | Usage |
|---------|-----------|------|--------|-------|
| Primary | `--color-accent-primary` | White | None | Main CTA |
| Secondary | `--color-bg-subtle` | `--color-text-primary` | `--color-border` | Secondary actions |
| Ghost | Transparent | `--color-text-secondary` | None | Tertiary/nav |
| Danger | `#FEF2F2` | `--color-accent-danger` | `#FECACA` | Destructive |
| Accent | `--color-accent-secondary` | White | None | Highlights |

- Padding: `10px 18px` (md), `8px 14px` (sm), `12px 24px` (lg)
- Border radius: `--radius-full` for primary, `--radius-sm` for secondary
- Icon buttons: 36×36px, `--radius-md`
- Loading state: spinner replaces icon, text fades to 60%

### 7.4 Form Inputs

```
Background:    --color-bg-surface
Border:        1px solid --color-border
Border-radius: --radius-sm
Padding:       10px 14px
Font:          --font-body, --text-base
Color:         --color-text-primary

Focus:         border-color: --color-accent-primary; box-shadow: --shadow-focus
Error:         border-color: --color-accent-danger; background: #FEF2F2
Disabled:      background: --color-bg-subtle; opacity: 0.6
```

### 7.5 Cards

- Background: `--color-bg-surface`
- Border: `1px solid --color-border`
- Border radius: `--radius-lg`
- Shadow: `--shadow-sm`
- Padding: `24px`
- Hover (interactive cards): `--shadow-md`, translate Y -1px, transition 200ms ease

**Event Type Card** (special):
- Color bar on left edge (4px, user-chosen color)
- Avatar/icon preview top-right
- Title (Fraunces, --text-md)
- Duration badge + meeting type icons
- Booking link copy button on hover reveal
- 3-dot overflow menu

### 7.6 Calendar Component

- Month/Week/Day view toggle (pill group)
- Time slots: 15/30/60 min granularity
- Available blocks: Forest green tint `--color-accent-primary-light`
- Booked blocks: Solid forest green with white text
- Unavailable: `--color-bg-subtle` hatched pattern
- Today indicator: Amber dot + underline
- Drag to set availability (week/day view)
- External calendar events shown in muted blue

### 7.7 Time Slot Picker (Booking Flow)

- Large, card-style time slots in a 2-column grid
- Selected: Forest green fill, white text, checkmark icon
- Hover: Light green tint, border color forest green
- AM/PM section separators
- Timezone dropdown (auto-detected, user-overridable)

### 7.8 Availability Editor

- Visual weekly grid (Mon–Sun columns)
- Drag handles for start/end of time windows
- "Copy to all days" action
- Multiple time ranges per day (+ Add range button)
- Date overrides section with calendar picker
- Preview panel showing how a booker would see availability

### 7.9 Routing Rules (Visual Builder)

- Node-based canvas (like a simple flowchart)
- Condition cards: IF / THEN / ELSE blocks
- Field mapping: Question → Route → Event type/Owner
- Connection lines with animated dot trail on hover
- Drag-and-drop reordering
- Test mode: Input → trace path visualization

### 7.10 Workflow Builder

- Timeline-style vertical flow
- Trigger block (top) → Action blocks (below)
- Trigger types: Before event, After event, On cancellation, On reschedule
- Actions: Send email, Send SMS, Webhook, Add to CRM, Slack message
- Each block: Icon (colored) + title + configure chevron
- Collapsible action config panels

### 7.11 Analytics Dashboard

- Top row: 4 KPI cards (Meetings booked, Completion rate, Avg lead time, Top event type)
- Line chart: Bookings over time (30d/90d/12m)
- Bar chart: Meetings by event type
- Donut chart: Booking sources
- Table: Recent bookings (sortable, filterable)
- All charts use the brand green palette with amber highlights

### 7.12 Notifications & Toasts

- Toast: Bottom-right, `--radius-md`, `--shadow-lg`, 4-second auto-dismiss
- Types: Success (green left border), Error (red), Warning (amber), Info (blue)
- Bell dropdown: Right-aligned panel, grouped by date

---

## 8. Page-by-Page Specifications

### 8.1 Dashboard / Home

**Layout:** Two-column (main content 8col + sidebar 4col)

**Sections:**
1. **Hero Welcome Bar** — Greeting with user name (Fraunces italic), today's date, quick-action pills: `+ New Event`, `Copy My Link`, `View Calendar`
2. **Today's Schedule** — Compact list of upcoming meetings (time, name, event type, avatar). Empty state: illustrated empty calendar with "Your day is clear" in Fraunces italic
3. **Quick Stats Row** — 3 metric cards: This week's meetings, This month's bookings, Pending confirmations
4. **Your Event Types** — 3-up card grid (top 3), "View all" link
5. **Recent Activity Feed** (sidebar) — Timeline of bookings, cancellations, workflow fires
6. **Getting Started Checklist** (new users only) — Collapsible progress card

---

### 8.2 Event Types

**Layout:** Full-width with filter/sort bar + card grid

**Features:**
- Filter: All / One-on-one / Group / Round Robin / Collective
- Sort: Recent / Most booked / Name
- Each card: Color stripe, name, duration, meeting medium icon, booking count, status toggle, copy link, 3-dot menu
- Create new: Large dashed card with `+` icon — first card in grid
- Bulk actions: Multi-select mode with floating action bar

**Create / Edit Event Type Modal (Multi-step):**
```
Step 1: What & When
  - Event name
  - Description (rich text)
  - Duration (preset chips: 15m / 30m / 60m / Custom)
  - Color picker (12 swatches)
  - Location type (Video call / In person / Phone / Custom)

Step 2: Scheduling
  - Availability schedule (select from saved schedules)
  - Date range (rolling / fixed window / indefinitely)
  - Buffer time (before / after)
  - Daily booking limit
  - Minimum notice period

Step 3: Invitee Experience
  - Custom questions (drag to reorder)
  - Require confirmation toggle
  - Allow rescheduling / cancellation
  - Confirmation page (redirect URL or custom message)

Step 4: Notifications
  - Confirmation email (customize)
  - Reminder emails (timing presets)
  - Follow-up emails (optional)

Preview Panel (right side): Live booking page preview updates in real time
```

---

### 8.3 Calendar View

**Layout:** Full viewport calendar

**Views:** Month / Week / Day — toggle in top bar  
**Features:**
- Drag to create availability blocks
- Click event to see booking details flyout (right side panel)
- Mini month navigator (top-left)
- Legend: Available / Booked / Busy (external) / Off
- "Sync calendar" button top-right — opens integrations drawer
- Week view shows hours grid with booked meetings as colored cards

---

### 8.4 Availability

**Layout:** Two-panel (Schedule list left, Editor right)

**Left Panel:**
- List of named availability schedules (e.g., "Working Hours", "Consulting Hours")
- Active indicator, event types using this schedule count
- `+ New Schedule` button

**Right Panel (Editor):**
- Schedule name (editable inline)
- Timezone selector (searchable dropdown)
- Weekly grid: Toggle on/off per day + time range drag handles
- `+ Add time range` per day
- `Copy to all weekdays` shortcut
- **Date Overrides** section: calendar to pick specific date exceptions
- **Preview** tab: See 14-day availability as a booker would

---

### 8.5 Contacts

**Layout:** Data table with left filter panel

**Left Filter:**
- Search
- Tags (multi-select)
- Source (Manual / Calendly import / CRM sync / Booking)
- Date range added

**Table Columns:**
Name | Email | Last Meeting | Total Meetings | Tags | Source | Actions

**Contact Detail Panel (right slide-in):**
- Avatar (initials fallback), name, email, phone
- Tags (add inline)
- Meeting history (timeline)
- Notes (rich text)
- CRM link (if integrated)
- "Book with Contact" shortcut button

---

### 8.6 Routing

**Layout:** Canvas-based builder (full width)

**Features:**
- New Routing Form wizard
- Visual node canvas with drag-drop
- Condition node types: Single select, Multi-select, Text match, Number comparison
- Destination types: Event type, User, Team, External URL
- Test panel (bottom drawer): Enter inputs, see routing path highlighted
- Embed code generator (button top-right)
- Version history (simple undo/redo + named saves)

---

### 8.7 Workflows

**Layout:** Two-panel (Workflow list left, Builder right)

**Workflow List:**
- Name, trigger type, status toggle, last run
- Filter: Active / Draft / Archived

**Builder:**
- Trigger block (colored header: amber for "before", green for "after")
- `+ Add Action` button between blocks
- Action types with color-coded icons:
  - 📧 Email (blue)
  - 💬 SMS (green)  
  - 🔗 Webhook (purple)
  - 📋 CRM update (orange)
  - 💼 Slack (yellow)
- Each action: Expand to configure, preview send, test button
- Save as Draft / Activate toggle

---

### 8.8 Integrations & Apps

**Layout:** Browsable grid with category tabs

**Categories:**
- All | Video Conferencing | Calendars | CRM | Payments | Communication | Analytics | Developer

**Integration Card:**
- App logo (clean, white card)
- App name + category label
- Short description
- Status: Connected (green pill) / Not connected
- `Connect` / `Manage` button

**Featured Section (top):** Horizontal scrollable strip for popular integrations (Google Calendar, Zoom, Salesforce, HubSpot, Stripe, Slack)

---

### 8.9 Analytics

**Layout:** Dashboard-style, full width

**Date Range Selector:** Top-right, presets + custom range picker

**Sections:**
1. KPI Row (4 cards): Total Bookings | Completion Rate | No-show Rate | Avg Response Time
2. Bookings Over Time (line chart, area fill)
3. Event Type Breakdown (horizontal bar chart)
4. Booking Sources (donut + legend)
5. Busiest Times (heatmap grid: Mon-Sun × hours)
6. Invitee Geography (world map dot density — optional)
7. Recent Bookings Table (last 50, exportable CSV)

---

### 8.10 Admin Center

**Layout:** Settings page with left sub-nav

**Sub-sections:**
- **Account** — Name, logo, brand color, subdomain
- **Team** — Members list, roles, invite
- **Billing** — Plan, usage, invoices, upgrade
- **Security** — 2FA, SSO, audit log
- **Branding** — Booking page appearance, custom domain
- **Notifications** — Global email/SMS preferences
- **Data & Privacy** — Export data, delete account, GDPR tools

---

### 8.11 Booking Page (Public — Invitee Experience)

This is the page a guest sees when clicking a booking link.

**Layout:** Centered, max 860px, very clean

**Step 1: Choose Time**
- Host profile card (top): Avatar, name, event name, duration, location type
- Month calendar (left/center)
- Available time slots (right): Scrollable list, 2-col on desktop
- Timezone auto-detected, editable dropdown

**Step 2: Your Details**
- Name, email (required)
- Custom questions from event type
- Notes field (optional)
- Progress indicator (2-step breadcrumb)

**Step 3: Confirmation**
- Large green checkmark animation
- Event summary card (date, time, location, add-to-calendar buttons)
- Social share optional (if enabled)

**Design tone for booking page:** Clean, trust-building. The host's brand color accent used for the CTA button. Subtle Schedsy watermark bottom (removable on paid plans).

---

## 9. Motion & Animation

### Principles
- Duration: Fast (100ms), Base (200ms), Slow (350ms), Scenic (500ms+)
- Easing: `cubic-bezier(0.25, 0.46, 0.45, 0.94)` (ease-out) for entrances; `cubic-bezier(0.55, 0, 1, 0.45)` (ease-in) for exits

### Key Animations

| Element | Animation | Duration |
|---------|-----------|----------|
| Page transitions | Fade + slide up 8px | 200ms |
| Sidebar item hover | Background fill + icon nudge right 2px | 150ms |
| Card hover | translateY(-2px) + shadow upgrade | 200ms |
| Modal open | Scale from 0.97 + fade | 250ms |
| Toast enter | Slide in from right | 300ms |
| Time slot select | Background fill + checkmark draw | 200ms |
| Booking confirmation | Checkmark path draw SVG | 600ms |
| Skeleton loader | Shimmer left-to-right | 1.2s loop |
| Calendar day hover | Background circle fill | 150ms |
| Toggle switch | Thumb slide + track color | 200ms |
| Routing node connect | Dashed line draw | 400ms |

### Reduced Motion
All animations respect `prefers-reduced-motion: reduce` — replaced with instant opacity transitions.

---

## 10. Empty States

Each section has a distinct illustrated empty state:

| Section | Illustration Concept | Headline | Action |
|---------|---------------------|--------------------------|--------|
| Event Types | Calendar with sparkles | *"Nothing scheduled yet"* | Create Event Type |
| Contacts | Person silhouette + envelope | *"No contacts added"* | Import / Add |
| Workflows | Gear with dotted path | *"Your workflows await"* | Create Workflow |
| Analytics | Chart outline, empty | *"Data will flow here"* | — |
| Routing | Branching lines | *"No forms yet"* | New Routing Form |

Illustrations: Simple 2-tone line art using brand green + warm white, 160×120px. Headlines use Bricolage Grotesque 400, 20px.

---

## 11. Responsive Breakpoints

| Breakpoint | Width | Sidebar | Layout Change |
|-----------|-------|---------|--------------|
| Mobile | < 768px | Hidden (hamburger) | Single column, bottom nav |
| Tablet | 768–1024px | Collapsed icon rail (64px) | 2-col layouts become 1-col |
| Desktop | 1024–1440px | Expanded (240px) | Full layout |
| Wide | > 1440px | Expanded | Content max-width 1200px centered |

---

## 12. Accessibility

- WCAG 2.1 AA compliance minimum
- Color contrast ratios: 4.5:1 for body, 3:1 for large text
- All interactive elements keyboard-navigable (Tab, Enter, Escape)
- Focus rings: `--shadow-focus` (3px green outline offset)
- ARIA roles: `role="dialog"`, `aria-label`, `aria-live` for dynamic content
- Skip to main content link (visible on focus)
- Screen reader labels on icon-only buttons
- Time inputs: `<input type="time">` with visible labels

---

## 13. Iconography

**Library:** Lucide Icons  
**Style:** Outline, stroke-width: 1.5, size: 18px (nav), 16px (inline), 20px (feature)  
**Key icons by section:**

| Section | Icon |
|---------|------|
| Home | `home` |
| Event Types | `calendar-plus` |
| Calendar | `calendar-days` |
| Availability | `clock` |
| Contacts | `users` |
| Routing | `git-branch` |
| Workflows | `workflow` |
| Analytics | `bar-chart-3` |
| Integrations | `plug` |
| Admin | `settings-2` |
| Help | `circle-help` |
| New Event | `plus-circle` |
| Copy link | `link` |
| Video | `video` |
| Phone | `phone` |
| Location | `map-pin` |

---

## 14. Brand Identity

**Logo Mark:** A stylized `S` formed by two overlapping calendar page corners — minimal, monoline, forest green  
**App Name:** "Schedsy" — DM Sans SemiBold, tracking -0.02em  
**Favicon:** Logo mark in 32×32, forest green on transparent  
**OG Image:** Dark forest green background, white Fraunces headline, logo mark — 1200×630px

---

## 15. Design Tokens Export (CSS Variables Summary)

```css
:root {
  /* Colors */
  --color-bg-base: #FAFAF8;
  --color-bg-surface: #FFFFFF;
  --color-bg-subtle: #F4F3EF;
  --color-bg-hover: #EEECEA;
  --color-border: #E5E3DE;
  --color-border-strong: #D0CEC8;
  --color-text-primary: #1A1916;
  --color-text-secondary: #6B6860;
  --color-text-tertiary: #A09E98;
  --color-accent-primary: #2D6A4F;
  --color-accent-primary-hover: #245C43;
  --color-accent-primary-light: #E8F5EE;
  --color-accent-secondary: #C4702A;
  --color-accent-secondary-light: #FDF0E5;

  /* Typography */
  --font-display: 'Bricolage Grotesque', 'Helvetica Neue', sans-serif;
  --font-body: 'Instrument Sans', 'Helvetica Neue', sans-serif;
  --font-mono: 'JetBrains Mono', monospace;

  /* Spacing */
  --space-1: 4px; --space-2: 8px; --space-3: 12px;
  --space-4: 16px; --space-5: 20px; --space-6: 24px;
  --space-8: 32px; --space-10: 40px; --space-12: 48px;
  --space-16: 64px; --space-20: 80px; --space-24: 96px;

  /* Radii */
  --radius-sm: 6px; --radius-md: 10px; --radius-lg: 16px;
  --radius-xl: 24px; --radius-full: 9999px;

  /* Shadows */
  --shadow-xs: 0 1px 2px rgba(26,25,22,0.04);
  --shadow-sm: 0 2px 6px rgba(26,25,22,0.06), 0 1px 2px rgba(26,25,22,0.04);
  --shadow-md: 0 4px 16px rgba(26,25,22,0.08), 0 2px 4px rgba(26,25,22,0.04);
  --shadow-lg: 0 8px 32px rgba(26,25,22,0.10), 0 4px 8px rgba(26,25,22,0.06);
  --shadow-focus: 0 0 0 3px rgba(45,106,79,0.25);

  /* Motion */
  --duration-fast: 100ms; --duration-base: 200ms;
  --duration-slow: 350ms; --duration-scenic: 500ms;
  --ease-out: cubic-bezier(0.25, 0.46, 0.45, 0.94);
  --ease-in: cubic-bezier(0.55, 0, 1, 0.45);
}
```
