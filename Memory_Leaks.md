## Memory Leaks can be caused by:

- References
  - Global variables
  - Multiple References
  - Singleton
- Closures / Scopes
  - Recursive closures
  - Require in the middle of code
  - Functions in loops
- OS and Language Objects
  - Descriptors: files, sockets...
  - setTimeout, setInterval
- Events / Subscription
  - EventEmitter
  - Callbacks
- Cache
  - Remove old values
  - Limit cache size
  - Remove rarely used values
- Mixins
  - Mixin to built-in Classes
  - Mixins to DOM
  - Mixins to process, console, require
- Concurrency
  - Processes
  - Threads
  - Workers

## Memory allocated to Nodejs process:

- C++ Code
- JavaScript Code
- Stack
- Heap
- External

Video: https://www.youtube.com/watch?v=0oZa64SB2wM&t=829s&ab_channel=TimurShemsedinov
