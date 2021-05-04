# ETH API wishlist

This Repo should document some use cases and possible endpoints for a new eth api.


## Authentication

Is completely ignored during this phase of the design.

### User related

Information about ETH users

* [Get user info](user/get.md) : `GET /api/user/`

### Lecture related

Information about ETH lectures

* [Get lecture info](lecture/get.md) : `GET /api/lecture/`
  
#### Groups
* [Get lecture group info](lecture/groups/get.md) : `GET /api/lecture/groups`
* [Get group tas](lecture/groups/getTAs.md) : `GET /api/lecture/groups/tas`
* [Get group students](lecture/groups/getStudents.md) : `GET /api/lecture/groups/students`
* [Add a student to a group](lecture/groups/putStudent.md) : `PUT /api/lecture/groups/students`
* [Add a TA to a group](lecture/groups/putTA.md) : `PUT /api/lecture/groups/tas`
* [Delete a student from a group](lecture/groups/deleteStudent.md) : `DELETE /api/lecture/groups/students`
* [Delete a TA from a group](lecture/groups/deleteTA.md) : `DELETE /api/lecture/groups/tas`

#### Marks
* [Add a mark for a student](lecture/marks/postMark.md) : `POST /api/lecture/marks`
