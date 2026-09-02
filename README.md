# Google Drop 2026 — Google API Research Integrations

Public project documentation for Google API integrations being prepared for an internal ecommerce research and Google Ads planning workflow.

This project is operated by an independent developer and advertiser for my own ecommerce project.

The integrations described below are currently in the access and validation-preparation stage. No claim is made that either API has already been approved, fully integrated, or validated for production use.

---

## Review summary

- **Operator:** Individual advertiser / independent developer
- **Project type:** Internal ecommerce research and advertising planning
- **Commercial use:** Yes
- **Intended users:** Internal use only
- **External clients:** None
- **Third-party account management:** None
- **Public software or SaaS:** No
- **Automated campaign management:** Not part of the current scope

### Google Ads API

- **Purpose:** Keyword research and Google Ads campaign planning
- **Primary service:** `KeywordPlanIdeaService`
- **Initial operation:** `GenerateKeywordHistoricalMetrics`
- **Campaign type:** Search
- **Requested access:** Basic Access
- **Current status:** Application submitted; review pending
- **Initial pilot:** P3 controlled validation against manual Google Keyword Planner exports

### Google Trends API

- **Purpose:** Ecommerce research, market comparison, seasonality analysis, and search-interest research
- **Access requested:** Google Trends API Alpha
- **Organization type:** Independent developer
- **Use case:** Commercial
- **Current status:** Alpha application submitted; access not yet granted
- **Planned use:** Internal research only

---

# Google Ads API

## Google Ads API project overview

I am developing an internal Google Ads API tool for my own ecommerce advertising workflow.

The tool is intended to support keyword research and planning for future Google Search advertising campaigns.

It is not:

- a commercial software product;
- a SaaS product;
- licensed or sold to other businesses;
- available to the general public;
- used to manage third-party Google Ads accounts.

The project is being developed for my own advertising research and planning.

## Google Ads API business model

I am an individual advertiser operating my own ecommerce project.

The Google Ads API tool is an internal operational tool supporting my own keyword research and Google Ads campaign planning.

There is:

- no sale or licensing of the tool;
- no subscription model;
- no public user access;
- no client access;
- no management of Google Ads accounts belonging to other companies.

Any advertising decisions based on the research remain manual decisions made for my own ecommerce project.

## Intended Google Ads API use

The initial controlled pilot is designed to use:

- Google Ads API;
- `KeywordPlanIdeaService`;
- `GenerateKeywordHistoricalMetrics`.

The tool will request historical Google Search keyword metrics for a small, controlled set of keywords.

Planned request inputs include, where supported:

- keyword text;
- geographic targeting;
- language;
- Google Search network settings;
- historical date range.

The resulting metrics are intended to support:

- keyword evaluation;
- keyword prioritization;
- Google Search campaign planning;
- comparison of potential keyword opportunities before advertising decisions are made.

The API is being requested specifically for Google Ads keyword planning, not for general-purpose market data collection unrelated to advertising.

## Initial P3 validation pilot

Before relying on Google Ads API data in the planning workflow, the initial P3 pilot will perform a controlled side-by-side comparison between:

1. historical keyword metrics returned by `GenerateKeywordHistoricalMetrics`; and
2. manual exports previously collected from the Google Keyword Planner interface.

The same relevant market, language, network, keyword, and date-range parameters will be used where the interfaces and API support equivalent settings.

The purpose of the pilot is to determine whether API output is sufficiently consistent with the existing manual Keyword Planner workflow for the intended Google Ads planning use case.

At the current stage:

- the comparison has not yet been executed;
- parity has not been established;
- no claim is made that API results exactly match Keyword Planner;
- the API is not treated as a replacement for the existing manual Keyword Planner workflow.

## Planned Google Ads pilot workflow

The planned workflow is:

1. Select a small set of keywords that have already been measured manually in Google Keyword Planner.
2. Preserve the corresponding market, language, network, and relevant historical-period settings.
3. Request historical metrics using `KeywordPlanIdeaService.GenerateKeywordHistoricalMetrics`.
4. Store the returned metrics for internal analysis.
5. Match API results to the corresponding manually collected Keyword Planner records.
6. Compare the results side-by-side.
7. Record material differences.
8. Determine whether the API output is suitable for the intended Google Ads keyword-planning workflow.
9. Keep human review as the final decision step.

No automatic Google Ads campaign changes occur in this workflow.

## Google Ads API scope limitations

During the P3 stage, the tool will not:

- create Google Ads accounts;
- create campaigns;
- create ad groups;
- create ads;
- automatically add keywords to campaigns;
- modify existing campaigns;
- change bids;
- change budgets;
- modify billing or payment settings;
- manage third-party Google Ads accounts;
- perform App Conversion Tracking operations;
- perform Remarketing API operations.

Campaign creation and automated campaign management are outside the scope of the current P3 pilot.

## Why Google Ads API Basic Access is requested

The developer token currently has Test Account Access.

Basic Access is requested so the controlled keyword-planning pilot can evaluate the required Google Ads API functionality in the appropriate production Google Ads environment.

The requested use is limited to keyword planning and research supporting my own advertising workflow.

The initial controlled use is intentionally small in scope.

