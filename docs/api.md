---
id: api
title: "Endpoints"
sidebar_label: Endpoints
---

## Courses List

Used to get a list of courses of a given type.

**URL** : `/api/courses/:type`

**Method** : `GET`

**Auth required** : Yes

**Data example**

```json
{
  "type": "all"
}
```

**Success Response**

**Code** : `200 OK`

**Content example**

```json
[
  {
    "_id": "5bd0000000000000000",
    "title": "course title",
    "slug": "B1pYCFH27-course-title",
    "bound": 300,
    "creator": {
      "_id": "5bd800987765544333223",
      "username": "H1NhiKr2m",
      "initials": "JD",
      "name": "John Doe"
    },
    "updated_at": "2018-10-31T09:09:56.710Z",
    "__v": 1,
    "join_code": "B16PblPn7",
    "count": {
      "resources": 0,
      "badges": 0,
      "time": 0,
      "learners": 0,
      "members": 1
    },
    "created_at": "2018-10-30T07:55:48.566Z",
    "tags": [],
    "faqs": [],
    "resources": [],
    "privacy": "private",
    "is_active": true,
    "org": {
      "name": "Xyz",
      "logo": "",
      "url": "www.xyz.co"
    },
    "image": {
      "m": "",
      "l": ""
    },
    "text": {
      "about": "This is an awesome course.",
      "tagline": "Awesome course"
    }
  }
]
```

**Error Response**

**Condition** : If type is invalid.

**Code** : `400 BAD REQUEST`

**Content** :

```json
{
  "err": ["Bad request error"]
}
```

## Course Page

Used to get a course using its id.

**URL** : `/api/course/:_id`

**Method** : `GET`

**Auth required** : Yes

**Data example**

```json
{
  "_id": "5bd87654334323443"
}
```

**Success Response**

**Code** : `200 OK`

**Content example**

```json
{
  "_id": "5bd87654334323443",
  "title": "course title",
  "slug": "B1pYCFH27-course-title",
  "bound": 300,
  "creator": {
    "_id": "5bd800987765544333223",
    "username": "H1NhiKr2m",
    "initials": "JD",
    "name": "John Doe"
  },
  "updated_at": "2018-10-31T09:09:56.710Z",
  "__v": 1,
  "join_code": "B16PblPn7",
  "count": {
    "resources": 0,
    "badges": 0,
    "time": 0,
    "learners": 0,
    "members": 1
  },
  "created_at": "2018-10-30T07:55:48.566Z",
  "tags": [],
  "faqs": [],
  "resources": [],
  "privacy": "private",
  "is_active": true,
  "org": {
    "name": "Xyz",
    "logo": "",
    "url": "www.xyz.co"
  },
  "image": {
    "m": "",
    "l": ""
  },
  "text": {
    "about": "This is an awesome course.",
    "tagline": "Awesome course"
  }
}
```

**Error Response**

**Condition** : If \_id is invalid.

**Code** : `404 Not Found`

**Content** :

```json
{
  "err": ["Not Found"]
}
```

## Course Actions

Used to update a course using its id and action.

**URL** : `/api/course/:_id/:action`

**Method** : `PUT`

**Auth required** : Yes

**Data example**

```json
{
  "_id": "5bd87654334323443",
  "action": "edit",
  "title": "course title changed"
}
```

**Success Response**

**Code** : `200 OK`

**Content example**

```json
{
  "_id": "5bd87654334323443",
  "title": "course title changed",
  "slug": "B1pYCFH27-course-title",
  "bound": 300,
  "creator": {
    "_id": "5bd800987765544333223",
    "username": "H1NhiKr2m",
    "initials": "JD",
    "name": "John Doe"
  },
  "updated_at": "2018-10-31T09:09:56.710Z",
  "__v": 1,
  "join_code": "B16PblPn7",
  "count": {
    "resources": 0,
    "badges": 0,
    "time": 0,
    "learners": 0,
    "members": 1
  },
  "created_at": "2018-10-30T07:55:48.566Z",
  "tags": [],
  "faqs": [],
  "resources": [],
  "privacy": "private",
  "is_active": true,
  "org": {
    "name": "Xyz",
    "logo": "",
    "url": "www.xyz.co"
  },
  "image": {
    "m": "",
    "l": ""
  },
  "text": {
    "about": "This is an awesome course.",
    "tagline": "Awesome course"
  }
}
```

**Error Response**

**Condition** : If \_id is invalid.

**Code** : `404 Not Found`

**Content** :

```json
{
  "err": ["Not Found"]
}
```

## Modules List

Used to get a list of modules for a course.

**URL** : `/api/modules/:_id`

**Method** : `GET`

**Auth required** : Yes

**Data example**

```json
{
  "_id": "5bd8752384523498325423"
}
```

