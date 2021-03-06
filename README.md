# ocaml-cordova-plugin-splashscreen

[![LGPL-v3 licensed](https://img.shields.io/badge/license-LGPLv3-blue.svg)](https://raw.githubusercontent.com/dannywillems/ocaml-cordova-plugin-splashscreen/master/LICENSE)
[![Build Status](https://travis-ci.org/dannywillems/ocaml-cordova-plugin-splashscreen.svg?branch=master)](https://travis-ci.org/dannywillems/ocaml-cordova-plugin-splashscreen)

Binding to
[cordova-plugin-splashscreen](https://github.com/apache/cordova-plugin-splashscreen)

## What does cordova-plugin-splashscreen do ?

```
This plugin is required to work with splash screens. This plugin displays and
hides a splash screen during application launch.
```

Source: [cordova-plugin-splashscreen](https://github.com/apache/cordova-plugin-splashscreen)

## Repository branches and tags

Only gen_js_api version is provided

## How to install and compile your project by using this plugin ?

Don't forget to switch to a compiler **>= 4.03.0**.
```Shell
opam switch 4.03.0
```

You can use opam by pinning the repository with
```Shell
opam pin add cordova-plugin-splashscreen https://github.com/dannywillems/ocaml-cordova-plugin-splashscreen.git
```

and to compile your project, use
```Shell
ocamlfind ocamlc -c -o [output_file] -package gen_js_api -package cordova-plugin-splashscreen [...] -linkpkg [other arguments]
```

Don't forget to install the cordova plugin splashscreen with
```Shell
cordova plugin add https://github.com/apache/cordova-plugin-splashscreen
```

## How to use ?

* See the official documentation: [cordova-plugin-splashscreen](https://github.com/apache/cordova-plugin-splashscreen)
