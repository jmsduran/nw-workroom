nw-workroom (v2.0.0)
=============

A node-webkit port of [node-workroom] (https://github.com/jmsduran/node-workroom). In order to run flawlessly as a desktop application via node-webkit, some minor alterations must be made.

Running
---

To package and run the nw-workroom app, please refer to the node-webkit [How to package and distribute your apps] (https://github.com/rogerwang/node-webkit/wiki/How-to-package-and-distribute-your-apps) article.

nw-workroom uses handlebars templates stored in `src/view/html`. These templates are then pre-compiled into `src/view/js/view.compiled.js` and included within the app's main HTML.

Whenever these templates are modified, the following handlebars command should be run prior to deployment:

```
handlebars src/view/html -e hbs -f src/view/js/view.compiled.js
```

Note: This application currently runs on port 1337. If nw-workroom interferes with any other application or web service running on the same machine, simply change the port numbers listed in `dashboard.html` and `app.js`, and redeploy the application.

Dependencies
---

[Node.js] (http://nodejs.org/) is required in order to run the nw-workroom app, in addition to the following dependencies:

* body-parser (version 1.6.4)
* express (version 4.8.2)
* nedb (version 0.10.7)
* handlebars (version 2.0.0-beta.1)

License
---

Released under the GPL V3 License. Refer to the `LICENSE` file in the project's root directory.