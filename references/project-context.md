# Project Context — Jo's Stack & Infrastructure

## General Preferences

- **Cost-efficient stack** — lean toward open source, self-hostable, or cheap SaaS
- **Simple > clever** — readable code over fancy abstractions
- **Ship it** — working and deployed beats perfect and local
- **AI-first workflows** — if something can be automated, automate it

---

## Studio 23 TTL

**What it is:** Photography/videography studio in Houston TX. Has a physical space.

**Stack (TBD — ask before assuming):**
- Likely static site or simple CMS (no heavy backend needed)
- Booking system: consider Cal.com (self-host) or Calendly embed
- Portfolio: image-heavy, needs fast loading, good mobile UX
- Payment: Stripe preferred

**Goals:**
- Premium client positioning
- Nightclub photography niche
- Online booking without back-and-forth DMs

**Known gaps:**
- No website yet
- No booking system
- No digital portfolio

---

## Northgate TV

**What it is:** Local media page covering College Station / Northgate nightlife. 450K+ views/month on Instagram.

**Stack (existing site):**
- Website recently built — check repo before rebuilding anything
- Instagram is primary platform
- Facebook page connected

**Goals:**
- Sell advertising/sponsorship packages to local businesses
- Grow Facebook presence
- Build email or outreach automation for leads

**Lead data:**
- File: `northgatetv-leads-bryan-cs-tx.csv` (67 businesses, Bryan/CS TX)
- Compiled: April 2026

---

## NGTV Outreach System

**What it is:** Automated outreach to the 67-business lead list for advertising sales.

**Stack (TBD):**
- Email automation: consider Resend, Postmark, or Nodemailer
- CRM-lite: Airtable or a simple SQLite DB to track status
- Personalization: pull business name/type from CSV, generate custom intros

**Goals:**
- Reach all 67 businesses without manual copy-paste
- Track: contacted / replied / interested / closed
- Follow-up sequences for non-responders

---

## Infrastructure Notes

- **Host machine:** Mac Mini (arm64, macOS)
- **Node version:** v25.8.1
- **Shell:** zsh
- **Package manager:** prefer npm or brew
- **AI tools:** OpenClaw + Bosley, Claude Code, Codex available
