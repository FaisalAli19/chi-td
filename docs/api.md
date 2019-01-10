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

## Lessons List

Used to get a list of lessons for a module.

**URL** : `/api/lessons/:_id`

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
    "_id": "5c04bd7c595445574b1a5ffd",
    "title": "Navigating Contradictions",
    "slug": "HkBtaVz1E-navigating-contradictions",
    "course": {
      "_id": "5c04ba76595445574b1a5fbb",
      "title": "Conflict Transformation",
      "slug": "H1CO5VMkE-navigating-contradictions",
      "creator": "5c04b84d595445574b1a5f4a",
      "members": [
        {
          "_id": "5c04bafa595445574b1a5fc9",
          "permit_val": "active",
          "added_at": "2018-12-03T05:11:22.997Z",
          "added_by": "5c04b84d595445574b1a5f4a",
          "user": "5be130e6a41f2a1c56152461",
          "modules": 0
        }
      ],
      "text": {
        "about": "Are conflicts unavoidable? Is yes, how do we make sense of them, do we need to go through the drill of mitigation, mediation, resolution and transformation, or can we aim to transform it right form the beginning?",
        "tagline": "Learning to Be, Learning to Live together"
      }
    },
    "module": {
      "_id": "5c04bbda595445574b1a5fe4",
      "title": "Conflict as a Lens",
      "slug": "HJG13EfkN-the-what-understanding-contradictions",
      "text": {
        "about": "In this module we will explore how conflicts are not necessarily evil, but can be windows of opportunity to create something beautiful, and Build Back Better.",
        "tagline": ""
      }
    },
    "creator": {
      "_id": "5c04b84d595445574b1a5f4a",
      "username": "BJ8UOVzJV",
      "initials": "JD",
      "name": "John Doe"
    },
    "updated_at": "2018-12-03T05:22:04.924Z",
    "__v": 0,
    "count": { "badges": 0, "time": 0 },
    "created_at": "2018-12-03T05:22:04.924Z",
    "resources": [],
    "nav": "horizontal",
    "is_active": true,
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

## Lesson Page

Used to get a lesson using its id.

**URL** : `/api/lesson/:_id`

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
  "_id": "5c04bd7c595445574b1a5ffd",
  "title": "Navigating Contradictions",
  "slug": "HkBtaVz1E-navigating-contradictions",
  "course": {
    "_id": "5c04ba76595445574b1a5fbb",
    "title": "Conflict Transformation",
    "slug": "H1CO5VMkE-navigating-contradictions",
    "creator": "5c04b84d595445574b1a5f4a",
    "members": [
      {
        "_id": "5c04bafa595445574b1a5fc9",
        "permit_val": "active",
        "added_at": "2018-12-03T05:11:22.997Z",
        "added_by": "5c04b84d595445574b1a5f4a",
        "user": "5be130e6a41f2a1c56152461",
        "modules": 0
      }
    ],
    "text": {
      "about": "Are conflicts unavoidable? Is yes, how do we make sense of them, do we need to go through the drill of mitigation, mediation, resolution and transformation, or can we aim to transform it right form the beginning?",
      "tagline": "Learning to Be, Learning to Live together"
    }
  },
  "module": {
    "_id": "5c04bbda595445574b1a5fe4",
    "title": "Conflict as a Lens",
    "slug": "HJG13EfkN-the-what-understanding-contradictions",
    "text": {
      "about": "In this module we will explore how conflicts are not necessarily evil, but can be windows of opportunity to create something beautiful, and Build Back Better.",
      "tagline": ""
    }
  },
  "creator": {
    "_id": "5c04b84d595445574b1a5f4a",
    "username": "BJ8UOVzJV",
    "initials": "JD",
    "name": "John Doe"
  },
  "updated_at": "2018-12-03T05:22:04.924Z",
  "__v": 0,
  "count": { "badges": 0, "time": 0 },
  "created_at": "2018-12-03T05:22:04.924Z",
  "resources": [],
  "nav": "horizontal",
  "is_active": true,
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

