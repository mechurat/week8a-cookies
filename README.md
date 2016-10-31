# Week 8a - Cookies and States
## HTTP & State
Stateless:

Stateless pages don't record any data from a user, or keep any data for browsing

Setting a State allows for the creation of user profiles and 'sessions'

## Cookies
Allows setting a state so that data from a user is recorded throughout navigating a webpage.

To see cookies in Chrome dev tools, go to the "Applications" tab. You can also look at individual requests in the "Network" tab -> Cookies

Server -> Sends request to Client to set Cookie
Client -> Sends data back to Server to make Cookie (unless blocked)

### Format
#### Installation
**cmd prompt:**

**npm install cookie-parser --save**

**IN INDEX.JS**
load module: var cookieParser = require('cookie-parser');

app assignment: app.use(cookieParser('secret'))


Express Cookies: See [Slides](https://docs.google.com/presentation/d/1GEPgDL3SmTis5ifQxx29t1PhGfqFDM3gpWsdpfYPX4E/edit) and [Expressjs cookie documentation](http://expressjs.com/en/api.html#res.cookie)

Assigning a Cookie: see [index.js](https://github.com/mechurat/week8a-cookies/blob/master/index.js)
* ServerID: 8081
* // home page
* // cookie creation (use /treat)
* // cookie deletion (use /clear)
* // load modules (var cookieParser)

res.cookie('name', value [, options])

Getting a Cookie from a request

var name = req.cookies.name

## Sessions
[LINK to github](https://github.com/expressjs/session)
**Module:** express-session

* npm install express-session --save

see [index.js](https://github.com/mechurat/week8a-cookies/blob/master/index.js) || session code is **uncommented** in the same areas as cookies

### Flash Messages in Sessions
This is **included** in express-session

**code:** req.session.flash = { contents }