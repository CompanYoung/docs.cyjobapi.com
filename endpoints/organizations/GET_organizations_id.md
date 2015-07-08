# Organization Resources

    GET organizations/:id

## Description
Returns detailed information of a single organization.

***

## Requires authentication
* A valid Access Key must be provided in header **access_key** parameter.

***

## Parameters
No parameters.

***

## Return format
A **JSON encoded** array with the following keys and values:

- **data** — A single **Organization** object in **[big format]**.

The response has no **meta** data.

***

## Errors
All known errors cause the resource to return HTTP error code header together with a JSON array containing at least 'status' and 'error' keys describing the source of error.

- **403 Forbidden** — The organization was either deleted, belongs to a deactivated user.
- **404 Not Found** — Organization with the specified ID does not exist.

***

## Example
**Request**

    https://api.cyjobapi.com/v1/organizations/1

**Return**
``` json
{
   "data":{
      "id":1,
      "name":"Fritidsjob.dk",
      "subdomain":"fritidsjob-dk",
      "created_at":"2015-05-04 10:06:08",
      "updated_at":"2015-05-26 10:42:11",
      "types":[
         {
            "id":1,
            "name":"Apprenticeship",
            "created_at":"2015-04-28 14:22:02",
            "updated_at":"2015-05-26 14:00:08",
            "categories":[
               {
                  "id":1,
                  "type_id":1,
                  "name":"Handel",
                  "created_at":"-0001-11-30 00:00:00",
                  "updated_at":"2015-05-26 13:59:51",
                  "positions":[
                     {
                        "id":1,
                        "category_id":1,
                        "name":"Position 1",
                        "created_at":"2015-05-20 15:11:17",
                        "updated_at":"2015-05-26 13:59:28",
                     },
                     {
                        "id":2,
                        "category_id":1,
                        "name":"Position 2",
                        "created_at":"2015-05-20 15:11:28",
                        "updated_at":"2015-06-01 09:01:31",
                     },
                     {
                        "id":20,
                        "category_id":1,
                        "name":"Navn!!",
                        "created_at":"-0001-11-30 00:00:00",
                        "updated_at":null,
                     },
                     {
                        "id":22,
                        "category_id":1,
                        "name":"Navn!",
                        "created_at":"-0001-11-30 00:00:00",
                        "updated_at":null,
                     }
                  ]
               }
            ]
         },
         {
            "id":2,
            "name":"Part-time job",
            "created_at":"2015-04-28 14:23:43",
            "updated_at":null,
            "categories":[
               {
                  "id":2,
                  "type_id":2,
                  "name":"Kontor",
                  "created_at":"-0001-11-30 00:00:00",
                  "updated_at":"2015-05-26 13:59:51",
                  "positions":[
                     {
                        "id":3,
                        "category_id":2,
                        "name":"Position 3",
                        "created_at":"2015-05-20 15:11:39",
                        "updated_at":"2015-06-01 09:01:31",
                     },
                     {
                        "id":4,
                        "category_id":2,
                        "name":"Position 4",
                        "created_at":"2015-05-20 15:11:45",
                        "updated_at":"2015-06-01 09:01:31",
                     }
                  ]
               },
               {
                  "id":3,
                  "type_id":2,
                  "name":"Finans",
                  "created_at":"-0001-11-30 00:00:00",
                  "updated_at":null,
                  "positions":[
                     {
                        "id":5,
                        "category_id":3,
                        "name":"Position 5",
                        "created_at":"2015-05-20 15:12:01",
                        "updated_at":"2015-05-26 11:04:24",
                     },
                     {
                        "id":6,
                        "category_id":3,
                        "name":"Position 6",
                        "created_at":"2015-05-26 13:05:18",
                        "updated_at":null,
                     },
                     {
                        "id":7,
                        "category_id":3,
                        "name":"Position 7",
                        "created_at":"2015-05-26 13:05:20",
                        "updated_at":null,
                     }
                  ]
               }
            ]
         }
      ],
      "countries":[
         {
            "id":1,
            "name":"Danmark",
            "created_at":"2015-05-22 15:11:58",
            "updated_at":"2015-05-26 14:01:34",
            "regions":[
               {
                  "id":1,
                  "country_id":1,
                  "name":"Nordjylland",
                  "created_at":"2015-05-22 12:45:47",
                  "updated_at":"2015-05-26 14:01:06",
                  "geographies":[
                     {
                        "id":1,
                        "region_id":1,
                        "name":"Aalborg",
                        "created_at":"-0001-11-30 00:00:00",
                        "updated_at":"2015-05-26 14:00:44",
                     },
                     {
                        "id":2,
                        "region_id":1,
                        "name":"Nørresundby",
                        "created_at":"-0001-11-30 00:00:00",
                        "updated_at":"2015-05-26 14:00:44",
                     },
                     {
                        "id":3,
                        "region_id":1,
                        "name":"Skørping",
                        "created_at":"-0001-11-30 00:00:00",
                        "updated_at":"2015-05-26 14:00:44",
                     },
                     {
                        "id":4,
                        "region_id":1,
                        "name":"Test 1",
                        "created_at":"-0001-11-30 00:00:00",
                        "updated_at":"2015-05-26 14:00:44",
                     },
                     {
                        "id":5,
                        "region_id":1,
                        "name":"Test 2",
                        "created_at":"-0001-11-30 00:00:00",
                        "updated_at":"2015-05-26 14:00:44",
                     },
                     {
                        "id":6,
                        "region_id":1,
                        "name":"Test 3",
                        "created_at":"-0001-11-30 00:00:00",
                        "updated_at":null,
                     },
                     {
                        "id":7,
                        "region_id":1,
                        "name":"test",
                        "created_at":"-0001-11-30 00:00:00",
                        "updated_at":null,
                     }
                  ]
               },
               {
                  "id":2,
                  "country_id":1,
                  "name":"Midtjylland",
                  "created_at":"2015-05-22 12:45:51",
                  "updated_at":"2015-05-26 14:01:06",
                  "geographies":[

                  ]
               }
            ]
         },
         {
            "id":2,
            "name":"Tyskland",
            "created_at":"2015-05-22 15:12:10",
            "updated_at":"2015-05-26 14:01:34",
            "regions":[

            ]
         },
         {
            "id":5,
            "name":"test",
            "created_at":"-0001-11-30 00:00:00",
            "updated_at":null,
            "regions":[

            ]
         }
      ]
   },
   "meta":[

   ],
   "success":true
}
```
