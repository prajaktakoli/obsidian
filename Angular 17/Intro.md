- Component
-  ✅ **What is a Component in Angular?**

A **component** is the fundamental building block of an Angular application, responsible for:
- **Controlling a section of the UI** (via its template).
- **Handling logic and data** via a TypeScript class.
- **Applying metadata** using the `@Component` decorator.
---

### ✅ **Key Parts of a Component**


`@Component({   selector: 'app-user',   templateUrl: './user.component.html',   styleUrls: ['./user.component.css'] }) export class UserComponent {   name = 'Prajakta'; }`

- `selector`: HTML tag used to embed the component.
- `templateUrl`: Path to the HTML file for the component's UI.
- `styleUrls`: CSS styles for that component.
- `class`: Contains data & methods (business logic).
---

🔸 Interview One-Liner

**"A component in Angular is a TypeScript class with a template and metadata that defines a part of the UI and its behavior."**

----------------------
Interpolation
https://chatgpt.com/share/687237b0-5784-8007-9189-12aaf26b8b5d

| Part                     | Description                                           |
| ------------------------ | ----------------------------------------------------- |
| **Component**            | Building blocks of UI (HTML + CSS + TS)               |
| **Template**             | HTML + Angular syntax (dynamic HTML rendering)        |
| **Module**               | Groups components, services into functional units     |
| **Service**              | Business logic (reusable across components)           |
| **Dependency Injection** | Manages creation of services and injects where needed |
| **Router**               | Manages navigation between views                      |
| **Directive**            | Changes DOM structure or appearance                   |
| **Pipe**                 | Transforms data in templates (e.g., date formatting)  |
| **HttpClient**           | Communicates with APIs                                |
Steps:
npm install -g @angular/cli
ng new my-first-app
cd my-first-app
ng serve
ng new app-name              # Create new Angular app
ng serve                     # Run app locally (localhost:4200)
ng generate component myComp # Create component (auto updates module)
ng generate service myService # Create service
ng build                     # Build app for production

Angular CLI is a command-line interface that automates project setup, building, testing, and code generation tasks.

### What’s inside `app.module.ts`?

**A:** It’s the root module that imports components, services, and other modules. It defines the bootstrap component of the app

### What’s the role of `angular.json`?

**A:** It configures how Angular builds your app (entry files, assets, output paths, styles/scripts).

### What happens when you run `ng serve`?

**A:** Angular compiles your app, starts a local development server, and hot-reloads the browser on changes.

### 
What is the `main.ts` file?

**A:** It’s the entry point of the Angular app — it bootstraps `AppModule` and launches the app.

Component:
- A **component** controls a **part of the screen (UI)**.
- It has:
    - a **TypeScript class** (business logic),
    - a **template** (HTML),
    - and optional **CSS styles**.
- Components are **reusable and modular**.
- ✔ `@Component` decorator tells Angular this is a component.  
✔ `selector` is used to insert the component into HTML (`<app-welcome></app-welcome>`).

| Lifecycle Hook            | Purpose                                                                                                                           |
| ------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| `ngOnChanges()`           | Called when **@Input()** values change (before ngOnInit). Good for reacting to input changes.                                     |
| `ngOnInit()`              | Called once when component is initialized. Best place to fetch **API data**, set default values.                                  |
| `ngDoCheck()`             | Called during **every change detection**. Used for custom change detection if needed (rarely used).                               |
| `ngAfterContentInit()`    | Called after Angular projects external content into the component (`<ng-content>`).                                               |
| `ngAfterContentChecked()` | Called after every check of projected content.                                                                                    |
| `ngAfterViewInit()`       | Called after component’s view and child views are fully initialized. Good for **DOM queries** (`@ViewChild`).                     |
| `ngAfterViewChecked()`    | Called after every check of the component's view.                                                                                 |
| `ngOnDestroy()`           | Called just before the component is destroyed. Best place to **unsubscribe** observables, **clear timers** to avoid memory leaks. |

@Input:
- **@Input()** is used to **pass data** from **Parent → Child** component.
    
- Child component **receives** the value.
- // parent.component.html
<app-child [childMessage]="parentMessage"></app-child>
// parent.component.ts
parentMessage = 'Hello from Parent!';
// child.component.ts
import { Component, Input } from '@angular/core';

@Component({
  selector: 'app-child',
  template: `<p>{{ childMessage }}</p>`
})
export class ChildComponent {
  @Input() childMessage: string = '';
}


@Output:
- **@Output()** is used to **send data or events** from **Child → Parent** component.
- Child component **emits** an event and parent **listens** to it.

// child.component.ts
import { Component, Output, EventEmitter } from '@angular/core';

@Component({
  selector: 'app-child',
  template: `<button (click)="sendMessage()">Send to Parent</button>`
})
export class ChildComponent {
  @Output() messageEvent = new EventEmitter<string>();

  sendMessage() {
    this.messageEvent.emit('Hello Parent!');
  }
}

// parent.component.html
<app-child (messageEvent)="receiveMessage($event)"></app-child>
<p>{{ receivedMessage }}</p>

// parent.component.ts
receivedMessage: string = '';

receiveMessage(msg: string) {
  this.receivedMessage = msg;
}

**How it works:**

- Clicking the button in the child **emits an event** carrying a string.
- The parent **catches the event** and updates its `receivedMessage`.

Data Binding means **connecting data** between the **Component (TypeScript)** and the **Template (HTML)**.

----------------------------------


| Type              | Syntax                   | Purpose                                                       |
|-------------------|---------------------------|----------------------------------------------------------------|
| Interpolation     | `{{ }}`                   | Display data from component to template.                       |
| Property Binding  | `[property]="value"`      | Bind DOM properties (like `src`, `href`) to component data.    |
| Event Binding     | `(event)="handler()"`     | Bind DOM events (like `click`) to component methods.           |
| Two-way Binding   | `[(ngModel)]="property"`  | Sync data between template and component both ways.            |



