# SCHEDSY — Build Tasks
> Implementation roadmap, broken into phases and atomic tasks.

**Stack:** React + TypeScript + Tailwind CSS (with design token overrides) + Framer Motion + Recharts  
**Fonts:** Bricolage Grotesque (display) + Instrument Sans (body) + JetBrains Mono (mono)  
**State:** Zustand (local app state) + React Query (server state)  
**Icons:** Lucide React  
**Calendar:** Custom-built (no third-party calendar lib)  
**Forms:** React Hook Form + Zod validation

---

## Phase 0 — Project Setup

- [ ] **T000** — Scaffold Vite + React + TypeScript project
- [ ] **T001** — Configure Tailwind CSS with custom design tokens from `design.md`
- [ ] **T002** — Install & configure dependencies: `framer-motion`, `lucide-react`, `recharts`, `zustand`, `@tanstack/react-query`, `react-router-dom`, `react-hook-form`, `zod`, `date-fns`
- [ ] **T003** — Set up Google Fonts import: `Bricolage Grotesque` (display) + `Instrument Sans` (body) + `JetBrains Mono` (mono)
- [ ] **T004** — Create global CSS variables file (`tokens.css`) from design token export
- [ ] **T005** — Configure path aliases (`@/components`, `@/pages`, `@/hooks`, `@/store`, `@/utils`)
- [ ] **T006** — Set up ESLint + Prettier with project rules
- [ ] **T007** — Set up mock data layer (`/src/mock/`) with JSON fixtures for all entities
- [ ] **T008** — Create base layout component: `AppShell` (sidebar + topbar + main content)
- [ ] **T009** — Create `ThemeProvider` with CSS variable injection
- [ ] **T010** — Set up React Router with all page routes defined

---

## Phase 1 — Design System Components

> Build all reusable UI components before pages. These are the atoms and molecules.

### 1.1 Foundation

- [ ] **T011** — `Button` component — variants: primary / secondary / ghost / danger / accent; sizes: sm / md / lg; loading state; icon support
- [ ] **T012** — `Input` component — text / email / password / search; label; error; helper text; icon prefix/suffix
- [ ] **T013** — `Textarea` component — with resize handle, char count optional
- [ ] **T014** — `Select` component — custom styled dropdown, searchable option, keyboard nav
- [ ] **T015** — `Toggle` / Switch component — animated thumb, on/off labels
- [ ] **T016** — `Checkbox` component — animated checkmark draw, indeterminate state
- [ ] **T017** — `RadioGroup` component — pill style + standard style
- [ ] **T018** — `Badge` / Tag component — colors, removable variant
- [ ] **T019** — `Avatar` component — image, initials fallback, size variants, group stack
- [ ] **T020** — `Tooltip` component — hover trigger, delay, positioning (top/bottom/left/right)
- [ ] **T021** — `Divider` component — horizontal / vertical, with optional label

### 1.2 Overlay & Feedback

- [ ] **T022** — `Modal` / Dialog component — overlay, scale+fade animation, close on Escape/backdrop
- [ ] **T023** — `Drawer` / SlidePanel component — right/left slide-in, 420px, overlay
- [ ] **T024** — `Toast` notification system — `useToast` hook, success/error/warning/info, auto-dismiss, dismiss button
- [ ] **T025** — `DropdownMenu` component — trigger + menu, keyboard navigation, nested support
- [ ] **T026** — `ContextMenu` component — right-click trigger variant
- [ ] **T027** — `Popover` component — anchored to trigger, arrow pointer
- [ ] **T028** — `ConfirmDialog` component — destructive action confirmation pattern

### 1.3 Data Display

- [ ] **T029** — `Card` component — base card, interactive hover variant, bordered variant
- [ ] **T030** — `Table` component — sortable columns, row hover, empty state, loading skeleton
- [ ] **T031** — `Skeleton` loader — shimmer animation, shape variants (text/card/avatar/chart)
- [ ] **T032** — `EmptyState` component — illustration slot, headline, description, action button
- [ ] **T033** — `StatCard` / KPI card — metric, label, trend indicator (up/down/neutral)
- [ ] **T034** — `Timeline` component — vertical event list with icons and connectors
- [ ] **T035** — `ProgressBar` component — animated fill, label, color variants
- [ ] **T036** — `Tabs` component — underline + pill variants, animated indicator

