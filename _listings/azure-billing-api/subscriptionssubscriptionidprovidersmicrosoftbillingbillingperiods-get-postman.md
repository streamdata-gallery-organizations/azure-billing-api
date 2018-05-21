{
  "info": {
    "name": "Azure Billing API Billing Periods List",
    "_postman_id": "1d85ba7d-92ba-4580-8e5b-206e9a85e856",
    "description": "Lists the available billing periods for a subscription in reverse chronological order.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "billing period",
      "item": [
        {
          "id": "523d72d3-72a9-4f61-82ce-0c386c260d8b",
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
            "description": "Lists the available billing periods for a subscription in reverse chronological order"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ac9f5316-9e23-42e6-9c71-3ebe883d7526"
            }
          ]
        }
      ]
    }
  ]
}