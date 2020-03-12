FORMAT: 1A
HOST: https://private-bd1af-listprofile.apiary-mock.com

# List Profile

API documentation for showing list a profile

## Categories Collection [/profiles]
### List Profiles [GET]
Showing all Profiles


+ Response 200 (application/json)

        {
            "data":[
                {
                    "id": 1,
                    "name": "Muhammad Zulfadli",
                    "username": "zulfadli",
                    "created_at": "7843731823",
                    "updated_at": "7843731823"
                },
                {
                    "id": 2,
                    "name": "Sandra Julia",
                    "username": "sandraaa",
                    "created_at": "7843731823",
                    "updated_at": "7843731823"
                }
            ],
            "meta": {
                "total": 100,
                "page": 1,
                "limit":20
                
            }
        }

### Create Profile [POST]
create a profile
+ Request (application/json)

        {
            "name": "Julia",
            "username": "Juliaaa"
        }

+ Response 201 (application/json)

    + Headers

            Location: /profiles/15

    + Body

            {
                "name": "Julia",
                "username": "Juliaaa",
                "created_at": "7843731823",
                "updated_at": "7843731823"
            }

### Update Profiles [PUT /{id}]
update a detail of profile

+ Parameters
    + id (number) - ID of profile must integer

+ Request (application/json)

        {
            "name": "Muhammad Zulfadli",
            "username": "zulfadli"
        }

+ Response 204 (application/json)


### Detail Profiles [GET /{id}]
Detail all profiles
+ Parameters
    + id: 1 (number) - ID of profile must integer

+ Response 200 (application/json)

        {
            "name": "Muhammad Zulfadli",
            "username": "zulfadli",
            "created_at": "7843731823",
            "updated_at": "7843731823"
        }
        
      

### Delete Profiles [DELETE /{id}]
Delete Profiles
+ Parameters
    + id (number) - ID of Profiles must integer

+ Response 204 (application/json)
