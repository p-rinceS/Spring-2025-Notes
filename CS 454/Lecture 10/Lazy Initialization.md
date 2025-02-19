
Singleton object needs to be initialized
- E.g., Configuration file needs to be parsed and made available


But we want to be lazy
- Most executions don't need that object
- Building that object takes a non-trivial amount of time.


Components are designed to perform initialization tasks when they are first called rather than when they are first created, Lazy concurrent initialization ensures that this initialization only occurs ONCE even when multiple threads may attempt the initialization.


