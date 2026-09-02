# Google Ads API Keyword Planning Tool

Public project documentation for a Google Ads API Basic Access application.

This page describes an internal keyword research and Google Ads campaign planning tool being developed by an individual advertiser for my own ecommerce project.

The tool is currently under development. The Google Ads API pilot described below has not yet been executed.

---

## Review summary

- **Operator:** Individual advertiser / developer
- **Project type:** Internal ecommerce advertising research tool
- **Primary purpose:** Google Ads keyword research and campaign planning
- **Intended users:** Internal use only
- **External clients:** None
- **Third-party Google Ads account management:** None
- **Primary API service:** `KeywordPlanIdeaService`
- **Initial API operation:** `GenerateKeywordHistoricalMetrics`
- **Campaign type supported:** Search
- **Campaign creation or management:** Not supported during the P3 pilot
- **Current status:** Tool under development; controlled API validation pilot not yet executed
- **Requested access:** Google Ads API Basic Access

## Supporting documentation

A detailed design document describing the planned P3 pilot, API scope, data flow, validation process, access model, and current development status is publicly available here:

[View the Google Ads API P3 Tool Design document (PDF)](./Google_Ads_API_P3_Tool_Design.pdf)

The document describes the planned tool and validation workflow. It does not claim that the API pilot has already been executed or that Google Ads API data has already been validated against Google Keyword Planner.

---

## Project overview

I am developing an internal Google Ads API tool for my own ecommerce advertising workflow.

The tool is intended to support keyword research and planning for future Google Search advertising campaigns.

It is not:

- a commercial software product;
- a SaaS product;
- licensed or sold to other businesses;
- available to the general public;
- used to manage third-party Google Ads accounts.

The project is being developed for my own advertising research and planning.

## Business model

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

## Planned pilot workflow

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

## Intended users and access model

The tool is for internal use only.

Access is limited to:

- me; and
- internal collaborators working on my own ecommerce advertising and research workflow, if needed.

The tool will not be provided to:

- clients;
- unrelated advertisers;
- third-party companies;
- the general public.

No third-party advertiser will be able to use my developer token through this tool.

## Google Ads campaign relationship

The keyword research produced by the tool is intended to support planning and keyword selection for future Google Search campaigns for my own ecommerce project.

The P3 pilot itself is read-only from an advertising-management perspective.

During this stage, the tool will not:

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

Campaign creation and campaign-management automation are outside the scope of the current P3 pilot.

## Why Basic Access is requested

The developer token currently has Test Account Access.

Basic Access is requested so the controlled keyword-planning pilot can use the Google Ads API functionality required to evaluate historical keyword metrics in the relevant production Google Ads environment.

The requested use is limited to keyword planning and research supporting my own advertising workflow.

The initial controlled use is intentionally small in scope.

## Current development status

The tool is currently under development.

The controlled Google Ads API pilot has not yet been executed.

Current preparation includes:

- defining the validation workflow;
- documenting the intended API scope;
- preparing the Google Cloud project;
- obtaining the appropriate Google Ads API access level;
- preserving existing manual Google Keyword Planner measurements for later comparison.

OAuth configuration, API execution, and the controlled comparison will only proceed when the required access and configuration are available.

No claim is made that:

- the P3 pilot is already running;
- API parity with Keyword Planner has already been confirmed;
- the API already replaces the manual Keyword Planner workflow;
- the tool currently performs production campaign management.

## Data handling and security

Sensitive authentication information is not published in this repository.

The following are never intentionally published here:

- Google Ads developer tokens;
- OAuth client secrets;
- OAuth refresh tokens;
- passwords;
- backup codes;
- private credentials;
- secret keys.

Public identifiers and project documentation may be used only where necessary to explain the tool and its intended Google Ads API use.

This repository exists to provide transparent public information about the project for Google Ads API review.

## Public documentation purpose

This public page is maintained so that the Google Ads API review team can examine:

- the business model;
- the purpose of the API tool;
- the intended audience;
- the planned Google Ads API functionality;
- the relationship between the API data and future Google Ads campaign planning;
- the current development status;
- the limitations of the initial pilot.

Because the tool is still under development, this documentation describes the planned implementation and validation workflow rather than representing an already completed production application.

## Project operator

This project is operated by **Oleksandr Okrepkyi** as an individual advertiser and developer.

Public professional profile:

https://www.linkedin.com/in/oleksandr-okrepkyi/

The active contact email for the Google Ads API application is provided directly to Google through the Google Ads API Center and Basic Access application.

## Official Google Ads API documentation

The planned functionality is based on the following Google Ads API documentation:

### Generate Historical Metrics

https://developers.google.com/google-ads/api/docs/keyword-planning/generate-historical-metrics

### Google Ads API Access Levels and Permissible Use

https://developers.google.com/google-ads/api/docs/api-policy/access-levels

### Google Ads API Developer Token

https://developers.google.com/google-ads/api/docs/api-policy/developer-token

---

## Important status statement

**This project is currently in the access and validation-preparation stage.**

The P3 API comparison has not yet been executed, Google Ads API parity with the existing manual Keyword Planner workflow has not been established, and the API does not currently replace that manual workflow.
