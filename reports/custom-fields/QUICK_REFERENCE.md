# Custom Fields - Quick Reference Guide

**Last Updated:** 2026-02-17

---

## 📊 Key Numbers

| Metric | Value |
|--------|-------|
| **Total VOC Mentions** | 6,206 feedback items |
| **High Priority Requests** | 42% of feedback (critical/blocking) |
| **Active Confluence Docs** | 8 planning/research documents |
| **Competitor Comparison** | Jobber (4.5★) vs ServiceTitan (Enterprise) |

---

## 🔥 Top 6 Customer Pain Points (Custom Fields Focus)

| Rank | Pain Point | Volume | Impact |
|------|------------|--------|--------|
| **#1** | Lead Form Flexibility | 20+ mentions | **HIGH** - Sales teams blocked from capturing industry-specific data |
| **#2** | Custom Invoice Fields | 18+ mentions | **HIGH** - Need company-specific data on invoices (custom headers, notes) |
| **#3** | Field Tech Reporting | 18+ mentions | **MEDIUM** - Can't create custom reports with field tech data |
| **#4** | Mandatory Field Enforcement | 15+ mentions | **HIGH** - Data quality issues, incomplete records |
| **#5** | PO Number Fields | 12+ mentions | **CRITICAL** - Required for payment from commercial/government clients |
| **#6** | Multi-Property Notes Access | 10+ mentions | **MEDIUM** - Can't easily find historical notes across properties |

---

## 💬 Top 10 Customer Quotes

### 1. Lead Form Limitations
> "I created a Trade partner lead form and would like to customize it some, but it seems that my choices are very limited unlike the link to Book now on our website that takes you to HCP"
**Relevance:** HIGH - Sales intake blocker

### 2. Basic Functionality Gap
> "I can't believe there's no way to add it my own field custom field to a form it's like so basic"
**Relevance:** HIGH - Expectation mismatch

### 3. Marketing Tracking
> "I just started with MAX, and I was wondering how I could add custom fields to my customers to track things like Meta Pixel ID and GCLID."
**Relevance:** MEDIUM - Marketing attribution

### 4. Mandatory Field Request
> "can i set job fields to be mandatory field to fill out when creating a new job?"
**Relevance:** HIGH - Data quality enforcement

### 5. Multi-property Notes Issue
> "Our technicians have a hard time finding private notes on some of our customers that have multiple properties"
**Relevance:** MEDIUM - Search/accessibility issue

### 6. PO Number Request
> "Hi do you have a feature or field for customer PO's. That won't pay unless the po is on the invoice"
**Relevance:** CRITICAL - Payment blocker

### 7. PO Field Need - Business Control
> "What I need is a PO Field on HCP, That field should be alpha numeric, but understanding different Pros, we should have the option to Create some extra personalized Fields, to get more control of our Customer and be able to identify better some specific scenarios"
**Relevance:** HIGH - Business control & customization

### 8. Invoice Customization Need
> "Please allow for custom inputs on the invoice like Progress Payment #1 or Service address or a custom space"
**Relevance:** MEDIUM - Invoice flexibility

### 9. Historical Data Access
> "I just want to make sure that you're understanding what I'm looking for. We're not trying to create something for the customer; this would simply be custom forms that are viewed on our side of things. The checklist add-on is very limited, and those forms only attached to the job itself not the customer or the property. So if I was looking for notes on a job from 10 years ago, I might be swiping through 10 years of visits before I find the one that has that note in the checklist."
**Relevance:** MEDIUM - Long-term data organization

---

## 🎯 Personas & Industries

### By Industry (Service Type)
- **HVAC/Home Services:** 35% - Equipment/property tracking focus
- **General Contracting:** 25% - PO numbers, field coordination
- **Property Management:** 20% - Multi-property billing
- **Specialized Trades:** 20% - Industry-specific fields

### By User Role
- **Office Managers/Dispatchers:** 45% - Forms, invoices, intake
- **Field Technicians:** 30% - Mobile access, required fields
- **Owners/Managers:** 25% - Reporting, analytics

---

## 🏗️ Internal Planning Status

