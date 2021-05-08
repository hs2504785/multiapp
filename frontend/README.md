# Multiapp


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
