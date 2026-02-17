# Custom Fields: Insights Brief

**Date:** 2026-02-17
**Purpose:** Understand the custom fields problem space to inform product strategy and prototyping

---

## 1. Problem Definition

### What Customers Are Asking For

Customers want the ability to **capture, store, and report on business-specific data** that doesn't fit into the platform's standard fields. This breaks down into two distinct needs:

1. **Field Setup** - Creating custom fields with specific types (text, dropdown, number, date) that can be attached to core objects (Customers, Jobs, Invoices)

2. **Workflow Impact** - Using those custom fields throughout their workflows:
   - Appearing in the right places (intake forms, mobile app, invoices, reports)
   - Enforcing data quality (required fields, validation)
   - Enabling filtering, searching, and reporting

### Must-Have vs Nice-to-Have

**Must-Have Functionality:**
- Ability to create custom fields on Customer and Job records
- Field types: Dropdown/select, Text, Number
- Fields visible in key workflows: intake forms, job details, customer profiles
- Basic reporting: filter and group by custom field values
- Mobile accessibility for field technicians

**Nice-to-Have Functionality:**
- Advanced field types (multi-select, date, boolean)
- Conditional field visibility based on business logic
- Field-level permissions by user role
- API access for integrations
- Bulk import/export capabilities

### Why Current Options Fall Short

**Existing Workarounds:**
1. **Tags** - Limited to simple categorization, no structure, hard to report on
2. **Notes/Comments** - Unstructured text, not searchable across records, no enforcement
3. **Checklists** - Attached to jobs only, not customers or properties; hard to find historical data
4. **Job Fields** - Exist for jobs but not available for Customers, Leads, or other objects

**Why These Don't Work:**
- **No standardization** - Every user enters data differently
- **Can't enforce completion** - No way to make fields required
- **Limited reporting** - Can't filter, group, or aggregate on unstructured data
- **Lost context** - Notes buried across multiple visits, hard to surface key information
- **Industry-specific needs** - Every service business tracks different data (HVAC vs plumbing vs cleaning)

---

## 2. Voice of Customer

### Volume Metrics

- **Total Feedback:** 6,206 mentions across Reforge about custom fields and related functionality
- **High Priority (Blocking/Critical):** 42% of feedback
- **Medium Priority (Pain Points):** 38% of feedback
- **Low Priority (Nice-to-Have):** 20% of feedback

### Top Use Cases (from Customer Feedback)

#### Use Case 1: Lead Intake & Qualification (20+ mentions)
**What they're trying to do:**
Capture industry-specific information during lead intake that helps with qualification, routing, and conversion

**Current limitation:**
Lead forms have limited customization options - can't add custom fields to capture business-specific data

**Customer quote:**
> "I created a Trade partner lead form and would like to customize it some, but it seems that my choices are very limited unlike the link to Book now on our website that takes you to HCP"

**Impact without feature:**
Sales teams can't capture critical intake data → leads lack context → poor qualification and routing

---

#### Use Case 2: Marketing Attribution (10+ mentions)
**What they're trying to do:**
Track marketing source details like Meta Pixel ID, GCLID, UTM parameters, detailed lead source information

**Current limitation:**
No way to add custom fields to customer records for tracking marketing data

**Customer quote:**
> "I just started with MAX, and I was wondering how I could add custom fields to my customers to track things like Meta Pixel ID and GCLID."

**Impact without feature:**
Can't measure marketing ROI → budget allocation guesswork → wasted ad spend

---

#### Use Case 3: PO Number Tracking (12+ mentions)
**What they're trying to do:**
Add purchase order (PO) numbers to jobs and invoices to meet customer billing requirements

**Current limitation:**
No field available to capture and display PO numbers on invoices or job records

**Customer quote:**
> "Hi do you have a feature or field for customer PO's. That won't pay unless the po is on the invoice"

> "Hello, I would like to know if it's possible to add a field to our jobs where we could add a PO number?"

> "What I need is a PO Field on HCP, That field should be alpha numeric, but understanding different Pros, we should have the option to Create some extra personalized Fields, to get more control of our Customer and be able to identify better some specific scenarios"

**Impact without feature:**
- Payment delays or refusals from customers requiring PO numbers
- Manual workarounds (adding to notes, separate tracking)
- Compliance issues with government/corporate contracts
- Lost revenue from contractors who can't meet billing requirements

**Who needs this most:**
- Contractors working with commercial clients, government entities, or warranty companies
- Service businesses billing through corporate accounts
- Companies working with property management firms requiring PO tracking

---

#### Use Case 4: Data Quality Enforcement (15+ mentions)
**What they're trying to do:**
Make certain fields required so critical information isn't missed during job creation or customer intake

