# Hydro Bot Dashboard - Design Guidelines

## Design Approach
**Hybrid Reference-Based + Material Design System**

Drawing inspiration from successful Discord bot dashboards (MEE6, Dyno, Discord's interface) combined with Material Design principles for data-heavy components. The dashboard balances professional utility with approachable brand personality through a water/hydro theme.

## Typography System

**Primary Font:** Inter (Google Fonts) - clean, modern, excellent readability
**Accent Font:** Poppins (Google Fonts) - friendly headers and branding

**Hierarchy:**
- Hero/Marketing Headlines: Poppins, 3xl-6xl, semibold-bold
- Dashboard Section Headers: Poppins, 2xl-3xl, semibold
- Navigation & Labels: Inter, sm-base, medium
- Body Content: Inter, sm-base, regular
- Stats/Numbers: Poppins, xl-4xl, bold
- Form Labels: Inter, sm, medium
- Helper Text: Inter, xs-sm, regular

## Layout System

**Spacing Primitives:** Tailwind units of 2, 4, 6, 8, 12, 16
- Component padding: p-4, p-6, p-8
- Section spacing: py-12, py-16, py-20
- Card gaps: gap-4, gap-6
- Grid gutters: gap-6, gap-8

**Responsive Breakpoints:**
- Mobile: base (single column)
- Tablet: md (2 columns max)
- Desktop: lg+ (3-4 columns for dashboards)

## Component Architecture

### Landing Page Components

**Hero Section (80vh):**
- Full-width with hero image (futuristic water/tech aesthetic, abstract blue flowing patterns)
- Centered content overlay with blurred-background buttons
- Headline + subheadline + dual CTAs ("Add to Discord" primary, "View Dashboard" secondary)
- Floating bot statistics (server count, command executions, uptime)

**Feature Showcase (4-column grid on desktop, 2 on tablet, 1 on mobile):**
- Category cards: Moderation, Utility, Fun, Automation
- Each card: icon (Heroicons), title, 3-4 feature bullets, "Learn More" link
- Elevated cards with subtle shadows

**Live Stats Section (3-column grid):**
- Real-time metrics: Active Servers, Commands Today, Users Helped
- Large numbers with animated counters, labels below

**Command Categories Section:**
- Tabbed interface showing command examples
- Code-block styling for command syntax
- Description and usage examples per command

**Dashboard Preview:**
- Screenshot mockup of dashboard interface
- Annotated features highlighting key functionality
- Split layout: image left, feature list right

**Pricing/CTA Section:**
- Centered layout with tier comparison
- Feature checklist per tier
- Prominent upgrade buttons

**Footer:**
- 4-column layout: Branding/tagline, Quick Links, Resources, Social/Legal
- Newsletter signup with email input
- Bot status indicator (online/offline badge)

### Dashboard Application Components

**Sidebar Navigation (Fixed, 260px wide):**
- Hydro Bot logo/branding at top
- Server selector dropdown with search
- Navigation sections: Overview, Commands, Moderation, Automation, Logs, Settings
- Collapsible menu groups
- User profile/logout at bottom

**Top Bar:**
- Breadcrumb navigation
- Global search
- Notification bell with badge
- User avatar dropdown

**Server Overview Page:**
- Stats grid (4 columns): Members, Messages Today, Active Commands, Violations
- Quick actions card: Test Command, View Logs, Configure
- Recent activity feed (timeline layout)
- Server health status indicators

**Command Management (Grid layout):**
- Category filters as pills/chips
- Command cards in 3-column grid
- Each card: command name, description, toggle switch, settings icon
- Search and filter bar above grid

**Configuration Panels:**
- Form layouts with clear sections
- Label-input pairings with helper text
- Toggle switches for boolean options
- Multi-select dropdowns for roles/channels
- Preview pane showing configuration results

**Moderation Logs:**
- Table layout with sortable columns (User, Action, Moderator, Timestamp, Reason)
- Pagination controls
- Filter sidebar (date range, action type, moderator)
- Export logs button

**Welcome Message Builder:**
- Split view: configuration form left, live preview right
- Rich text editor for message content
- Variable insertion buttons (user, server name, member count)
- Image upload for welcome banner

## Icon System
**Heroicons** via CDN (solid for actions, outline for navigation)
- Navigation icons: outline style
- Action buttons: solid style
- Status indicators: custom badges with icons

## Animations
**Minimal, purposeful animations:**
- Stat counter animations on scroll-into-view
- Smooth page transitions (fade)
- Dropdown/modal entrance (slide + fade)
- Loading states (pulse skeleton screens)
- NO hover animations, NO scroll-triggered effects beyond stat counters

## Images

**Hero Image:** Abstract, flowing water patterns with tech/digital overlay, blue-dominant, high-quality 1920x1080. Should convey both fluidity (water theme) and technical prowess.

**Dashboard Preview:** Clean screenshot mockup showing command management interface with multiple servers, positioned in "Dashboard Preview" section.

**Optional Feature Icons:** Simple illustrations representing each command category (shield for mod, wrench for utility, smile for fun, gear for automation).

## Accessibility

- Consistent form styling across all inputs with visible focus states
- All interactive elements minimum 44px touch target
- Clear visual hierarchy through size and weight, not just treatment
- Skip navigation link for keyboard users
- ARIA labels for icon-only buttons
- Proper heading structure (h1→h2→h3)

## Dashboard-Specific Patterns

**Server Selector:** Dropdown with avatar icons, server names, member counts. Search functionality with keyboard navigation.

**Command Toggle Cards:** Visual state (enabled/disabled) with clear labeling, settings accessible via icon button.

**Configuration Forms:** Grouped by functionality, save/cancel buttons fixed to bottom of form sections, unsaved changes warning.

**Data Tables:** Striped rows for readability, sticky headers on scroll, responsive collapse to cards on mobile.

**Empty States:** Friendly illustrations with actionable CTAs when no data exists.

This design balances professional dashboard functionality with approachable branding, ensuring Hydro Bot feels both powerful and user-friendly across hundreds of servers.