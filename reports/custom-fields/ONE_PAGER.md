# Custom Fields: One-Pager

**Date:** 2026-02-18
**Author:** [Your Name]
**Status:** Draft for Review

---

## 🎯 Executive Summary

Service businesses need to capture industry-specific data that doesn't fit our standard fields—most critically, **purchase order numbers that literally block payment collection** for commercial contractors. Without custom fields, customers resort to unstructured workarounds (tags, notes, spreadsheets) that break reporting and create data quality issues. This is table-stakes functionality (Jobber and ServiceTitan both offer it) driving pain at scale: 6,206+ feedback mentions, 42% High Priority, with use cases spanning PO tracking, lead intake, equipment management, and marketing attribution.

---

## ✍️ Problem Definition

### 💼 Jobs to be Done

Service businesses need to **capture, standardize, and report on business-specific data** that varies by industry, workflow, and customer type. Key personas: Office Managers/Admins (45%) configure and enforce fields, Field Technicians (30%) fill business-critical data on mobile, Business Owners (25%) report on custom metrics.

### 🔤 The Problem

**Current State:**

We offer **Job Fields** (Job Type, Business Unit dropdowns) but customers **cannot create custom fields** on key objects: Customers (churn reasons, marketing attribution), Leads (qualification data), Properties (equipment/warranty info), or Invoices (PO numbers, billing fields).

**Current workarounds:** Tags (unstructured, hard to report), Notes (not searchable, inconsistent), Checklists (job-only, historical data lost), External spreadsheets (manual, siloed).

**Pain Points:**

| Pain Point | Volume | Severity | Impact |
|------------|--------|----------|---------|
| **Can't track PO numbers on invoices/jobs** | 12+ mentions | **CRITICAL** | **Blocks payment collection** - Customers refuse to pay without PO on invoice; affects contractors with commercial clients, government contracts, warranty companies |
| **Can't customize property profiles** | 25+ mentions | **HIGH** | HVAC/service companies can't track equipment-specific data (models, install dates, service history); forces reliance on notes |
| **Can't customize lead intake forms** | 20+ mentions | **HIGH** | Sales teams miss critical qualification data; leads lack context for routing and conversion |
| **Can't enforce required fields** | 15+ mentions | **HIGH** | Incomplete records break reporting, create compliance issues, force manual data cleanup |
| **Can't remove irrelevant dropdown options** | 15+ mentions | **MEDIUM** | Cluttered menus confuse users, reduce data quality (e.g., Canadian companies can't remove US-specific lead sources) |
| **Can't track marketing attribution** | 10+ mentions | **MEDIUM** | Growth companies can't measure ROI by channel; budget allocation is guesswork |

**Representative customer quotes:**

> "Hi do you have a feature or field for customer PO's. **That won't pay unless the po is on the invoice**"

> "Let us remove the toaster and other things we don't need and add fireplace, HRV, and things that we install. If we were to filter through the property profile **a majority of it is other.**"

> "I just started with MAX, and I was wondering how I could add custom fields to my customers to **track things like Meta Pixel ID and GCLID.**"

> "**can i set job fields to be mandatory field** to fill out when creating a new job?"

**Users impacted:** HVAC/Home Services (35%), General Contracting (25%), Property Management (20%), Specialized Trades (20%). Key business types: franchises (standardization), marketing-driven (attribution), commercial contractors (PO tracking), compliance-heavy industries.

### 📊 Problem Validation

**Scale:**
- **6,206 total feedback mentions** across Reforge (searches: "custom fields", "job fields", "custom properties", "field configuration")
- **42% High Priority** (Blocking/Critical) - Problems that directly impact revenue or operations
- **38% Medium Priority** (Pain Points) - Workarounds exist but are inefficient
- **20% Low Priority** (Nice-to-Have) - User-specific edge cases

**Evidence:**
- **Customer verbatims** show critical pain (see quotes above)
- **Competitive validation:** Both Jobber (4.5⭐, SMB leader) and ServiceTitan (Enterprise leader) offer custom fields as **table-stakes infrastructure**
  - Jobber: Available on 6+ objects (Properties, Clients, Quotes, Jobs, Invoices, Team members)
  - ServiceTitan: Available on 10+ objects with required field enforcement, conditional logic, advanced reporting
- **Prior internal research:** 8 Confluence documents, phased roadmap already drafted, architecture decisions made

---

## 💎 Opportunity & Impact

### 👑 Customer Value

1. **Capture business-specific data** without workarounds—industry-specific fields matching their terminology
2. **Structured, reportable data** - Filter, group, and export custom data; no more digging through notes
3. **Enforce data quality** - Required fields ensure critical information isn't missed
4. **Mobile accessibility** - Field technicians access and fill custom fields on the go
5. **Foundation for automation** - Custom fields enable workflow triggers and better business insights

### 📈 Business Value

**Retention & Revenue:**
- Reduce churn from "lack of customization" (6,206+ mentions, 42% High Priority)
- Prevent deal losses - custom fields are table-stakes in sales evaluations
- [NEED DATA] Quantify MRR at risk, lost deals per quarter, support ticket volume reduction (expected 20%)

