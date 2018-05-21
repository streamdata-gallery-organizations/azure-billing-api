{
  "info": {
    "name": "Azure Billing API Usage Details List",
    "_postman_id": "f09990c3-b38d-4b77-8ce5-f421c8998b17",
    "description": "Lists the usage details for a scope in reverse chronological order by billing period. Usage details are available via this API only for January 1, 2017 or later.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Billing Period",
      "item": [
        {
          "id": "0f92a08d-c8b1-42f7-8685-4f850b3e9f33",
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
              "id": "93a4f288-678b-4ee6-9652-75aaba823aa2"
            }
          ]
        },
        {
          "id": "429a705f-1c05-4861-893c-c998a10f6713",
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
              "id": "0540c339-eb12-49d9-8852-8b66390ee1b3"
            }
          ]
        }
      ]
    },
    {
      "name": "Invoice",
      "item": [
        {
          "id": "8f9c054e-2c4f-4c00-886e-fb170a3e3ff0",
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
              "id": "22b6e469-e159-4fab-a0ae-494d1aace2a0"
            }
          ]
        },
        {
          "id": "d5df6fc4-c7a9-4967-bf29-069b7b2b9131",
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
              "id": "f65dc2f6-cf56-4020-8af3-ead31973d43f"
            }
          ]
        },
        {
          "id": "6965161a-afbc-46f9-abcc-5b3e10c9cd47",
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
              "id": "be45bb90-e020-4680-bca7-5c68620debe3"
            }
          ]
        }
      ]
    },
    {
      "name": "Operation",
      "item": [
        {
          "id": "44c9c62c-1d38-44c6-8332-b342baf07b58",
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
              "id": "8a9b539f-f176-4f7b-ab2d-8d8ef731a6c0"
            }
          ]
        }
      ]
    },
    {
      "name": "Usage",
      "item": [
        {
          "id": "c46acd5c-cf0f-4e30-9b5b-6eccea2727df",
          "name": "UsageDetails_List",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                ":scope/providers/Microsoft.Consumption/usageDetails"
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
                  "id": "scope",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists the usage details for a scope in reverse chronological order by billing period. Usage details are available via this API only for January 1, 2017 or later."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "30e6b561-1979-4990-b6ad-e7aea6ba63ce"
            }
          ]
        }
      ]
    }
  ]
}