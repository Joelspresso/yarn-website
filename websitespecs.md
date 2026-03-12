# Yarn — Website & App Specifications

> *Woven from life. Spun by you.*

---

## Overview

Yarn (app codebase: LifeinPages) is a personal memoir platform that helps users capture their memories — one thread at a time — and weave them into a story worth passing on. Built with React Native / Expo and Supabase, it is designed for older adults preserving their legacy, families capturing shared history, and storytellers who believe every life matters.

The product consists of a marketing website (currently a waitlist/early-access landing page) and a companion mobile app where users write, organise, and share their life stories.

---

## Target Audience

- Older adults who want to preserve their legacy for future generations
- Families who want to capture and share their shared history
- Storytellers and writers who believe every life deserves to be told

---

## Website Sections

### Navigation
- Logo (Yarn wordmark + icon)
- Links: Features · How it works · Pricing
- CTA button: *Join the waitlist*

### Hero
- Headline: *Your life story, beautifully told.*
- Tagline: *Woven from life. Spun by you.*
- Description: Yarn is the personal memoir platform that helps you capture your memories — one thread at a time — and weave them into a story worth passing on.
- Waitlist email sign-up form
- Note: *Free to join · No credit card required · No spam, ever*
- App mockup shown below hero

### Audience Banner
- Built for: Older adults preserving their legacy · Families capturing shared history · Storytellers who believe every story matters

### Features Section
Six core feature cards:

1. **Focused Writing Editor** — A clean, simple, and distraction-free editor with @mention and #tag autocomplete. Auto-tags people, places, and topics. Autosaves every few seconds.
2. **Timeline & Life Epochs** — Chronological view grouped into epochs: Childhood, Young Adult, Middle Age, Later Years. Shows pages, milestones, and key dates together.
3. **1000s Memory Prompts** — Curated questions. Daily push notifications. A "Spark a different memory" button cycles through prompts in the editor.
4. **Editor Collaboration** *(subscription only)* — Invite a trusted family member or friend as an editor via a secure 8-character code. They can read threads you choose to share and ask questions to help fill the gaps. You stay in full control.
5. **Photos, Audio & Video** — Attach media directly into your threads with captions and tags.
6. **Export Your Memoir** — Export as a beautifully formatted HTML, Epub and PDF file and plain-text backup. Share via AirDrop, email, or save to Files. Content stored in open Markdown — never locked in.

### Big Feature Callouts

**Timeline & Life Epochs**
- Pages with memory dates, milestones, and key dates all unified in one chronological view
- 50+ content-aware icons automatically matched by keyword (weddings, graduations, travel, etc.)
- Colour-coded dots by event category
- Filter by person, place, or status
- Multi-select and export any slice of your story

**Memory Prompts**
- 1000s of questions to spark imagination and memories
- Daily push notifications on your schedule
- Tap "Spark a different memory" for a fresh prompt in the editor
- Prompts tailored to your profile and the people in your life

**Editor Collaboration** *(subscription required)*
**Editor features:**
- Editors can send questions or reminders to authors 
- Editors can view progress and offer encouragement
- Editors can add questions and comments into a thread
- Editors can read and edit threads written by the author (a full version of changes is saved)
- An editor can assist multiple authors  
- Invite editors with a secure 8-character code from Settings → My Editors
- Editors can only see threads you choose to share
- Private threads stay completely hidden
- Editors ask questions; you stay in control of every word
- Revoke access any time, instantly

### Prompt Categories
Covers all 10 life categories:
Childhood & Family · School & Education · Love & Relationships · Career & Work · Places & Travel · Milestones & Life Events · Hobbies & Interests · Challenges & Growth · Sensory & Emotional · Wisdom & Reflection

### Pricing Section
*(See full pricing details below)*

### Final CTA
- Headline: *Be among the first to tell your story.*
- Email sign-up for early access / waitlist
- Note: *Free to join · No credit card required*

### Footer
- Brand: Yarn — *Woven from life. Spun by you.*
- Links: Product (Features, How it works, Pricing, Join waitlist) · Story (About Yarn, Our mission, Blog) · Support (Help centre, Privacy policy, Terms of use, Contact us)
- © 2026 Yarn. All rights reserved.

---

## App — Feature Detail

### Authentication
- Email/password sign-up and login via Supabase Auth
- Forgot password flow
- Guest mode — try the app without an account (pages stored in-memory for the session; all guest data cleared on logout)
- Sessions persisted securely with expo-secure-store

### Writing Threads (Pages)




**Page statuses:** not shown on web site

| Status | Description |
|--------|-------------|
| 🔒 Private | Visible only to you, kept off lists by default |
| ✏️ Draft | Work-in-progress, not polished |
| ✅ Final | Complete and considered finished |
| 📖 Published | Shareable / ready to export |

**Metadata toolbar (inside editor):**
- Tag people from your profile
- Tag locations/places
- Link to a life milestone
- Set or edit the memory date

### Page Management
- Full list of all pages with sort and filter controls
- Sort by: Last updated or Date created
- Filter by status: All, Draft, Final, Published, Private
- Full-text search across title, content, people, places, tags, and memory date
- Each card shows: title/preview, memory date, status badge, word count, people/places/topic chips, last updated

