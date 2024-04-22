# Minimal Express + Handlebars Template

## Changelog
### **v0.1.0**
- The first iteration of this template come directly from the recommendations an references found on the MDN Express Tutorial.
- Initial setup was done with `bun init -y` because Bun is way faster than Node and almost fully compatible with it.
- Development middleware, plugins and the base Model-View-Controller structure was generated with `bunx express-generator --no-view`
  - `morgan` is the request logger. In this case is used with the predefined `dev` format which, as its name implies, is tuned for development.
  - `debug` is the application logger for the specified modules and variables.
  - `cookie-parser` parses `Cookie` header and populates `req.cookies` with an object keyed by the cookie names.
- The remaining libraries were obtained from the MDN Express Tutorial with the exception of `http-errors` that I found navigating the internet. The use of this last one is very specific: simplify the creation of HTTP response errors by the specifying the status code.
- The `Handlebars` modules are standard for a working and functional Handlebars-powered application. You need the `allow-prototype-access` plugin to access properties on complex objects when it comes to `Handlebars` and the `handlebars-helpers` are a public library with fairly common helpers to avoid writing them yourself.

See `package.json` to check all the dependencies.