### 1.4 Navigation

- [ ] **T037** — `Sidebar` component — full + collapsed states, group labels, active state, hover animations
- [ ] **T038** — `TopBar` component — page title slot, actions slot, responsive
- [ ] **T039** — `Breadcrumb` component — separator, truncation for long paths
- [ ] **T040** — `StepIndicator` component — linear stepper, active/complete/pending states
- [ ] **T041** — `BottomNav` component — mobile only, 4–5 items, active indicator

### 1.5 Scheduling-Specific Components

- [ ] **T042** — `TimeSlotGrid` component — available slots in 2-col grid, select state, AM/PM sections
- [ ] **T043** — `DurationChip` — pill selector for 15m / 30m / 60m / Custom
- [ ] **T044** — `TimezoneSelector` — searchable select with city names, auto-detect on mount
- [ ] **T045** — `ColorSwatch` picker — 12 preset colors + custom hex input
- [ ] **T046** — `MeetingTypeIcon` — icon + label for Video / Phone / In-person / Custom
- [ ] **T047** — `EventTypeCard` — full card with color stripe, duration badge, actions menu
- [ ] **T048** — `BookingLinkCopy` — URL display + copy-to-clipboard with toast confirmation
- [ ] **T049** — `AvailabilityBar` — visual weekly overview strip (compact read-only)

---

## Phase 2 — App Shell & Navigation

- [ ] **T050** — Build `AppShell` layout: sidebar (240px) + top bar (56px) + main content area
- [ ] **T051** — Implement sidebar collapse/expand with animation (240px → 64px)
- [ ] **T052** — Sidebar active route highlighting with `NavLink`
- [ ] **T053** — Sidebar group sections with collapsible headers
- [ ] **T054** — Top bar: page title synced to current route
- [ ] **T055** — Top bar: Global search trigger (`⌘K`) — opens `CommandPalette` modal
- [ ] **T056** — `CommandPalette` modal — search across pages, event types, contacts; keyboard nav
- [ ] **T057** — Top bar: Notification bell — badge count + dropdown panel with grouped notifications
- [ ] **T058** — Top bar: User avatar menu — profile link, settings, logout
- [ ] **T059** — Top bar: "New Event" primary button — opens event type creation flow
- [ ] **T060** — Mobile: hamburger trigger, full-screen sidebar drawer
- [ ] **T061** — Mobile: Bottom navigation bar (5 key sections)
- [ ] **T062** — Route transitions: fade + slide-up 8px via Framer Motion `AnimatePresence`

---

## Phase 3 — Dashboard / Home

- [ ] **T063** — `DashboardPage` layout: hero bar + 2-column content + sidebar
- [ ] **T064** — Hero welcome bar: greeting with Fraunces italic, date, quick-action pills
- [ ] **T065** — "Today's Schedule" section: meeting list, time, avatar, event type badge
- [ ] **T066** — Empty state for today's schedule (illustrated, Fraunces italic headline)
- [ ] **T067** — Quick Stats row: 3 KPI cards with trend indicators
- [ ] **T068** — "Your Event Types" preview grid (top 3 cards + "View all" link)
- [ ] **T069** — Recent Activity feed (right sidebar): timeline component, last 10 items
- [ ] **T070** — Getting Started checklist (new user only): collapsible progress card, persisted in localStorage
- [ ] **T071** — Dashboard skeleton loading state (all sections shimmer before data)

---

## Phase 4 — Event Types

- [ ] **T072** — `EventTypesPage` layout: filter/sort bar + card grid
- [ ] **T073** — Filter pills: All / One-on-one / Group / Round Robin / Collective
- [ ] **T074** — Sort dropdown: Recent / Most booked / Name
- [ ] **T075** — Event type card grid: 3-col desktop, 2-col tablet, 1-col mobile
- [ ] **T076** — "Create New" dashed card as first grid item
- [ ] **T077** — Card: status toggle (active/inactive), copy link, 3-dot menu (Edit / Clone / Delete)
- [ ] **T078** — Multi-select mode: checkboxes appear on hover, floating bulk action bar
- [ ] **T079** — Bulk actions: Activate / Deactivate / Delete selected

