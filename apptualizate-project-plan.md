# APPTUALIZATE — Website Project Execution Plan

**Project:** Full website rebuild for Apptualizate (UpdateYourself)
**Stack:** Astro 5 + Tailwind CSS 4 + React Islands + Netlify
**Language:** English first → Spanish translation phase
**Tone:** Premium consultancy
**Date:** April 2026

---

## 1. CONTENT ARCHITECTURE

### Sitemap & Page Hierarchy

```
/                           → Home (landing + conversion)
/about                      → Company story, philosophy, hybrid model
/services                   → Services overview (5 phases + transversal)
  /services/diagnostic           → Phase 1: Operational Diagnostic
  /services/process-design       → Phase 2: Process Design & Documentation
  /services/digitalization       → Phase 3: Digital Transformation & Integration
  /services/intelligence         → Phase 4: Data & Business Intelligence
  /services/continuous-support   → Phase 5: Ongoing Support & Evolution
  /services/ai-automation        → AI Integration & Intelligent Automation
  /services/training             → Training & Capacity Building
  /services/compliance           → Compliance Audits
  /services/custom-development   → Custom Software Development
  /services/outsourcing          → Operational Outsourcing
/methodology                → How we work, tech stack, frameworks
/cases                      → Case studies index
  /cases/[slug]                  → Individual case study (MDX)
/insights                   → Blog / thought leadership index
  /insights/[slug]               → Individual post (MDX)
/contact                    → Smart contact form + CTA
```

**Total pages:** 19 static + dynamic blog/cases
**MVP pages (Sprint 1-2):** 8 (Home, About, Services overview, 5 phase pages, Contact)

### Content Model

| Collection | Format | Fields |
|---|---|---|
| `services` | `.astro` pages | title, subtitle, icon, phase_number, benefits[], deliverables[], cta |
| `cases` | `.mdx` content | title, client_type, industry, services_used[], metrics{}, thumbnail, date |
| `insights` | `.mdx` content | title, excerpt, category, tags[], author, date, cover_image |

---

## 2. SPRINT PLAN

### SPRINT 1 — Foundation & Core Structure (Week 1–2)

**Goal:** Deployable skeleton with design system, navigation, and Home page live on Netlify.

| # | Task | Priority | Est. |
|---|---|---|---|
| 1.1 | Project scaffolding: `npm create astro@latest`, Tailwind 4, React integration | P0 | 2h |
| 1.2 | Git repo + Netlify deploy pipeline (auto-deploy on push to `main`) | P0 | 1h |
| 1.3 | Design system: color tokens, typography scale, spacing, shadows | P0 | 3h |
| 1.4 | Base layout component (`BaseLayout.astro`): SEO head, OG tags, fonts, analytics slot | P0 | 2h |
| 1.5 | Header component: logo, nav links, mobile hamburger, CTA button | P0 | 3h |
| 1.6 | Footer component: links, social, copyright, newsletter signup slot | P0 | 2h |
| 1.7 | Reusable UI components: Button, Card, SectionHeader, Badge, Container | P0 | 4h |
| 1.8 | Home page — Hero section (animated headline, subtitle, dual CTA) | P0 | 4h |
| 1.9 | Home page — Services preview (5 phases as interactive cards) | P0 | 3h |
| 1.10 | Home page — Value proposition section (3 pillars with icons) | P1 | 2h |
| 1.11 | Home page — Social proof / metrics strip | P1 | 2h |
| 1.12 | Home page — CTA banner (bottom conversion section) | P1 | 1h |
| 1.13 | 404 page | P2 | 1h |
| 1.14 | Favicon, OG image defaults, robots.txt, sitemap config | P1 | 1h |
| 1.15 | Netlify deploy verification + custom domain config | P0 | 1h |

**Sprint 1 Acceptance Criteria:**
- [ ] Site loads in < 1.5s on mobile (3G throttled)
- [ ] Lighthouse Performance > 90
- [ ] Navigation works on desktop and mobile
- [ ] Home page is complete with all sections
- [ ] Auto-deploys from `main` branch to Netlify
- [ ] Custom domain resolves with HTTPS
- [ ] Design system is documented in code (CSS variables / Tailwind config)
- [ ] All components are responsive (320px → 1440px)

---

### SPRINT 2 — Services & About (Week 3–4)

**Goal:** Complete services ecosystem and About page. Visitor can understand full offering.

