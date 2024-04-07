
# NodeJS

[Official NodeJS Getting Started](https://nodejs.org/en/learn/getting-started/introduction-to-nodejs) | [Official NodeJS Guides](https://nodejs.org/en/docs/guides/) | [Official NodeJS Docs](https://nodejs.org/dist/latest-v16.x/docs/api/)

[Mixu's Node book](https://book.mixu.net/node/single.html)

The basic philosophy of node.js is:
- Non-blocking I/O - every I/O call must take a callback, whether it is to retrieve information from disk, network or another process.
- Built-in support for the most important protocols (HTTP, DNS, TLS)
- Low-level. Do not remove functionality present at the POSIX layer. For example, support half-closed TCP connections.
- Stream everything; never force the buffering of data.

Node.js is different from client-side Javascript in that it removes certain things,
like DOM manipulation, and adds support for evented I/O, processes, streams, HTTP, SSL, DNS, string and buffer processing and C/C++ addons.

### Event Loop

The event loop is a mechanism which allows you to specify what happens when a particular event occurs.
You can think of the event loop as a simple list of tasks (code) bound to events.
When an event happens, the code/task associated with that event is executed.

Remember that all of your code in Node is running in a single process.
There is no parallel execution of Javascript code that you write - you can only be running a single piece of code at any time.

If you have a CPU-intensive task that takes four seconds to complete, then a Node server would not be able to respond to other requests during those four seconds,
since the event loop is only checked for new tasks once your code finishes.

Even with a single process model, you can move CPU-intensive work to other background processes,
for example by setting up a queue which is processed by a pool of workers, or by load balancing over multiple processes.
If you are performing CPU-bound work, then the only real solutions are to either figure out a better algorithm (to use less CPU)
or to scale to multiple cores and multiple machines (to get more CPU's working on the problem).

## NodeJS Tools:

- [nvm](https://github.com/nvm-sh/nvm#intro) - allows you to quickly install and use different versions of node via the command line.
- [npm-check-updates](https://www.npmjs.com/package/npm-check-updates) - upgrades your `package.json` dependencies to the latest versions, ignoring specified versions.
- [more tools...](https://github.com/stepanenko/nodejs-info/blob/master/TOOLS.md#tools-to-try)

## Antipatterns:

Mixin, middleware, reference pollution, prototype pollution

## Vulnerabilities:

- Routing: ReDOS, Path traversal. Don't parse URLs by RegExp, instead search URL endpoints in collection (Map - hash map)
- XSS, SQLI, XSRF. Learn CSP (Content Security Policy)
- Use `npm audit`, snyk, Github Security Alert



