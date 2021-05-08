# Multiapp

## Advantages
Here are some advantages of having multiple Angular apps in one project.
1. A single source-control repository (E.g. git).
2. Time-consuming — no need to run npm install for every app.
3. Saving disk space by having a shared node_modules folder for all apps.
4. Easy to update to the next version for all apps.

```
// create workspace
ng new multiapp --createApplication=false --directory=frontend --interactive=false

// Create an Application
cd frontend
ng generate application administration --style=scss --routing=true
ng generate application demos --style=scss --routing=true

// Create a Library
ng generate library tools
ng generate library vendors

// Create a Shared Service
ng generate service hello-world --project=tools

// Install Angular Material
ng add @angular/material


// Run
ng serve --project=administrations
ng serve --project=demos
```

## Feature
- Workspace
- 2 application
  - administration
  - demos
- 2 library
  - tools ( shared service )
  - vendors ( mat lib )
- shared assets
- shared scss


# Angular Library

## Advantages

1. Building a reusable component library for sharing between applications.
2. Building shared service layer functionality - eg. a client for working with an external data source such as an API.

## Creating an Angular library project

```
ng new example-component-library --create-application=false
cd example-component-library
ng generate library example-component-library
ng generate application example-component-library-app

// build
ng build --prod --project=example-component-library
```

## Consuming our Angular library

```
// from library
cd dist/example-component-library
npm link

// from application
npm link example-component-library
ng build --project=example-component-library
ng serve
```

## Publish Library

```
npm login
cd dist/example-component-library
npm publish
```


## Resources

https://levelup.gitconnected.com/create-multiple-angular-apps-under-one-project-ff44541a259b
