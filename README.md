
# NodeJS Information Repo

Created: 16.10.2021

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

---
## Tools to try:

- [npm-check](https://www.npmjs.com/package/npm-check)  

Check for outdated, incorrect, and unused dependencies.

- [undici](https://www.npmjs.com/package/undici)

A HTTP/1.1 client, written from scratch for Node.js.

- [ws](https://www.npmjs.com/package/ws)

`ws` is a simple to use, blazing fast, and thoroughly tested WebSocket client and server implementation.

- [pino](https://www.npmjs.com/package/pino)

Very low overhead Node.js logger.

- [fastify](https://www.npmjs.com/package/fastify)

 Fastify is a web framework highly focused on providing the best developer experience with the least overhead and a powerful plugin architecture. 
 
 