### Metadata & Tagging
- **People** — names linked to profiles (e.g. @Mum, @Joel)
- **Places** — locations (e.g. London, Grandma's house)
- **Topics/Tags** — freeform keywords (e.g. #childhood, #travel)
- **Memory date** — date or approximate year the memory is from
- Auto-tagging: @mentions and #tags in writing are automatically applied as structured metadata

### Dashboard
- **Stats strip**: Total pages, pages in draft, total word count
- **Epochs**: Pages grouped by life period (Childhood 0–17, Young Adult 18–35, Middle Age 36–55, Later Years 56+)
- **People & Places**: Everyone and everywhere mentioned across your story, with page counts
- **Milestones**: Key life events linked to related pages
- **Top Topics**: 8 most-used tags with tap-through to related pages
- Any section navigates to a filtered page list

### Timeline
- Chronological view combining pages (with memory dates), milestones, and key dates
- Vertical line with coloured dot indicators and year labels
- 50+ content-aware icons matched by keyword
- Filter by status and by person or place
- Multi-select mode for exporting a slice of your story
- Tap any entry to open the full editor

### Family Tree
- Connect the people in your life across generations
- Go to About Me → People, open a person, and set their mother and father to build the tree
- Each person card shows how many threads mention them

### Profile
- **Important People**: Role/type + name pairs (e.g. Mother — Helen), pre-populated from @mentions
- **Important Places**: Type + location pairs, pre-populated from location tags
- **Milestones**: Event + date pairs shown on the Timeline
- **Key Dates**: Description + date pairs shown on the Timeline
- **Tags**: All unique tags across your pages
- **Stats**: Active days, people count, milestones count, places count

### Search & Discovery
- Full-text search across all pages
- Tag-based navigation from Dashboard, Timeline, and page cards
- Filtered page collections scoped by person, place, tag, epoch, or milestone
- Sort controls and reorderable lists

### Export & Sharing
- Select multiple pages from the Timeline or filtered page views
- Generate a formatted HTML document (great for reading in a browser) and a plain-text backup
- Includes title, content, metadata, and summary statistics
- Share via AirDrop, Messages, email, or save to Files
- Import from file: Settings → Download & Backup → Import from file (.txt backup)

### Word Goals & Settings
- Word goals with toggle, period (Daily/Weekly/Monthly), and configurable target
- Progress bar and celebration modal on goal completion
- Notification preferences: daily writing prompts, weekly digest, milestone reminders
- Privacy settings: pages private by default, anonymous analytics toggle
- Display preferences: compact view, show/hide word count on cards
- Recently Deleted: deleted threads held for 30 days, restorable

### Memory Prompts
- 1000s of curated questions across 10 categories to help users start writing. A random prompt button in the editor cycles through them. 
- Editors or family members can also spark memories and send questions.

### Help & Support
- FAQs (loaded from Supabase, falls back to hardcoded list)
- Getting started tips
- Contact: hello@getyarn.app

---

## Pricing

### Free Trial — 2 months

New users get 2 months of full access at no cost.

- No credit card required to join
- After 2 months, the account is restricted to **download only** — no new pages can be added and no edits can be made until a subscription is activated
- **Accounts inactive for 12 months will be permanently deleted**

### Lifetime Access — $10 (one-time payment)

A single upfront payment grants permanent access to:

- View all pages and content
- Download all pages and content
- Up to **50,000 words** stored in total
- Up to **200 images or audio files**

> Lifetime access covers the right to read and export existing content at any time, permanently. Inactive accounts may be archived.

### Subscription — $5 / month (ongoing)

Required in addition to the lifetime access fee for active use of the app:

- Add new pages and threads
- Edit existing pages and threads
- Continue receiving **daily notifications and memory prompts**
- Access to **Editor Collaboration** (subscription-only feature)

### Extended storage Add-on — +$5 / month

Double the media allowance from 200 to **400 images or audio files**. Doubles the word limit from 50,000 to **100,000 words**.



### Pricing Summary

| | Free Trial | Lifetime Access | + Subscription | + Extended storage |
|---|---|---|---|---|
| Duration | 2 months | Forever | Monthly | Monthly |
| Price | $0 | $10 once | $5/mo | +$5/mo |
| View & download content | ✓ | ✓ | ✓ | ✓ |
| Add & edit pages | ✓ | — | ✓ | ✓ |
| Daily prompts & notifications | ✓ | — | ✓ | ✓ |
| Editor Collaboration | ✓ | — | ✓ | ✓ |
| Word limit | 50,000 | 50,000 | 50,000 | 100,000 |
| Images / audio files | 200 | 200 | 200 | 400 |

### Admin / Licensing Management *(internal — not shown on website)*

The sysadmin has full control over the licensing structure, including:
- Lifetime access price
- Subscription price
- Media add-on price
- Base word limit and media limits
- Add-on pricing and increment sizes
- Feature access per tier
- Free trial duration

---

## Tech Stack

| Layer | Technology |
|-------|------------|
| Framework | React Native + Expo (SDK 54) |
| Styling | NativeWind 4 (Tailwind CSS) + Ionicons |
| State | React hooks + custom data hooks |
| Forms | react-hook-form + Zod |
| Backend | Supabase (PostgreSQL + Auth + Row-Level Security) |
| Session storage | expo-secure-store |
| Export | expo-file-system + expo-sharing |

### Database Tables

| Table | Purpose |
|-------|---------|
| `profiles` | User profile base info |
| `pages` | All written pages |
| `profile_people` | Structured people list |
| `profile_places` | Structured places list |
| `profile_milestones` | Life milestones |
| `profile_key_dates` | Key recurring dates |
| `epochs` | Life period definitions |
| `memory_prompts` | 140+ writing prompt questions |
| `help_faqs` | FAQ content (editable via Supabase) |

### Website
- Single-file `index.html` with embedded CSS and JS
- Font: Plus Jakarta Sans (Google Fonts)
- Colour palette: Amber (#C88A0A), Amber glow (#E8A820), Rope tan (#C4956A), Cream background (#FAF7F2), Warm dark (#1E1008)
- Waitlist signup handler needs wiring to real `/api/waitlist` endpoint
- Contact: hello@getyarn.app

---

*Last updated: March 2026*
