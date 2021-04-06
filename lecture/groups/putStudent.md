# Signs up a student to the groups.

Updates the group and adds the student to the group if possible.

**URL** : `/api/lecture/groups/students/:groupId`

**URL Parameters** :
- `groupId=[string]` the groupId

**Method** : `PUT`

**Auth required** : TODO

**Permissions required** : TODO

**Data constraints**

```json
{
    "switchEduId": "[string]"
}
```

**Data example** 

```json
{
    "switchEduId": "12345"
}
```

## Success Responses

**Condition** : Update can be performed only fully.

**Code** : `200 OK`

**Content example** : 

```json
{ }
```

## Error Response

**Condition** : Group does not exist at URL

**Code** : `404 NOT FOUND`

**Content** : `{}`

### Or

**Condition** :  Failed to do the update

**Code** : `409 Conflict`

**Content** : `{
  "error": "The group has no free places left."
}`

