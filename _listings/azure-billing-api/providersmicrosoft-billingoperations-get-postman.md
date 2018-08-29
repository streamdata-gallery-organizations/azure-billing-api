{
  "info": {
    "name": "Azure Billing API Operations List",
    "_postman_id": "016b73d1-67fa-468f-bda5-168da0c6058e",
    "description": "Lists all of the available billing REST API operations.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Billing Period",
      "item": [
        {
          "id": "d39014b9-09d2-4ed2-910d-400645ff3516",
          "name": "BillingPeriods_List",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/providers/Microsoft.Billing/billingPeriods"
              ],
              "query": [
                {
                  "key": "$filter",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "$skiptoken",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "$top",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "No Name",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "subscriptionId",
                  "value": "subscriptionId",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists the available billing periods for a subscription in reverse chronological order."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "094d09de-ff4f-49e2-8f79-579b4de4b0e7"
            }
          ]
        },
        {
          "id": "33ad0b13-be2a-4c30-be0e-a11e9a41e736",
          "name": "BillingPeriods_Get",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/providers/Microsoft.Billing/billingPeriods/:billingPeriodName"
              ],
              "query": [
                {
                  "key": "No Name",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "billingPeriodName",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "subscriptionId",
                  "value": "subscriptionId",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets a named billing period."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "50bbd60a-11f4-42cc-be4c-28cb025471b1"
            }
          ]
        }
      ]
    },
    {
      "name": "Invoice",
      "item": [
        {
          "id": "658774a1-aae8-4f83-aec8-474b0a8b01dd",
          "name": "Invoices_List",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/providers/Microsoft.Billing/invoices"
              ],
              "query": [
                {
                  "key": "$expand",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "$filter",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "$skiptoken",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "$top",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "No Name",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "subscriptionId",
                  "value": "subscriptionId",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists the available invoices for a subscription in reverse chronological order beginning with the most recent invoice. In preview, invoices are available via this API only for invoice periods which end December 1, 2016 or later."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "bd56486a-8798-4e6f-8f20-cf1b2dfe9a3d"
            }
          ]
        },
        {
          "id": "e1eb4664-f94a-4f9b-9729-ad9f2662c0c1",
          "name": "Invoices_Get",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/providers/Microsoft.Billing/invoices/:invoiceName"
              ],
              "query": [
                {
                  "key": "No Name",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "invoiceName",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "subscriptionId",
                  "value": "subscriptionId",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets a named invoice resource. When getting a single invoice, the downloadUrl property is expanded automatically."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "960d93b3-950a-40d3-886c-c06dfce9ff04"
            }
          ]
        },
        {
          "id": "d00f033f-c2d1-4cb9-baa2-fcef8acbc703",
          "name": "Invoices_GetLatest",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/providers/Microsoft.Billing/invoices/latest"
              ],
              "query": [
                {
                  "key": "No Name",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "subscriptionId",
                  "value": "subscriptionId",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets the most recent invoice. When getting a single invoice, the downloadUrl property is expanded automatically."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "35f0c4ea-6199-40c6-92c0-8f5595ddc4d1"
            }
          ]
        }
      ]
    },
    {
      "name": "Operation",
      "item": [
        {
          "id": "81637bbe-2fa2-43c2-96d0-d992fbcdc168",
          "name": "Operations_List",
          "request": {
            "url": "http://management.azure.com/providers/Microsoft.Billing/operations?No Name=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists all of the available billing REST API operations."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "85b5d473-444c-4eaf-ac56-2d15649ffc53"
            }
          ]
        }
      ]
    }
  ]
}