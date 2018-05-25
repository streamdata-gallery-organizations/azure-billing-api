---
swagger: "2.0"
x-collection-name: Azure Billing API
x-complete: 0
info:
  title: Azure Billing API Usage Details List
  description: Lists the usage details for a scope in reverse chronological order
    by billing period. Usage details are available via this API only for January 1,
    2017 or later.
  version: 1.0.0
host: management.azure.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /subscriptions/{subscriptionId}/providers/Microsoft.Billing/billingPeriods:
    get:
      summary: Billing Periods List
      description: Lists the available billing periods for a subscription in reverse
        chronological order.
      operationId: BillingPeriods_List
      x-api-path-slug: subscriptionssubscriptionidprovidersmicrosoft-billingbillingperiods-get
      parameters:
      - in: query
        name: $filter
        description: May be used to filter billing periods by billingPeriodEndDate
      - in: query
        name: $skiptoken
        description: Skiptoken is only used if a previous operation returned a partial
          result
      - in: query
        name: $top
        description: May be used to limit the number of results to the most recent
          N billing periods
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Billing Period
  /subscriptions/{subscriptionId}/providers/Microsoft.Billing/billingPeriods/{billingPeriodName}:
    get:
      summary: Billing Periods Get
      description: Gets a named billing period.
      operationId: BillingPeriods_Get
      x-api-path-slug: subscriptionssubscriptionidprovidersmicrosoft-billingbillingperiodsbillingperiodname-get
      parameters:
      - in: path
        name: billingPeriodName
        description: The name of a BillingPeriod resource
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Billing Period
  /subscriptions/{subscriptionId}/providers/Microsoft.Billing/invoices:
    get:
      summary: Invoices List
      description: Lists the available invoices for a subscription in reverse chronological
        order beginning with the most recent invoice. In preview, invoices are available
        via this API only for invoice periods which end December 1, 2016 or later.
      operationId: Invoices_List
      x-api-path-slug: subscriptionssubscriptionidprovidersmicrosoft-billinginvoices-get
      parameters:
      - in: query
        name: $expand
        description: May be used to expand the downloadUrl property within a list
          of invoices
      - in: query
        name: $filter
        description: May be used to filter invoices by invoicePeriodEndDate
      - in: query
        name: $skiptoken
        description: Skiptoken is only used if a previous operation returned a partial
          result
      - in: query
        name: $top
        description: May be used to limit the number of results to the most recent
          N invoices
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Invoice
  /subscriptions/{subscriptionId}/providers/Microsoft.Billing/invoices/{invoiceName}:
    get:
      summary: Invoices Get
      description: Gets a named invoice resource. When getting a single invoice, the
        downloadUrl property is expanded automatically.
      operationId: Invoices_Get
      x-api-path-slug: subscriptionssubscriptionidprovidersmicrosoft-billinginvoicesinvoicename-get
      parameters:
      - in: path
        name: invoiceName
        description: The name of an invoice resource
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Invoice
  /subscriptions/{subscriptionId}/providers/Microsoft.Billing/invoices/latest:
    get:
      summary: Invoices Get Latest
      description: Gets the most recent invoice. When getting a single invoice, the
        downloadUrl property is expanded automatically.
      operationId: Invoices_GetLatest
      x-api-path-slug: subscriptionssubscriptionidprovidersmicrosoft-billinginvoiceslatest-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Invoice
  /providers/Microsoft.Billing/operations:
    get:
      summary: Operations List
      description: Lists all of the available billing REST API operations.
      operationId: Operations_List
      x-api-path-slug: providersmicrosoft-billingoperations-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Operation
  /{scope}/providers/Microsoft.Consumption/usageDetails:
    get:
      summary: Usage Details List
      description: Lists the usage details for a scope in reverse chronological order
        by billing period. Usage details are available via this API only for January
        1, 2017 or later.
      operationId: UsageDetails_List
      x-api-path-slug: scopeprovidersmicrosoft-consumptionusagedetails-get
      parameters:
      - in: query
        name: $expand
        description: May be used to expand the additionalProperties or meterDetails
          property within a list of usage details
      - in: query
        name: $filter
        description: May be used to filter usageDetails by usageEnd (Utc time)
      - in: query
        name: $skiptoken
        description: Skiptoken is only used if a previous operation returned a partial
          result
      - in: query
        name: $top
        description: May be used to limit the number of results to the most recent
          N usageDetails
      - in: query
        name: No Name
      - in: path
        name: scope
        description: The scope of the usage details
      responses:
        200:
          description: OK
      tags:
      - Usage
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---