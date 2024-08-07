# Quandis Website Requirements

Quandis will contract with a website designer to create a new site, hosted on a platform like WordPress.com, by restructuring our [existing site](https://www.quandis.com/) and porting existing content into the restructured site. High level requirements include:

- Designing a site navigation layout (menuing)
- Choosing a theme
- Porting existing content into the new site
  - suggestions on editing existing content are encouraged, but not required
- Enabling some content to require social sign-in, so we can identify the user(s) access some resources
  - example: right now, our [Business Continuity Plan](https://www.quandis.com/about/support/business-continuity) requires a simple password
  - we'd prefer to collect an email address via SSO to access similar resources
- Propose e-commerce integration (see below for details)

We expect the site to maintained by:

- Marketing employee for landing pages and other marketing content
- Developers for technical documentation, using markdown
- Automation for technical documentation, pushing markdown to the site using an API for additions and updates

We're looking for an estimate to execute on these requirements.

# Background

Quandis is a Fintech software company that sells:

- Quandis Business Objects (QBO) which is a Platform-as-a-Service
- Several Software-as-a-Service products built upon QBO
  - [Military Compliance](https://www.quandis.com/qmc): search or monitor contacts for eligibility for MLA and SCRA protections
  - [Bankruptcy Search](https://www.quandis.com/products/data-services/qbs): search or monitor contacts for bankruptcy
  - [Title Direct](https://www.quandis.com/products/applications/quandis-title-direct): centralize ordering of Title products across departments
  - [Attorney Data Reporting](https://www.quandis.com/freddiemacadr_attorneyguide_html): enable foreclosure and bankruptcy attorneys to report case status to their clients

# Goals

Quandis wished to redesign it's website with the following goals:

- For a software company, our current site looks old and unprofessional - need to modernize it
  - however, it's got lots of content that can probably be repurposed
- Clearly demonstrate the value proposition of QBO, and each product
- Include landing pages for email campaigns for each product, targeting different industries
  - industries include Banking, Mortgage Servicing, Insurance, Fintech Software Platforms, Debt Recovery
- Port our user documentation current in an Azure Devops Blog into the www.quandis.com site

## Sites we like

Some websites that we think convey a technology platform/product well include:

- [Twilio](https://www.twilio.com/en-us)
- [LogicMonitor](https://www.logicmonitor.com/)
- [Microsoft Dynamics](https://dynamics.microsoft.com/en-us/)
- [Microsoft Learn](https://learn.microsoft.com/en-us/docs/)
- [Decisions](https://decisions.com/)

# Site Structure

As part of this project, create at least one page for each of the bulleted items listed below. Specified goals are annoated in italics. 

## Navigation

Our suggested main menu structure is below. We expect at a minimum the sub of each second-level page (unless 'optional' is specified).

- Home: company overview
- [Platform](https://www.quandis.com/products/platform): QBO, with sub-menu items for each module 
- Services: _describe SaaS products to decision makers / check writers, with a "Sign up Now" form to hook into the e-commerce portion noted below_
  - [Military Compliance](https://www.quandis.com/products/qmc)
  - [Bankruptcy Search](https://www.quandis.com/products/data-services/qbs)
  - [Attorney Data Reporting](https://www.quandis.com/freddiemacadr_attorneyguide_html) (optional)
- Industries: _brief overview of industries that Quandis products are in use_
  - Mortgage Servicing: _showcase use cases_
  - Auto Finance: _showcase use cases_ (optional)
  - Bridge Loans: _showcase use cases_ (optional)
  - Debt Recovery: _showcase use cases_ (optional)
- Learn: describe QBO and SaaS products to **end users**, **power users**, and **developers**
  - Platform
    - Overview
    - Documents: example content for [end user](https://www.quandis.com/products/platform/document-management), [power user](https://dev.azure.com/quandisopensource/Documentation/_wiki/wikis/Documentation.wiki/5/Document-Management), [developer](https://github.com/quandis/qbo3-Documentation/wiki/document-api)
  - Military Compliance (optional)
  - Bankruptcy Search (optional)
  - Attorney Data Reporting (optional)
  - _eventually, this portion of the site will be auto-updated from our code repos via docfx, pushing markdown via API calls_
  - [existing content is here](https://dev.azure.com/quandisopensource/Documentation/_wiki/wikis/Documentation.wiki/72/Introduction-to-QBO)
    - suggestions on restructing this existing content are welcome
- Partners: content describing our existing partners, with a 'Become a Reseller' and 'Become an Integrator' link to a contact form
- Support: content info, ISO info, etc, akin to our [existing support page](https://www.quandis.com/about/support)

## The Learn portion of the website is the most complicated

A specific navigation requirement for the Learn portion of the website:  we're looking for suggestions on how to present the same concepts, in different depth, to difference audiences.
For example, when looking at the `learn/platform/document page`, I should be able to toggle between:
- End User: `learn/platform/document/enduser`, 
- Power User: `learn/platform/document/poweruser`, and
- Developer: `learn/platform/document/developer pages` views

Once I'm on the 'poweruser' view, navigating to `learn/platform/message` in the main menu should take me to `learn/platform/message/poweruser`.
If there is no `learn/platform/message/poweruser` page, revert to `learn/platform/message`.

## Minimum Pages 

The minimum deliverable should include the following routes:

- /home: content based on https://www.quandis.com/
- /platform: content from https://www.quandis.com/products/platform
- /services: content based on https://www.quandis.com/products/data-services
- /services/militarycompliance: content based on https://www.quandis.com/qmc
- /services/bankruptcysearch: content based on https://www.quandis.com/products/data-services/qbs
- /industry: our industries are Financial Services, Insurance, and Mortgage
  - something like https://www.twilio.com/en-us/solutions/real-estate or
  - https://www.twilio.com/en-us/solutions/financial-services
- /industry/mortgageservicing
- /learn: content based on https://dev.azure.com/quandisopensource/Documentation/_wiki/wikis/Documentation.wiki/72/Introduction-to-QBO
- /learn/platform: content based on https://dev.azure.com/quandisopensource/Documentation/_wiki/wikis/Documentation.wiki/85/Configuration-Guide
- /learn/platform/document
- /learn/platform/document/enduser: content based on https://dev.azure.com/quandisopensource/Documentation/_wiki/wikis/Documentation.wiki/92/Document-Management
- /learn/platform/document/poweruser: content based on https://dev.azure.com/quandisopensource/Documentation/_wiki/wikis/Documentation.wiki/5/Document-Management
- /learn/platform/document/developer: **the core content must be done in markdown**,  content based on https://github.com/quandis/qbo3-Documentation/wiki/document-api
- /partners: something like https://appsource.microsoft.com/en-us/marketplace/partner-dir
- /support: content based on https://www.quandis.com/about/support
- /support/policy/businesscontinuity: content based on https://www.quandis.com/about/support/business-continuity, password is QuandisPolicie$
  - this should require that we collect an email address before the user can access it, preferably via social sign-in

# E-Commerce integration

For Quandis' SaaS products, we'd like a "Sign up Now" button that accepts a credit card / ACH information from the user. However, the SaaS charges are pay-as-you-go, so each client's bill will change each month. Thus, we need:

- Credit card / bank account info handled in a PCI-compliant manner
- Basic user information stored in a location easily fetch via API
- The ability to trigger an invoice monthly

If there is a third-party component that you propose using that meets these requirements, great.

If not, Quandis's system include APIs to do much of this, so calling our APIs direct from the website form(s) is an option.