| # | Task | Priority | Est. |
|---|---|---|---|
| 2.1 | Services overview page — Phase timeline (React island, animated) | P0 | 5h |
| 2.2 | Services overview page — Transversal services grid | P0 | 3h |
| 2.3 | Service page template (`ServiceLayout.astro`) | P0 | 3h |
| 2.4 | Phase 1: Diagnostic — full page with copy | P0 | 2h |
| 2.5 | Phase 2: Process Design — full page with copy | P0 | 2h |
| 2.6 | Phase 3: Digitalization — full page with copy | P0 | 2h |
| 2.7 | Phase 4: Business Intelligence — full page with copy | P0 | 2h |
| 2.8 | Phase 5: Continuous Support — full page with copy | P0 | 2h |
| 2.9 | AI & Automation service page | P0 | 2h |
| 2.10 | Training service page | P1 | 2h |
| 2.11 | Compliance Audits service page | P1 | 2h |
| 2.12 | Custom Development service page | P1 | 2h |
| 2.13 | Outsourcing service page | P1 | 2h |
| 2.14 | About page — Story, philosophy, hybrid model explanation | P0 | 4h |
| 2.15 | About page — Tech stack visual / tools we use | P1 | 3h |
| 2.16 | Cross-linking between services (related services component) | P1 | 2h |
| 2.17 | Breadcrumb component for service pages | P2 | 1h |

**Sprint 2 Acceptance Criteria:**
- [ ] All 10 service pages are live with final copy
- [ ] Services overview shows clear journey from Phase 1 → 5
- [ ] Each service page has: problem statement, what we do, deliverables, CTA
- [ ] About page communicates the hybrid human+AI model clearly
- [ ] Internal linking between related services works
- [ ] View transitions between pages are smooth
- [ ] Mobile experience is polished (no layout shifts, readable typography)

---

### SPRINT 3 — Methodology, Cases, Contact & SEO (Week 5–6)

**Goal:** Full credibility layer + lead capture + technical SEO complete.

| # | Task | Priority | Est. |
|---|---|---|---|
| 3.1 | Methodology page — Process framework visual | P0 | 4h |
| 3.2 | Methodology page — Tech stack showcase (tools, integrations) | P0 | 3h |
| 3.3 | Methodology page — "Why us" differentiation section | P1 | 2h |
| 3.4 | Case study template (`CaseLayout.astro`) | P0 | 3h |
| 3.5 | Case study #1 — Write and publish (reposition existing project) | P0 | 3h |
| 3.6 | Case study #2 — Write and publish | P1 | 3h |
| 3.7 | Cases index page with filtering | P1 | 2h |
| 3.8 | Contact page — Netlify Forms integration | P0 | 3h |
| 3.9 | Contact form — Smart fields (company size, service interest, urgency) | P0 | 2h |
| 3.10 | Contact form — Success/error states, spam protection (honeypot) | P1 | 1h |
| 3.11 | SEO: JSON-LD schema markup (Organization, Service, BreadcrumbList) | P0 | 3h |
| 3.12 | SEO: Dynamic OG images per page (using `@vercel/og` or static) | P1 | 3h |
| 3.13 | SEO: Canonical URLs, meta descriptions for all pages | P0 | 2h |
| 3.14 | SEO: XML sitemap generation + robots.txt finalization | P0 | 1h |
| 3.15 | Google Search Console + Analytics setup | P0 | 1h |

**Sprint 3 Acceptance Criteria:**
- [ ] Methodology page clearly shows "how we work" with visual framework
- [ ] At least 2 case studies published with metrics and outcomes
- [ ] Contact form submits successfully to Netlify Forms dashboard
- [ ] Form includes pre-qualification fields (not just name/email)
- [ ] All pages have unique meta titles, descriptions, OG images
- [ ] JSON-LD schema validates without errors
- [ ] Sitemap is submitted to Google Search Console
- [ ] Lighthouse SEO score > 95

---

### SPRINT 4 — Blog, Polish & Launch (Week 7–8)

**Goal:** Content engine ready, performance optimized, production launch.

| # | Task | Priority | Est. |
|---|---|---|---|
| 4.1 | Blog content collection setup (Astro Content Collections) | P0 | 2h |
| 4.2 | Blog index page with category filters | P0 | 3h |
| 4.3 | Blog post template with TOC, reading time, share buttons | P0 | 3h |
| 4.4 | Blog post #1: "Why Your Business Needs Documented Processes" | P0 | 3h |
| 4.5 | Blog post #2: "AI in Operations: Beyond the Hype" | P1 | 3h |
| 4.6 | Blog post #3: "The Real Cost of Not Having a Management System" | P1 | 3h |
| 4.7 | Animations & microinteractions polish (scroll reveals, hovers) | P1 | 4h |
| 4.8 | Image optimization: WebP/AVIF, lazy loading, responsive images | P0 | 2h |
| 4.9 | Performance audit: bundle analysis, CSS purge, font optimization | P0 | 3h |
| 4.10 | Accessibility audit: ARIA labels, focus states, contrast ratios | P0 | 2h |
| 4.11 | Cross-browser testing (Chrome, Safari, Firefox, Edge) | P0 | 2h |
| 4.12 | Mobile testing on real devices (iOS Safari, Android Chrome) | P0 | 2h |
| 4.13 | Final copy review — tone consistency, grammar, CTAs | P0 | 3h |
| 4.14 | Netlify production config: headers, redirects, cache rules | P0 | 1h |
| 4.15 | Pre-launch checklist execution (see Section 7) | P0 | 2h |
| 4.16 | LAUNCH | P0 | 🚀 |