**Competitive Positioning:**
- Table-stakes feature - Jobber and ServiceTitan both offer as core infrastructure
- Gap opportunity: Position between Jobber's simplicity (6 objects) and ServiceTitan's complexity (10+ objects)
- Our differentiation: Franchise/Command & Control integration + future automation/AI

**Strategic Value:**
- Platform foundation for automation triggers, conditional logic, AI-suggested configurations
- Increased product stickiness once customers configure and populate custom data
- TAM expansion to mid-market (commercial contractors, franchises, marketing-driven businesses)

### 📏 Success Metrics

**Target metrics based on internal Product Strategy document:**

| **Pro/Business Outcome** | **Current State** | **Target** | **Measurement** |
|-------------------------|-------------------|------------|-----------------|
| **Adoption** - Orgs create custom fields | 0% have custom fields | 30% create ≥1 field within 90 days of launch | Amplitude - field creation events |
| **Usage** - Fields actively populated | N/A | Average 3-5 custom fields per company | Amplitude - custom field creation |
| **Engagement** - Churn tracking adoption | N/A | 50% of companies use Churn Reason field within 6 months | Snowflake - field population rate |
| **Support Deflection** - Reduced tickets | [NEED BASELINE] | 20% reduction in "can we add field X?" tickets | Zendesk - ticket volume by topic |
| **NPS Impact** - Satisfaction | [NEED BASELINE] | Positive NPS impact from adopters | NPS survey data |
| **Retention** - Churn reduction | [NEED DATA] - % citing "lack of customization" | [TO BE DEFINED based on baseline] | Customer Success - churn reason analysis |
| **Deal Closure** - Sales wins | [NEED DATA] - Lost deals per quarter | [TO BE DEFINED based on baseline] | Sales - closed-lost analysis |

**Leading indicators:** Time to first field created, number of fields per org, custom field usage in reports, % of records with custom values populated.

**Baselines needed:** Support ticket volume (Zendesk), churn reasons (Customer Success), lost deals (Sales closed-lost analysis).

---

## 🏃‍♀️ Next Steps

### 🔬 Further Research Needed

**Business case validation:**
1. **Quantify churn impact** - Work with Customer Success to extract churn reason data from exit surveys/interviews. Specifically:
   - How many customers (count and MRR) cited "lack of customization" or mentioned custom fields as a churn reason in the past 6-12 months?
   - What's the MRR impact if we could prevent 20% of these churns?
2. **Quantify lost deals** - Work with Sales to analyze closed-lost data from past 6 months:
   - How many deals listed "missing custom fields" or "lack of flexibility" as a lost reason?
   - What was the total contract value of these lost opportunities?
   - Which specific use cases came up most often in lost deals? (PO tracking, lead forms, etc.)
3. **Support ticket baseline** - Work with Support/CS Ops to query Zendesk:
   - How many tickets mention "custom fields", "add field", "dropdown options", or "field customization" in the past quarter?
   - What's the average handling time and cost per ticket?
4. **Prioritize use cases** - Validate with customers whether Phase 1 (dropdowns on Customers) matches their most urgent needs, or if PO tracking (text fields) should come first

**Technical validation:**
1. **Performance impact** - Validate database schema approach supports filtering/reporting at scale
2. **API requirements** - Understand integration partner needs for custom fields access
3. **Mobile experience** - Validate field configuration and filling workflows on iOS/Android

**Open questions:**
1. **Phase 1 scope alignment:** Internal roadmap focuses on dropdown fields on Customers first, but VOC shows PO numbers (text fields on Invoices/Jobs) is most critical. Should we adjust Phase 1?
2. **Required field enforcement:** Customers need this (15+ mentions), but it's listed as "future work." Can we include basic required field logic in Phase 1?
3. **Dropdown management:** Customers want to REMOVE irrelevant system options (15+ mentions), not just add custom ones. Is this in scope?
4. **Property-level custom fields:** 25+ mentions for Property Profile customization, but Properties aren't in Phase 1-3 roadmap. Why the gap?

### 🚸 Identify Dependencies

| **Potential Dependency** | **Impact?** | **Description** |
|--------------------------|-------------|-----------------|
| **Mobile updates** | ✅ YES | Custom fields must be accessible and editable in iOS/Android apps (field technicians are primary users) |
| **Integrations (Quickbooks, INHA)** | ⚠️ MAYBE | If custom fields are added to Invoices/Estimates, integration payloads may need updating |
| **Introduce/increase Risk** | ⚠️ MAYBE | Custom fields add user-generated data; potential for misuse (PII, sensitive info). May need field-level permissions. |
| **New data tracking for metrics** | ✅ YES | Need Amplitude events for field creation, usage; Snowflake queries for adoption/engagement tracking |
| **Billing updates** | ❌ NO | No direct billing impact unless we plan to gate custom fields by plan tier |
| **Roles & Permissions** | ✅ YES | Need to define who can create/delete fields (admins) vs fill fields (all users) |
| **Reporting system** | ✅ YES | Custom fields must be filterable, groupable, exportable in existing reports |
| **Franchise/Command & Control** | ✅ YES | Template account management for franchises (unique differentiator) |

