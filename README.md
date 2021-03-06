This project was created by following the step-by-step, and sometimes not so clear steps, of the tutorial at http://sahatyalkabov.com/create-a-tv-show-tracker-using-angularjs-nodejs-and-mongodb/

We've deployed this application using nodejitsu and it can be found at: http://showtracker.jit.su

During the course of creating file, typing in code, downloading modules, and other libraries, we've encountered some issue. Here we document the enhancements we'd like to work on, as well as some of the problems we see with the project, so we can try to enhance it, as we learn MEAN.

NOTE: This project was not forked from the github repo indicated in the link above.


Enhancement Ideas:

1. Should be able to view top shows on what? the db api, in general?
- how should this be kept updated

2. User should not only be able to unsuscribe from getting e-mail alerts, but should also be able to delete a show from their view/list

3. When adding a show, it would be good to see which shows match the words entered, such that the user can pick the right show

4. When an image for a show is not available from the shows db, the image should be grabbed from another location

5. Info about what "subscribe" means

6. Ability to change frequency or time of alerts

7. Shows list when the next episode is coming, disambiguate if this is the next NEW episode (see bug #4)

8. On logout, we should not see the shows of the person who was logged in before, e.g. even me, it should show the top shows of all users or the top shows based on the shows db


Bug Fixes:

1. Server crashed sometimes when adding a new show when signed in (need to check if when signed out)

2. Some libraries and methods seem to have depracated, so these should be udpated

3. Sometimes, when adding a new show, when one clicks on Home to go back, the server crashes with the following error

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

4. Shows list when the next episode is occurring, but there are repeats, and according to TV Guide, sometimes NEW episodes are occurring sooner than the app is calculating right now.


