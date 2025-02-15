# Eclipse GLSP Server Node Changelog

## v1.1.0 - upcoming

-   [node] Update minimum requirements for Node to >=16.11.0 [#210](https://github.com/eclipse-glsp/glsp-client/pull/210)

### Breaking Changes

-   [graph] Align GGraph model with newest changes from glsp-server [#22](https://github.com/eclipse-glsp/glsp-server-node/pull/22) - Contributed on behalf of STMicroelectronics
    -   Renamed interfaces:
        -   `EdgePlacement` -> `GEdgePlacement` (affected classes: `GEdgeLayoutable`, `GLabel`)
        -   `GLayoutContainer` -> `GLayouting` (affected classes: `GCompartment`, `GGraph`, `GNode`)
        -   `GShapePreRenderedElement` -> `GShapedPreRenderedElement`

## [v1.0.0 - 30/06/2022](https://github.com/eclipse-glsp/glsp-server-node/releases/tag/v1.0.0)

Inception of the Node GLSP Server.
This project provides the Node based server component for the Eclipse Graphical Language Platform (GLSP).
The implementation of this server is aligned with the default Java based [GLSP Server](https://github.com/eclipse-glsp/glsp-server).
The [initial implementation](https://github.com/eclipse-glsp/glsp-server-node/commit/4fba8e8beef07798a7eff27c9c04ca68583e5960) was contributed on behalf of STMicroelectronics.
The following list composes changes that have been made since the initial implementation.

### Changes (since the initial contribution )

-   [core] Implement `dispatchOnNextUpdate` method that enables queuing of actions that should be dispatched after the next graphical model update. [#1](https://github.com/eclipse-glsp/glsp-server-node/pull/1) - Contributed on behalf of STMicroelectronics
-   [diagram] Implement LayoutEngine API for server-side autolayouting & provide an integration package for layout engines based on ELK. [#2](https://github.com/eclipse-glsp/glsp-server-node/pull/2) [#5](https://github.com/eclipse-glsp/glsp-server-node/pull/5) - Contributed on behalf of STMicroelectronics

### Breaking Changes

-   [model] Source model refactorings [#11](https://github.com/eclipse-glsp/glsp-server-node/pull/11)
    -   `ModelSourceLoader` → `SourceModelStorage`
    -   Added method to `SourceModelStorage`
-   [model] Refactor `ModelState` API [#20](https://github.com/eclipse-glsp/glsp-server-node/pull/20)
    -   Introduce `updateRoot` method
    -   `DefaultModelState` => make root setter protected
-   [gmodel] Refactor & Move all base & helper classes for the direct GModel usecase into own `gmodel-lib` subdirectory [#16](https://github.com/eclipse-glsp/glsp-server-node/pull/16)
