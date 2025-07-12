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