## Google Ads API supporting documentation

A detailed design document describing the planned P3 pilot, API scope, data flow, validation process, access model, and development status is publicly available here:

[View the Google Ads API P3 Tool Design document (PDF)](./Google_Ads_API_P3_Tool_Design.pdf)

The document describes the planned tool and validation workflow. It does not claim that the API pilot has already been executed or that Google Ads API data has already been validated against Google Keyword Planner.

---

# Google Trends API Alpha

## Google Trends API use case

I have applied for access to the Google Trends API Alpha for the same internal ecommerce research project.

The planned use is commercial internal research supporting my own ecommerce and future Google Ads planning.

The Google Trends API would be used programmatically to:

- compare search interest for product-related queries;
- analyze changes in search interest over time;
- identify seasonality;
- compare search-interest patterns across markets and regions;
- evaluate groups of related search terms;
- support product and market research;
- support keyword prioritization;
- provide an additional signal for future Google Ads planning.

## Relationship to other research sources

Google Trends data will be treated as one research signal among multiple sources.

It will not be treated as:

- proof of product demand by itself;
- a replacement for Google Keyword Planner;
- a replacement for Google Ads API keyword metrics;
- proof of profitability;
- an automatic product-selection decision.

The purpose is to combine Trends data with other evidence while preserving human review and source-specific limitations.

## Planned Google Trends workflow

If Alpha access is granted, the initial workflow will be:

1. Select a controlled set of product-related search terms.
2. Query Google Trends data for relevant time periods.
3. Compare search-interest patterns across selected markets where supported.
4. Analyze seasonality and material changes over time.
5. Compare related terms using consistent API-derived data.
6. Store results for internal research.
7. Compare Trends observations with other independent research sources.
8. Record limitations and disagreements instead of automatically treating Trends as definitive evidence.
9. Keep all product, market, and advertising decisions subject to human review.

## Intended users

The Google Trends API integration is for internal use only.

Access would be limited to:

- me; and
- internal collaborators working on my own ecommerce research and advertising workflow, if needed.

It will not be offered to:

- clients;
- unrelated advertisers;
- third-party companies;
- the general public.

## Current Google Trends API status

The Google Trends API Alpha application has been submitted.

Access has not yet been granted.

The planned integration has therefore not yet been implemented or executed.

I am prepared to begin controlled testing shortly after access is granted and to provide feedback to Google regarding:

- API integration experience;
- query workflows;
- data coverage;
- regional comparisons;
- time-series analysis;
- practical use in an ecommerce research workflow.

---

# Shared access model

Both integrations are intended for the same internal ecommerce research project.

They serve different purposes:

- **Google Ads API:** historical keyword metrics and Google Ads keyword planning;
- **Google Trends API:** relative search-interest patterns, time trends, seasonality, and regional comparisons.

Neither integration grants external users access to the underlying API credentials.

No third-party advertiser will be able to use my developer token or API credentials through these tools.

---

# Current development status

The project is currently in the access and validation-preparation stage.

Current work includes:

- defining controlled research workflows;
- documenting API scope and limitations;
- preparing the Google Cloud project;
- requesting the appropriate API access;
- preserving manually collected research data for later comparison;
- preparing validation procedures before relying on API-derived results.

No claim is made that:

- Google Ads API Basic Access has already been approved;
- Google Trends API Alpha access has already been approved;
- either API integration is currently running in production;
- Google Ads API parity with Keyword Planner has been confirmed;
- Google Trends data independently validates product demand;
- either API automatically makes product, market, or campaign decisions.

---

# Data handling and security

Sensitive authentication information is not published in this repository.

The following are never intentionally published here:

- Google Ads developer tokens;
- OAuth client secrets;
- OAuth refresh tokens;
- passwords;
- backup codes;
- private credentials;
- API keys;
- secret keys.

Public documentation is limited to information necessary to explain the project, intended API use, access model, and validation approach.

---

# Project operator

This project is operated by **Oleksandr Okrepkyi** as an individual advertiser and independent developer.

Public professional profile:

[Oleksandr Okrepkyi on LinkedIn](https://www.linkedin.com/in/oleksandr-okrepkyi/)

The active contact email used for API applications is provided directly to Google through the relevant application forms and Google API interfaces.

---

# Official Google documentation

## Google Ads API — Generate Historical Metrics

[Google Ads API — Generate Historical Metrics](https://developers.google.com/google-ads/api/docs/keyword-planning/generate-historical-metrics)

## Google Ads API — Access Levels and Permissible Use

[Google Ads API — Access Levels and Permissible Use](https://developers.google.com/google-ads/api/docs/api-policy/access-levels)

## Google Ads API — Developer Token

[Google Ads API — Developer Token](https://developers.google.com/google-ads/api/docs/api-policy/developer-token)

## Google Trends API Alpha

[Google Trends API](https://developers.google.com/search/apis/trends)

---

# Important status statement

**Google Ads API Basic Access and Google Trends API Alpha are currently access requests, not completed integrations.**

The Google Ads P3 comparison has not yet been executed, API parity with the existing manual Keyword Planner workflow has not been established, and Google Trends API Alpha access has not yet been granted.
