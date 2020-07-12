# angular10-from-angular9-ngrx-example

[![Netlify Status](https://api.netlify.com/api/v1/badges/cf8eda18-21ac-4502-8ae2-3bd39b18ff79/deploy-status)](https://app.netlify.com/sites/angular10-from-angular9-ngrx-example/deploys)

[angular9-ngrx-example](https://github.com/hosomi/angular9-ngrx-example) を Angular 10 に更新します。  

---　  

リリース内容、更新方法、ガイドはこちらを参考に。

:link: [Version 10 of Angular Now Available - Angular Blog](https://blog.angular.io/version-10-of-angular-now-available-78960babd41)  
:link: [Angular - Updating to Angular version 10](https://next.angular.io/guide/updating-to-version-10)  
:link: [Angular Update Guide](https://update.angular.io/#9.0:10.0)  

## Angular CLI を v9 -> v10 

Angular CLI  を削除:

```
PS> npm uninstall -g @angular/cli
```

Angular CLI 最新をインストール:

```
PS> npm install -g @angular/cli
```

バージョン確認:

```
PS>ng version

     _                      _                 ____ _     ___
    / \   _ __   __ _ _   _| | __ _ _ __     / ___| |   |_ _|
   / △ \ | '_ \ / _` | | | | |/ _` | '__|   | |   | |    | |
  / ___ \| | | | (_| | |_| | | (_| | |      | |___| |___ | |
 /_/   \_\_| |_|\__, |\__,_|_|\__,_|_|       \____|_____|___|
                |___/


Angular CLI: 10.0.0
Node: 12.18.1
OS: win32 x64

Angular: 10.0.0
... animations, cli, common, compiler, compiler-cli, core, forms
... language-service, platform-browser, platform-browser-dynamic
... router
Ivy Workspace: Yes

Package                           Version
-----------------------------------------------------------
@angular-devkit/architect         0.1000.0
@angular-devkit/build-angular     0.1000.0
@angular-devkit/build-optimizer   0.1000.0
@angular-devkit/build-webpack     0.1000.0
@angular-devkit/core              10.0.0
@angular-devkit/schematics        10.0.0
@ngtools/webpack                  10.0.0
@schematics/angular               10.0.0
@schematics/update                0.1000.0
rxjs                              6.5.5
typescript                        3.9.5
webpack                           4.43.0
```



## 更新

このリポジトリを ``git clone`` 直後は ``npm i`` してください。

```
PS angular10-from-angular9-ngrx-example> npm i
```


### ng update



更新内容確認:

```
PS angular10-from-angular9-ngrx-example> ng update
Your global Angular CLI version (10.0.0) is greater than your local
version (9.1.9). The local Angular CLI version is used.

To disable this warning use "ng config -g cli.warnings.versionMismatch false".
The installed local Angular CLI version is older than the latest stable version.
Installing a temporary version to perform the update.
Installing packages for tooling via npm.
Installed packages for tooling via npm.
Using package manager: 'npm'
Collecting installed dependencies...
Found 36 dependencies.
    We analyzed your package.json, there are some packages to update:

      Name                               Version                  Command to update
     --------------------------------------------------------------------------------
      @angular/cli                       9.1.9 -> 10.0.0          ng update @angular/cli
      @angular/core                      9.1.11 -> 10.0.0         ng update @angular/core
```

問題が表示されたら [Angular - Updating to Angular version 10](https://next.angular.io/guide/updating-to-version-10)
あたりを参考にしてマイグレーションしてください。


### ng update --all


問題がなければ ``ng update --all`` を実行。

```
PS angular10-from-angular9-ngrx-example> ng update --all
Your global Angular CLI version (10.0.0) is greater than your local
version (9.1.9). The local Angular CLI version is used.

To disable this warning use "ng config -g cli.warnings.versionMismatch false".
The installed local Angular CLI version is older than the latest stable version.
Installing a temporary version to perform the update.
Installing packages for tooling via npm.
Installed packages for tooling via npm.
Using package manager: 'npm'
Collecting installed dependencies...
Found 36 dependencies.
Fetching dependency metadata from registry...
Package '@ngrx/effects' is already up to date.
Package '@ngrx/entity' is already up to date.
Package '@ngrx/store' is already up to date.
Package '@ngrx/store-devtools' is already up to date.
Package 'bootstrap' is already up to date.
Package 'rxjs' is already up to date.
Package 'zone.js' is already up to date.
Package '@types/jasminewd2' is already up to date.
Package 'codelyzer' is already up to date.
Package 'jasmine-core' is already up to date.
Package 'karma' is already up to date.
Package 'karma-chrome-launcher' is already up to date.
Package 'karma-jasmine-html-reporter' is already up to date.
Package 'tslint' is already up to date.
    Updating package.json with dependency @angular-devkit/build-angular @ "0.1000.0" (was "0.901.9")...
    Updating package.json with dependency @angular/cli @ "10.0.0" (was "9.1.9")...
    Updating package.json with dependency @angular/compiler-cli @ "10.0.0" (was "9.1.11")...
    Updating package.json with dependency @angular/language-service @ "10.0.0" (was "9.1.11")...
    Updating package.json with dependency @types/jasmine @ "3.5.11" (was "3.5.10")...
    Updating package.json with dependency @types/node @ "14.0.14" (was "12.12.47")...
    Updating package.json with dependency angular-in-memory-web-api @ "0.11.0" (was "0.10.0")...
    Updating package.json with dependency jasmine-spec-reporter @ "5.0.2" (was "4.2.1")...
    Updating package.json with dependency karma-coverage-istanbul-reporter @ "3.0.3" (was "2.1.1")...
    Updating package.json with dependency karma-jasmine @ "3.3.1" (was "3.0.3")...
    Updating package.json with dependency protractor @ "7.0.0" (was "5.4.4")...
    Updating package.json with dependency ts-node @ "8.10.2" (was "8.3.0")...
    Updating package.json with dependency typescript @ "3.9.5" (was "3.8.3")...
    Updating package.json with dependency @angular/animations @ "10.0.0" (was "9.1.11")...
    Updating package.json with dependency @angular/common @ "10.0.0" (was "9.1.11")...
    Updating package.json with dependency @angular/compiler @ "10.0.0" (was "9.1.11")...
    Updating package.json with dependency @angular/core @ "10.0.0" (was "9.1.11")...
    Updating package.json with dependency @angular/forms @ "10.0.0" (was "9.1.11")...
    Updating package.json with dependency @angular/platform-browser @ "10.0.0" (was "9.1.11")...
    Updating package.json with dependency @angular/platform-browser-dynamic @ "10.0.0" (was "9.1.11")...
    Updating package.json with dependency @angular/router @ "10.0.0" (was "9.1.11")...
    Updating package.json with dependency tslib @ "2.0.0" (was "1.13.0")...
UPDATE package.json (1508 bytes)
√ Packages installed successfully.
** Executing migrations of package '@angular/cli' **

> Update Browserslist configuration file name to '.browserslistrc' from deprecated 'browserslist'.
RENAME browserslist => .browserslistrc
  Migration completed.

> Update tslint to version 6 and adjust rules to maintain existing behavior.
  Migration completed.

> Remove deprecated 'es5BrowserSupport' browser builder option.
  The inclusion for ES5 polyfills will be determined from the browsers listed in the browserslist configuration.
  Migration completed.

> Replace deprecated and removed 'styleext' and 'spec' Angular schematic options with 'style' and 'skipTests', respectively.
  Migration completed.

> Remove deprecated options from 'angular.json' that are no longer present in v10.
  Migration completed.

> Add "Solution Style" TypeScript configuration file support.
  This improves developer experience using editors powered by TypeScript’s language server.
  Read more about this here: https://v10.angular.io/guide/migration-solution-style-tsconfig
RENAME tsconfig.json => tsconfig.base.json
CREATE tsconfig.json (427 bytes)
UPDATE tsconfig.app.json (229 bytes)
UPDATE tsconfig.spec.json (293 bytes)
UPDATE e2e/tsconfig.json (232 bytes)
  Migration completed.

> Add the tslint deprecation rule to tslint JSON configuration files.
  Migration completed.

> Update library projects to use tslib version 2 as a direct dependency.
  Read more about this here: https://v10.angular.io/guide/migration-update-libraries-tslib
  Migration completed.

> Update 'module' and 'target' TypeScript compiler options.
  Read more about this here: https://v10.angular.io/guide/migration-update-module-and-target-compiler-options
UPDATE e2e/tsconfig.json (235 bytes)
  Migration completed.

> Update workspace dependencies to match a new v10 project.
UPDATE package.json (1509 bytes)
√ Packages installed successfully.
  Migration completed.

** Executing migrations of package '@angular/core' **

> Missing @Injectable and incomplete provider definition migration.
  As of Angular 9, enforcement of @Injectable decorators for DI is a bit stricter and incomplete provider definitions behave differently.
  Read more about this here: https://v9.angular.io/guide/migration-injectable
  Migration completed.

> ModuleWithProviders migration.
  As of Angular 10, the ModuleWithProviders type requires a generic.
  This migration adds the generic where it is missing.
  Read more about this here: https://v10.angular.io/guide/migration-module-with-providers
  Migration completed.

> Undecorated classes with Angular features migration.
  In version 10, classes that use Angular features and do not have an Angular decorator are no longer supported.
  Read more about this here: https://v10.angular.io/guide/migration-undecorated-classes
  Migration completed.
```

元ソースは v9 最新で作成したものなので、エラーなく ``ng update --all`` できました。


## 動作確認

```
PS angular10-from-angular9-ngrx-example> ng serve

chunk {main} main.js, main.js.map (main) 92.4 kB [initial] [rendered]
chunk {polyfills} polyfills.js, polyfills.js.map (polyfills) 141 kB [initial] [rendered]
chunk {runtime} runtime.js, runtime.js.map (runtime) 6.15 kB [entry] [rendered]
chunk {styles} styles.js, styles.js.map (styles) 690 kB [initial] [rendered]
chunk {vendor} vendor.js, vendor.js.map (vendor) 3.28 MB [initial] [rendered]
Date: 2020-06-25T04:12:19.569Z - Hash: c2d15ef1620a876d7c68 - Time: 7298ms
** Angular Live Development Server is listening on localhost:4200, open your browser on http://localhost:4200/ **
: Compiled successfully.
```

browser:  
``http://localhost:4200``

---

## :books: リファレンス

:link: [Angular 日本語ドキュメンテーション](https://angular.jp/)  
:link: [Angular CLI](https://cli.angular.io/)  

