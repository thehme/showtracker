Enhancement Ideas:

1. Should be able to view top shows on what? the db api, in general?
- how should this be kept updated

2. User should not only be able to unsuscribe from getting e-mail alerts, but should also be able to delete a show from their view/list

3. When adding a show, it would be good to see which shows match the words entered, such that the user can pick the right show

4. When an image for a show is not available from the shows db, the image should be grabbed from another location

5. Info about what "subscribe" means

6. Ability to change frequency or time of alerts

Bug Fixes:

1. Server crashed sometimes when adding a new show when signed in (need to check if when signed out)

2. Some libraries and methods seem to have depracated, so these should be udpated

3. Sometimes, when adding a new show, it takes several seconds and then the server crashes with the following error

```
TypeError: Cannot read property 'message' of undefined 
at /showtracker/server.js:320:46
at Nodemailer.sendMail (/showtracker/node_modules/nodemailer/src/nodemailer.js:85:16)
at Promise.<anonymous> (/showtracker/server.js:319:19)
at Promise.<anonymous> (/showtracker/node_modules/mongoose/node_modules/mpromise/lib/promise.js:177:8)
at Promise.emit (events.js:95:17l)
at Promise.emit (/showtracker/node_modules/mongoose/node_modules/mpromise/lib/promise.js:84:38)
at Promise.fulfill (/showtracker/node_modules/mongoose/node_modules/mpromise/lib/promise.js:97:20)
at Promise.resolve (/showtracker/node_modules/mongoose/lib/promise.js:113:23)
at Promise.<anonymous> (/showtracker/node_modules/mongoose/node_modules/mpromise/lib/promise.js:177:8)
at Promise.emit (events.js:95:17)
```
