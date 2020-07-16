#### /machines

**GET**

_List machine IDs._

    # Example

    curl http://host:8000/machine-registry/machines
    [
        "3f2c8eccc5064346b97b70785c95a729",
        "735d39eb6dc94acdadc9d019ff54fb1f"
    ]

----

#### /machines/{machine-id}

**GET**

_Retrieve machine data._

    # Example

    curl http://host:8000/machine-registry/machines/3f2c8eccc5064346b97b70785c95a729
    {
        "name": "Test Machine",
        "pipeline_id": "783c1c1f-7680-4420-8a0c-9e00752ee22b",
        "type_id": null
    }


**PUT**

_Add / Update a machine._

    # Example

    cat machine_data.json
    {
        "name": "Example Machine",
        "pipeline_id": "5bae2dd2-2786-4858-b51f-dad3f3774af8",
        "type_id": null
    }

    curl \
    -d @machine_data.json \
    -H 'Content-Type: application/json' \
    -X PUT http://host:8000/machine-registry/machines/m345f5h46u542ui
