# Angular Interview Questions and Answers

> **Updated for Angular 17+** — Simple, clear, and memorable explanations to help you ace your next interview.

---

##  **1. What is Angular?**
Angular is a TypeScript-based web framework by Google for building single-page applications (SPAs). It offers two-way data binding, modular architecture, and reactive forms.

---

##  **2. What are the main building blocks of Angular?**
- **Modules** — organize the app into functional units.  
- **Components** — define UI and logic.  
- **Templates** — define the view (HTML).  
- **Services** — reusable business logic.  
- **Directives & Pipes** — modify DOM and data view.

---

##  **3. What is a Component in Angular?**
A component controls a part of the screen (view) with:
- An HTML template
- A TypeScript class
- A CSS style file
It’s the heart of any Angular app.

---

##  **4. What is a Module (`NgModule`)?**
A module groups related components, directives, and services.  
The root module is usually `AppModule`.

---

##  **5. What is Data Binding?**
Data Binding connects HTML and TypeScript.  
Types:
1. **Interpolation** → `{{value}}`
2. **Property Binding** → `[property]="value"`
3. **Event Binding** → `(event)="handler()"`
4. **Two-way Binding** → `[(ngModel)]="value"`

---

##  **6. What is Two-Way Data Binding?**
It syncs data between the model and view in real-time using `[(ngModel)]`.

---

##  **7. What are Directives?**
Directives are instructions for the DOM.
- **Structural** (`*ngIf`, `*ngFor`)
- **Attribute** (`[ngClass]`, `[ngStyle]`)
- **Custom** (user-defined)

---

##  **8. What are Pipes?**
Pipes transform displayed data — e.g., `{{price | currency:'USD'}}`.

---

##  **9. What is Dependency Injection (DI)?**
DI provides required objects (services) automatically instead of manually creating them — improves modularity.

---

##  **10. What are Services?**
Services contain reusable business logic shared across components.

---

##  **11. Difference between AngularJS and Angular?**
| AngularJS | Angular |
|------------|----------|
| JS-based | TypeScript-based |
| MVC pattern | Component-based |
| Dirty checking | Reactive change detection |

---

##  **12. What is RxJS?**
RxJS (Reactive Extensions for JS) handles asynchronous data streams using Observables.

---

##  **13. What is an Observable?**
An Observable emits data over time. You can **subscribe** to receive updates and **unsubscribe** to stop listening.

---

##  **14. What is a Subject in RxJS?**
A Subject is both an **Observable** and an **Observer** — allows multicasting (multiple subscribers).

---

##  **15. What is Change Detection?**
Angular tracks component data and updates the DOM automatically when data changes.

---

##  **16. What is a Template?**
A template defines the HTML structure linked to a component.

---

##  **17. What is a Decorator in Angular?**
Decorators add metadata — like:
- `@Component`
- `@NgModule`
- `@Injectable`
- `@Input`, `@Output`

---

##  **18. What is @Input and @Output?**
- **@Input** — receive data from parent.  
- **@Output** — send events to parent.

---

##  **19. What is ngOnInit()?**
A lifecycle hook that runs once after component initialization — best for fetching data or setup logic.

---

##  **20. List Angular Lifecycle Hooks**
1. `ngOnChanges`
2. `ngOnInit`
3. `ngDoCheck`
4. `ngAfterContentInit`
5. `ngAfterContentChecked`
6. `ngAfterViewInit`
7. `ngAfterViewChecked`
8. `ngOnDestroy`

---

##  **21. What is Routing in Angular?**
Routing lets you navigate between views or components using the `RouterModule`.

---

