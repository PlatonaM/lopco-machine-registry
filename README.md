#### /machines

**GET**

_List machines._

    # Example

    curl http://<host>/machines
    {
        "34z4u5i75iu53i": "{\"name\": \"Demo Machine\", \"pipeline_id\": \"335ab4e5-2872-4a2d-8cfe-3bfb4854c31f\", \"platform_id\": \"device:aeb83bf0-c50c-48e9-91b6-4db07c65c99c\", \"platform_type_id\": \"device-type:c5940477-afe5-493c-9a9e-8043f8de7acd\"}",
        "098z0g976gf76ftfj": "{\"name\": \"Demo Machine 2\", \"pipeline_id\": \"677f99d4-2ec7-450c-add2-8b7c5f7f171c\", \"platform_id\": \"device:aeb83bf0-c50c-48e9-91b6-4db07c65c99c\", \"platform_type_id\": \"device-type:c5940477-afe5-493c-9a9e-8043f8de7acd\"}"
    }

----

#### /machines/{machine-id}

**GET**

_Retrieve machine data._

    # Example

    curl http://<host>/machines/34z4u5i75iu53i
    {
        "name": "Demo Machine",
        "pipeline_id": "335ab4e5-2872-4a2d-8cfe-3bfb4854c31f",
        "platform_id": "device:aeb83bf0-c50c-48e9-91b6-4db07c65c99c",
        "platform_type_id": "device-type:c5940477-afe5-493c-9a9e-8043f8de7acd"
    }


**PUT**

_Add / Update a machine._

    # Example

    cat machine_data.json
    {
        "name": "My Machine",
        "pipeline_id": "677f99d4-2ec7-450c-add2-8b7c5f7f171c",
        "platform_id": "device:aeb83bf0-c50c-48e9-91b6-4db07c65c99c",
        "platform_type_id": "device-type:c5940477-afe5-493c-9a9e-8043f8de7acd"
    }

    curl \
    -d @machine_data.json \
    -H 'Content-Type: application/json' \
    -X PUT http://<host>/machines/34z4u5i75iu53i
