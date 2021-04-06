# Get Info about a lecture

Get the details of an eth lecture.

**URL** : `/api/lecture/:vvz_number/:vvz_type/semester`

**URL Parameters** : 
 - `vvz_number=[string]` is the code of the lecture in vvz.
 - `vvz_type=[string]` is the type of the lecture in vvz.
 - `semester=[string]` is the semester identifier used at the ETH.

**Method** : `GET`

**Auth required** : TODO

**Permissions required** : TODO

## Success Response

**Code** : `200 OK`

**Content examples**


```json
{
  "id": 1234,
  "title": "The best lecture ever",
  "language": "de",
  "lecturers": [
    "switchEduId",
    "switchEduId"
  ],
  "description": "A very nice lecturer",
  "hasGroups": true
}
```

## Error Responses

**Condition** : If Lecture does not exist with provided parameters

**Code** : `404 NOT FOUND`

**Content** : `{}`

### OR

**Condition** : If provided data is invalid, e.g. vvz_number is missing.

**Code** : `400 BAD REQUEST`

**Content example** :

```json
{
    "vvz_number": [
        "Please provide the vvz_number"
    ]
}
```

## Note

The content is not complete we need to think about more information that should be provided.

