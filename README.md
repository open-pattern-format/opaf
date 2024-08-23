<p align="center">
    <img src="assets/opaf_banner.png" height="400">
</p>

`OPAF` is a comprehensive pattern file format aimed at yarn based crafts including knitting and crochet. The pattern is defined using a custom XML like syntax and can be compiled to a true XML project interpretation using any of the supported libraries or apps.

Patterns are built using several core elements including `values`, `components`, `instructions`, `repeats` and `actions`. `blocks` can be used to store sets of elements which get repeated throughout the pattern to limit duplication. You can define configurable values and use math expressions and conditions throughout to generate bespoke patterns based on size, gauge or other parameters.

##  Features

* Configuration definitions
* Value definitions for static and dynamic values used throughout the pattern
* Block definitions to limit duplication
* Familiar math expressions (`ROUND`, `CEIL`, `FLOOR`, `MROUND`, `ABS`)
* Conditions for creating dynamic patterns
* Helper functions (`ISEMPTY`, `MULTIPLE`, `CHOOSE`, `LT`, `GT`, `EQ`, `NEQ`, `AND`, `OR`, `NOT`)
* Library of common `actions` pre-defined
* Define your own custom `actions`
* Charting support
* Image support
* Text element with Markdown support
* Comprehensive metadata support

### OPAF basic template

```xml
<pattern name="My Awesome Pattern" >
    <opaf:component name="my_first_component" >
        <opaf:instruction name="Round 1" >
            <opaf:action name="knit" />
        </opaf:instruction>
    </opaf:component>
    <opaf:component name="my_second_component" condition="${EQ(size, 0)}" >
        <opaf:instruction name="Round 2" >
            <opaf:actions ... />
        </opaf:instruction>
    </opaf:component>
</pattern>
```
