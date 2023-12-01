# Angular Interview Guide

Angular is a popular front-end framework for building dynamic web applications. This guide provides an overview of essential Angular concepts for interview preparation.

## 1. **Angular Basics**

### 1.1 Components

- **What is a component in Angular?**
  - A component is a basic building block in Angular that represents a part of the user interface. It consists of a template, class, and metadata.

- **How are components created in Angular?**
  - Components are created using the `@Component` decorator. This decorator includes metadata such as the selector, template, and styles.

### 1.2 Modules

- **Explain Angular modules.**
  - Angular modules are containers for organizing the application into cohesive blocks. They group related components, directives, services, and pipes.

- **What is the purpose of the `@NgModule` decorator?**
  - The `@NgModule` decorator is used to define a module in Angular. It takes metadata that determines how the module should be compiled and executed.

## 2. **Data Binding**

- **What is data binding in Angular?**
  - Data binding is a mechanism for coordinating the parts of a template with the parts of a component. It allows you to synchronize the model and the view.

- **Explain one-way data binding and two-way data binding.**
  - One-way data binding binds data from the component to the template (e.g., {{ data }}).
  - Two-way data binding uses the `[(ngModel)]` directive to bind data both from the component to the template and vice versa.

## 3. **Directives**

- **What are directives in Angular?**
  - Directives are instructions in the DOM that Angular transforms, updates, and deletes based on your application's logic.

- **Give examples of built-in Angular directives.**
  - Examples include `ngIf`, `ngFor`, and `ngSwitch`.

## 4. **Services**

- **What is an Angular service?**
  - An Angular service is a singleton object that provides methods for application-wide functionality. It can be injected into components and other services.

- **How is a service created in Angular?**
  - Services are created using the `@Injectable` decorator. The service class is then provided in the module.

## 5. **Dependency Injection**

- **What is dependency injection in Angular?**
  - Dependency injection is a design pattern where components and services request dependencies from a higher-level container rather than creating them directly.

- **How is dependency injection achieved in Angular?**
  - Angular uses its built-in dependency injection system. You can inject dependencies into a component or service constructor.

## 6. **Routing**

- **Explain Angular routing.**
  - Angular routing allows navigation between different components while maintaining the single-page application (SPA) feel.

- **How is routing configured in Angular?**
  - Routing is configured using the `RouterModule` and `Routes` in the Angular module.

## 7. **Lifecycle Hooks**

- **What are Angular lifecycle hooks?**
  - Lifecycle hooks are methods that provide visibility into the component lifecycle. Examples include `ngOnInit`, `ngOnChanges`, and `ngOnDestroy`.

- **Explain the purpose of the `ngOnInit` hook.**
  - The `ngOnInit` hook is used to perform initialization logic in a component after Angular has initialized the component's data-bound properties.

## 8. **Forms and Validations**

- **How do you handle forms in Angular?**
  - Angular provides both template-driven forms and reactive forms. Template-driven forms are driven by directives in the template, while reactive forms are more programmatically defined.

- **Explain Angular form validations.**
  - Angular offers built-in validators and the ability to create custom validators for form fields.

## 9. **Observables and HTTP Client**

- **What are Observables in Angular?**
  - Observables are a powerful feature used for handling asynchronous operations. Angular extensively uses observables, especially in the context of the HTTP client.

- **How do you make HTTP requests in Angular?**
  - Angular provides the `HttpClient` module for making HTTP requests. Observables are typically used to handle the asynchronous nature of HTTP operations.

## 10. **Unit Testing in Angular**

- **Why is unit testing important in Angular?**
  - Unit testing ensures that individual units of code (components, services) work as expected. Angular comes with a testing framework, and tools like Jasmine and Karma are commonly used.

- **How do you write unit tests for an Angular component?**
  - Tests are written using Jasmine syntax, and the Angular testing utilities facilitate component testing.

## Conclusion

This Angular interview guide covers fundamental concepts that are likely to be discussed during an Angular interview. Be prepared to demonstrate practical examples, share experiences, and discuss best practices related to Angular development.


# Angular Directives Explained

In Angular, directives are powerful features that allow you to extend the functionality of HTML elements. They provide a way to create reusable components, handle DOM manipulations, and enhance the behavior of elements on the page. Angular has several built-in directives, and you can also create custom directives to suit your application's specific needs.

## 1. Structural Directives

Structural directives manipulate the structure of the DOM by adding or removing elements based on conditions.

### 1.1. *ngIf

The `*ngIf` directive conditionally renders or removes an element based on the truthiness of an expression.

```html
<p *ngIf="isVisible">This paragraph is visible.</p>

```
### 1.2. *ngFor

The `*ngFor` directive is used for iterating over a collection (array) and rendering elements for each item.

```html
<ul>
  <li *ngFor="let item of items">{{ item }}</li>
</ul>

```

### 1.3. *ngSwitch

The `*ngSwitch` and `*ngSwitchCase` directives are used for conditional rendering based on multiple conditions.
html

```html
<div [ngSwitch]="value">
  <p *ngSwitchCase="'A'">Condition A</p>
  <p *ngSwitchCase="'B'">Condition B</p>
  <p *ngSwitchDefault>Default Condition</p>
</div>
```

## 2. Attribute Directives

- Attribute directives modify the appearance or behavior of an element.

### 2.1. *ngClass

The `*ngClass` directive dynamically adds or removes CSS classes based on the evaluation of expressions.

```html
<div [ngClass]="{ 'active': isActive, 'error': hasError }">Styled Div</div>
```
### 2.2. *ngStyle

The `*ngStyle` directive dynamically applies inline styles based on the evaluation of expressions.
```html
<div [ngStyle]="{ 'color': textColor, 'font-size.px': fontSize }">Styled Text</div>
```

### 2.3. *ngModel
The `*ngModel` directive is used for two-way data binding in forms. It binds the value of an input element to a variable in the component.
```html
<input [(ngModel)]="name" />
```

## 3. Custom Directives

- You can create custom directives to encapsulate and reuse behavior across different parts of your application.

### 3.1. Directive Definition

Define a directive using the @Directive decorator.

```javascript
import { Directive, ElementRef } from '@angular/core';

@Directive({
  selector: '[appCustomDirective]'
})
export class CustomDirective {
  constructor(private el: ElementRef) {
    el.nativeElement.style.backgroundColor = 'yellow';
  }
}

```

### 3.2. Using Custom Directive
Use the directive in your HTML by adding the selector as an attribute.

```html
<p appCustomDirective>Custom Directive Applied</p>
```

This will apply the defined behavior (changing background color to yellow) to the specified element.

Understanding and using directives effectively is crucial for building dynamic and interactive Angular applications. They provide a declarative way to manipulate the DOM and enhance the overall user experience.
