# Delete TA from a group

Delete the TA from a group

**URL** : `/api/lecture/groups/:groupId`

**URL Parameters** :
- `groupId=[string]` the groupId

**Method** : `DELETE`

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

## Success Response

**Condition** : If the TA exists in the group.

**Code** : `204 NO CONTENT`

**Content** : `{}`

## Error Responses

**Condition** : If there was no TA to delete.

**Code** : `404 NOT FOUND`

**Content** : `{}`
