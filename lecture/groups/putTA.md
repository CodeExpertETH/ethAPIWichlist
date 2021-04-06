# Signs up a TA to the group.

Updates the group and adds the ta to the group if possible.

**URL** : `/api/lecture/groups/tas/:groupId`

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