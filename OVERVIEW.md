
## Quick Node.js Overview

Node.js fully embraces the **Continuation-Passing Style (CPS)** pattern throughout its internal modules by way of **callbacks** — functions
that are passed around and invoked by the event loop once a task is complete. In Node.js, functions that are invoked in the future
with a new stack are said to be run **asynchronously**. Conversely, when one function calls another function in the same stack,
that code is said to run **synchronously**.

Node.js itself is **multithreaded**. The lower levels of Node.js are written in C++.
This includes third-party tools like libuv, which handles operating system abstractions and I/O,
as well as V8 (the JavaScript engine) and other third-party modules. The layer above that,
the Node.js binding layer, also contains a bit of C++. It’s only the highest layers of Node.js that are written in
JavaScript, such as parts of the Node.js APIs that deal directly with objects provided by userland.

More in the book: Distributed Systems with Node.js
