# ocaml-cordova-plugin-splashscreen

* gen_js_api (master branch): [![Build Status](https://travis-ci.org/dannywillems/ocaml-cordova-plugin-splashscreen.svg?branch=master)](https://travis-ci.org/dannywillems/ocaml-cordova-plugin-splashscreen)

Binding to
[cordova-plugin-splashscreen](https://github.com/apache/cordova-plugin-splashscreen)

[Example
application](https://github.com/dannywillems/ocaml-cordova-plugin-splashscreen-example).

## What does cordova-plugin-splashscreen do ?

```
This plugin is required to work with splash screens. This plugin displays and
hides a splash screen during application launch.
```

Source: [cordova-plugin-splashscreen](https://github.com/apache/cordova-plugin-splashscreen)

## Repository branches and tags

Only gen_js_api version is provided

## How to use ?

TODO

## ! BE CAREFUL !

The plugin creates a new object called *navigator.splashscreen*, but the object is
available when the *deviceready* event is handled.

We don't provide a *navigator.splashscreen* variable in this plugin (as said in the official
documentation on js_of_ocaml). If we did, *navigator.splashscreen* will be set to **undefined**
because the *navigator.splashscreen* object doesn't exist when we create the variable.

Instead, we provide a function *Splashscreen.t* of type *unit -> Splashscreen.splashscreen* which creates the
binding to the *navigator.splashscreen* object. You must call it when the deviceready
event is handled, eg

```OCaml
let on_device_ready _ =
  let s = Splashscreen.t () in
  (* Some code *)

let _ =
  Dom.addEventListener Dom_html.document (Dom.Event.make "deviceready")
  (Dom_html.handler on_device_ready) Js._false
```
