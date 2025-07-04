# Changelog

## 1.0.17
* Update superluminal to 0.4
* Update tracy-client to 0.18 

## 1.0.16
* Address warnings from upstream rustc changes
* Update puffin to 0.19.1
* Update tracing-tracy to 0.11.3 and tracing-subscriber to 0.3
* Implement finish_frame! for tracing
* Add fuction_scope!() as an alternative to the function proc macro
* Avoid local variable names that don't start with an underscore introduced into a function's namespace

## 1.0.15
* Update tracy-client to 0.17
* Misc. egui/puffin_egui version bumps in the puffin demo

## 1.0.14
* Due to MSRV being practically limited by selected profiling backend, the formally declared
  MSRV has been removed. See readme.md for details.
* Update puffin to 0.19

## 1.0.13
* Update MSRV to 1.60
* Make feature dependency on profiling-procmacros optional so that it is no longer being unintentionally enabled

## 1.0.12
* Update to puffin 0.18
* Puffin example moved to a demo project, rewritten to use egui/eframe

## 1.0.11
* Update tracy-client to 0.16.2

## 1.0.10
* Add `profiling::all_functions`
* Add `profiling::skip`

## 1.0.9
 * Update to newer version of puffin, updates to several other dev-dependencies
 * Update to syn 2.0

## 1.0.8
 * Update tracy-client to 0.15.1
 * Add no_std (std likely is still required for any backends to be turned on)

## 1.0.7
 * Update tracy-client to 0.14.1

## 1.0.6
 * Update tracy-client to 0.13

## 1.0.5
 * Update puffin to 0.12.1

## 1.0.4
 * Update puffin to 0.10

## 1.0.3
 * Update puffin to 0.6 and puffin-imgui to 0.8

## 1.0.2
 * Fix tracing backend failing to compile when tracing crate is not a dependency in the downstream crate

## 1.0.1
 * Rework feature flags so that downstream *libraries* no longer have to add feature flags per profiling backend.
 * Add a backend that does type checking (for CI purposes)

## 1.0.0
 * Republish 0.1.10 as 1.0.0

## 0.1.10
 * Build fix for when the default feature "procmacros" is disabled

## 0.1.9
 * Bump tracy client version to 0.12 (tracy now uses the 0.7.6 protocol)
 * Bump puffin to 0.4
 * Update the puffin demo to use rafx
 * Aesthetic changes to the puffin example

## 0.1.8
 * Bump tracy client version to 0.11 (tracy now uses the 0.7.5 protocol)

## 0.1.7
 * Re-release due to root cargo.toml referencing 0.1.2 of procmacro crate instead of 0.1.3

## 0.1.6
 * Use tracy directly instead of going through tracy (use the profile-with-tracy feature).
 * Going through tracing is still possible and demonstrated in the example (use the profile-with-tracing feature).
 * Function instrumentation is now recorded to superluminal

## 0.1.5
 * More info in readme, no functional change

## 0.1.4
 * Fix the color passed to superluminal so that scopes are default-colored

## 0.1.3
 * Re-export the profiler crates, simplifying changes needed in end-user's cargo.toml

## 0.1.2
 * Remove unintended and unnecessary dependencies from the procmacro crate
 * Republish the bindings crate mainly to fix readme typos and add a bit more info about the exposed APIs

## 0.1.1
 * Add profiling::function procmacro
 * Add profiling::register_thread!()
 * Add profiling::finish_frame!()
 * Add support for superluminal
 * Fixed incorrect usage of span!() that affected tracy captures
 * More examples, improved documentation

## 0.1.0
 * Initial release