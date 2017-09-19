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
Create HTML file and write the route in the  `` templateUrl: '' ``, and create the SCSS file and write the route in the ``styleUrls:``

## module
Create a 'app.module.ts' file
```
import { BrowserModule } from '@angular/platform-browser';
import { NgModule } from '@angular/core';
import { FormsModule } from '@angular/forms';
import { FormsModule } from '@angular/http';

import { AppComponent } from './app.component';
import { KSCToolbarModule } from '../../basic-components/ksc-toolbar/ksc-toolbar.module'
@NgModule({
  declarations: [
    AppComponent
  ],
  imports: [
    BrowserModule,
    FormsModule,
    HttpModule,
    KSCToolbarModule
  ],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule { }
```
The ``BrowserModule``,`` NgModule``,``FormsModule``,``FormsModule`` is must be import, beside of these you have import ``AppComponent``

and then you should ``declaraction`` and ``imports``them

## import { KSCToolbarModule } 

if you want to display a children component, you must import the module in app.module, such as ``KSCToolbarModule``

And then write the children``selector: ``in the app.component.html

Such as:
```
<ksc-toolbar></ksc-toolbar>
```