### Event Type Creation Flow (Multi-step Modal)

- [ ] **T080** — Multi-step modal shell: `StepIndicator` (4 steps), progress auto-save
- [ ] **T081** — Step 1 "What & When": name, description (rich text), duration chips, color picker, location type
- [ ] **T082** — Step 2 "Scheduling": availability schedule select, date range picker, buffer time, booking limit, notice period
- [ ] **T083** — Step 3 "Invitee Experience": custom questions builder (add/remove/reorder), confirmation/rescheduling settings, redirect URL
- [ ] **T084** — Step 4 "Notifications": confirmation email toggle + preview, reminder email timing, follow-up email
- [ ] **T085** — Live preview panel (right side): renders booking page in real time as user edits
- [ ] **T086** — Form validation with Zod schema per step, error states
- [ ] **T087** — Save as draft (persist to localStorage/mock API) on step navigation
- [ ] **T088** — Edit mode: pre-populate all steps from existing event type data
- [ ] **T089** — Delete confirmation dialog with event type name input confirmation

---

## Phase 5 — Calendar View

- [ ] **T090** — `CalendarPage` layout: full-viewport calendar with top controls
- [ ] **T091** — View toggle: Month / Week / Day pill switcher
- [ ] **T092** — `MonthView` component: 6-row grid, day cells, event chips (truncated), "+N more" overflow
- [ ] **T093** — `WeekView` component: 7-col time grid (48 half-hour rows), event blocks with overlap handling
- [ ] **T094** — `DayView` component: single column time grid, detailed event blocks
- [ ] **T095** — Navigation: Prev/Next arrows + "Today" button + month/week label
- [ ] **T096** — Mini month navigator (top-left panel): compact month grid for quick date jump
- [ ] **T097** — Click time slot → create booking (quick-add or open event type picker)
- [ ] **T098** — Click existing booking → right panel slide-in with booking details
- [ ] **T099** — Booking detail panel: guest info, event type, actions (Reschedule / Cancel / Copy link)
- [ ] **T100** — Calendar legend: Available / Booked / Busy / Off color key
- [ ] **T101** — "Sync Calendar" button → opens integrations drawer
- [ ] **T102** — External calendar events rendered in muted blue (mock data)
- [ ] **T103** — Drag-to-set-availability in Week view (drag creates availability block)

---

## Phase 6 — Availability

- [ ] **T104** — `AvailabilityPage` layout: two-panel (schedule list left, editor right)
- [ ] **T105** — Schedule list: name, event type count badge, active indicator, select on click
- [ ] **T106** — `+ New Schedule` button → create with default name + Mon–Fri 9–5 preset
- [ ] **T107** — Inline schedule name editing (click to edit)
- [ ] **T108** — Timezone selector (searchable, auto-detected default)
- [ ] **T109** — Weekly grid editor: day toggle switches + time range inputs per day
- [ ] **T110** — Time range: start/end dropdowns (15-min increments), `+` add range, `×` remove
- [ ] **T111** — "Copy times to all weekdays" action button
- [ ] **T112** — **Date Overrides** section: calendar date picker + custom hours for that date
- [ ] **T113** — Add / remove / edit date overrides list
- [ ] **T114** — **Preview tab**: 14-day calendar view showing exactly when booker can book
- [ ] **T115** — Delete schedule (only if no event types using it — validation warning)
- [ ] **T116** — Unsaved changes indicator + save / discard bar (sticky bottom)

---

## Phase 7 — Contacts

- [ ] **T117** — `ContactsPage` layout: left filter panel + data table
- [ ] **T118** — Filter panel: search input, tags multi-select, source filter, date range
- [ ] **T119** — Contacts table: Name, Email, Last Meeting, Total Meetings, Tags, Source, Actions
- [ ] **T120** — Table sorting by any column
- [ ] **T121** — Row hover: reveal action icons (View / Edit / Delete)
- [ ] **T122** — Contact detail right panel (slide-in on row click)
- [ ] **T123** — Contact detail: avatar, name/email/phone, tags editor, meeting history timeline
- [ ] **T124** — Contact detail: Notes rich text editor, auto-save
- [ ] **T125** — "Book with Contact" shortcut → pre-fills invitee email in booking flow
- [ ] **T126** — Add contact manually: modal form (name, email, phone, tags)
- [ ] **T127** — Import contacts: CSV upload with column mapping UI
- [ ] **T128** — Bulk delete contacts with confirmation
- [ ] **T129** — Empty state with import / add CTAs

