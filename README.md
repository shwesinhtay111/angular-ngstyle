ngStyle
==========
-allow to set many inline style of HTML element using an expression

-expression evaluated at run time and allow to dynamically change style of html element


ngSytle Syntax
==============

Syntax:

<element [ngStyle]="{'styleNames': styleExp}">...</element>

Example:

<some-element [ngStyle]="{'font-size': '20px'}">Set Font size to 20px</some-element>

=================================================================

Syntax:

<element [ngStyle]="{'styleName.unit': widthExp}">...</element>
 
Example:

<some-element[ngStyle]="{'font-size.em': '3'}">...</some-element>


Change Style Dynamically
========================

In component,

color: string= 'red'

In html template,

<input [(ngModel)]="color" />

<div [ngStyle]="{'color': color}">Change my color</div>

Ternary operator
==================

<div [ngStyle]="{'background-color':status === 'error' ? 'red' : 'blue' }"></<div>

ngStyle multiple attributes
===========================

<p [ngStyle]="{'color': 'purple',

               'font-size': '20px',
               
               'font-weight': 'bold'}">
               
     Multiple styles
     
</p>

Specifying CSS Units in ngStyle
===============================
<input [(ngModel)]="size" /> 

<div [ngStyle]="{'font-size.px': size}">Change my size</div>

Using object from Controller
================================
In Component,

class StyleClass {

   'color': string= 'blue';
   
   'font-size.px': number= 20;
   
   'font-weight': string= 'bold'; 
   
}


styleClass: StyleClass = new StyleClass();

In template,

<div [ngStyle]="styleClass">size & Color</div>


 

# NgstyleTest

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 9.0.4.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README
