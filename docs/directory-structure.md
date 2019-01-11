---
id: directory-structure
title: Directory Structure
sidebar_label: Directory Structure
---

```
CHI
├── app
│   ├── models
│   │   ├── entity.js
│   │   ├── logintoken.js
│   │   └── user.js
│   ├── api.js
│   ├── nlu.js
│   ├── online.js
│   ├── realtime.js
│   ├── routes.js
│   └── utility.js
├── config
│   ├── auth.js
│   ├── database.js
│   ├── mail.js
│   └── passport.js
├── email_templates
│   ├── course_invite_new.html
│   ├── course_invite.html
│   ├── password_changed.html
│   └── reset.html
├── log
│   └── app.log
├── static
│   ├── css
│   │   ├── lib
│   │   │ 	├── fonts
│   │   │ 	│ 	├── videojs-record.eot
│   │   │ 	│ 	├── videojs-record.svg
│   │   │ 	│ 	├── videojs-record.ttf
│   │   │ 	│ 	└── videojs-record.woff
│   │   │ 	├── audioplayer.css
│   │   │ 	├── canvas.css
│   │   │ 	├── charts.css
│   │   │ 	├── chosen-sprite.png
│   │   │ 	├── chosen-sprite@2x.png
│   │   │ 	├── chosen.css
│   │   │ 	├── dark-charts.css
│   │   │ 	├── sweet-alert.css
│   │   │ 	├── video-js.min.css
│   │   │ 	└── videojs.record.min.css
│   │   ├── themes
│   │   │ 	└── dark.css
│   │   ├── login_style.css
│   │   └── style.css
│   ├── images
│   │   ├── app
│   │   └── site
│   ├── js
│   │   ├── data
│   │   │   └── country_data.csv
│   │   ├── lib
│   │   │ 	├── alloy-editor
│   │   │ 	├── async
│   │   │ 	├── audio
│   │   │ 	├── autosize
│   │   │ 	├── backbone
│   │   │ 	├── canvas
│   │   │ 	├── chosen
│   │   │ 	├── cookie
│   │   │ 	├── d3
│   │   │ 	├── d3-cloud
│   │   │ 	├── dateformat
│   │   │ 	├── drive
│   │   │ 	├── fileupload
│   │   │ 	├── handlebars
│   │   │ 	├── hotkeys
│   │   │ 	├── jquery
│   │   │ 	├── jquery-visible
│   │   │ 	├── jqueryui
│   │   │ 	├── marionette
│   │   │ 	├── masonry
│   │   │ 	├── modernizr
│   │   │ 	├── phaser
│   │   │ 	├── swag
│   │   │ 	├── sweetalert
│   │   │ 	├── timepicker
│   │   │ 	├── tipsy
│   │   │ 	├── topojson
│   │   │ 	├── typeahead
│   │   │ 	├── underscore
│   │   │ 	├── uuid
│   │   │ 	├── validator
│   │   │ 	├── video
│   │   │ 	└── webflow
│   │   ├── editor.js
│   │   ├── global.js
│   │   ├── helpers.js
│   │   ├── loadTemplate.js
│   │   ├── loginApp.js
│   │   └── mainApp.js
│   ├── templates
│   │   ├── oneReplyTemplate.handlebars
│   │   ├── blockItemTemplate.handlebars
│   │   ├── commentsTemplate.handlebars
│   │   ├── courseMembersTemplate.handlebars
│   │   ├── courseObjectivesTemplate.handlebars
│   │   ├── courseOneTemplate.handlebars
│   │   ├── dashboardTemplate.handlebars
│   │   ├── dashboardUserTemplate.handlebars
│   │   ├── discussionAnalyticsOne.handlebars
│   │   ├── discussionOneTemplate.handlebars
│   │   ├── discussionsSectionTemplate.handlebars
│   │   ├── editingToolbarTemplate.handlebars
│   │   ├── emptyCommentsTemplate.handlebars
│   │   ├── emptyDiscussionsTemplate.handlebars
│   │   ├── emptyModulesTemplate.handlebars
│   │   ├── emptyPagesTemplate.handlebars
│   │   ├── faqOneTemplate.handlebars
│   │   ├── fillOneTemplate.handlebars
│   │   ├── fillsTemplate.handlebars
│   │   ├── forgotTemplate.handlebars
│   │   ├── fullCourseTemplate.handlebars
│   │   ├── groupMembersTemplate.handlebars
│   │   ├── groupOneTemplate.handlebars
│   │   ├── lessonOneTemplate.handlebars
│   │   ├── lessonToolbarTemplate.handlebars
│   │   ├── linkDiscussionTemplate.handlebars
│   │   ├── loadingTemplate.handlebars
│   │   ├── loginTemplate.handlebars
│   │   ├── matchOptionOneTemplate.handlebars
│   │   ├── matchOptionsTemplate.handlebars
│   │   ├── mcqOptionOneTemplate.handlebars
│   │   ├── mcqOptionsTemplate.handlebars
│   │   ├── memberOneTemplate.handlebars
│   │   ├── moduleOneTemplate.handlebars
│   │   ├── newBlockTemplate.handlebars
│   │   ├── newConnectionTemplate.handlebars
│   │   ├── newCourseTemplate.handlebars
│   │   ├── newDiscussionTemplate.handlebars
│   │   ├── newGroupTemplate.handlebars
│   │   ├── newModuleTemplate.handlebars
│   │   ├── oneCommentTemplate.handlebars
│   │   ├── pageOneTemplate.handlebars
│   │   ├── resourceOneTemplate.handlebars
│   │   ├── signupTemplate.handlebars
│   │   ├── tagOneTemplate.handlebars
│   │   └── userSettingsTemplate.handlebars
│   ├── manifest.json
│   └── sw.js
├── views
│   ├── app
│   │   └── index.hbs
│   ├── site
│   │   ├── index.hbs
│   │   └── reset.hbs
│   └── partials
├── .env
├── server.js
├── readme.md
└── package.json
```

