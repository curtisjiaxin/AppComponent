# AppComponent
Write a main component of a project to connect with other children component

## Component
Create a 'app.component.ts' file
```ts
import { Component } from '@angular/core';
@Component({
  selector: 'ksc-demo-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.scss']
})
export class AppComponent {
}
```
Create HTML file and write the route in the  `` templateUrl: '' ``,

and create the SCSS file and write the route in the ``styleUrls:``.

## module
Create a 'app.module.ts' file
```
import { BrowserModule } from '@angular/platform-browser';
import { NgModule } from '@angular/core';
import { FormsModule } from '@angular/forms';
import { FormsModule } from '@angular/http';

import { AppComponent } from './app.component';
@NgModule({
  declarations: [
    AppComponent
  ],
  imports: [
    BrowserModule,
    FormsModule,
    HttpModule,
  ],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule { }
```
The ``BrowserModule``,`` NgModule``,``FormsModule``,``FormsModule`` is must be import, beside of these you have import ``AppComponent``

and then you should ``declaraction``and ``imports``them .

and export AppModule for main.ts use.

## router 

Create app-routing-module.ts file 
```

import { NgModule } from '@angular/core';
import { Routes, RouterModule } from '@angular/router';

const routes: Routes = [
  { path: 'basic-components/ksc-dragable-dashboard', loadChildren: './ksc-dragable-dashboard/ksc-dragable-dashboard-demo.module#KSCDragableDashboardDemoModule'},
  { path: 'basic-components/ksc-select-picker', loadChildren: './ksc-select-picker/ksc-select-picker-demo.module#KSCSelectPickerDemoModule'},
  { path: 'basic-components/ksc-dropdown-picker', loadChildren: './ksc-dropdown-picker/ksc-dropdown-picker-demo.module#KSCDropdownPickerDemoModule'},
  { path: 'basic-components/ksc-bread-crumbs', loadChildren: './ksc-bread-crumbs/ksc-bread-crumbs-demo.module#KSCBreadCrumbsDemoModule'},
  { path: 'basic-components/ksc-date-range-picker', loadChildren: './ksc-date-range-picker/ksc-date-range-picker-demo.module#KSCDateRangePickerDemoModule'},
  { path: 'basic-components/ksc-table', loadChildren: './ksc-table/ksc-table-demo.module#KSCTableDemoModule'}

];

@NgModule({
  imports: [RouterModule.forRoot(routes)],
  exports: [RouterModule]
})
export class AppRoutingModule { }

```
Declare const routes for display those component.

Export the ``AppRoutingModule``, and import in 'app.module.ts'.
```
import { AppRoutingModule } from './app-routing.module'
```


