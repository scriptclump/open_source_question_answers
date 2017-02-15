# AngularJs

AngularJS is a very powerful JavaScript Framework. It is used in Single Page Application (SPA) projects. It extends HTML DOM with additional attributes and makes it more responsive to user actions.

***Advantages of AngularJS***

- Provides capability to create Single Page Application in a very clean and maintainable way.
- Provides data binding capability to HTML thus giving user a rich and responsive experience
- AngularJS code is unit testable.
- AngularJS uses dependency injection and make use of separation of concerns.
- AngularJS provides reusable components.
- With AngularJS, developer write less code and get more functionality.
- In AngularJS, views are pure html pages, and controllers written in JavaScript do the business processing.

***Core Features:***

- **Data-binding**: automatic synchronization of data between model and view components.
- **Scope**: These are objects that refer to the model. They act as a glue between controller and view.
- **Controller**: Functions that are bound to a particular scope.
- **Services**: AngularJS come with several built-in services for example $https: to make a XMLHttpRequests. These are singleton objects which are instantiated only once in app.
- **Filters**: These select a subset of items from an array and returns a new array.
- **Directives**: Directives are markers on DOM elements (such as elements, attributes, css, and more). These can be used to create custom HTML tags that serve as new, custom widgets. AngularJS has built-in directives (ngBind, ngModel...)
- **Templates**: These are the rendered view with information from the controller and model. These can be a single file (like index.html) or multiple views in one page using "partials".
- **Routing**: It is concept of switching views.
- **Model View Whatever**: MVC is a design pattern for dividing an application into different parts (called Model, View and Controller), each with distinct responsibilities. AngularJS does not implement MVC in the traditional sense, but rather something closer to MVVM (Model-View-ViewModel). The Angular JS team refers it humorously as Model View Whatever.
- **Deep Linking**: Deep linking allows you to encode the state of application in the URL so that it can be bookmarked. The application can then be restored from the URL to the same state.
- **Dependency Injection**: AngularJS has a built-in dependency injection subsystem that helps the developer by making the application easier to develop, understand, and test.

***Components:***

The AngularJS framework can be divided into following three major parts −

- **ng-app**: This directive defines and links an AngularJS application to HTML.
- **ng-model**: This directive binds the values of AngularJS application data to HTML input controls.
- **ng-bind**: This directive binds the AngularJS Application data to HTML tags.

## Directives

AngularJS directives are used to extend HTML. These are special attributes starting with ng- prefix. Examples:

- **ng-app**: This directive starts an AngularJS Application.
- **ng-init**: This directive initializes application data.
- **ng-model**: This directive defines the model that is variable to be used in AngularJS.

- **ng-repeat**: This directive repeats html elements for each item in a collection.

## Expressions

Expressions are used to bind application data to html. Expressions are written inside double braces like {{ expression}}.

## Controllers

A controller is defined using ng-controller directive. A controller is a JavaScript object containing attributes/properties and functions. Each controller accepts $scope as a parameter which refers to the application/module that controller is to control.

## Filters

Filters are used to change modify the data and can be clubbed in expression or directives using pipe character. Following is the list of commonly used filters.

<table>
   <tbody>
      <tr>
         <th width="30%">Name</th>
         <th width="70%">Description</th>
      </tr>
      <tr>
         <td>uppercase</td>
         <td>converts a text to upper case text.</td>
      </tr>
      <tr>
         <td>lowercase</td>
         <td>converts a text to lower case text.</td>
      </tr>
      <tr>
         <td>currency</td>
         <td>formats text in a currency format.</td>
      </tr>
      <tr>
         <td>filter</td>
         <td>filter the array to a subset of it based on provided criteria.</td>
      </tr>
      <tr>
         <td>orderby</td>
         <td>orders the array based on provided criteria.</td>
      </tr>
   </tbody>
</table>

## DOM

Following directives can be used to bind application data to attributes of HTML DOM Elements.

<table>
   <tbody>
      <tr>
         <th width="30%">Name</th>
         <th width="70%">Description</th>
      </tr>
      <tr>
         <td>ng-disabled</td>
         <td>disables a given control.</td>
      </tr>
      <tr>
         <td>ng-show</td>
         <td>shows a given control.</td>
      </tr>
      <tr>
         <td>ng-hide</td>
         <td>hides a given control.</td>
      </tr>
      <tr>
         <td>ng-click</td>
         <td>represents a AngularJS click event.</td>
      </tr>
   </tbody>
</table>

## Modules

AngularJS supports modular approach. Modules are used to separate logics say services, controllers, application etc. and keep the code clean. We define modules in separate js files and name them as per the module.js file. In this example we're going to create two modules.

- **Application Module**: used to initialize an application with controller(s).
- **Controller Module**: used to define the controller.

**Application Module**

```
var mainApp = angular.module("mainApp", []);
```

**Controller Module**

```
mainApp.controller("basantController", function($scope) {
});
```