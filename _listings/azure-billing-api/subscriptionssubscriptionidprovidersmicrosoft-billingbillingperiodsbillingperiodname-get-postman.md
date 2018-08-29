{
  "info": {
    "name": "Azure Billing API Billing Periods Get",
    "_postman_id": "ea6ac605-4864-45d0-b068-9269064bf76b",
    "description": "Gets a named billing period.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "billing period",
      "item": [
        {
          "id": "d2f33015-9b45-4e78-8f49-dab119008e6f",
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
            "description": "Gets a named billing period"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ddfbd77b-babb-41aa-b94b-056f62dc313e"
            }
          ]
        }
      ]
    }
  ]
}