---

## Phase 8 — Routing

- [ ] **T130** — `RoutingPage` layout: list view + create/edit canvas
- [ ] **T131** — Routing form list: name, status, response count, created date, actions
- [ ] **T132** — "New Routing Form" wizard (3 steps: Name → Questions → Rules)
- [ ] **T133** — Visual canvas builder: node-based drag layout
- [ ] **T134** — Trigger node (start): "Form submission" — locked at top
- [ ] **T135** — Condition nodes: IF block with field / operator / value selectors
- [ ] **T136** — Destination nodes: Event Type / Team member / External URL
- [ ] **T137** — ELSE / fallback destination node
- [ ] **T138** — Connect nodes with animated connector lines (SVG path)
- [ ] **T139** — Drag-to-reorder nodes (y-axis only in list mode)
- [ ] **T140** — Test mode panel (bottom drawer): input form fields → highlight matched path
- [ ] **T141** — Embed code modal: copy `<script>` / `<iframe>` snippet + preview
- [ ] **T142** — Undo/Redo history (Zustand action stack, 20 steps)

---

## Phase 9 — Workflows

- [ ] **T143** — `WorkflowsPage` layout: list left + builder right
- [ ] **T144** — Workflow list: name, trigger type icon, status toggle, last run time
- [ ] **T145** — Filter: All / Active / Draft / Archived
- [ ] **T146** — "New Workflow" button → blank builder with trigger picker
- [ ] **T147** — Trigger block: dropdown (Before event / After event / On cancel / On reschedule)
- [ ] **T148** — Trigger timing config: X minutes/hours/days before/after
- [ ] **T149** — Action blocks: Email / SMS / Webhook / CRM / Slack
- [ ] **T150** — `+ Add Action` button (appears between blocks and at bottom)
- [ ] **T151** — Action config panels: expand inline (accordion)
- [ ] **T152** — Email action: subject, body (template vars: `{{name}}`, `{{event}}`, `{{time}}`), send preview
- [ ] **T153** — Webhook action: URL, method, custom headers, body template, test send
- [ ] **T154** — Drag-to-reorder actions (above/below)
- [ ] **T155** — Delete action (with confirm for live workflows)
- [ ] **T156** — Save as Draft / Activate toggle in top bar
- [ ] **T157** — Run history drawer: list of executions, status, timestamp, payload peek

---

## Phase 10 — Integrations & Apps

- [ ] **T158** — `IntegrationsPage` layout: category tabs + card grid
- [ ] **T159** — Category tabs: All / Video / Calendars / CRM / Payments / Communication / Analytics / Developer
- [ ] **T160** — Featured strip: horizontal scroll, 6 hero integrations
- [ ] **T161** — Integration card: logo, name, category, description, status badge
- [ ] **T162** — `Connect` button → opens auth flow modal (mock OAuth redirect)
- [ ] **T163** — `Manage` button (connected integrations) → settings panel slide-in
- [ ] **T164** — Connected state: green "Connected" pill, disconnect option
- [ ] **T165** — Integration settings panel: scopes list, sync frequency, last synced time
- [ ] **T166** — Disconnect confirmation dialog
- [ ] **T167** — Search integrations input (filters cards live)

**Integration cards to include (mock):**
- Google Calendar, Outlook, Apple Calendar
- Zoom, Google Meet, Microsoft Teams, Around
- Salesforce, HubSpot, Pipedrive
- Stripe, PayPal
- Slack, Zapier, Make
- Google Analytics

---

## Phase 11 — Analytics