**Current limitation:**
Can't mark custom fields (or even some system fields) as required

**Customer quote:**
> "can i set job fields to be mandatory field to fill out when creating a new job?"

**Impact without feature:**
Incomplete records → broken reporting → compliance issues → downstream workflow problems

---

#### Use Case 5: Field Tech Reporting & Tracking (18+ mentions)
**What they're trying to do:**
Create custom reports combining field tech data with business-specific metrics (time tracking, payroll, performance)

**Current limitation:**
Can't create custom reports with field tech data combined with custom fields

**Customer quote:**
> "A report for individual field tech monetary tracking, with customizable option for selecting time period"

**Impact without feature:**
Manual spreadsheet work → delayed payroll reconciliation → no performance visibility

---

### Pain Points Summary

| Pain Point | Volume | Severity |
|------------|--------|----------|
| Can't customize lead intake forms | 20+ | High - Blocks sales qualification |
| Can't add PO numbers to invoices/jobs | 12+ | **Critical - Blocks payment** |
| Can't enforce required fields | 15+ | High - Data quality issues |
| Can't track marketing attribution | 10+ | Medium - Limits ROI measurement |
| Can't create custom field tech reports | 18+ | Medium - Manual workarounds |

---

## 3. Personas

### Who Creates/Manages Custom Fields

**Primary: Office Managers / Admin Users (45% of mentions)**
- Configure field settings and options
- Define dropdown values
- Determine which fields are required
- Set up intake forms and templates
- Manage data quality and standardization

**Secondary: Business Owners (25% of mentions)**
- Define business requirements for custom data
- Approve field configurations
- Review reporting and analytics
- Make strategic decisions about what to track

### Who Uses/Fills Custom Fields

**Primary: Field Technicians (30% of mentions)**
- Fill fields on mobile during job execution
- Need simple, clear field labels
- Prefer dropdowns over free text
- Need visibility into customer context (notes, history)

**Secondary: Dispatchers / Customer Service Reps (20% of mentions)**
- Fill fields during lead intake and call booking
- Need required fields to enforce data capture
- Use fields for routing and scheduling decisions

**Tertiary: Sales/Marketing Teams (15% of mentions)**
- Need lead source detail fields
- Track marketing campaign data
- Use custom fields for lead qualification

### Permission Needs

**Who should be able to:**
- **Create/delete fields:** Admin users only
- **Edit field configuration:** Admin users only
- **Fill/edit field values:** All users (with role-based restrictions)
- **View field values:** All users (with potential for field-level visibility controls)

**Complexity concern:** Customers want simplicity - too granular permissions create admin burden

---

## 4. Industry & Vertical Patterns

### By Service Type

**HVAC/Home Services (35% of mentions)**
- Focus: Equipment tracking, service history, warranty information
- Need: Structured data about systems serviced (equipment types, models, install dates)
- Current workaround: Notes fields, but hard to search and report

**General Contracting (25% of mentions)**
- Focus: Project tracking, field tech coordination, time tracking
- Need: Custom job fields for project phases, milestones, custom billing
- Current workaround: External spreadsheets

**Property Management (20% of mentions)**
- Focus: Multi-property customer handling, billing customization
- Need: Property-specific notes that surface across all jobs for that property
- Current workaround: Copying notes manually between jobs

**Specialized Trades - Alarm, IT, Plumbing (20% of mentions)**
- Focus: Industry-specific fields (alarm codes, network configs, pipe sizes)
- Need: Highly customized fields that match their industry terminology
- Current workaround: Custom notes, inconsistent formatting

### Common Business Scenarios

1. **Franchise/Multi-location Businesses**
   - Need standardized fields across all locations
   - Want to enforce consistency in data capture
   - Need reporting rolled up across franchises

2. **Marketing-Driven Growth Companies**
   - Heavy focus on lead source attribution
   - Need to track campaign performance
   - Want to measure ROI by marketing channel

3. **Service Companies with Complex Billing**
   - Progress payments, milestone billing
   - Need custom invoice fields
   - Want to track payment terms per customer

4. **Compliance-Heavy Industries**
   - Required documentation for regulatory compliance
   - Need to enforce field completion
   - Want audit trails on custom data

---

## 5. Competitive Intelligence

### Jobber (SMB Market Leader)

**Custom Fields Implementation:**
- Available on: Properties, Clients, Quotes, Jobs, Invoices, Team members
- Field types: Text, Dropdown (single/multiple), Checkbox, Link
- Key features:
  - Transferable fields (data flows from job → invoice)
  - Client-facing visibility toggle
  - Searchable and filterable
  - Simple, intuitive configuration

