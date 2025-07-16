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
 