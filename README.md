# kotoba-lang/org-accellera-uvm

Zero-dep portable `.cljc` implementation of core UVM (Universal
Verification Methodology) concepts, published by Accellera Systems
Initiative (accellera.org). UVM is a SystemVerilog class library/
methodology for building reusable, layered testbenches. Part of the
kotoba-lang EDA standards-substrate reverse-domain naming initiative
(ADR-2607072500, `com-junkawasaki/root`).

| Namespace | Purpose |
|---|---|
| `uvm.component` | component-tree model + find-by-type tree walk |
| `uvm.sequence` | sequence/sequence-item model + apply-sequence driver execution |
| `uvm.phase` | the 9 standard UVM phases + a real top-down phasing engine (run-phases) |
| `uvm.factory` | uvm_factory-style type-override registry with create/override resolution |

## Status

New — simplified but functionally real: component trees, phase
execution ordering, sequence-driving, and factory overrides all actually
execute (not just modeled as inert data). Not implemented: the
SystemVerilog class-library surface itself (uvm_object/uvm_transaction
base classes, TLM ports/exports/analysis, config_db, register
abstraction layer). 22 tests / 52 assertions, 0 failures.

## Develop

```bash
clojure -M:test
```
