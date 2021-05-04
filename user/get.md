# Show Current User

Get the details of an eth user.

**URL** : `/api/user/:switchEduId` or  `/api/user/:nethz`

**URL Parameters** : 

- `switchEduId=[string]` where `switchEduId` is the Switch Edu Id of the user.
- `nethz=[string]` where `nethz` is the nethz username of the user.

**Method** : `GET`

**Auth required** : TODO

**Permissions required** : TODO

## Success Response

**Code** : `200 OK`

**Content examples**

For a User with ID 1234 on the local database where that User has saved an
email address and name information.

```json
{
    "switchEduId": "xxxxxx",
    "first_name": "Joe",
    "last_name": "Bloggs",
    "title": "Dr.",
    "gender": "m",
    "nethz": "jbloggs",
    "legi": "07-957-658",
    "email": "joe25@example.com",
}
```

## Error Responses

**Condition** : If Account does not exist with `switchEduId`.

**Code** : `404 NOT FOUND`

**Content** : `{}`

### OR

**Condition** : If provided data is invalid, e.g. switchEduId is missing.

**Code** : `400 BAD REQUEST`

**Content example** :

```json
{
    "switchEduId": [
        "Please provide the switchEduId"
    ]
}
```


