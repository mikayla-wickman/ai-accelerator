# Custom Fields: One-Pager

**Date:** 2026-02-18
**Author:** [Your Name]
**Status:** Draft for Review

---

## 🎯 Executive Summary

Service businesses need to capture industry-specific data that doesn't fit our standard fields. Most critically, commercial contractors cannot track **purchase order numbers, which blocks payment collection** when customers refuse to pay without a PO on the invoice. Without custom fields, customers use unstructured workarounds (tags, notes, spreadsheets) that break reporting and create data quality issues. Customer feedback shows 6,206+ mentions, with 42% marked High Priority. Both Jobber and ServiceTitan offer custom fields. Use cases include PO tracking, lead intake, equipment management, and marketing attribution.

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
- **Competitive validation:** Both Jobber (4.5⭐, SMB leader) and ServiceTitan (Enterprise leader) offer custom fields
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

### 📊 Competitive Landscape

Both leading competitors offer custom fields as core infrastructure:
- **Jobber:** Custom fields available on 6 objects (Properties, Clients, Quotes, Jobs, Invoices, Team members)
- **ServiceTitan:** Custom fields available on 10+ objects with required field enforcement, conditional logic, and advanced reporting

---

## 📚 Supporting Materials

- [Custom Fields: Insights Brief](/Users/mikaylawickman/dev/reports/custom-fields/INSIGHTS_BRIEF.md) - Comprehensive problem space research
- [Research Findings](/Users/mikaylawickman/dev/reports/custom-fields/research-findings.md) - Detailed VOC data and competitive analysis
- [PRD: Custom Fields](https://housecall.atlassian.net/wiki/spaces/EE/pages/3791880362) | [Product Strategy & Roadmap](https://housecall.atlassian.net/wiki/spaces/EE/pages/3811770933) | [Competitive Research](https://housecall.atlassian.net/wiki/spaces/EE/pages/3839591526) (Confluence)

**Data Sources:** Reforge (6,206 VOC mentions), 8 internal Confluence docs, Jobber/ServiceTitan product documentation