- [ ] **T168** — `AnalyticsPage` layout: date range header + dashboard sections
- [ ] **T169** — Date range selector: 7d / 30d / 90d / 12m / Custom range picker
- [ ] **T170** — KPI row: 4 stat cards — Total Bookings, Completion Rate, No-show Rate, Avg Response Time
- [ ] **T171** — Trend indicators on KPI cards: percentage change vs previous period (up/down arrow)
- [ ] **T172** — Bookings Over Time: `recharts` AreaChart, gradient fill, tooltip
- [ ] **T173** — Event Type Breakdown: horizontal `BarChart`, color per event type
- [ ] **T174** — Booking Sources: `PieChart`/donut with legend (Direct / Routing / Embed / Manual)
- [ ] **T175** — Busiest Times heatmap: 7×24 grid, cell opacity = booking density
- [ ] **T176** — Recent Bookings table: last 50 rows, sortable, guest name / event / time / status columns
- [ ] **T177** — Export CSV button (downloads mock data as `.csv`)
- [ ] **T178** — Loading skeletons for all chart sections

---

## Phase 12 — Admin Center

- [ ] **T179** — `AdminCenterPage` layout: left sub-nav + content area
- [ ] **T180** — Sub-nav items: Account / Team / Billing / Security / Branding / Notifications / Data & Privacy
- [ ] **T181** — **Account tab**: workspace name, logo upload, brand color picker, subdomain input + availability check
- [ ] **T182** — **Team tab**: members table (name, email, role, last active), invite by email, role dropdown (Admin/Member/Viewer)
- [ ] **T183** — Invite modal: email field, role select, optional message, send invite
- [ ] **T184** — **Billing tab**: current plan card, usage bar (bookings this month), upgrade CTA, invoice history table
- [ ] **T185** — **Security tab**: 2FA setup toggle + QR code modal, active sessions list, audit log table
- [ ] **T186** — **Branding tab**: booking page preview, color picker, font select, custom domain input
- [ ] **T187** — Branding live preview: iframe-like card that updates in real time
- [ ] **T188** — **Notifications tab**: global toggles for email/SMS by event type
- [ ] **T189** — **Data & Privacy tab**: export all data button, delete account danger zone, GDPR consent records

---

## Phase 13 — Booking Page (Public)

- [ ] **T190** — `BookingPage` layout: centered, max-860px, no app shell
- [ ] **T191** — Host profile card: avatar, name, event name, duration chip, meeting type icon
- [ ] **T192** — Step 1 — Time selection: month calendar + time slot grid (right)
- [ ] **T193** — Calendar: navigate months, disabled past dates, highlight available dates
- [ ] **T194** — Time slots: fetch available for selected date, display in 2-col grid
- [ ] **T195** — Timezone selector: auto-detect, user override, display selected TZ below slots
- [ ] **T196** — Step 2 — Invitee details: name, email, custom questions, notes, step breadcrumb
- [ ] **T197** — Form validation: required fields, email format
- [ ] **T198** — Step 3 — Confirmation screen: animated SVG checkmark, event summary card
- [ ] **T199** — Add to calendar buttons: Google / Outlook / Apple (.ics) 
- [ ] **T200** — Schedsy watermark (bottom, subtle)
- [ ] **T201** — Mobile-first layout for booking page (stacked single column)
- [ ] **T202** — Back navigation between steps (no data loss)

---

## Phase 14 — Help Center Page

- [ ] **T203** — `HelpPage` layout: search hero + category cards + recent articles
- [ ] **T204** — Search bar (Fraunces italic placeholder: *"What can we help with?"*)
- [ ] **T205** — Category cards: Getting Started / Event Types / Integrations / Billing / API / Troubleshooting
- [ ] **T206** — Featured articles list (mock content, 6 items)
- [ ] **T207** — "Contact support" CTA → opens intercom-style chat widget (mock)
- [ ] **T208** — Article detail page: breadcrumb, content, "Was this helpful?" thumbs

---

## Phase 15 — Polish & QA

### Animations & Interactions
- [ ] **T209** — Audit all page transitions (route changes) — ensure `AnimatePresence` wraps routes
- [ ] **T210** — Sidebar collapse animation: smooth width tween, icon label fade
- [ ] **T211** — Card hover micro-interactions across all card types
- [ ] **T212** — Button loading states verified on all async actions
- [ ] **T213** — Booking confirmation: SVG checkmark path draw animation (600ms)
- [ ] **T214** — Toast enter/exit animations (Framer Motion spring)
- [ ] **T215** — Modal open/close animations (scale + fade)
- [ ] **T216** — Skeleton loaders on all async data sections

