# Ember Inspector Changelog


## Ember Inspector 1.6.1

* [BUGFIX] Used general dot replacement in regex expressions to support nested routes
* Used `document.defaultView.eval` to support FF >= 34
* Added npm `prepublish` hook

## Ember Inspector 1.6.0

* [FEATURE] Added new "Container" tab
* [FEATURE] Added `EmberInspector.inspect(obj)` to send objects to the inspector
* [FEATURE] Views generated by `each` helper are now shown by default
* [FEATURE] Added a link to Github issues
* [FEATURE] Object inspector can now drill into arrays
* [FEATURE] Added support for dates in the object inspector
* [IMPROVEMENT] Main nav is now resizable
* [IMPROVEMENT] Performance improvement by making promise tracing opt-in
* [IMPROVEMENT] Model types are now sorted alphabetically
* [IMPROVEMENT] Separated regular tabs from advanced tabs
* [IMPROVEMENT] Detecting the application view no longer depends on `ember-application` class
* [BUGFIX] `null` values now show up as "null" in the object inspector
* [BUGFIX] Empty values in the object inspector should be editable
* [BUGFIX] Support views without a controller
* [BUGFIX] Firefox Tomster script no longer conflicts with WYSIWYGs
* [BUGFIX] Fixed issue with toolbar and expanding the object inspector
* [BUGFIX] Removed 404 image errors from tests

## Ember Inspector 1.5.0

* [IMPROVEMENT] Redesigned the UI to be more consistent with Chrome dev tools
* [IMPROVEMENT] Improved "appeared" performance by instrumenting out of band
* [BUGFIX] Fixed compatibility issue between promise inspection and Ember >= 1.7
* [BUGFIX] Fixed view highlighting after metal-views upgrade
* [BUGFIX] Fixed conflict between injecting Tomster script and file upload libraries

## Ember Inspector 1.4.0

* [FEATURE] Added bookmark option to support all browsers
* [FEATURE] Added support for multiple iframes
* [FEATURE] Added optional Tomster to Firefox
* [FEATURE] Added "display current route" option to the routes tab
* [IMPROVEMENT] Removed redundant prefixes from class names in the view tree
* [IMPROVEMENT] Added search field to the render performance tab
* [BUGFIX] Fixed current route match when resource same as route name
* [BUGFIX] Fixed bug where a maximum of one namespace was assumed
* [BUGFIX] Fixed render perf tab for apps with prototype extensions disabled
* [BUGFIX] Routes tab no longer instantiates controllers
* `data-ember-extension` is now only added to the HTML tag (instead of the body).

## Ember Inspector 1.3.1

* [IMPROVEMENT] Better view names in the render performance tab
* [IMPROVEMENT] Object inspector now skips properties ending with `Binding`
* [IMPROVEMENT] Removed several `Ember.View` private props from the Object Inspector
* [BUGFIX] Fixed hierarchy issue in render perf tree causing duplication of views
* [BUGFIX] Fixed scrollbar in render performance tab on OS X
* [BUGFIX] Object inspector should not assume all `_debugInfo` props exist

## Ember Inspector 1.3.0

* [FEATURE] Added new "Render Performance" tab
* [FEATURE] Added new column "Duration" to the view tree
* [BUGFIX] Fixed bug with editing json strings in the object inspector
* [BUGFIX] Fixed permission denied exception on Firefox >= 30
* Removed dummy URLs created by Ember for error and loading routes
* Removed methods from the object inspector

## Ember Inspector 1.2.0

* [FEATURE] Add info tab that shows a list of libraries used and their versions
* [FEATURE] Add a Tomster icon to Chrome bar on any page with an Ember app (opt-in in chrome://extensions -> Ember Inspector -> options)
* [FEATURE] Promise chains can now be collapsed / expanded. Fulfilled promises are collapsed by default. Rejected and pending are expanded.
* Replaced $E button with "Stack trace" when the promise rejects with an instance of `Error`.
* Added support for async loading of Ember (such as requirejs)
* Added a hint to refresh the page when the Inspector is open after a few promises were created and uncaught.
* [BUGFIX] Error message about file:// protocol should only be shown on Chrome
* [BUGFIX] Add missing ember.prod.js file in vendors
