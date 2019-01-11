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
- `app/api.js`: contains all the endpoints.
- `docs/.vuepress/theme`: Used to store local theme.
- `docs/.vuepress/styles`: Stores style related files.
- `docs/.vuepress/styles/index.styl`: Automatically applied global style files, generated at the ending of the CSS file, have a higher priority than the default style.
- `docs/.vuepress/styles/palette.styl`: The palette is used to override the default color constants and to set the color constants of Stylus.
- `docs/.vuepress/public`: Static resource directory.
- `docs/.vuepress/templates`: Store HTML template files.
- `docs/.vuepress/templates/dev.html`: HTML template file for development environment.
- `docs/.vuepress/templates/ssr.html`: Vue SSR based HTML template file in the built time.
- `docs/.vuepress/config.js`: Entry file of configuration, can also be `yml` or `toml`.
- `docs/.vuepress/enhanceApp.js`: App level enhancement.
