# kendo-ui-forms

## About kendo-ui-forms

A Full-Featured HTML5 Forms Polyfill that leverages Kendo UI Widgets and Framework Validation

[![Build Status](https://travis-ci.org/kendo-labs/kendo-ui-forms.png)](https://travis-ci.org/kendo-labs/kendo-ui-forms)

## Purpose & Goals

The purpose of this project is to serve as a complete polyfill for [HTML5 Forms](http://www.w3.org/TR/2011/WD-html5-20110525/forms.html) functionality, including support for new input types--like color and datetime--new attributes--like placeholder and pattern--and validation. This project includes built-in feature detection and, by-default, will only polyfill those forms features not present in the user's browser. To polyfill forms features, Kendo UI widgets and framework features will be used.

If developers prefer not to use the default behavior, they will be able to configure the polyfill to always use Kendo UI widgets and features, even in cases where the browser natively supports these.

This library will function as an opt-in polyfill, meaning that the developer will need to initialize a form using Kendo UI's imperative, plugin syntax (eg. `$('form').kendoForm();`) or with declarative syntax on an HTML form element (eg. `<form data-role="form">`). 

**Goals**

- **Provide a complete HTML5 Forms solution that leverages Kendo UI for visual widgets and features like validation**.
- **Enable developers to mark up forms using HTML5 Forms semantics and automatically gain support for these in non-supporting browsers**. Anecdotally, in a future world where all browser fully support the forms spec, a developer should be able to remove the script reference for this library and the single attribute or line of code that initializes it and have a non-broken, fully-functional experience.
- **Ensure that performance is a feature**. This library should tax the developer and end user as little as possible, making the benefit of use far higher than the cost of development, maintenance or performance.

**Non-Goals**

- This library will not support configurable or drop-in replacement for another UI/Widget library.
- This library will not diverge from the [HTML5 Forms spec](http://www.w3.org/TR/2011/WD-html5-20110525/forms.html) in order to add convenience features or non-standard behaviors.

## Features

1. Ability to initialize a `kendoForm` custom widget from a Form in the DOM
2. Ability to interrogate types on a form and upgrade visual elements (Date, Color, etc.)
3. Ability to give all inputs a kendo look and feel ('k-input')
4. Ability to upgrade visual form types only when not present in the current browser.
5. Ability to add Kendo UI Validation to a form
6. Ability to support forms attributes (placeholder, to be specific)
7. Ability to swap-in the Kendo UI File Upload control

## Roadmap

- v0.1 - Support upgrading all HTML5 input types (color, numeric, range, file, datatime, time, month, week)
- v0.1.1 (Current) - button support & date type support
- v0.2 - Add support for progress and datalist elements; add a placeholder fallback and search box UI; autocomplete attribute support.
- v0.3 - Add validation support 

## Compatibility and Requirements

kendo-ui-forms was designed to work with Kendo UI Web. The project currently depends on the following libraries:

- [jQuery](http://www.jquery.com) v1.8.3+
- [Kendo UI](http://www.kendoui.com) vCurrent

kendo-ui-forms has not been tested against any other versions of these libraries. You may find that versions other than these are compatible with kendo-ui-forms, but we make no claims to support those version, nor can we troubleshoot issues that arise when using those versions.

## Source Code

This repository contains both the full and minified builds of the library in the `dist` folder

## Documentation

Check out the [Getting Started guide](https://github.com/kendo-labs/kendo-ui-forms/wiki/Getting-Started) in the Wiki.

A working sample of the plugin can be found in the `samples` directory

## How to Contribute

If you would like to contribute to kendo-ui-forms's source code, please read the [guidelines for pull requests and contributions](CONTRIBUTING.md). Following these guidelines will help make your contributions easier to bring in to the next release.

## Downloading and Installing

Once you clone the repo, run

	npm install

to grab all of the essential dependencies for dev, build and test. The repo uses grunt for all of these, so run

	grunt

to make sure everything is working. If you see text indicating that the jshint, concat and uglify tasks have run without errors, you're golden!

## Running the Tests

Tests are written in [jasmine](http://pivotal.github.io/jasmine/) and can be found in the spec/ directory. The Kendo UI Forms Project uses the [Karma](http://karma-runner.github.io/0.8/index.html) test runner to ensure cross-browser coverage of all tests. Browsers tested include:

- Google Chrome
- Google Chrome Canary
- Firefox
- Opera
- Safari [OSX Only]
- IE [Windows Only]

If you don't have any of these browsers, Karma will fail. But hey, this is cross-browser polyfill development here, so just install them all!

To run Karma, you can call

	grunt test

and Karma will take care of launching each browser, running the specs and shutting them down again (except for Safari, for some reason, so that's awesome).

If you want to run the jasmine tests in your browser, as opposed to running the multi-browser tests every time, you can spin up a local webserver and navigate to spec/runner.html, or navigate directly via the filesystem

	file://localhost/Users/brandon/Dropbox/Development/kendo-ui-forms/spec/runner.html

NOTE: If you're using Chrome and taking the latter approach, some of the tests will fail because of cross-domain features in Chrome. To work around this, run Chrome with the `--allow-file-access-from-files` terminal command. 

For OSX:

	open -a /Applications/Google\ Chrome.app --args --allow-file-access-from-files

And Windows:

	C:\Users\[UserName]\AppData\Local\Google\Chrome[ SxS]\Application\chrome.exe --allow-file-access-from-files

## Getting Help

Use this section to list ways that a developer can obtain help or support for this project, for instance, Stack Overflow. Make sure to also leave the following section:

As a part of Kendo UI Labs, kendo-ui-forms is intended to be a community-run project, and not an official part of any Kendo UI SKU (Web, DataViz, Mobile or Complete). As such, this project is not a supported part of Kendo UI, and is not covered under the support agreements for Kendo UI license holders. Please do not create support requests for this project, as these will be immediately closed and you'll be directed to post your question on a community forum.

## Release Notes

For change logs and release notes, see the [changelog](CHANGELOG.md) file.

## License Information

This project has been released under the [Apache License, version 2.0](http://www.apache.org/licenses/LICENSE-2.0.html), the text of which is included below. This license applies ONLY to the project-specific source of each repository and does not extend to Kendo UI itself, or any other 3rd party libraries used in a repository. For licensing information about Kendo UI, see the [License Agreements page](https://www.kendoui.com/purchase/license-agreement.aspx) at [KendoUI.com](http://www.kendoui.com).

> Copyright © 2013 Telerik

> Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

> [http://www.apache.org/licenses/LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0)

>  Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.