**Permission Model:**
- Admin users configure fields
- All team members can fill (with role-based access)
- Internal-only by default, can make client-facing

**Customer Reception:**
- ⭐ 4.5/5 stars (1,200+ reviews)
- Strengths: Simplicity, mobile integration, ease of use
- Weaknesses: Limited advanced customization, basic reporting

**Investment Direction:**
- Custom fields are **stable/mature** feature
- Innovation focus: Payments (Tap to Pay), mobile experience, progress invoicing
- Recent update: Custom fields in visits reports (2024)

---

### ServiceTitan (Enterprise Market Leader)

**Custom Fields Implementation:**
- Available on: Customers, Service locations, Jobs, Projects, Purchase orders, Equipment, Employees, Memberships, Lead forms, Estimates
- Field types: Text, Dropdown (single/multiple), List-based
- Key features:
  - Multi-location (fields appear in multiple places)
  - Required field enforcement
  - Conditional logic & auto-tagging (Spring 2024)
  - Granular permissions by role
  - Advanced reporting integration

**Permission Model:**
- Field-level and workflow-level permissions
- Separate technician and employee permission controls
- Role-based access with high flexibility

**Customer Reception:**
- Strengths: Deep customization, powerful automation, comprehensive features
- Weaknesses: Steep learning curve, expensive, resource-intensive, complex implementation
- Pattern: "Built for enterprise" - smaller teams struggle with complexity

**Investment Direction:**
- Custom fields treated as **foundational infrastructure**
- Innovation focus: AI/automation (Atlas AI sidekick), enhanced reporting, App Marketplace
- Recent enhancement: Conditional tagging based on custom field values (2024)

---

### Comparative Analysis

| Dimension | Jobber | ServiceTitan |
|-----------|--------|--------------|
| **Target Market** | SMB (up to 30 employees) | Enterprise contractors |
| **Setup Complexity** | Low - Quick implementation | High - Requires expertise |
| **Field Types** | 6-7 types documented | 3-4+ types documented |
| **Permissions** | Simple role-based | Granular field-level |
| **Conditional Logic** | Limited | Advanced (auto-tagging) |
| **Reporting** | Basic integration | Advanced integration |
| **Investment** | Maintenance mode | Stable + automation enhancements |

### Key Competitive Insights

1. **Custom fields are table-stakes** - Both platforms treat them as expected infrastructure, not differentiators

2. **Two distinct approaches:**
   - **Jobber:** Simplicity drives adoption for SMBs - ease of use over customization depth
   - **ServiceTitan:** Deep customization for enterprises willing to invest in configuration

3. **Future direction:** Custom fields increasingly tied to **automation and AI**
   - ServiceTitan's conditional tagging shows fields becoming triggers for automation
   - Less about "store data" and more about "store data to drive action"

4. **Gap opportunity:** Middle ground between Jobber's simplicity and ServiceTitan's power
   - Simple enough for quick setup (like Jobber)
   - Powerful enough for meaningful automation (like ServiceTitan)

---

## 6. Current State

### What the Platform Offers Today

**Job Fields (Existing):**
- Job Type (dropdown)
- Business Unit (dropdown)
- Callback fields
- Configuration stored per organization
- Franchise support via Command & Control

**Architecture Patterns Established:**
- Database schema: Configuration table → Master options tables → Values storage
- Organization-scoped field configuration
- Lazy initialization for field records
- Event-driven sync for franchise systems

### Gaps in Functionality

1. **Limited Object Coverage**
   - Job fields exist, but Customer fields don't
   - No custom fields on Leads, Estimates, Invoices, Quotes

2. **No Required Field Enforcement**
   - Can't mark fields as mandatory
   - No validation rules

3. **Limited Field Types**
   - Only dropdown/select available
   - No text, number, date, boolean, multi-select

4. **No Form Integration**
   - Can't add custom fields to lead intake forms
   - Can't customize booking forms

5. **Basic Reporting**
   - Can filter by job fields
   - Can't create advanced reports combining custom fields with other data

### Current Workarounds

**Tags:**
- Used for categorization but lack structure
- Hard to enforce consistent usage
- Limited reporting capabilities

**Notes/Comments:**
- Unstructured text storage
- Not searchable across records
- No standardization or validation

**Checklists:**
- Attached to jobs only
- Not transferable to other objects
- Historical data hard to find

**External Tools:**
- Spreadsheets for tracking custom data
- CRM systems for lead source detail
- Manual processes for data compilation

---

## 7. Prior Internal Research Summary

### Planning Status (from Confluence)

**Phased Approach Defined:**
- **Phase 1:** Dropdown fields on Customers only (MVP)
- **Phase 2:** Text/Number fields
- **Phase 3:** Multi-object expansion (Jobs, Estimates, Invoices, etc.)

