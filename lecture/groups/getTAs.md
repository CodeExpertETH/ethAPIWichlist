# Get the TAs of a group

This returns the registered TAs of a group.

**URL** : `/api/lecture/groups/tas/:groupId`

**URL Parameters** : 
 - `groupId=[string]` the groupId

**Method** : `GET`

**Auth required** : TODO

**Permissions required** : TODO

## Success Response

**Code** : `200 OK`

**Content examples**

```json
{
  "students": [
    "switchEduId1",
    "switchEduId2",
    "switchEduId3"
  ]
}
```

## Error Responses

**Condition** : If group does not exist with provided parameters

**Code** : `404 NOT FOUND`

**Content** : `{}`

### OR

**Condition** : If provided data is invalid, e.g. groupId is missing.

**Code** : `400 BAD REQUEST`

**Content example** :

```json
{
    "groupId": [
        "Please provide the groupId"
    ]
}
```
