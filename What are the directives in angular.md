# What are the directives in angular ?

Tags: Theory

## What Are Directives in Angular**:**

- Directives are angular syntaxes witch you can write inside html DOM
- directives help to attach behavior to the HTML DOM
- There are Three types of directives in angular
    - Structural Directives
    - Attribute Directives
    - Component Directives
- Examples: `*ngIf`, `*ngFor`, `*ngSwitch`, `ngStyle`, `ngClass`, and `ngModel`.

## **Structural Directives**:

- structural directives changes the structure of the DOM elements
- it adds or removes elements from HTML DOM based on certain conditions
- they are denoted by an asterisk (*) prefix in the Angular syntax
- examples: `*ngIf`, `*ngFor`, and `ngSwitch` `*ngSwitchCase`.

### Syntax:

```html
// *ngIf
<div *ngIf="obj.active">// text here</div>

// *ngFor
<div *ngFor="let user of users">
  <p>{{user.name}}</p>
</div>

// ngSwitch and *ngSwitchCase
<div [ngSwitch]="switch_expression">
  <div *ngSwitchCase="match_expression_1">// text here</div>
  <div *ngSwitchCase="match_expression_2">// text here</div>
  <div *ngSwitchDefault>// text here</div>
</div>
```

## **Attribute Directives**:

- attribute directives changes the appearance and behavior or look an feel of the existing HTML DOM
- They are applied to elements as attributes
- These directives allow you to modify the attributes or properties of elements, apply styles dynamically, or add custom behavior to elements.
- Examples: `ngStyle`, `ngClass`, and `ngModel`.

### Syntax:

```html
// ngClass
<div [ngClass]="{'activeClass': user.active}"></div>
<div [ngClass]="{'activeClass greenBg': user.active}"></div>
<div [ngClass]="{'activeClass': user.active, 'cirleClass': !user.active}"></div>
<div [class.sticky]="sticky"></div>

// ngStyle
<div [ngStyle]="{'width.px': widthExpresion}"></div>
<div [ngStyle]="{'font-style': styleExpresion ? 'areal' : 'open san'}"></div>
<div [ngStyle]="{'width': widthExpresion}"></div>

// ngModel directive or also called two way data binding
<input [(ngModel)]="value" value="" />
```

## **Component Directives**:

- Directives with template. its like a user control
- its a component its own UI and logics decorated with the @component decorator.
- Examples: `<app-about-me></app-about-me>`,`<app-contact></app-contact>`

### Syntax:

```html
<div>
  <app-box-background></app-box-background>
  <app-home [pageId]="navSky"></app-home>
</div>
```