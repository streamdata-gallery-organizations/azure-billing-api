---
swagger: "2.0"
info:
  title: ConsumptionManagementClient
  description: Consumption management client provides access to consumption resources
    for Azure Web-Direct subscriptions. Other subscription types which were not purchased
    directly through the Azure web portal are not supported through this preview API.
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
  /providers/Microsoft.Billing/operations:
    get:
      summary: Operations List
      description: Lists all of the available billing REST API operations
      operationId: Operations_List
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - operation
definitions:
  BillingPeriod:
    properties: []
  BillingPeriodsListResult:
    properties:
      value:
        description: This is a default description.
        type: get
      nextLink:
        description: This is a default description.
        type: get
  BillingPeriodProperties:
    properties:
      billingPeriodStartDate:
        description: This is a default description.
        type: get
      billingPeriodEndDate:
        description: This is a default description.
        type: get
      invoiceIds:
        description: This is a default description.
        type: get
  DownloadUrl:
    properties:
      expiryTime:
        description: This is a default description.
        type: get
      url:
        description: This is a default description.
        type: get
  ErrorDetails:
    properties:
      code:
        description: This is a default description.
        type: get
      message:
        description: This is a default description.
        type: get
      target:
        description: This is a default description.
        type: get
  ErrorResponse:
    properties: []
  Invoice:
    properties: []
  InvoicesListResult:
    properties:
      value:
        description: This is a default description.
        type: get
      nextLink:
        description: This is a default description.
        type: get
  InvoiceProperties:
    properties:
      invoicePeriodStartDate:
        description: This is a default description.
        type: get
      invoicePeriodEndDate:
        description: This is a default description.
        type: get
      billingPeriodIds:
        description: This is a default description.
        type: get
  Operation:
    properties:
      name:
        description: This is a default description.
        type: get
  OperationListResult:
    properties:
      value:
        description: This is a default description.
        type: get
      nextLink:
        description: This is a default description.
        type: get
  Resource:
    properties:
      id:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      type:
        description: This is a default description.
        type: get
      tags:
        description: This is a default description.
        type: get
  MeterDetails:
    properties:
      meterName:
        description: This is a default description.
        type: get
      meterCategory:
        description: This is a default description.
        type: get
      meterSubCategory:
        description: This is a default description.
        type: get
      unit:
        description: This is a default description.
        type: get
      meterLocation:
        description: This is a default description.
        type: get
      totalIncludedQuantity:
        description: This is a default description.
        type: get
      pretaxStandardRate:
        description: This is a default description.
        type: get
  UsageDetail:
    properties: []
  UsageDetailsListResult:
    properties:
      value:
        description: This is a default description.
        type: get
      nextLink:
        description: This is a default description.
        type: get
  UsageDetailProperties:
    properties:
      billingPeriodId:
        description: This is a default description.
        type: get
      invoiceId:
        description: This is a default description.
        type: get
      usageStart:
        description: This is a default description.
        type: get
      usageEnd:
        description: This is a default description.
        type: get
      instanceName:
        description: This is a default description.
        type: get
      instanceId:
        description: This is a default description.
        type: get
      instanceLocation:
        description: This is a default description.
        type: get
      currency:
        description: This is a default description.
        type: get
      usageQuantity:
        description: This is a default description.
        type: get
      billableQuantity:
        description: This is a default description.
        type: get
x-collection-name: Azure Billing API
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