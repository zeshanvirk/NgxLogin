# Angular Jonas Login

## Getting Started

### Installation

```
npm install ngx-jonas-login --save
```
And then include it in your module 

```ts
import {NgxJonasLoginModule} from 'ngx-jonas-login'
// ...

@NgModule({
  declarations: [
    ....
  ],
  imports: [
    ...
    NgxJonasLoginModule
  ]
})
export class AppModule { }
```

### Usage

```ts
import { Component, OnInit } from '@angular/core';

export class AppComponent implements OnInit {
  title = 'Client Login';
  logo = './images/white_-logo.png';
  background = './images/black_white_background.png';
  version = '2019.45.321'
  isJonasBrowser = true;
  
   onFormSubmit(event){
      //your logic here
  }
}
```

```html
<ngx-jonas-login 
[title]="title" 
[version]="version" 
[logo]="logo" 
[backgroundImage]="background" 
[isJonasBrowser]="isJonasBrowser"
(onSubmit)="onFormSubmit($event)" 
>
</ngx-jonas-login>
```

### Settings

| Setting                        | Type       | Description                                                                                                                                                                                                                                                                                                                                              | Default Value       |
| :----------------------------- | :--------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :------------------ |
| title                          | String     | Title of Login Form                                                                                                                                                                                                                                                                                                                                      | Login               |
| version                        | String     | Version No. of Application                                                                                                                                                                                                                                                                                                                               | ''                  |
| logo                           | String     | Logo that will be displayed on the top of form                                                                                                                                                                                                                                                                                                           | ''                  |
| backgroundImage                | String     | Background image of login form. (Default will be white)                                                                                                                                                                                                                                                                                                  | ''                  |
| isJonasBrowser                 | Boolean    | Enable the option to select all items in list                                                                                                                                                                                                                                                                                                            | false               |                                                                                                                                                                                                                                                                                                                        | false               |

### Callback Methods

- `onSubmit` - Return the selected item when an item is checked.
  Example : (onSelect)="onFormSubmit($event)"

## Running unit tests

Run `ng test` to execute the unit tests.

## Development

This project was generated with Angular CLI version 7.1.4.

## Contributions

Contributions are welcome, please open an issue and preferrably file a pull request.

### Opening Issue

Please share sample code using codesandbox.com or stackblitz.com to help me re-produce the issue.

## License

MIT License.
