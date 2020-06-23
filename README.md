# sample-service-locator
This app was built following AndroidDevelopers Codelabs. The app demonstrates use of service locator pattern as an <b>alternative dependency injection.</b>


## What is the service locator?
+ The service locator design pattern improves decoupling of classes from concrete dependencies. 

+ You create a class known as the service locator. The ServiceLocator creates and stores dependencies that are obtained on demand by the classes that need it. 

+ Think of it as a <b>container of dependencies</b> that is attached to the app's lifecycle as it'll <b>get destroyed when the app does.</b>

+ A container is a class which is in charge of providing dependencies in your codebase and knows how to create instances of other types of your app. It manages the graph of dependencies required to provide those instances by creating them and <b>managing their lifecycle</b>.

+ A container exposes methods to get instances of the types it provides. Those methods can always return a different instance or the same instance. If the method always provides the same instance, we say that the type is <b>scoped to the container.</b>

+ The service locator pattern is different from dependency injection in the way the elements are consumed. With the service locator pattern, <b>classes have control and ask for objects to be injected;</b> with dependency injection, the app has control and proactively injects the required objects.

## Compared to dependency injection:
+ The collection of dependencies required by a service locator makes code harder to test because all the tests have to interact with the same global service locator.

+ Dependencies are encoded in the class implementation, not in the API surface. As a result, it's <b>harder</b> to know what a class needs from the outside. As a result, changes to the dependencies available in the service locator might result in <b>runtime or test failures</b> by causing references to fail.

+ Managing lifetimes of objects is more <b>difficult if you want to scope</b> to anything other than the lifetime of the entire app.

+ Service Locators start with relatively little boilerplate code, but also <b>scale poorly</b>. 

## License
Copyright 2019 Google, Inc (all resources are from Codelabs Google Developers).
