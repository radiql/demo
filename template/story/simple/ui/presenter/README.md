# UI Presenters

UI Presenters contain the smart business logic that is independent of any 
particular view technology or platform.

Presenters are responsible for converting data from an Interactor in the form of
a domain model into a view model representation of the same data.

In other words, Presenters are responsible for bridging the impedance mismatch 
between the UI view model and the business data model (used by Interactors) 
for data supplied to the UI Tier from the Business Logic Tier of an application.

Please note that the view model (used by the UI Tier) and the business domain
model (used by the Business Logic Tier) may be very similar but are likely to
be different. Sometimes these differences are subtle. But often the two models
will diverge over time.

# Autogeneration of Controllers

RADiQL can automatically generate presenters for a particular style of UI
and HTTP data transport protocol. For example:

- React-Redux over REST
- React-Apollo over GraphQL
- React-RADiQL over websockets 

# RADiQL ReduxLink

This is middleware for Redux

# RADiQL ApolloLink

This is an Apollo Link for RADiQL

## Implementations

UI Presenters can be compiled into a form that is executable on a target 
platform. For example:

- A UI Presenter for a web browser can be written in Javascript, Typescript, 
Coffeescript of any other language that can be transpiled to Javascript. 
- A UI Presenter for a web browser can be written in C, C++, C#, Go, Rust, 
Python, Elixr or any other language that can be transpiled to WASM (WebAssembly)
- A UI Presenter may be written in any compatible language for a target platform.