### Accessibility
- [ ] **T217** — Keyboard nav audit: Tab order, Enter/Space activation, Escape dismissal
- [ ] **T218** — Focus rings on all interactive elements (`--shadow-focus`)
- [ ] **T219** — ARIA labels on icon-only buttons
- [ ] **T220** — `aria-live` regions for toast notifications
- [ ] **T221** — Color contrast check (all text combinations ≥ 4.5:1)
- [ ] **T222** — `prefers-reduced-motion` media query applied to all Framer Motion components

### Responsiveness
- [ ] **T223** — Mobile layout audit: all pages (< 768px)
- [ ] **T224** — Tablet layout audit: all pages (768–1024px)
- [ ] **T225** — Sidebar: mobile drawer mode, tablet icon-rail mode
- [ ] **T226** — Calendar views: mobile-optimized Day view default on narrow screens
- [ ] **T227** — Booking page: stacked mobile layout verified

### Performance
- [ ] **T228** — Route-based code splitting (`React.lazy` + `Suspense`)
- [ ] **T229** — Image optimization: lazy loading, correct sizing
- [ ] **T230** — Debounce search inputs (300ms)
- [ ] **T231** — Memoize expensive renders (`useMemo`, `React.memo`) on calendar grid

### Final QA
- [ ] **T232** — Cross-browser test: Chrome, Firefox, Safari, Edge
- [ ] **T233** — All mock data wired to all pages (no empty/broken states)
- [ ] **T234** — All form validations tested (success + error paths)
- [ ] **T235** — All modal/drawer open+close flows verified
- [ ] **T236** — Copy-to-clipboard working with toast feedback
- [ ] **T237** — Date/timezone calculations verified with `date-fns`

---

## Task Summary

| Phase | Tasks | Focus |
|-------|-------|-------|
| 0 | T000–T010 | Project setup |
| 1 | T011–T049 | Design system components |
| 2 | T050–T062 | App shell & navigation |
| 3 | T063–T071 | Dashboard |
| 4 | T072–T089 | Event Types + creation flow |
| 5 | T090–T103 | Calendar view |
| 6 | T104–T116 | Availability editor |
| 7 | T117–T129 | Contacts |
| 8 | T130–T142 | Routing |
| 9 | T143–T157 | Workflows |
| 10 | T158–T167 | Integrations |
| 11 | T168–T178 | Analytics |
| 12 | T179–T189 | Admin Center |
| 13 | T190–T202 | Public Booking Page |
| 14 | T203–T208 | Help Center |
| 15 | T209–T237 | Polish, accessibility, QA |
| **Total** | **238 tasks** | |

---

## Suggested Build Order

For a solo developer or AI-assisted build:

1. **Phase 0** — Setup (1 session)
2. **Phase 1** — Components (3–4 sessions, build & test in isolation)
3. **Phase 2** — Shell + Nav (1 session)
4. **Phase 13** — Booking page first (it's the most user-visible, great for early sharing)
5. **Phase 3** — Dashboard (motivating to see a full page)
6. **Phase 4** — Event Types (core of the product)
7. **Phase 5 + 6** — Calendar + Availability (tightly related)
8. **Phases 7–12** — Remaining sections in any order
9. **Phase 14** — Help
10. **Phase 15** — Polish last

---

## Notes for Claude Code

- Keep all design token usage consistent with `design.md` — never hardcode color hex values outside of `tokens.css`
- All components should accept `className` prop for extension
- Framer Motion variants should be defined as named constants in a `/src/motion/variants.ts` file
- Mock data should feel realistic: use real Nigerian + international names, real company names, realistic durations
- The `EventTypesPage` and `BookingPage` should be demo-able independently (good for screenshots/sharing)
- Use `date-fns` for all date arithmetic — no native `Date` manipulation
- Never use `any` type in TypeScript — unknown is acceptable where necessary
