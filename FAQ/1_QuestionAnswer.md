## 1. What is Angular?
Angular is a TypeScript-based open-source front-end platform developed by Google for building web, mobile, and desktop applications.

## 2. What are the key features introduced in Angular 18?
- Improved performance with the Ivy compiler
- Standalone components
- New control flow syntax
- Deferred loading
- Server-side rendering improvements
- Enhanced developer tooling

## 3. What is a component in Angular?
A component controls a portion of the UI (view) and consists of a template, styles, and a class that defines its behavior.

## 4. What is a module in Angular?
A module groups related components, directives, pipes, and services to form cohesive blocks of functionality.

## 5. Difference between Component and Module?
- Component: Controls a specific view.
- Module: Contains a collection of components, directives, and services.

## 6. What is data binding?
Data binding synchronizes data between the model and the view. Types include:
- Interpolation: `{{value}}`
- Property binding: `[property]="value"`
- Event binding: `(event)="handler()"`
- Two-way binding: `[(ngModel)]="value"`

## 7. What are directives?
Directives add behavior to DOM elements. Types:
- Structural (e.g., *ngIf, *ngFor)
- Attribute (e.g., ngClass, ngStyle)

## 8. What are pipes?
Pipes transform data in templates, such as formatting dates, numbers, or filtering arrays.

## 9. What is Dependency Injection (DI)?
DI is a design pattern that provides a way to supply dependencies (services) to components or classes.

## 10. What is the use of `ngOnInit()`?
It is a lifecycle hook that is called after Angular initializes the component’s data-bound properties.

## 11. Difference between constructor and `ngOnInit()`?
- Constructor: Instantiates the class.
- `ngOnInit()`: Performs component initialization after constructor and data-bound properties are set.

## 12. What are services in Angular?
Services hold reusable logic and business functionality which can be injected into components or other services.

## 13. What is the `async` pipe?
It subscribes to an Observable or Promise and returns the latest emitted value, handling unsubscribe automatically.

## 14. Difference between Promise and Observable?
- Promise emits a single value.
- Observable emits multiple values over time and offers operators like map and filter.

## 15. What is AOT (Ahead-of-Time) compilation?
AOT compiles the Angular app during the build process, improving performance and reducing runtime errors.

## 16. What is `NgZone`?
`NgZone` helps Angular run change detection only when necessary, optimizing performance.

## 17. What are guards in Angular?
Guards control navigation and protect routes. Types include:
- CanActivate
- CanDeactivate
- CanActivateChild
- CanLoad
- Resolve

## 18. What is lazy loading?
Lazy loading loads modules only when needed, reducing initial load time.

## 19. Difference between `ViewChild` and `ContentChild`?
- `ViewChild`: Access elements inside the component’s view.
- `ContentChild`: Access elements projected into the component.

## 20. What is `ngOnChanges()`?
Lifecycle hook called when input properties change, used to act on those changes.

## 21. Difference between `ngOnChanges()` and `ngDoCheck()`?
- `ngOnChanges()`: Called when data-bound input properties change.
- `ngDoCheck()`: Called during every change detection run.

## 22. What is change detection?
Change detection keeps the UI in sync with the model by checking for changes in the application state.

## 23. What is `ngTemplateOutlet`?
Directive to insert an `<ng-template>` dynamically into the DOM.

## 24. Difference between `@ViewChild()` and `@ViewChildren()`?
- `@ViewChild()`: Access a single child element/component.
- `@ViewChildren()`: Access multiple child elements/components.

## 25. What is `Renderer2`?
`Renderer2` is used for safe DOM manipulations across platforms like browsers and servers.