### Phased Approach (from Confluence)
- **Phase 1:** Dropdown fields on Customers only
- **Phase 2:** Text/Number fields + Gate Code support
- **Phase 3:** Multi-object expansion

### Internal Use Cases Identified
1. Churn Reason (dropdown)
2. Gate Code (text/number) - Phase 2
3. Time Preference (dropdown)
4. Lead Source Detail (text/dropdown)
5. Non-booking Reason (dropdown)

### Architecture Decided
- **Shared field model** (not duplicated across objects)
- **Organization-scoped** configuration
- **Franchise support** (Command & Control integration)
- **Performance:** JSONB rejected for filtering/reporting needs

---

## 🔍 Competitive Landscape

### Jobber (SMB Focus)
- ✅ Simple, intuitive setup
- ✅ Strong mobile (4.7-4.8★ rating)
- ✅ Transferable fields (job → invoice)
- ✅ Client-facing visibility toggle
- ⚠️ Limited customization depth
- ⚠️ Basic reporting

### ServiceTitan (Enterprise Focus)
- ✅ Deep customization capabilities
- ✅ Conditional logic & auto-tagging
- ✅ Granular permissions
- ✅ Advanced reporting integration
- ⚠️ Steep learning curve
- ⚠️ Expensive, resource-intensive
- ⚠️ Complex implementation

### Investment Direction
- **Jobber:** Maintenance mode on custom fields; innovating in payments/mobile
- **ServiceTitan:** Stable infrastructure; innovating in AI/automation tied to fields

---

## ⚠️ Gaps: VOC vs Internal Planning

| VOC Priority | Volume | Internal Plan | Gap Status |
|--------------|--------|---------------|------------|
| **PO Number Fields** | 12+ | Not in core use cases | ⚠️ **Phase 2** (text fields) but not prioritized |
| **Property Customization** | 25+ | Not in Phase 1-3 scope | 🔴 **Missing** from roadmap |
| **Required Field Enforcement** | 15+ | Listed in "Future Work" | ⚠️ **Not planned** for Phase 1-2 |
| **Lead Form Flexibility** | 20+ | Partial (Lead Source Detail) | ⚠️ **Form-level** customization missing |
| **Dropdown Removal** | 15+ | Can add, not remove | ⚠️ **Hide/remove** system defaults not planned |

---

## 📋 Checklist: What to Include in Insights Brief

### Problem Definition
- [ ] Distinguish field setup vs workflow impact
- [ ] Identify must-have vs nice-to-have functionality
- [ ] Explain why current workarounds (tags, notes) fall short

### Voice of Customer
- [ ] Volume metrics by theme
- [ ] Top 10 customer quotes with relevance scores
- [ ] Specific use cases (PO tracking, equipment types, marketing attribution)
- [ ] Pain points without feature (blocked payments, data quality, lost context)

### Personas
- [ ] Who creates/manages fields (Office Managers, Admins)
- [ ] Who fills/uses fields (Field Techs, Dispatchers)
- [ ] Who should/shouldn't edit (permissions needed)
- [ ] Industry patterns (HVAC heavy, Property Management needs)

### Competitive Intelligence
- [ ] Jobber implementation (simplicity, transferable fields)
- [ ] ServiceTitan implementation (conditional logic, permissions)
- [ ] Permission models comparison
- [ ] Investment direction (stable infrastructure, innovation in automation)

### Current State
- [ ] Existing Job Fields system (Job Type, Business Unit)
- [ ] Architecture patterns already established
- [ ] Known gaps (required fields, property scope, form customization)
- [ ] Workarounds customers use today (tags, notes, checklists)

---

## 🚀 Next Steps

1. **User Review:** Present findings for validation
2. **Gap Analysis:** Discuss VOC vs Planning misalignment
3. **Brief Creation:** Consolidate into INSIGHTS_BRIEF.md after approval
4. **Follow-up Research:** Deeper dive on high-priority gaps if needed

---

## 📎 Sources

- **Reforge VOC:** 6,206 feedback mentions analyzed
- **Confluence:** 8 active planning/research documents
- **Competitive:** Jobber & ServiceTitan public documentation + reviews
- **Research Date:** 2026-02-17