**Sprint 4 Acceptance Criteria:**
- [ ] Blog system works: new post = new `.mdx` file → auto-published
- [ ] 3 launch posts published
- [ ] Lighthouse all scores > 95 (Performance, SEO, Accessibility, Best Practices)
- [ ] Page load < 1s on cable, < 2s on 3G
- [ ] Zero console errors
- [ ] All images are optimized and lazy-loaded
- [ ] Site works perfectly on mobile
- [ ] All forms tested and receiving submissions
- [ ] Analytics tracking confirmed
- [ ] HTTPS, redirects, and headers configured correctly

---

## 3. REUSABLE UI COMPONENTS

### Component Library (Atomic Design)

**Atoms:**
| Component | Props | Usage |
|---|---|---|
| `Button` | variant (primary/secondary/ghost), size (sm/md/lg), href?, icon? | CTAs, navigation, forms |
| `Badge` | text, color | Tags, labels, status indicators |
| `Icon` | name (from Lucide), size | Throughout the site |
| `SectionLabel` | text | Small caps label above headings |

**Molecules:**
| Component | Props | Usage |
|---|---|---|
| `SectionHeader` | label?, title, subtitle?, alignment | Every section opener |
| `ServiceCard` | title, description, icon, href, phase_number? | Services grid, home preview |
| `MetricCard` | value, label, icon? | Social proof, case study metrics |
| `TestimonialCard` | quote, author, role, company, avatar? | Social proof sections |
| `BlogPostCard` | title, excerpt, date, category, slug, image? | Blog index, home preview |
| `CaseStudyCard` | title, client_type, services[], metrics{}, slug | Cases index |
| `TechStackItem` | name, icon, category | Methodology page |

**Organisms:**
| Component | Props | Usage |
|---|---|---|
| `Hero` | title, subtitle, cta_primary, cta_secondary, variant | Home, service pages |
| `PhaseTimeline` | phases[] (React island) | Services overview, home |
| `ServiceGrid` | services[], columns | Services overview |
| `CTABanner` | title, subtitle, cta_text, cta_href | Bottom of every page |
| `ContactForm` | (React island) | Contact page |
| `Header` | currentPath | Global layout |
| `Footer` | — | Global layout |

---

## 4. DESIGN SYSTEM

### Color Palette (Premium Consultancy)

```css
/* Primary — Deep Navy (trust, authority) */
--color-primary-50: #f0f4ff;
--color-primary-100: #dbe4ff;
--color-primary-500: #364fc7;
--color-primary-600: #2b3fad;
--color-primary-700: #1e3093;
--color-primary-900: #0d1b4a;

/* Accent — Electric Cyan (tech, innovation) */
--color-accent-400: #22d3ee;
--color-accent-500: #06b6d4;
--color-accent-600: #0891b2;

/* Neutral — Cool Gray */
--color-neutral-50: #f8fafc;
--color-neutral-100: #f1f5f9;
--color-neutral-200: #e2e8f0;
--color-neutral-400: #94a3b8;
--color-neutral-600: #475569;
--color-neutral-800: #1e293b;
--color-neutral-900: #0f172a;

/* Semantic */
--color-success: #10b981;
--color-warning: #f59e0b;
--color-surface: #ffffff;
--color-background: #f8fafc;
```

### Typography

```
Headings: "Plus Jakarta Sans" (Google Fonts) — weight 600, 700
Body: "Inter" (Google Fonts) — weight 400, 500
Mono/Tech: "JetBrains Mono" — for code snippets, tech labels

Scale (clamp for responsiveness):
h1: clamp(2.5rem, 5vw, 4rem)
h2: clamp(2rem, 4vw, 3rem)
h3: clamp(1.5rem, 3vw, 2rem)
body: 1.125rem (18px)
small: 0.875rem (14px)
```

---

