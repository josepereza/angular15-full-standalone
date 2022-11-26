# ModernAngular

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 15.0.0.
* Tutorial:  https://devm.io/angular/angular-15-features-javascript
## Notas para  standalone
### provideAnimations
function

Returns the set of dependency-injection providers to enable animations in an application. See animations guide to learn more about animations in Angular.

      
      
provideAnimations(): Provider[]

    

Parameters

There are no parameters.
Returns

Provider[]
### Usage notes

The function is useful when you want to enable animations in an application bootstrapped using the bootstrapApplication function. In this scenario there is no need to import the BrowserAnimationsModule NgModule at all, just add providers returned by this function to the providers list as show below.

      

```
      
bootstrapApplication(RootComponent, {
  providers: [
    provideAnimations()
  ]
});
```

* Otra forma de hacerlo:
The importProvidersFrom function provides a bridge back to the NgModule world. It should not be used in component provide as it is only usable in an application injector

Add importProvidersFrom function to provide BrowserAnimationModule inside main.ts.

main.ts
```
bootstrapApplication(AppComponent,{
  providers:[importProvidersFrom([BrowserAnimationsModule])]
}); 
```
## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The application will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via a platform of your choice. To use this command, you need to first add a package that implements end-to-end testing capabilities.

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.
# angular15-full-standalone