## Lesson Actions

Used to update a lesson using its id and action.

**URL** : `/api/lesson/:_id/:action`

**Method** : `PUT`

**Auth required** : Yes

**Data example**

```json
{
  "_id": "5bd87654334323443",
  "action": "edit",
  "title": "lesson title changed"
}
```

**Success Response**

**Code** : `200 OK`

**Content example**

```json
{
  "_id": "5c04bd7c595445574b1a5ffd",
  "title": "lesson title changed",
  "slug": "HkBtaVz1E-navigating-contradictions",
  "course": {
    "_id": "5c04ba76595445574b1a5fbb",
    "title": "Conflict Transformation",
    "slug": "H1CO5VMkE-navigating-contradictions",
    "creator": "5c04b84d595445574b1a5f4a",
    "members": [
      {
        "_id": "5c04bafa595445574b1a5fc9",
        "permit_val": "active",
        "added_at": "2018-12-03T05:11:22.997Z",
        "added_by": "5c04b84d595445574b1a5f4a",
        "user": "5be130e6a41f2a1c56152461",
        "modules": 0
      }
    ],
    "text": {
      "about": "Are conflicts unavoidable? Is yes, how do we make sense of them, do we need to go through the drill of mitigation, mediation, resolution and transformation, or can we aim to transform it right form the beginning?",
      "tagline": "Learning to Be, Learning to Live together"
    }
  },
  "module": {
    "_id": "5c04bbda595445574b1a5fe4",
    "title": "Conflict as a Lens",
    "slug": "HJG13EfkN-the-what-understanding-contradictions",
    "text": {
      "about": "In this module we will explore how conflicts are not necessarily evil, but can be windows of opportunity to create something beautiful, and Build Back Better.",
      "tagline": ""
    }
  },
  "creator": {
    "_id": "5c04b84d595445574b1a5f4a",
    "username": "BJ8UOVzJV",
    "initials": "JD",
    "name": "John Doe"
  },
  "updated_at": "2018-12-03T05:22:04.924Z",
  "__v": 0,
  "count": { "badges": 0, "time": 0 },
  "created_at": "2018-12-03T05:22:04.924Z",
  "resources": [],
  "nav": "horizontal",
  "is_active": true,
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

## Pages List

Used to get a list of pages for a lesson.

**URL** : `/api/pages/:_id`

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
    "_id": "5c04ca44595445574b1a607f",
    "slug": "SJTHqBzyN-",
    "course": "5c04ba76595445574b1a5fbb",
    "module": "5c04bbda595445574b1a5fe4",
    "lesson": "5c04bd7c595445574b1a5ffd",
    "creator": {
      "_id": "5c04b84d595445574b1a5f4a",
      "username": "BJ8UOVzJV",
      "initials": "JD",
      "name": "John Doe"
    },
    "updated_at": "2018-12-03T06:16:36.709Z",
    "__v": 0,
    "blocks": [
      {
        "updated_at": "2018-12-03T06:19:12.850Z",
        "creator": "5c04b84d595445574b1a5f4a",
        "text": "<p>Zen in the face of Hell</p><hr /><p>Big fish in a pond</p>",
        "page": "5c04ca44595445574b1a607f",
        "type": "text",
        "slug": "BkFkjSM1V",
        "_id": "5c04cae0595445574b1a608a",
        "created_at": "2018-12-03T06:19:12.851Z",
        "todos": [],
        "shape": { "size": 1 },
        "is_chat": false,
        "answers": [],
        "is_draggable": false,
        "options": [],
        "fills": [],
        "is_multiple": false,
        "mcqs": [],
        "images": [],
        "order": 1
      }
    ],
    "count": { "time": 0 },
    "created_at": "2018-12-03T06:16:36.709Z",
    "resources": [],
    "is_active": true,
    "notes": [],
    "badges": [],
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

## Page

Used to get a page using its id.

**URL** : `/api/page/:_id`

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
  "_id": "5c04ca44595445574b1a607f",
  "slug": "SJTHqBzyN-",
  "course": "5c04ba76595445574b1a5fbb",
  "module": "5c04bbda595445574b1a5fe4",
  "lesson": "5c04bd7c595445574b1a5ffd",
  "creator": {
    "_id": "5c04b84d595445574b1a5f4a",
    "username": "BJ8UOVzJV",
    "initials": "JD",
    "name": "John Doe"
  },
  "updated_at": "2018-12-03T06:16:36.709Z",
  "__v": 0,
  "blocks": [
    {
      "updated_at": "2018-12-03T06:19:12.850Z",
      "creator": "5c04b84d595445574b1a5f4a",
      "text": "<p>Zen in the face of Hell</p><hr /><p>Big fish in a pond</p>",
      "page": "5c04ca44595445574b1a607f",
      "type": "text",
      "slug": "BkFkjSM1V",
      "_id": "5c04cae0595445574b1a608a",
      "created_at": "2018-12-03T06:19:12.851Z",
      "todos": [],
      "shape": { "size": 1 },
      "is_chat": false,
      "answers": [],
      "is_draggable": false,
      "options": [],
      "fills": [],
      "is_multiple": false,
      "mcqs": [],
      "images": [],
      "order": 1
    }
  ],
  "count": { "time": 0 },
  "created_at": "2018-12-03T06:16:36.709Z",
  "resources": [],
  "is_active": true,
  "notes": [],
  "badges": [],
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

## Page Actions

Used to update a page using its id and action.

**URL** : `/api/page/:_id/:action`

**Method** : `PUT`

**Auth required** : Yes

**Data example**

```json
{
  "_id": "5bd87654334323443",
  "action": "edit",
  "is_active": false
}
```

**Success Response**

**Code** : `200 OK`

**Content example**

```json
{
  "_id": "5c04ca44595445574b1a607f",
  "slug": "SJTHqBzyN-",
  "course": "5c04ba76595445574b1a5fbb",
  "module": "5c04bbda595445574b1a5fe4",
  "lesson": "5c04bd7c595445574b1a5ffd",
  "creator": {
    "_id": "5c04b84d595445574b1a5f4a",
    "username": "BJ8UOVzJV",
    "initials": "JD",
    "name": "John Doe"
  },
  "updated_at": "2018-12-03T06:16:36.709Z",
  "__v": 0,
  "blocks": [
    {
      "updated_at": "2018-12-03T06:19:12.850Z",
      "creator": "5c04b84d595445574b1a5f4a",
      "text": "<p>Zen in the face of Hell</p><hr /><p>Big fish in a pond</p>",
      "page": "5c04ca44595445574b1a607f",
      "type": "text",
      "slug": "BkFkjSM1V",
      "_id": "5c04cae0595445574b1a608a",
      "created_at": "2018-12-03T06:19:12.851Z",
      "todos": [],
      "shape": { "size": 1 },
      "is_chat": false,
      "answers": [],
      "is_draggable": false,
      "options": [],
      "fills": [],
      "is_multiple": false,
      "mcqs": [],
      "images": [],
      "order": 1
    }
  ],
  "count": { "time": 0 },
  "created_at": "2018-12-03T06:16:36.709Z",
  "resources": [],
  "is_active": false,
  "notes": [],
  "badges": [],
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

## Blocks List

Used to get all the blocks of a page.

**URL** : `/api/blocks/:_id`

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
    "updated_at": "2018-12-03T06:19:12.850Z",
    "creator": "5c04b84d595445574b1a5f4a",
    "text": "<p>Zen in the face of Hell</p><hr /><p>Big fish in a pond</p>",
    "page": "5c04ca44595445574b1a607f",
    "type": "text",
    "slug": "BkFkjSM1V",
    "_id": "5c04cae0595445574b1a608a",
    "created_at": "2018-12-03T06:19:12.851Z",
    "todos": [],
    "shape": { "size": 1 },
    "is_chat": false,
    "answers": [],
    "is_draggable": false,
    "options": [],
    "fills": [],
    "is_multiple": false,
    "mcqs": [],
    "images": [],
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

## Block

Used to get a block using its id.

**URL** : `/api/page/:_id`

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
  "updated_at": "2018-12-03T06:19:12.850Z",
  "creator": "5c04b84d595445574b1a5f4a",
  "text": "<p>Zen in the face of Hell</p><hr /><p>Big fish in a pond</p>",
  "page": "5c04ca44595445574b1a607f",
  "type": "text",
  "slug": "BkFkjSM1V",
  "_id": "5c04cae0595445574b1a608a",
  "created_at": "2018-12-03T06:19:12.851Z",
  "todos": [],
  "shape": { "size": 1 },
  "is_chat": false,
  "answers": [],
  "is_draggable": false,
  "options": [],
  "fills": [],
  "is_multiple": false,
  "mcqs": [],
  "images": [],
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

## Block Actions

Used to update a block using its id and action.

**URL** : `/api/page/:_id/:action`

**Method** : `PUT`

**Auth required** : Yes

**Data example**

```json
{
  "_id": "5bd87654334323443",
  "action": "edit",
  "is_multiple": false
}
```

**Success Response**

**Code** : `200 OK`

**Content example**

```json
{
  "updated_at": "2018-12-03T06:19:12.850Z",
  "creator": "5c04b84d595445574b1a5f4a",
  "text": "<p>Zen in the face of Hell</p><hr /><p>Big fish in a pond</p>",
  "page": "5c04ca44595445574b1a607f",
  "type": "text",
  "slug": "BkFkjSM1V",
  "_id": "5c04cae0595445574b1a608a",
  "created_at": "2018-12-03T06:19:12.851Z",
  "todos": [],
  "shape": { "size": 1 },
  "is_chat": false,
  "answers": [],
  "is_draggable": false,
  "options": [],
  "fills": [],
  "is_multiple": true,
  "mcqs": [],
  "images": [],
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

## Discussions List

Used to get a list of discussions of a given type.

**URL** : `/api/discussions/:type`

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
    "_id": "5bd80fdc1e639148b869b191",
    "course": {
      "_id": "5bd80e841e639148b869b189",
      "title": "This is a new course",
      "slug": "B1pYCFH27-this-is-a-new-course",
      "text": {
        "about": "This is an awesome course.",
        "tagline": "Awesome course"
      }
    },
    "slug": "Syr1g9B2Q-dummy",
    "type": "file",
    "title": "dummy",
    "creator": {
      "_id": "5bd80bab1e639148b869b187",
      "username": "H1NhiKr2m",
      "initials": "JD",
      "name": "John Doe"
    },
    "updated_at": "2018-10-30T08:01:32.687Z",
    "count": { "members": 0, "comments": 0 },
    "comments": [],
    "is_restricted": false,
    "privacy": "public",
    "created_at": "2018-10-30T08:01:32.688Z",
    "groups": [],
    "has_voted": false,
    "polls": [],
    "file": { "size": 509, "ext": "txt" },
    "provider": { "name": "CHI", "url": "" }
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

## Discussion Page

Used to get a discussion using its id.

**URL** : `/api/discussion/:_id`

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
  "_id": "5bd80fdc1e639148b869b191",
  "course": {
    "_id": "5bd80e841e639148b869b189",
    "title": "This is a new course",
    "slug": "B1pYCFH27-this-is-a-new-course",
    "text": {
      "about": "This is an awesome course.",
      "tagline": "Awesome course"
    }
  },
  "slug": "Syr1g9B2Q-dummy",
  "type": "file",
  "title": "dummy",
  "creator": {
    "_id": "5bd80bab1e639148b869b187",
    "username": "H1NhiKr2m",
    "initials": "JD",
    "name": "John Doe"
  },
  "updated_at": "2018-10-30T08:01:32.687Z",
  "count": { "members": 0, "comments": 0 },
  "comments": [],
  "is_restricted": false,
  "privacy": "public",
  "created_at": "2018-10-30T08:01:32.688Z",
  "groups": [],
  "has_voted": false,
  "polls": [],
  "file": { "size": 509, "ext": "txt" },
  "provider": { "name": "CHI", "url": "" }
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

## Discussion Actions

Used to update a discussion using its id and action.

**URL** : `/api/discussion/:_id/:action`

**Method** : `PUT`

**Auth required** : Yes

**Data example**

```json
{
  "_id": "5bd87654334323443",
  "action": "edit",
  "title": "discussion title changed"
}
```

**Success Response**

**Code** : `200 OK`

**Content example**

```json
{
  "_id": "5bd80fdc1e639148b869b191",
  "course": {
    "_id": "5bd80e841e639148b869b189",
    "title": "This is a new course",
    "slug": "B1pYCFH27-this-is-a-new-course",
    "text": {
      "about": "This is an awesome course.",
      "tagline": "Awesome course"
    }
  },
  "slug": "Syr1g9B2Q-dummy",
  "type": "file",
  "title": "discussion title changed",
  "creator": {
    "_id": "5bd80bab1e639148b869b187",
    "username": "H1NhiKr2m",
    "initials": "JD",
    "name": "John Doe"
  },
  "updated_at": "2018-10-30T08:01:32.687Z",
  "count": { "members": 0, "comments": 0 },
  "comments": [],
  "is_restricted": false,
  "privacy": "public",
  "created_at": "2018-10-30T08:01:32.688Z",
  "groups": [],
  "has_voted": false,
  "polls": [],
  "file": { "size": 509, "ext": "txt" },
  "provider": { "name": "CHI", "url": "" }
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

## Comment

To add a new comment.

**URL** : `/api/comment/:_id`

**Method** : `POST`

**Auth required** : Yes

**Data example**

```json
{
  "discussion_id": "5bfbc44c5f558a48477bcfe0",
  "comment": "Hello"
}
```

**Success Response**

**Code** : `200 OK`

**Content example**

```json
{
  "_id": "5bfbc4595f558a48477bcfe1",
  "updated_at": "2018-11-26T10:00:57.888Z",
  "creator": {
    "_id": "5bfbbf435f558a48477bcf5c",
    "username": "rynHJrK07",
    "initials": "JD",
    "name": "John Doe",
    "job": { "org": "", "title": "" }
  },
  "comment": "Hello",
  "created_at": "2018-11-26T10:00:57.888Z",
  "likes": ["5bfbbf435f558a48477bcf5c"]
}
```

**Error Response**

**Condition** : If discussion_id is invalid.

**Code** : `404 Not Found`

**Content** :

```json
{
  "err": ["Not Found"]
}
```

## Comment Actions

Used to update a comment using action.

**URL** : `/api/comment/:_id/:action`

**Method** : `PUT`

**Auth required** : Yes

**Data example**

```json
{
  "_id": "5bfbc4595f558a48477bcfe1",
  "action": "edit",
  "comment": "comment changed"
}
```

**Success Response**

**Code** : `200 OK`

**Content example**

```json
{
  "_id": "5bfbc4595f558a48477bcfe1",
  "updated_at": "2018-11-26T10:00:57.888Z",
  "creator": {
    "_id": "5bfbbf435f558a48477bcf5c",
    "username": "rynHJrK07",
    "initials": "JD",
    "name": "John Doe",
    "job": { "org": "", "title": "" }
  },
  "comment": "comment changed",
  "created_at": "2018-11-26T10:00:57.888Z",
  "likes": ["5bfbbf435f558a48477bcf5c"]
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

## Current User

Used to get logged in user's details.

**URL** : `/api/me`

**Method** : `GET`

**Auth required** : Yes

**Data example**

```json
{}
```

**Success Response**

**Code** : `200 OK`

**Content example**

```json
{
  "is_local": true,
  "_id": "5bd971341e639148b869b1e5",
  "username": "BypE-gv27",
  "initials": "JD",
  "name": "John Doe",
  "password": "",
  "email": "john.doe@example.com",
  "__v": 0,
  "theme": "dark",
  "accountCreated": "2018-10-31T09:09:08.818Z",
  "anon": { "name": "Mark", "id": "SkgTVWgPh7" },
  "karma": 10,
  "type": "normal"
}
```

## User Details

Used to get user details by id.

**URL** : `/api/user/:_id`

**Method** : `GET`

**Auth required** : Yes

**Data example**

```json
{
  "_id": "5bd971341e639148b869b1e5"
}
```

**Success Response**

**Code** : `200 OK`

**Content example**

```json
{
  "_id": "5bd971341e639148b869b1e5",
  "username": "BypE-gv27",
  "initials": "JD",
  "name": "John Doe",
  "accountCreated": "2018-10-31T09:09:08.818Z",
  "karma": 10
}
```

## Learner Dashboard

Used to get user learner analytics data.

**URL** : `/api/dashboard/learner`

**Method** : `GET`

**Auth required** : Yes

**Data example**

```json
{}
```

**Success Response**

**Code** : `200 OK`

**Content example**

```json
{
  "nlu": [
    {
      "_id": "5c062f30131ed805e958fa86",
      "creator": "5be8f2c6d30da1044296b538",
      "type": "audio",
      "sourceType": "lesson",
      "sourceId": "5be8f35ed30da1044296b53c",
      "answerId": "5c062f28131ed805e958fa85",
      "blockId": "5be8f3bbd30da1044296b53f",
      "__v": 0,
      "emotions": {
        "sadness": 0,
        "joy": 0,
        "fear": 0,
        "disgust": 0,
        "anger": 0
      },
      "sentiment": {
        "score": 0.52252,
        "label": "positive"
      }
    }
  ],
  "blocks": [
    {
      "_id": "5be8f3bbd30da1044296b53f",
      "text": "Record your view on this topic in audio",
      "slug": "r17pQOU6X",
      "type": "journal",
      "page": "5be8f362d30da1044296b53d",
      "title": "Record you view",
      "journal_type": "audio",
      "creator": "5be8f2c6d30da1044296b538",
      "updated_at": "2018-11-12T03:30:03.437Z",
      "optionsB": [],
      "optionsA": [],
      "__v": 10,
      "created_at": "2018-11-12T03:30:03.437Z",
      "todos": [],
      "shape": {
        "size": 1
      },
      "is_chat": false,
      "answers": [
        {
          "_id": "5c062f28131ed805e958fa85",
          "creator": "5be8f2c6d30da1044296b538",
          "created_at": "2018-12-04T07:39:20.493Z",
          "provider": {
            "url": "",
            "name": "CHI"
          },
          "file": {
            "ext": "webm",
            "size": 11706
          }
        }
      ],
      "is_draggable": false,
      "options": [],
      "fills": [],
      "is_multiple": false,
      "mcqs": [],
      "images": [],
      "order": 1
    }
  ],
  "users": {
    "_id": "5be8f2c6d30da1044296b538",
    "username": "B1yCf_L6X",
    "initials": "JD",
    "name": "John Doe",
    "email": "johndoe@example.co",
    "__v": 0,
    "about": "",
    "city": "",
    "country": "India",
    "phone": null,
    "theme": "dark",
    "loginAttempts": 0,
    "accountCreated": "2018-11-12T03:25:59.128Z",
    "job": {
      "org": "",
      "title": ""
    },
    "anon": {
      "name": "Hannah",
      "id": "S1lk0G_U6m"
    },
    "karma": 10,
    "type": "normal"
  },
  "lessons": [
    {
      "_id": "5be8f35ed30da1044296b53c",
      "title": "Analytic Lesson"
    }
  ],
  "wordCloud": {
    "_id": "5be93cbb04d9110914688751",
    "user": "5be8f2c6d30da1044296b538",
    "__v": 0,
    "global_data": [
      {
        "relevance": 0.960949,
        "text": "awesome people",
        "_id": "5c1b63f0a9af1b0758f2fb99",
        "emotion": {
          "anger": 0.003333,
          "disgust": 0.004936,
          "fear": 0.01961,
          "joy": 0.944444,
          "sadness": 0.025886
        },
        "sentiment": {
          "label": "positive",
          "score": 0.99789
        }
      }
    ]
  }
}
```

## Creator's Dashboard

Used to get user creator's analytics data.

**URL** : `/api/dashboard/:type/:id`

**Method** : `GET`

**Auth required** : Yes

**Data example**

```json
{
  "type": "all",
  "id": "all"
}
```

**Success Response**

**Code** : `200 OK`

**Content example**

```json
{
  "nlu": [
    {
      "_id": "5c062f30131ed805e958fa86",
      "creator": "5be8f2c6d30da1044296b538",
      "type": "audio",
      "sourceType": "lesson",
      "sourceId": "5be8f35ed30da1044296b53c",
      "answerId": "5c062f28131ed805e958fa85",
      "blockId": "5be8f3bbd30da1044296b53f",
      "__v": 0,
      "emotions": {
        "sadness": 0,
        "joy": 0,
        "fear": 0,
        "disgust": 0,
        "anger": 0
      },
      "sentiment": {
        "score": 0.52252,
        "label": "positive"
      }
    }
  ],
  "blocks": [
    {
      "_id": "5be8f3bbd30da1044296b53f",
      "text": "Record your view on this topic in audio",
      "slug": "r17pQOU6X",
      "type": "journal",
      "page": "5be8f362d30da1044296b53d",
      "title": "Record you view",
      "journal_type": "audio",
      "creator": "5be8f2c6d30da1044296b538",
      "updated_at": "2018-11-12T03:30:03.437Z",
      "optionsB": [],
      "optionsA": [],
      "__v": 10,
      "created_at": "2018-11-12T03:30:03.437Z",
      "todos": [],
      "shape": {
        "size": 1
      },
      "is_chat": false,
      "answers": [
        {
          "_id": "5c062f28131ed805e958fa85",
          "creator": "5be8f2c6d30da1044296b538",
          "created_at": "2018-12-04T07:39:20.493Z",
          "provider": {
            "url": "",
            "name": "CHI"
          },
          "file": {
            "ext": "webm",
            "size": 11706
          }
        }
      ],
      "is_draggable": false,
      "options": [],
      "fills": [],
      "is_multiple": false,
      "mcqs": [],
      "images": [],
      "order": 1
    }
  ],
  "users": [
    {
      "_id": "5be8f2c6d30da1044296b538",
      "username": "B1yCf_L6X",
      "initials": "JD",
      "name": "John Doe",
      "email": "johndoe@example.co",
      "__v": 0,
      "about": "",
      "city": "",
      "country": "India",
      "phone": null,
      "theme": "dark",
      "loginAttempts": 0,
      "accountCreated": "2018-11-12T03:25:59.128Z",
      "job": {
        "org": "",
        "title": ""
      },
      "anon": {
        "name": "Hannah",
        "id": "S1lk0G_U6m"
      },
      "karma": 10,
      "type": "normal"
    }
  ],
  "lessons": [
    {
      "_id": "5be8f35ed30da1044296b53c",
      "title": "Analytic Lesson"
    }
  ],
  "wordCloud": {
    "_id": "5be93cbb04d9110914688751",
    "user": "5be8f2c6d30da1044296b538",
    "__v": 0,
    "global_data": [
      {
        "relevance": 0.960949,
        "text": "awesome people",
        "_id": "5c1b63f0a9af1b0758f2fb99",
        "emotion": {
          "anger": 0.003333,
          "disgust": 0.004936,
          "fear": 0.01961,
          "joy": 0.944444,
          "sadness": 0.025886
        },
        "sentiment": {
          "label": "positive",
          "score": 0.99789
        }
      }
    ]
  }
}
```

## Dashboard Filters

Used to get user creator analytics filtered data.

**URL** : `/api/dashboard/filter/:type/:id`

**Method** : `GET`

**Auth required** : Yes

**Data example**

```json
{
  "type": "user",
  "id": "5be8f2c6d30da1044296b538"
}
```

**Success Response**

**Code** : `200 OK`

**Content example**

```json
{
  "nlu": [
    {
      "_id": "5c062f30131ed805e958fa86",
      "creator": "5be8f2c6d30da1044296b538",
      "type": "audio",
      "sourceType": "lesson",
      "sourceId": "5be8f35ed30da1044296b53c",
      "answerId": "5c062f28131ed805e958fa85",
      "blockId": "5be8f3bbd30da1044296b53f",
      "__v": 0,
      "emotions": {
        "sadness": 0,
        "joy": 0,
        "fear": 0,
        "disgust": 0,
        "anger": 0
      },
      "sentiment": {
        "score": 0.52252,
        "label": "positive"
      }
    }
  ],
  "blocks": [
    {
      "_id": "5be8f3bbd30da1044296b53f",
      "text": "Record your view on this topic in audio",
      "slug": "r17pQOU6X",
      "type": "journal",
      "page": "5be8f362d30da1044296b53d",
      "title": "Record you view",
      "journal_type": "audio",
      "creator": "5be8f2c6d30da1044296b538",
      "updated_at": "2018-11-12T03:30:03.437Z",
      "optionsB": [],
      "optionsA": [],
      "__v": 10,
      "created_at": "2018-11-12T03:30:03.437Z",
      "todos": [],
      "shape": {
        "size": 1
      },
      "is_chat": false,
      "answers": [
        {
          "_id": "5c062f28131ed805e958fa85",
          "creator": "5be8f2c6d30da1044296b538",
          "created_at": "2018-12-04T07:39:20.493Z",
          "provider": {
            "url": "",
            "name": "CHI"
          },
          "file": {
            "ext": "webm",
            "size": 11706
          }
        }
      ],
      "is_draggable": false,
      "options": [],
      "fills": [],
      "is_multiple": false,
      "mcqs": [],
      "images": [],
      "order": 1
    }
  ],
  "users": {
    "_id": "5be8f2c6d30da1044296b538",
    "username": "B1yCf_L6X",
    "initials": "JD",
    "name": "John Doe",
    "email": "johndoe@example.co",
    "__v": 0,
    "about": "",
    "city": "",
    "country": "India",
    "phone": null,
    "theme": "dark",
    "loginAttempts": 0,
    "accountCreated": "2018-11-12T03:25:59.128Z",
    "job": {
      "org": "",
      "title": ""
    },
    "anon": {
      "name": "Hannah",
      "id": "S1lk0G_U6m"
    },
    "karma": 10,
    "type": "normal"
  },
  "lessons": [
    {
      "_id": "5be8f35ed30da1044296b53c",
      "title": "Analytic Lesson"
    }
  ],
  "wordCloud": {
    "_id": "5be93cbb04d9110914688751",
    "user": "5be8f2c6d30da1044296b538",
    "__v": 0,
    "global_data": [
      {
        "relevance": 0.960949,
        "text": "awesome people",
        "_id": "5c1b63f0a9af1b0758f2fb99",
        "emotion": {
          "anger": 0.003333,
          "disgust": 0.004936,
          "fear": 0.01961,
          "joy": 0.944444,
          "sadness": 0.025886
        },
        "sentiment": {
          "label": "positive",
          "score": 0.99789
        }
      }
    ]
  }
}
```

**Error Response**

**Condition** : If id is invalid.

**Code** : `404 Not Found`

**Content** :

```json
{
  "err": ["Not Found"]
}
```