## 5. INITIAL COPY — KEY PAGES

### Home — Hero

**Headline:**
> We Turn Operational Chaos Into Intelligent Systems

**Subheadline:**
> From undocumented processes and disconnected tools to a fully integrated, data-driven operation. We diagnose, design, digitalize, and support your business transformation — powered by AI.

**CTA Primary:** Start Your Diagnostic
**CTA Secondary:** Explore Our Services

### Home — Value Proposition (3 Pillars)

**Pillar 1: Process Architecture**
We map your reality, design your ideal state, and document everything with ISO-grade precision. No more tribal knowledge or "ask Juan, he knows."

**Pillar 2: Tech Integration**
We connect your tools, automate your workflows, and eliminate manual handoffs. Your ERP talks to your CRM talks to your dashboards — seamlessly.

**Pillar 3: Data-Driven Decisions**
Every process we digitalize generates data. We turn that data into real-time dashboards so you can stop guessing and start deciding.

### About — Core Narrative

**Opening:**
Apptualizate was founded on a simple observation: most businesses don't have a process problem — they have a visibility problem. Operations run on habit, knowledge lives in people's heads, and decisions are made on gut feeling.

We change that.

We're an operational transformation consultancy that combines industrial engineering methodology with cutting-edge AI tools. Where traditional consultancies send teams of five for months, we deploy smarter — one senior engineer armed with intelligent systems that multiply output without multiplying cost.

**The Hybrid Model:**
Our model is deliberately different. We don't believe in consultancy bloat. Every engagement is led by a senior industrial engineer who leverages AI-powered tools for documentation, process modeling, data analysis, and system integration. The result: faster delivery, lower cost, and solutions that are built to last — not to generate more billable hours.

### Services Overview — Intro

**Headline:**
A Complete System. Not Just Another Tool.

**Body:**
Most businesses don't need another SaaS subscription. They need someone to look at their operation end-to-end, understand what's broken, fix the foundation, and then — and only then — bring in the right technology. That's what our five-phase methodology delivers.

### Service Page Template — Copy Structure

Each service page follows this flow:

1. **The Problem** (2-3 sentences) — What pain does the client feel?
2. **What We Do** (1 paragraph) — Our approach in plain language
3. **How It Works** (3-4 steps) — Concrete process
4. **What You Get** (deliverables list) — Tangible outputs
5. **Why It Matters** (1 paragraph) — Business impact
6. **CTA** — Next step

### Phase 1: Operational Diagnostic — Full Copy

**The Problem:**
You know something isn't working, but you can't pinpoint where the bottlenecks are, who's responsible for what, or how much inefficiency is costing you. Decisions are based on assumptions, not data.

**What We Do:**
We immerse ourselves in your operation. Through structured interviews, process observation, document review, and data analysis, we build a complete picture of how your business actually works — not how you think it works. The gap between those two is where your biggest opportunities hide.

**How It Works:**
1. **Discovery sessions** — We interview key stakeholders across all departments
2. **Process mapping** — We document current workflows as they actually happen
3. **Gap analysis** — We identify bottlenecks, redundancies, risks, and blind spots
4. **Roadmap delivery** — We present findings with a prioritized action plan

**What You Get:**
- Current-state process maps (BPMN notation)
- Organizational gap analysis report
- Technology audit (tools in use vs. tools needed)
- Risk and bottleneck identification matrix
- Prioritized transformation roadmap with estimated timelines

**Why It Matters:**
You can't improve what you can't see. The diagnostic gives you — often for the first time — a clear, honest view of your operation. It's the foundation everything else is built on.

---

## 6. SEO TECHNICAL BASE

### On-Page SEO Checklist (Every Page)

- [ ] Unique `<title>` tag (50-60 chars) with primary keyword
- [ ] Unique `<meta name="description">` (150-160 chars) with CTA language
- [ ] Single `<h1>` per page containing primary keyword
- [ ] Hierarchical heading structure (h1 → h2 → h3, no skips)
- [ ] Internal links to related services/content (3-5 per page)
- [ ] Image alt text (descriptive, keyword-aware, not stuffed)
- [ ] URL slug is clean, lowercase, hyphenated, keyword-rich
- [ ] Open Graph tags: og:title, og:description, og:image, og:url
- [ ] Twitter Card tags: twitter:card, twitter:title, twitter:description

### Technical SEO Setup

