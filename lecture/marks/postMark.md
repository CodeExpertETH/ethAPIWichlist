# Sends a mark to edoz

Sets a mark for the student. This would simplify the process for tools like code expert to send the correct marks to the correct student.

**URL** : `/api/lecture/marks/:vvz_number/:vvz_type/:semester/:studentNethz`

**URL Parameters** :
- `vvz_number=[string]` is the code of the lecture in vvz.
- `vvz_type=[string]` is the type of the lecture in vvz.
- `semester=[string]` is the semester identifier used at the ETH.
- `studentNethz=[string]` is the nethz identifier of the user

**Method** : `POST`

**Auth required** : TODO

**Permissions required** : TODO

**Data constraints**

```json
{
    "mark": "[number]"
}
```

**Data example** 

```json
{
    "mark": "4.5"
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

**Condition** : Student or lecture does not exist at URL

**Code** : `404 NOT FOUND`

**Content** : `{}`

### Or

**Condition** :  Failed to do the update

**Code** : `409 Conflict`

**Content** : `{
  "error": "The the mark has alreay been looked."
}`

