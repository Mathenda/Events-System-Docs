# How to use NX

[NX](https://nx.dev/) is a suite of powerful, extensible dev tools to help you architect, test, and build at any scale — integrating seamlessly with modern technologies and libraries while providing a robust CLI, caching, dependency management, and more.

## NX Console

NX Console is a VS Code plugin that provides a UI for NX commands. This means you can create components, serve your application, run tests, and more, all from the comfort of your code editor.

### Generating New Pages

To generate a new page using NX Console:

1. Open NX Console in VS Code. You can do this by clicking on the NX icon in the Activity Bar on the side of VS Code.
2. Click on the `Generate` button in the NX Console sidebar.
3. In the `Select Schematic` dropdown 
   - Search for `component`
   - Select `@nx/angular:component`.
4. Fill in the required fields such as `name`.
5. in the Directory Field, enter `src/<component-name>/`.
6. make sure `standalone` is selected.
7. Click `Generate` to generate your new component.
#### using a generated Page
1. Navigate to the folder of the page you wish to add the component to.
2. Navigate to 
```typescript 
`app.routes.ts`
```
3. import the component 
```typescript 
import { <NewComponent> } from 'src/<ComponentName>/<ComponentName>.component';.
```     
4. within appRoutes, add a path to the component eg. 
```typescript
`{ path: 'component', component: <NewComponent> },`.
```
5. to route to the page, use routerLink
```html 
`<button class="btn btn-primary" routerLink="/component"></button>`
```


### Generating New Components

To generate a new component using NX Console:

1. Open NX Console in VS Code. You can do this by clicking on the NX icon in the Activity Bar on the side of VS Code.
2. Click on the `Generate` button in the NX Console sidebar.
3. In the `Select Schematic` dropdown 
   - Search for `component`
   - Select `@nx/angular:component`.
4. Fill in the required fields such as `name`.
5. in the Directory Field, enter `src/Components/<component-name>/`.
6. make sure `standalone` is selected.
7. Click `Generate` to generate your new component.

#### using a generated Component
1. Navigate to the folder of the page you wish to add the component to.
2. Navigate to 
```typescript 
`<intended-page>.component.ts`
```
3. import the component 
```typescript 
import { <NewComponent> } from '../Components/<ComponentName>/<ComponentName>.component';.
```     
4. add the new import to the imports eg. 
```typescript
`  imports: [CommonModule, RouterModule, <NewComponent>],`.
```
5. Navigate to 
```typescript 
`<intended-page>.component.html`
```
6. add the component using the components selector (found in the components .ts file labelled as 
7. ` selector: 'app-<component-name>'`) eg. 
```html
   <app-ComponentName></app-ComponentName>
```
### Serving Your Application
To serve your application using NX Console:

1. Open NX Console in VS Code.
2. Click on the `Serve` button in the NX Console sidebar.
3. In the `Project to run` dropdown, select `Events system`.
4. Click `Execute: nx run Events-system:serve` to serve your application.

### Running Tests

To run tests using NX Console:

1. Open NX Console in VS Code.
2. Click on the `Test` button in the NX Console sidebar.
3. In the `Project to test` dropdown, select `Events system`.
4. Click `Execute: nx run Events-system:test` to test your application.

### Linting

To run tests using NX Console:

1. Open NX Console in VS Code.
2. Click on the `lint` button in the NX Console sidebar.
3. In the `Project to lint` dropdown, select `Events system`.
4. Click `Execute: nx run Events-system:lint` to test your application.

By using NX and the NX Console, you can streamline your development process and focus more on writing code rather than running commands.