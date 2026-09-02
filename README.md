# Google Ads API Keyword Planning Tool

## Project overview

This repository provides public information about an internal Google Ads API tool being developed by an individual advertiser for my own ecommerce project.

The tool is not a commercial software product, is not offered to clients or the general public, and is not used to manage third-party Google Ads accounts.

Its purpose is to support keyword research and planning for future Google Search advertising campaigns for my own ecommerce project.

## Intended Google Ads API use

The initial pilot is designed to use:

- Google Ads API
- `KeywordPlanIdeaService`
- `GenerateKeywordHistoricalMetrics`

The tool will retrieve historical Google Search keyword metrics for a small, controlled set of keywords.

The planned inputs include:

- keywords
- geographic targeting
- language
- Google Search network settings
- historical date range where applicable

The resulting metrics will be used to evaluate and prioritize keywords for future Google Ads campaign planning.

## Initial validation pilot

Before relying on Google Ads API data in the planning workflow, the initial P3 pilot will perform a controlled side-by-side comparison between:

1. historical keyword metrics returned by `GenerateKeywordHistoricalMetrics`; and
2. manual exports previously collected from the Google Keyword Planner interface.

The purpose of this comparison is to evaluate whether the API results are sufficiently consistent with the manual Keyword Planner workflow.

At this stage, parity has not been established and the API is not treated as a replacement for manual Google Keyword Planner exports.

## Business model

I am an individual advertiser operating my own ecommerce project.

This API tool is an internal operational tool supporting my own Google Ads research and campaign planning.

There is:

- no sale or licensing of the tool;
- no public user access;
- no client access;
- no management of third-party advertiser accounts.

## Intended users

The tool is for internal use only.

Access is limited to me and internal collaborators working on my own ecommerce advertising and research workflow.

It will not be made available to external clients or the general public.

## Google Ads campaign relationship

The keyword research produced by the tool is intended to support planning and keyword selection for future Google Search campaigns for my own ecommerce project.

The P3 pilot itself is read-only.

During this stage, the tool will not:

- create Google Ads accounts;
- create campaigns, ad groups, ads, or keywords;
- modify existing campaigns;
- change bids or budgets;
- change billing or payment settings;
- manage third-party accounts;
- perform conversion tracking or remarketing operations.

Any future campaign decisions based on the research remain manual human decisions.

## Pilot workflow

The planned workflow is:

1. Select a small set of keywords already measured manually in Google Keyword Planner.
2. Use the same relevant market, language, network, and date-range parameters where supported.
3. Request historical metrics through `KeywordPlanIdeaService.GenerateKeywordHistoricalMetrics`.
4. Store the returned metrics for analysis.
5. Compare API output with the corresponding manual Keyword Planner export.
6. Record differences and determine whether the API data is suitable for the intended Google Ads planning workflow.
7. Keep manual review as the decision step.

No automatic campaign changes occur in this workflow.

## Why Basic Access is requested

The current developer token has Test Account Access.

Basic Access is requested so the controlled keyword-planning pilot can use the required Google Ads API planning functionality with the appropriate production Google Ads account.

The requested capability is limited to keyword planning for my own advertising workflow.

## Current development status

The tool is currently under development.

The controlled API pilot has not yet been executed.

Google Cloud and API access are being prepared specifically for this validation stage. No claim is made that Google Ads API data already matches or replaces the manual Keyword Planner workflow.

## Data and security

Developer tokens, OAuth credentials, refresh tokens, client secrets, passwords, and other private credentials are never published in this repository.

This repository exists only to provide public project and use-case information for Google Ads API review.

## Official Google Ads API functionality used

The planned API functionality is documented by Google here:

- Google Ads API — Generate Historical Metrics  
  https://developers.google.com/google-ads/api/docs/keyword-planning/generate-historical-metrics

- Google Ads API — Access Levels and Permissible Use  
  https://developers.google.com/google-ads/api/docs/api-policy/access-levels

## Contact

This project is operated by an individual developer and advertiser.

The active contact email for the Google Ads API application is provided directly to Google through the API Center and Basic Access application.