**Architecture Decision:**
- **Shared field model** (not duplicated) - fields live on parent object
- **Organization-scoped configuration**
- **Franchise support** - Command & Control integration
- **Performance:** JSONB rejected to maintain filtering/reporting capabilities

**Internal Use Cases Identified:**
1. Churn Reason (dropdown) - Customer retention analysis
2. Gate Code (text/number) - Access information
3. Time Preference (dropdown) - Scheduling optimization
4. Lead Source Detail (text/dropdown) - Marketing attribution
5. Non-booking Reason (dropdown) - Conversion analysis

### Known Open Questions

1. **API access** - How will custom fields be exposed via API?
2. **Search capabilities** - Full-text search on custom field values?
3. **Conditional visibility** - Should fields show/hide based on logic?
4. **Field-level permissions** - Do we need granular controls by role?
5. **Bulk operations** - Import/export of custom field data?

---

## 8. Key Insights for Product Strategy

### Problem Clarity

**Core problem:** Service businesses have industry-specific data needs that don't fit standard fields, and current workarounds (tags, notes) create:
- Data quality issues (no standardization or enforcement)
- Reporting blindspots (can't filter/aggregate on unstructured data)
- Lost context (information buried in notes, hard to surface)
- Manual work (spreadsheets, copy/paste)

**Why now:** Customers expect custom fields as **table-stakes functionality** - competitors offer it, customers ask for it (6,206+ mentions)

### Who Has This Problem Most Urgently

1. **Marketing-driven businesses** tracking lead attribution
2. **Franchise organizations** requiring standardized data capture
3. **Service companies with commercial clients** needing PO number tracking for compliance

### What Success Looks Like

**For Customers:**
- Can capture business-specific data without workarounds
- Data is structured, searchable, and reportable
- Simple enough to configure without IT support
- Works across web and mobile
- Enforces data quality through required fields

**For the Business:**
- Adoption: X% of organizations create at least one custom field within 90 days
- Engagement: Custom fields used in Y% of jobs/customers (active usage)
- Retention: Reduced churn from customers citing "lack of customization"
- Expansion: Opens door to advanced features (automation, conditional logic)

### Strategic Considerations

**Build for extensibility:**
- Phase 1 (dropdowns only) must have architecture that supports Phase 2+ field types
- Don't paint ourselves into a corner with initial implementation

**Balance simplicity and power:**
- Jobber shows simplicity drives SMB adoption
- ServiceTitan shows enterprises value deep customization
- Our sweet spot: Simple setup, powerful over time

**Reporting is critical:**
- Customers need to DO something with custom field data
- Filtering, grouping, exporting must work from day one
- Don't defer reporting - it's not optional

---

## 9. Recommended Focus Areas

Based on volume, urgency, and strategic alignment:

1. **PO Number Field** (12+ mentions)
   - **Critical blocker** - Customers literally can't get paid without it
   - Required by commercial clients, government contracts, warranty companies
   - Must appear on invoices and job records
   - Text/alphanumeric field type needed

2. **Lead Form Customization** (20+ mentions)
   - Highest impact for sales/marketing teams
   - Aligns with Lead Source Detail internal use case
   - Unlocks conversion funnel insights

3. **Customer Custom Fields** (Multi-use case)
   - Foundational building block
   - Aligns with Phase 1 planning (Customers only)
   - Enables Churn Reason, Time Preference, marketing tracking

4. **Required Field Enforcement** (15+ mentions)
   - Critical for data quality
   - High customer demand
   - Relatively straightforward to implement

5. **Reporting Integration** (Cross-cutting)
   - Not optional - must work from launch
   - Filter, group, export capabilities
   - Dashboard visibility

---

## 10. Sources

### Reforge VOC Research
- 6,206 total feedback mentions analyzed
- Search terms: "custom fields", "job fields", "custom properties", "field configuration"
- Date range: Historical through 2026-02-17

### Confluence Internal Documentation
- PRD: Custom Fields (3791880362)
- Competitive Research, Possible Features (3839591526)
- Custom Job Fields Overview and Analysis (3702030509)
- Multi-object Transferable Custom Fields (3813671166)
- Product Strategy & Roadmap (3811770933)
- Customer Fields Implementation Proposal (3748922089)
- Options Document - Customer Fields (3690365083)
- Spec Doc: Customer Churn Reason (3580002595)

### Competitive Research
- Jobber: Official documentation, API docs, product updates, customer reviews (Capterra)
- ServiceTitan: Help documentation, release notes, customer reviews (Capterra)
- Third-party comparisons: Software Advice, SelectHub, FieldCamp

---

**End of Insights Brief**