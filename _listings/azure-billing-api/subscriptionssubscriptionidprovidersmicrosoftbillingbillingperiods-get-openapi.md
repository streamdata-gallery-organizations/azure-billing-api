---
swagger: "2.0"
x-collection-name: Azure Billing API
x-complete: 0
info:
  title: Azure Billing API Billing Periods List
  description: Lists the available billing periods for a subscription in reverse chronological
    order.
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
      x-api-path-slug: subscriptionssubscriptionidprovidersmicrosoftbillingbillingperiods-get
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