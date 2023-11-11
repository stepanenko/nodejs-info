
# NodeJS

The basic philosophy of node.js is:
- Non-blocking I/O - every I/O call must take a callback, whether it is to retrieve information from disk, network or another process.
- Built-in support for the most important protocols (HTTP, DNS, TLS)
- Low-level. Do not remove functionality present at the POSIX layer. For example, support half-closed TCP connections.
- Stream everything; never force the buffering of data.

Node.js is different from client-side Javascript in that it removes certain things,
like DOM manipulation, and adds support for evented I/O, processes, streams, HTTP, SSL, DNS, string and buffer processing and C/C++ addons.

[Official NodeJS Getting Started](https://nodejs.dev/learn) | [Official NodeJS Guides](https://nodejs.org/en/docs/guides/) | [Official NodeJS Docs](https://nodejs.org/dist/latest-v16.x/docs/api/) | [Mixu's Node book](https://book.mixu.net/node/single.html)

## Useful NodeJS tools:

- [nvm](https://github.com/nvm-sh/nvm#intro)

`nvm` allows you to quickly install and use different versions of node via the command line. It is a version manager for **node.js**, designed to be installed per-user, and invoked per-shell. `nvm` works on any POSIX-compliant shell (sh, dash, ksh, zsh, bash), in particular on these platforms: unix, macOS, and windows WSL.

---
- [npm-check-updates](https://www.npmjs.com/package/npm-check-updates)

Upgrades your `package.json` dependencies to the latest versions, ignoring specified versions.  
Only modifies `package.json` file. Run `npm install` to update your installed packages and `package-lock.json`.  

- `npm install -g npm-check-updates` - install ncu globally
- `ncu -u` updates `package.json` (if ommited displays old packages that could be updated)
- `ncu -x "package_to_not_update" -u` - upgrade `package.json` (omit packages following the `-x` flag)
- `npx npm-check-updates -u` - run with npx (without a global install)

### [Tools to try...](https://github.com/stepanenko/nodejs-info/blob/master/TOOLS.md#tools-to-try)

## Antipatterns:

Mixin, middleware, reference pollution, prototype pollution

## Vulnerabilities:

- Routing: ReDOS, Path traversal. Don't parse URLs by RegExp, instead search URL endpoints in collection (Map - hash map)
- XSS, SQLI, XSRF. Learn CSP (Content Security Policy)
- Use `npm audit`, snyk, Github Security Alert