---

## 📚 Supporting Materials

- [Custom Fields: Insights Brief](/Users/mikaylawickman/dev/reports/custom-fields/INSIGHTS_BRIEF.md) - Comprehensive problem space research
- [Research Findings](/Users/mikaylawickman/dev/reports/custom-fields/research-findings.md) - Detailed VOC data and competitive analysis
- [PRD: Custom Fields](https://housecall.atlassian.net/wiki/spaces/EE/pages/3791880362) | [Product Strategy & Roadmap](https://housecall.atlassian.net/wiki/spaces/EE/pages/3811770933) | [Competitive Research](https://housecall.atlassian.net/wiki/spaces/EE/pages/3839591526) (Confluence)

**Data Sources:** Reforge (6,206 VOC mentions), 8 internal Confluence docs, Jobber/ServiceTitan product documentation

---

## 🤔 Critical Discussion Topics

**Note:** This section is intentionally included to surface key strategic questions and misalignments that require leadership input before finalizing the proposal. These are not weaknesses—they are decision points that will strengthen the proposal once resolved.

### 1. Problem Focus: One Problem or Many?

**The question:** Are we solving "custom fields" broadly, or are we solving 5 distinct problems (PO tracking, lead intake, marketing attribution, etc.) that happen to need custom fields?

**Why it matters:** If this feels like "customers want everything customizable," it won't get buy-in. We need a clear through-line that makes this ONE coherent problem space.

**Draft framing:** The core problem is **structured data capture** - businesses need to capture industry-specific data in a standardized, reportable way. Current workarounds (notes, tags) fail because they lack structure, enforcement, and reporting capabilities.

**Does this framing resonate?**

### 2. Proving Pain at Scale: What Does 6,206 Really Mean?

**The question:** The 6,206 number includes multiple search terms ("custom fields", "job fields", "custom properties"). Are we double-counting? Are we conflating different problems?

**Why it matters:** We need to be honest about what this number represents. Credibility matters more than impressive-sounding volume.

**Draft approach:** Acknowledge the 6,206 is across multiple search terms (some overlap), then pivot to the CRITICAL pain points:
- PO Numbers = can't get paid (12+ unique mentions)
- Property customization = major HVAC blocker (25+ mentions)
- Data quality = broken reporting (15+ mentions)

**Is this the right balance of honesty + urgency?**

### 3. Competitive Positioning: Catching Up or Leapfrogging?

**The question:** Both Jobber and ServiceTitan have custom fields. Are we building this because they have it, or because customers genuinely need it?

**Why it matters:** "Competitors have it" makes us look behind. We need to frame this as table-stakes expectation + unique opportunity.

**Draft framing:**
- Custom fields are **table-stakes infrastructure** (like jobs, customers, invoicing - expected, not differentiating)
- **Gap opportunity:** Jobber = too simple (limited objects, basic reporting); ServiceTitan = too complex (expensive, resource-intensive)
- **Our differentiation:** Franchise/Command & Control integration + future automation/AI capabilities

**Does this position us effectively?**

### 4. Business Value: Beyond "Customers Are Asking For It"

**The question:** What's the business case beyond retention? Can we quantify revenue impact?

**Why it matters:** "Customers are asking" isn't enough justification for engineering investment.

**What we need:**
- **Churn data:** How many customers cite "lack of customization" as a churn reason? What's the MRR impact?
- **Lost deals:** How many deals did we lose in the past 6 months because we don't have custom fields?
- **TAM impact:** What market segments are we locked out of without this feature?

**Can we get these numbers from Customer Success and Sales?**

---

## 📝 Notes for Collaborative Review

**Strengths of this draft:**
- Clear problem definition with customer quotes
- Honest about data (6,206 mentions across multiple searches)
- Prioritizes critical pain (PO tracking) over volume
- Acknowledges gaps between VOC and internal planning (Phase 1 = dropdowns, but customers need PO text fields)
- Positions competitively (table-stakes + gap opportunity)
- Identifies open questions and dependencies

**Areas needing validation:**
- [ ] Success metrics: Need baseline numbers (current state churn, lost deals, support tickets)
- [ ] Phase 1 scope: Should we adjust to include text fields if PO tracking is most critical?
- [ ] Required field enforcement: Can we include in Phase 1 given 15+ customer mentions?
- [ ] Property-level fields: Why aren't they in roadmap when there are 25+ mentions?

**Next steps:**
1. Review this draft together - poke holes, challenge assumptions
2. Validate business metrics with Customer Success and Sales teams
3. Align on Phase 1 scope based on customer urgency vs technical feasibility
4. Finalize problem statement and competitive positioning
5. Get stakeholder buy-in before moving to solution design