##  **22. How to set up routing?**
```ts
const routes: Routes = [
  { path: 'home', component: HomeComponent },
];
@NgModule({ imports: [RouterModule.forRoot(routes)] })
export class AppRoutingModule {}
````

---

##  **23. What is Lazy Loading?**

Loading feature modules **only when needed**, improving performance.

---

##  **24. What is Preloading Strategy?**

Preloads lazy-loaded modules **after app load** for faster next navigation.

---

##  **25. What is Angular CLI?**

A command-line tool to create, build, test, and deploy Angular apps.
Example:
`ng new app-name`, `ng serve`, `ng build`

---

##  **26. What are Guards in Angular?**

Guards protect routes:

* `CanActivate`
* `CanDeactivate`
* `CanLoad`
* `Resolve`
* `CanActivateChild`

---

##  **27. What is CanActivate?**

Prevents unauthorized users from accessing routes.

---

##  **28. What is ngOnDestroy()?**

Lifecycle hook to clean up subscriptions or timers before component destruction.

---

##  **29. What is AOT Compilation?**

Ahead-Of-Time compiles HTML and TypeScript before the browser loads the app → faster startup.

---

##  **30. What is JIT Compilation?**

Just-In-Time compiles in the browser during runtime — useful for development.

---

##  **31. What is Ivy Engine?**

Ivy is Angular’s rendering engine improving speed, debugging, and bundle size.

---

##  **32. What is Zone.js?**

Zone.js tracks asynchronous operations to trigger change detection automatically.

---

##  **33. What are Reactive Forms?**

Forms managed using TypeScript code and Observables.

```ts
this.form = new FormGroup({
  name: new FormControl(''),
});
```

---

##  **34. What are Template-driven Forms?**

Forms created in HTML using directives like `[(ngModel)]`.

---

##  **35. Reactive vs Template-driven Forms**

| Reactive         | Template-driven |
| ---------------- | --------------- |
| Code-driven      | HTML-driven     |
| Scalable         | Simple          |
| Synchronous data | Two-way binding |

---

##  **36. What is ngModel?**

Directive for two-way data binding in template-driven forms.

---

##  **37. What is FormBuilder?**

A helper service to create forms easily:

```ts
this.form = this.fb.group({ name: [''] });
```

---

##  **38. What is FormGroup and FormControl?**

* **FormControl** → represents a single input.
* **FormGroup** → collection of FormControls.

---

##  **39. What is EventEmitter?**

Used with `@Output()` to emit custom events from a child component.

---

##  **40. What is ViewChild?**

`@ViewChild` accesses child components, DOM elements, or directives from the parent.

---

##  **41. What is RouterOutlet?**

Placeholder in the template where routed components are displayed.

---

##  **42. What is RouterLink?**

Directive to navigate between routes:
`<a routerLink="/home">Home</a>`

---

##  **43. What is State Management?**

Technique to manage shared app data — often done using **NgRx** or **RxJS BehaviorSubjects**.

---

##  **44. What is NgRx?**

A reactive state management library using Redux pattern — helps manage large-scale app states.

---

##  **45. What is BehaviorSubject?**

An RxJS Subject that holds a current value and emits it to new subscribers.

---

##  **46. What are Interceptors?**

Used in HTTP to modify requests or responses globally (e.g., add headers or handle errors).

---

##  **47. What is HttpClient?**

Angular’s service to make HTTP requests easily (GET, POST, PUT, DELETE).

---

##  **48. What is async pipe?**

Automatically subscribes to Observables and unsubscribes on destroy:
`{{ data$ | async }}`

---

##  **49. What is ng-content?**

Used for **content projection** — embedding dynamic HTML into components.

---

##  **50. What is ng-template?**

A template that isn’t rendered until explicitly used with `*ngIf` or `ngTemplateOutlet`.

---

##  **51. What is ng-container?**

A logical container that doesn’t render an actual DOM element — helps group structural directives.

---

##  **52. What is Renderer2?**

Used for safe DOM manipulations without direct access to the browser API.

---

##  **53. What is ViewEncapsulation?**

Controls how component styles are scoped.

* `Emulated` (default)
* `ShadowDom`
* `None`

---

##  **54. What are Structural Directives?**

Directives that change DOM structure — e.g. `*ngIf`, `*ngFor`.

---

##  **55. What is ngFor TrackBy?**

Improves performance by uniquely identifying list items:
`*ngFor="let item of items; trackBy: trackByFn"`

---

##  **56. What is Async/Await in Angular?**

Used with Promises to handle asynchronous code more cleanly.

---

##  **57. Difference between Promise and Observable**

| Promise         | Observable      |
| --------------- | --------------- |
| Single value    | Multiple values |
| Eager           | Lazy            |
| Not cancellable | Cancellable     |

---

##  **58. What is the difference between Subject and BehaviorSubject?**

BehaviorSubject stores the **latest value** and emits it to new subscribers, while Subject does not.

---

##  **59. What is RouterModule.forRoot() vs forChild()?**

* `forRoot()` → main app routing.
* `forChild()` → feature module routing.

---

##  **60. What are Custom Pipes?**

User-defined pipes to transform data:

```ts
@Pipe({name: 'capitalize'})
transform(value: string) { return value.toUpperCase(); }
```

---

##  **61. What is Dynamic Component Loading?**

Creating components at runtime using `ViewContainerRef` and `ComponentFactoryResolver`.

---

##  **62. What is ChangeDetectorRef?**

Used to manually trigger or control change detection.

---

##  **63. What is Pure vs Impure Pipe?**

* **Pure** → executes only when input changes.
* **Impure** → executes on every change detection.

---

##  **64. What is the purpose of package.json?**

It holds dependencies, scripts, and project metadata.

---

##  **65. What is tsconfig.json?**

TypeScript configuration file defining compiler options and paths.

---

##  **66. What is polyfills.ts?**

Provides browser compatibility for older browsers.

---

##  **67. What is environment.ts?**

Holds app configuration for dev or prod environments.

---

##  **68. What is index.html?**

Main entry HTML file for Angular apps — bootstraps the root component.

---

##  **69. What is main.ts?**

Bootstraps the root Angular module using `platformBrowserDynamic().bootstrapModule(AppModule)`.

---

##  **70. What is AppModule?**

Root module that declares components and imports other modules.

---

##  **71. What is Schematics in Angular CLI?**

Blueprints used by CLI to generate files like components, services, modules, etc.

---

##  **72. What are Angular Animations?**

Animations built using Angular’s API (`@angular/animations`) for smooth transitions.

---

##  **73. What is Renderer2 vs ElementRef?**

* `Renderer2` is safer for DOM operations.
* `ElementRef` directly accesses DOM (avoid when possible).

---

##  **74. What is Zone-less Angular?**

Upcoming approach removing Zone.js, allowing manual control of change detection (Angular 18+ direction).

---

##  **75. What are Standalone Components?**

Introduced in Angular 14 — components that don’t require a module.

---

##  **76. What is Signals (Angular 17)?**

Signals are reactive primitives for state management — a simpler alternative to Observables.

---

##  **77. What is SSR (Server-Side Rendering)?**

Pre-renders the app on the server using **Angular Universal** for faster load and SEO.

---

##  **78. What is Angular Universal?**

Tool for enabling server-side rendering in Angular apps.

---

##  **79. What is Differential Loading?**

Builds modern and legacy bundles for different browsers automatically.

---

##  **80. What is ViewEngine vs Ivy?**

* **ViewEngine** → older rendering engine.
* **Ivy** → newer, faster, modular.

---

##  **81. What is PWA in Angular?**

Progressive Web App — adds offline support, installability, and caching.

---

##  **82. What is Service Worker?**

Script that runs in the background to enable offline support.

---

##  **83. What is RendererFactory2?**

Used internally to create instances of Renderer2.

---

##  **84. What is HostListener?**

Listens to DOM events directly inside a component.

---

##  **85. What is HostBinding?**

Binds class or style properties to host element.

---

##  **86. What is ngZone.run()?**

Executes code inside Angular’s zone to trigger change detection.

---

##  **87. What is APP_INITIALIZER?**

A function that runs before app startup — useful for loading configs.

---

##  **88. What is Ahead-of-Time (AOT) advantage?**

* Faster rendering
* Fewer runtime errors
* Smaller bundle size

---

##  **89. What is Webpack’s role in Angular?**

Bundles all scripts, assets, and modules for production.

---

##  **90. What are Validators in Angular Forms?**

Used to enforce input rules:

```ts
Validators.required, Validators.minLength(5)
```

---

##  **91. What is Custom Validator?**

User-defined rule for form validation:

```ts
function noSpace(control: FormControl) { ... }
```

---

##  **92. What is Resolve Guard?**

Pre-fetches data before loading a route.

---

##  **93. What is the difference between ngIf and hidden?**

* `*ngIf` removes the element from DOM.
* `[hidden]` just hides it via CSS.

---

##  **94. What are lifecycle hooks in directives?**

Same as components (`ngOnInit`, `ngOnDestroy`, etc.)

---

##  **95. What is Incremental DOM?**

Rendering strategy in Ivy that updates only changed nodes for better performance.

---

##  **96. What is Micro Frontend in Angular?**

Splitting an app into smaller, independently deployable frontends.

---

##  **97. What is TestBed in Angular Testing?**

Utility to configure and test components in isolation.

---

##  **98. What is Karma?**

Default test runner for Angular unit tests.

---

##  **99. What is Protractor?**

(Deprecated) End-to-end testing tool, replaced by **Cypress** or **Playwright**.

---

##  **100. What is the Future of Angular?**

Angular 18+ is focusing on **signals, zone-less architecture**, **simpler reactivity**, and **better performance** — making it even more developer-friendly.

---

**Conclusion**

Angular remains one of the most powerful frameworks for building scalable and reactive frontends.
Master these 100 questions, and you’ll stand out in any interview with both clarity and confidence.

---