- `app/models`: contains all the schemas.
- `app/api.js`: contains all the api endpoints.
- `app/nlu.js`: contains the functions for sentiment, tones and emotions analysis.
- `app/routes.js`: contains the application routes.
- `app/utility.js`: contains common utility functions like upload_file, get_cropped_image, etc.
- `config/auth.js`: contains auth credentials.
- `config/database.js`: contains database configurations.
- `config/mail.js`: contains sendOneMail function to send an email using sendgrid.
- `config/passport.js`: contains passport authentication code.
- `email_templates/*`: contains different email templates like course_invite.html, password_changed.html, etc.
- `log/app.log`: contains application logs.
- `static/css/lib`: contains all the css libraries like sweetalert.css, chosen.css, etc.
- `static/css/*`: contains all the styles and themes.
- `static/images/*`: contains all the images used in the application.
- `static/js/data`: contains country_data.csv for the geo chart in dashboard.
- `static/js/lib`: contains all the js libraries like sweetalert.js, backbone.js, etc.
- `static/js/editor.js`: contains CKEDITOR functions to edit and add rich text styles.
- `static/js/global.js`: contains the global functions used across the application.
- `static/js/helpers.js`: contains the handlebars helper functions.
- `static/js/loadTemplate.js`: contains the functions to load and compile handlebar templates.
- `static/js/loginApp.js`: contains the functions to support user login.
- `static/js/mainApp.js`: contains the functions for rendering templates with data after user login.
- `static/templates/*`: contains the handlebar templates.
- `static/manifest.json`: contains the files that need to be cached for offline functionalitys.
- `static/sw.js`: contains the functions related to service worker.
- `views/app/index.hbs`: Barebone structure for the application after login.
- `views/site/index.hbs`: Barebone structure for the application before login.
- `views/site/reset.hbs`: Barebone structure to reset password.
- `.env`: contains all the environment variables.
- `server.js`: contains the code for setting up express server.
- `package.json`: contains all the packages list and scripts to start or watch the server.
