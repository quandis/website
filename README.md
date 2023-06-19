# Quandis Website Requirements

Quandis will contract with a WordPress designer to create a new site, hosted on WordPress.com, by restructuring our [existing site](https://www.quandis.com/) and porting existing content into the restructured site. High level requirements include:

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
- Automation for technical documentation, pushing markdown to the site using the WordPress API

We're looking for an estimate to execute on these requirements.

# Background

Quandis is a Fintech software company that sells:

- Quandis Business Objects (QBO) which is a Platform-as-a-Service
- Several Software-as-a-Service products built upon QBO
  - [Military Search](https://www.quandis.com/products/data-services/qms): search or monitor contacts for eligibility for MLA and SCRA protections
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

# Site Structure

Our suggested main menu structure includes:

- Home: company overview
- [Platform](https://www.quandis.com/products/platform): QBO, with sub-menu items for each module 
- Services: describe SaaS products to decision makers / check writers
  - sub-menu for each product? /military/insurance, /bankruptcy/insurance ?
  - sub-menu for each industry? /insurance/miliary, /insurance/bankruptcy ?
- Learn: describe QBO and SaaS products to end users, power users, and developers
  - eventually, this portion of the site will be auto-updated from our code repos via docfx, pushing markdown via WordPress API calls
  - [existing content is here](https://dev.azure.com/quandisopensource/Documentation/_wiki/wikis/Documentation.wiki/72/Introduction-to-QBO)
    - suggestions on restructing this existing content are welcome
- Partners: content describing our existing partners
- Support: content info, ISO info, etc, akin to our [existing support page](https://www.quandis.com/about/support)

> Not sure how to best mesh the concept that Military Search is the same product offering different value to different industries.
> Perhaps another main menu for Industry? 

# E-Commerce integration

For Quandis' SaaS products, we'd like a "Sign up Now" button that accepts a credit card / ACH information from the user. However, the SaaS charges are pay-as-you-go, so each client's bill will change each month. Thus, we need:

- Credit card / bank account info handled in a PCI-compliant manner
- Basic user information stored in a location easily fetch via API
- The ability to trigger an invoice monthly

If there is a third-party component that you propose using that meets these requirements, great.

If not, Quandis's system include APIs to do much of this, so calling our APIs direct from the WordPress form(s) is an option.
