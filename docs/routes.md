---
id: routes
title: Routes
sidebar_label: Routes
---

### Site Routing (Before login)

| Route     | Description           |
| --------- | --------------------- |
| `/`       | Landing page          |
| `/login`  | Login modal           |
| `/signup` | Signup modal          |
| `/forgot` | Forgot password modal |

### App Routing (After login)

| Route                     | Description                |
| ------------------------- | -------------------------- |
| `/`                       | Courses list page          |
| `/course/:slug`           | Course page                |
| `/lesson/:slug/:page_num` | Lesson page                |
| `/discussions`            | Discussions list page      |
| `/discussions/edit`       | Edit discussions           |
| `/discussion/:slug`       | Discussion page            |
| `/discussion/:slug/edit`  | Edit individual discussion |
| `/groups`                 | Groups list page           |
| `/groups/edit`            | Edit Groups                |
| `/group/:slug`            | Group page                 |
| `/group/:slug/edit`       | Edit individual group      |
| `/dashboard`              | User analytics dashboard   |