```javascript
// astro.config.mjs
import { defineConfig } from 'astro/config';
import tailwind from '@astrojs/tailwind';
import react from '@astrojs/react';
import sitemap from '@astrojs/sitemap';

export default defineConfig({
  site: 'https://apptualizate.com',
  integrations: [
    tailwind(),
    react(),
    sitemap({
      filter: (page) => !page.includes('/draft/'),
      changefreq: 'weekly',
      priority: 0.7,
    }),
  ],
  prefetch: {
    defaultStrategy: 'hover',
  },
  experimental: {
    clientPrerender: true,
  },
});
```

### JSON-LD Schema (Home Page)

```json
{
  "@context": "https://schema.org",
  "@type": "ProfessionalService",
  "name": "Apptualizate",
  "alternateName": "UpdateYourself",
  "description": "Operational transformation consultancy combining industrial engineering with AI-powered tools",
  "url": "https://apptualizate.com",
  "areaServed": ["CL", "LATAM"],
  "serviceType": [
    "Business Process Consulting",
    "Digital Transformation",
    "Business Intelligence",
    "AI Integration",
    "Operations Management"
  ],
  "knowsAbout": [
    "BPMN Process Modeling",
    "ISO Documentation",
    "Workflow Automation",
    "Business Intelligence Dashboards",
    "AI Integration"
  ]
}
```

### Netlify Headers (Performance + Security)

```toml
# netlify.toml
[build]
  command = "npm run build"
  publish = "dist"

[[headers]]
  for = "/*"
  [headers.values]
    X-Frame-Options = "SAMEORIGIN"
    X-Content-Type-Options = "nosniff"
    Referrer-Policy = "strict-origin-when-cross-origin"
    Permissions-Policy = "camera=(), microphone=(), geolocation=()"

[[headers]]
  for = "/_astro/*"
  [headers.values]
    Cache-Control = "public, max-age=31536000, immutable"

[[headers]]
  for = "/fonts/*"
  [headers.values]
    Cache-Control = "public, max-age=31536000, immutable"

[[redirects]]
  from = "/servicios/*"
  to = "/services/:splat"
  status = 301

# Future: Spanish version redirects
```

---

## 7. NETLIFY DEPLOY CHECKLIST

### Pre-Launch

- [ ] Custom domain configured in Netlify dashboard
- [ ] DNS records pointing correctly (A record or CNAME)
- [ ] HTTPS/SSL certificate provisioned (Netlify auto-SSL)
- [ ] `netlify.toml` configured with build command and publish dir
- [ ] Environment variables set (if any: analytics ID, form keys)
- [ ] Branch deploys enabled for staging (`develop` → preview URL)
- [ ] Deploy notifications configured (Slack/email on deploy)
- [ ] Form detection verified (Netlify recognizes `data-netlify="true"`)

### Post-Deploy Verification

- [ ] All pages load without 404s or console errors
- [ ] Forms submit and appear in Netlify Forms dashboard
- [ ] Lighthouse audit: all scores > 95
- [ ] Mobile responsiveness verified on real devices
- [ ] OG images render correctly (test with https://opengraph.xyz)
- [ ] Sitemap accessible at `/sitemap-index.xml`
- [ ] robots.txt accessible and correct
- [ ] Google Search Console verified and sitemap submitted
- [ ] Analytics tracking firing on all pages
- [ ] All internal links work (no broken links)
- [ ] 301 redirects tested (if migrating from old site)
- [ ] Cache headers verified for static assets
- [ ] HTTPS redirect working (http → https)
- [ ] www → non-www (or vice versa) redirect configured

### Performance Targets

| Metric | Target | Tool |
|---|---|---|
| Lighthouse Performance | > 95 | Chrome DevTools |
| Lighthouse SEO | > 95 | Chrome DevTools |
| Lighthouse Accessibility | > 95 | Chrome DevTools |
| First Contentful Paint | < 1.0s | WebPageTest |
| Largest Contentful Paint | < 1.5s | WebPageTest |
| Total Blocking Time | < 100ms | WebPageTest |
| Cumulative Layout Shift | < 0.05 | WebPageTest |
| Total page weight (home) | < 500KB | Chrome DevTools |

---

## 8. BACKLOG — FUTURE ENHANCEMENTS (Post-Launch)

| Feature | Priority | Sprint |
|---|---|---|
| Spanish translation (i18n with Astro) | High | S5 |
| Service calculator / ROI estimator (React widget) | Medium | S5 |
| Client portal (status tracking) | Low | S6+ |
| Newsletter integration (Resend or Buttondown) | Medium | S5 |
| Chatbot / AI assistant on site | Medium | S6 |
| Case study video embeds | Low | S6 |
| Dark mode toggle | Low | S6 |
| Decap CMS integration (if non-technical editors needed) | Low | S7 |

---

*This document is the single source of truth for the Apptualizate website project. Update as decisions are made.*
