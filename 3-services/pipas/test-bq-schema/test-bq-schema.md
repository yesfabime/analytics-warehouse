---
title: Analytics Warehouse - Pipas Stream Test BQ Schema
layout: template
filename: test-bq-schema.md
permalink: /services/pipas/stream/test-bq-schema/
--- 
# Test your BQ schema
After creating the schema table of your business object in BigQuery, you have to test the schema with an example json file. If you're not doing this, you will not able to deploy a Pipas. To ease the testing process, we created for you an API. This API takes the json from "json_to_check" and tries to stream it into the example table 

```
v135-5213-pipass-test-two:schema_for_beverages_sales.schema_table
```

- URL: [https://pipas-generator-service-d4dx3jifoa-ew.a.run.app/v1/apis/customerCheck](https://pipas-generator-service-d4dx3jifoa-ew.a.run.app/v1/apis/customerCheck){:target="_blank"}

- POST

- **Important**: The business object name needs to be lowercase and underscores (e.g. example_business_object_name) and the EXACT same name you want to be displayed within the Data Catalog

- Example (correct data schema and datatypes):
    - Request body:

        ```json
        {
            "bo_name": "beverages_sales",
            "project_id": "v135-5213-pipass-test-two",
            "dataset_id": "schema_for_beverages_sales",
            "table_id": "data",
            "json_to_check": {
                "kind": "beer",
                "country_iso": "DE",
                "amount": 100,
                "properties": {
                    "manufacturer": "Augustiner Bräu München",
                    "volume_l": 0.5
                },
                "customer": "Matthias Riepl",
                "brand": "MMS",
                "timestamp_of_sale": "2020-01-22 15:08:27.026540+00:00"
            }
        }
        ```

    - Response body (for the example above):

        ```
        "Successfully imported JSON to BigQuery - you are ready to go!", 200
        ```

{:refdef: style="text-align: center;"}
![Create Dataset - 1]({{site.baseurl}}/3-services/pipas/test-bq-schema/success-import.png)
{: refdef}

As you can see the data which was provided at "json_to_check" was inserted to BigQuery.<br/>
Below you can find an example of a failed check:

- Example (wrong data schema)
    - Request body:

        ```json
        {
            "bo_name": "beverages_sales",
            "project_id": "v135-5213-pipass-test-two",
            "dataset_id": "schema_for_beverages_sales",
            "table_id": "data",
            "json_to_check": {
                "kind": "beer",
                "country_iso": "DE",
                "amount": "HUNDERT"
            }
        }
        ```

    - Response body (for example above):

        ```
        "Failed to insert JSON to BigQuery: [{'index': 0, 'errors': [{'reason': 
        'invalid', 'location': 'amount', 'debugInfo': '', 'message': 'Cannot 
        convert value to integer (bad value):HUNDERT'}]}]", 400
        ```

<br/>
You can use the test route as often  you want to, the data is simply streamed  into your schema table, which is not used later on. 
<br/>
**IMPORTANT: The LATEST test needs to be successful otherwise the Pipas won't get deployed**