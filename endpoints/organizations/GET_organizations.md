# Organization Resources

    GET organizations

## Description
Returns a listing of twenty (up to one hundred) organizations.

***

## Requires authentication
* A valid Access Key must be provided in header **access_key** parameter.

***

## Parameters
- **sort** — Sort organizations in the specified order.
    ###### Recognized values:
    - 'created_at' — Sort by time of created
    - 'times_viewed' — Sort by view count

- **sort_direction** — Control the order of the sorting.  You can provide a **sort_direction** without providing a **sort**, in which case the default sort for the requested feature will be adjusted.
    ###### Recognized values:
    - 'asc' — Sort in ascending order (lowest or least-recent first)
    - 'desc' — Sort in descending order (highest or most-recent first).  This is the default.

- **page** — Return a specific page in the organization stream. Page numbering is 1-based.
- **rpp** — The number of results to return. Can not be over 50, default 10.

***

## Return format
A **JSON encoded** array with the following keys and values:

- **data** — An array of **Organization** objects in **[short format]**.

The response also has the following **meta** data:

- **current_page** — Number of the page that is returned.
- **total_pages** — Total number of pages in this feature's stream.
- **total_items** — Total number of items in this feature's stream.

***

## Errors
None

***

## Example
**Request**

    https://api.cyjobapi.com/v1/organizations

**Return**
``` json
{
   "data":[
      {
         "id":2,
         "name":"Elevplads.dk",
         "created_at":"2015-05-05 09:08:17",
         "updated_at":null,
         "deleted_at":null
      },
      {
         "id":1,
         "name":"Fritidsjob.dk",
         "created_at":"2015-05-04 10:06:08",
         "updated_at":null,
         "deleted_at":null
      }
   ],
   "meta":{
      "current_page":1,
      "total_pages":1,
      "total_items":2
   },
   "success":true
}
```