**Success Response**

**Code** : `200 OK`

**Content example**

```json
[
  {
    "_id": "5c04bbda595445574b1a5fe4",
    "title": "Conflict as a Lens",
    "slug": "HJG13EfkN-the-what-understanding-contradictions",
    "module": "5c04ba76595445574b1a5fbb",
    "creator": {
      "_id": "5c04b84d595445574b1a5f4a",
      "username": "BJ8UOVzJV",
      "initials": "JD",
      "name": "John Doe"
    },
    "updated_at": "2018-12-03T05:41:52.519Z",
    "__v": 2,
    "count": { "badges": 0, "time": 0 },
    "created_at": "2018-12-03T05:15:06.142Z",
    "resources": [],
    "privacy": "open",
    "is_active": true,
    "lessons": [
      {
        "_id": "5c04bd7c595445574b1a5ffd",
        "title": "Navigating Contradictions",
        "slug": "HkBtaVz1E-navigating-contradictions",
        "nav": "horizontal",
        "is_active": true,
        "order": 1
      }
    ],
    "text": {
      "about": "In this module we will explore how conflicts are not necessarily evil, but can be windows of opportunity to create something beautiful, and Build Back Better.",
      "tagline": ""
    },
    "order": 1
  }
]
```

**Error Response**

**Condition** : If type is invalid.

**Code** : `400 BAD REQUEST`

**Content** :

```json
{
  "err": ["Bad request error"]
}
```

## Module Page

Used to get a module using its id.

**URL** : `/api/module/:_id`

**Method** : `GET`

**Auth required** : Yes

**Data example**

```json
{
  "_id": "5bd87654334323443"
}
```

**Success Response**

**Code** : `200 OK`

**Content example**

```json
{
  "_id": "5c04bbda595445574b1a5fe4",
  "title": "Conflict as a Lens",
  "slug": "HJG13EfkN-the-what-understanding-contradictions",
  "course": "5c04ba76595445574b1a5fbb",
  "creator": {
    "_id": "5c04b84d595445574b1a5f4a",
    "username": "BJ8UOVzJV",
    "initials": "JD",
    "name": "John Doe"
  },
  "updated_at": "2018-12-03T05:41:52.519Z",
  "__v": 2,
  "count": { "badges": 0, "time": 0 },
  "created_at": "2018-12-03T05:15:06.142Z",
  "resources": [],
  "privacy": "open",
  "is_active": true,
  "lessons": [
    {
      "_id": "5c04bd7c595445574b1a5ffd",
      "title": "Navigating Contradictions",
      "slug": "HkBtaVz1E-navigating-contradictions",
      "nav": "horizontal",
      "is_active": true,
      "order": 1
    }
  ],
  "text": {
    "about": "In this module we will explore how conflicts are not necessarily evil, but can be windows of opportunity to create something beautiful, and Build Back Better.",
    "tagline": ""
  },
  "order": 1
}
```

**Error Response**

**Condition** : If \_id is invalid.

**Code** : `404 Not Found`

**Content** :

```json
{
  "err": ["Not Found"]
}
```

## Module Actions

Used to update a module using its id and action.

**URL** : `/api/module/:_id/:action`

**Method** : `PUT`

**Auth required** : Yes

**Data example**

```json
{
  "_id": "5bd87654334323443",
  "action": "edit",
  "title": "module title changed"
}
```

**Success Response**

**Code** : `200 OK`

**Content example**

```json
{
  "_id": "5c04bbda595445574b1a5fe4",
  "title": "module title changed",
  "slug": "HJG13EfkN-the-what-understanding-contradictions",
  "course": "5c04ba76595445574b1a5fbb",
  "creator": {
    "_id": "5c04b84d595445574b1a5f4a",
    "username": "BJ8UOVzJV",
    "initials": "JD",
    "name": "John Doe"
  },
  "updated_at": "2018-12-03T05:41:52.519Z",
  "__v": 2,
  "count": { "badges": 0, "time": 0 },
  "created_at": "2018-12-03T05:15:06.142Z",
  "resources": [],
  "privacy": "open",
  "is_active": true,
  "lessons": [
    {
      "_id": "5c04bd7c595445574b1a5ffd",
      "title": "Navigating Contradictions",
      "slug": "HkBtaVz1E-navigating-contradictions",
      "nav": "horizontal",
      "is_active": true,
      "order": 1
    }
  ],
  "text": {
    "about": "In this module we will explore how conflicts are not necessarily evil, but can be windows of opportunity to create something beautiful, and Build Back Better.",
    "tagline": ""
  },
  "order": 1
}
```

**Error Response**

**Condition** : If \_id is invalid.

**Code** : `404 Not Found`

**Content** :

```json
{
  "err": ["Not Found"]
}
```
