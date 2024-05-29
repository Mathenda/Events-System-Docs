# Frontend Coding Standards

The section serves as a way to set the standard for the codebase. It is important to have a consistent codebase to make it easier for developers to read and understand the code.

## Angular
project structure the frontend  will use

```bash

└─ Events-system
   ├─ .vscode
   │  └─ extensions.json
   ├─ e2e
   │  ├─ ...
   │  └─ src
   │     └─ example.spec.ts
   │  
   ├─ src
   │  ├─ app
   │  │  ├─ app.component.css
   │  │  ├─ app.component.html
   │  │  ├─ app.component.spec.ts
   │  │  ├─ app.component.ts
   │  │  ├─ app.config.ts
   │  │  └─ app.routes.ts
   │  │  
   │  ├─ assets
   │  ├─ Components
   │  ├─ home
   │  │  ├─ home.component.css
   │  │  ├─ home.component.html
   │  │  ├─ home.component.spec.ts
   │  │  └─ home.component.ts
   │  │  
   │  ├─ index.html
   │  ├─ main.ts
   │  ├─ styles.css
   │  └─ test-setup.ts
   │
   ├─ jest.config.ts
   ├─ jest.preset.js
   ├─ nx.json
   ├─ package-lock.json
   ├─ package.json
   ├─ project.json
   ├─ README.md
   ├─ tsconfig.app.json
   ├─ tsconfig.editor.json
   ├─ tsconfig.json
   └─ tsconfig.spec.json

```
## Components

- Use `PascalCase` for component names.
- Use a noun or noun phrase that describes the component's purpose.
- Append the word "Component" at the end.

**Example:** `UserProfileComponent`

## Variables and Properties

- Use `camelCase` for variable and property names.
- Use descriptive names that reflect their purpose.

**Example:** `loggedInUser`

## Methods and Functions

- Use `camelCase` for method and function names.
- Use descriptive names that reflect their action or purpose.

**Example:** `getUserProfile`

## HTML Templates

- Use `kebab-case` for HTML element selectors and attribute names.
- Use descriptive names that reflect the purpose of the element or attribute.

**Example:** `<app-user-profile></app-user-profile>`

## Indentation

- Use consistent indentation with four spaces or tabs.
- Indent code blocks, such as components, services, and modules.

**Example:**

```typescript
@Component({
    selector: 'app-example',
    templateUrl: './example.component.html',
    styleUrls: ['./example.component.css']
})
export class ExampleComponent implements OnInit {
    // ...
}

```

## CSS Styles (only when necessary)

- Use consistent indentation and formatting in CSS/SCSS files.
- Organize styles logically and group related properties together.
- Use comments to describe sections or important styles.

**Example:**

```css
.user-profile {
    font-size: 16px;
    color: #333;

    .name {
        font-weight: bold;
    }
}
```