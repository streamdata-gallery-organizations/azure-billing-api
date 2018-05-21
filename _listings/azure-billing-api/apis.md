---
name: Azure Billing API
x-slug: azure-billing-api
description: Use Azure Billing APIs to pull usage and resource data into your preferred
  data analysis tools. The Azure Resource Usage and RateCard APIs can help you accurately
  predict and manage your costs. The APIs are implemented as a Resource Provider and
  part of the family of APIs exposed by the Azure Resource Manager.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-billing-api.png
x-kinRank: "10"
x-alexaRank: ""
tags: Azure Billing API
created: "2018-05-21"
modified: "2018-05-21"
url: https://raw.githubusercontent.com/streamdata-gallery-organizations/azure-billing-api/master/_listings/azure-billing-api/apis.md
specificationVersion: "0.14"
apis:
- name: Azure Billing API Billing Periods List
  x-api-slug: azure-billing-api
  description: Lists the available billing periods for a subscription in reverse chronological
    order.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-billing-api.png
  humanURL: https://docs.microsoft.com/en-us/azure/billing/billing-usage-rate-card-overview
  baseURL: ://management.azure.com////subscriptions/{subscriptionId}/providers/Microsoft.Billing/billingPeriods
  tags: Billing Period
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/azure-billing-api/master/_listings/azure-billing-api/subscriptionssubscriptionidprovidersmicrosoftbillingbillingperiods-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/azure-billing-api/master/_listings/azure-billing-api/subscriptionssubscriptionidprovidersmicrosoftbillingbillingperiods-get-openapi.md
- name: Azure Billing API Billing Periods Get
  x-api-slug: azure-billing-api
  description: Gets a named billing period.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-billing-api.png
  humanURL: https://docs.microsoft.com/en-us/azure/billing/billing-usage-rate-card-overview
  baseURL: ://management.azure.com////subscriptions/{subscriptionId}/providers/Microsoft.Billing/billingPeriods/{billingPeriodName}
  tags: Billing Period
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/azure-billing-api/master/_listings/azure-billing-api/subscriptionssubscriptionidprovidersmicrosoftbillingbillingperiodsbillingperiodname-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/azure-billing-api/master/_listings/azure-billing-api/subscriptionssubscriptionidprovidersmicrosoftbillingbillingperiodsbillingperiodname-get-openapi.md
- name: Azure Billing API Invoices List
  x-api-slug: azure-billing-api
  description: Lists the available invoices for a subscription in reverse chronological
    order beginning with the most recent invoice. In preview, invoices are available
    via this API only for invoice periods which end December 1, 2016 or later.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-billing-api.png
  humanURL: https://docs.microsoft.com/en-us/azure/billing/billing-usage-rate-card-overview
  baseURL: ://management.azure.com////subscriptions/{subscriptionId}/providers/Microsoft.Billing/invoices
  tags: Invoice
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/azure-billing-api/master/_listings/azure-billing-api/subscriptionssubscriptionidprovidersmicrosoftbillinginvoices-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/azure-billing-api/master/_listings/azure-billing-api/subscriptionssubscriptionidprovidersmicrosoftbillinginvoices-get-openapi.md
- name: Azure Billing API Invoices Get
  x-api-slug: azure-billing-api
  description: Gets a named invoice resource. When getting a single invoice, the downloadUrl
    property is expanded automatically.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-billing-api.png
  humanURL: https://docs.microsoft.com/en-us/azure/billing/billing-usage-rate-card-overview
  baseURL: ://management.azure.com////subscriptions/{subscriptionId}/providers/Microsoft.Billing/invoices/{invoiceName}
  tags: Invoice
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/azure-billing-api/master/_listings/azure-billing-api/subscriptionssubscriptionidprovidersmicrosoftbillinginvoicesinvoicename-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/azure-billing-api/master/_listings/azure-billing-api/subscriptionssubscriptionidprovidersmicrosoftbillinginvoicesinvoicename-get-openapi.md
- name: Azure Billing API Invoices Get Latest
  x-api-slug: azure-billing-api
  description: Gets the most recent invoice. When getting a single invoice, the downloadUrl
    property is expanded automatically.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-billing-api.png
  humanURL: https://docs.microsoft.com/en-us/azure/billing/billing-usage-rate-card-overview
  baseURL: ://management.azure.com////subscriptions/{subscriptionId}/providers/Microsoft.Billing/invoices/latest
  tags: Invoice
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/azure-billing-api/master/_listings/azure-billing-api/subscriptionssubscriptionidprovidersmicrosoftbillinginvoiceslatest-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/azure-billing-api/master/_listings/azure-billing-api/subscriptionssubscriptionidprovidersmicrosoftbillinginvoiceslatest-get-openapi.md
- name: Azure Billing API Operations List
  x-api-slug: azure-billing-api
  description: Lists all of the available billing REST API operations.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-billing-api.png
  humanURL: https://docs.microsoft.com/en-us/azure/billing/billing-usage-rate-card-overview
  baseURL: ://management.azure.com////providers/Microsoft.Billing/operations
  tags: Operation
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/azure-billing-api/master/_listings/azure-billing-api/providersmicrosoftbillingoperations-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/azure-billing-api/master/_listings/azure-billing-api/providersmicrosoftbillingoperations-get-openapi.md
- name: Azure Billing API Usage Details List
  x-api-slug: azure-billing-api
  description: Lists the usage details for a scope in reverse chronological order
    by billing period. Usage details are available via this API only for January 1,
    2017 or later.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-billing-api.png
  humanURL: https://docs.microsoft.com/en-us/azure/billing/billing-usage-rate-card-overview
  baseURL: ://management.azure.com////{scope}/providers/Microsoft.Consumption/usageDetails
  tags: Usage
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/azure-billing-api/master/_listings/azure-billing-api/scopeprovidersmicrosoftconsumptionusagedetails-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/azure-billing-api/master/_listings/azure-billing-api/scopeprovidersmicrosoftconsumptionusagedetails-get-openapi.md
- name: Azure Billing API Operations List
  x-api-slug: azure-billing-api
  description: Lists all of the available consumption REST API operations.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-billing-api.png
  humanURL: https://docs.microsoft.com/en-us/azure/billing/billing-usage-rate-card-overview
  baseURL: ://management.azure.com////providers/Microsoft.Consumption/operations
  tags: Operation
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/azure-billing-api/master/_listings/azure-billing-api/providersmicrosoftconsumptionoperations-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/azure-billing-api/master/_listings/azure-billing-api/providersmicrosoftconsumptionoperations-get-openapi.md
- name: Azure Billing API
  x-api-slug: azure-billing-api
  description: Use Azure Billing APIs to pull usage and resource data into your preferred
    data analysis tools. The Azure Resource Usage and RateCard APIs can help you accurately
    predict and manage your costs. The APIs are implemented as a Resource Provider
    and part of the family of APIs exposed by the Azure Resource Manager.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-billing-api.png
  humanURL: https://docs.microsoft.com/en-us/azure/billing/billing-usage-rate-card-overview
  baseURL: ://management.azure.com//
  tags: Azure Billing API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/azure-billing-api/master/_listings/azure-billing-api/openapi.md
x-common:
- type: x-website
  url: https://docs.microsoft.com/en-us/azure/billing/billing-usage-rate-card-overview
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---