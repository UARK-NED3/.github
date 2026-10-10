# NED3 software portfolio roadmap

**Status:** proposed roadmap; not a validation, deployment, or release claim.
**Prepared:** 2026-10-10
**Portfolio principle:** retain each project's canonical repository and maintainer; connect compatible projects through versioned contracts, evidence reports, and explicit user-facing boundaries.

## Purpose

NED3 software should help a researcher or engineer move from a stated physical question and available evidence to a reproducible, bounded result. The portfolio should not become a collection of generic AI chat interfaces or a monorepo. The near-term objective is to make existing methods easier to discover, configure, execute, interpret, and audit.

Every public product should state:

- the supported decision or research task;
- required inputs, units, time basis, and applicability limits;
- output type: measured, derived, simulated, screening-level, or model-derived;
- validation/evidence status and known exclusions;
- software, data, and model versions needed to reproduce a result; and
- the canonical repository, maintainer, license, citation, and issue tracker.

## Portfolio architecture

```text
Source data, instruments, literature, and simulation inputs
                         |
                         v
Canonical NED3 packages and archives
  CFDTwin | BoilingLab | FlowLab | BubbleID-family | SeqReg | OpenDC-LCA
                         |
                         v
Thermal AI Commons: manifests, version pinning, grouped splits,
provenance, evidence reports, and compatibility checks
                         |
                         v
Decision products and guided workflows
  Water Atlas | LCA Scope Builder | Experiment Passport | Workflow Navigator
```

The Commons is an interoperability/evidence layer, not an owner of component source code, raw data, trained weights, or third-party licenses.

## Product priorities

| Priority | Product | User question | First release boundary | Primary canonical homes |
| --- | --- | --- | --- | --- |
| 1 | Data Center Water Atlas | Where may proposed data-center capacity coincide with water- and grid-stress indicators under declared scenarios? | Geographic and scenario screening; not facility metering, permitting advice, utility interconnection analysis, or a forecast of actual withdrawal/consumption. | `hanhuark/Data-Center-Water-Research`; `UARK-NED3/OpenDC-LCA`; `UARK-NED3/Data-Center-Cooling-Research-Tools` |
| 2 | Experiment Passport | Is an experimental or multimodal analysis package sufficiently described to reproduce and compare? | Metadata, synchronization, calibration, and provenance validation; not experimental certification. | `UARK-NED3/Thermal-AI-Commons`; BoilingLab; FlowLab; AELab |
| 3 | Thermal Workflow Navigator | What NED3 workflow fits this physical question and available data? | Structured workflow routing and missing-information checks; no autonomous engineering approval or unqualified conclusion. | Thermal AI Commons; Data Center Cooling Research Tools |
| 4 | OpenDC-LCA Scope Builder | What functional unit, system boundary, inventory, and uncertainty information are needed for a defensible cooling comparison? | Scenario construction and claim gating; not ISO-conformant comparative LCA without required inventory, review, and reproduction evidence. | `UARK-NED3/OpenDC-LCA` |
| 5 | CFDTwin Evidence Report | Is this surrogate appropriate for the selected geometry and operating range? | Record DOE, solver, split, error, and extrapolation boundaries; no claim of validity beyond the documented design space. | `UARK-NED3/CFDTwin` |

## Water Atlas: recommended beta specification

### User workflow

1. Select or upload a site record with source, location precision, capacity basis, and as-of date.
2. Select a fully declared cooling scenario: IT load or capacity basis, utilization/load assumption, PUE, water-intensity/WUE assumption, cooling technology, geography, and annual or hourly time basis.
3. View separate water-context and grid-context indicators; do not collapse them into one opaque score.
4. Inspect sensitivity to high-consequence assumptions and missing inputs.
5. Export a screening evidence packet containing the source snapshot, transforms, formulas, assumptions, geographic joins, exclusions, scenario ID, and software/data versions.

### Required guardrails

- Label all map and scenario outputs as **screening-level** unless matched, measured facility-operating data support a stronger claim.
- Keep water **withdrawal** and **consumption** distinct, with units and time basis visible.
- Preserve unknown cooling technology, PUE/WUE, utility territory, water source, and interconnection fields as unknown; never silently impute them into a facility-specific claim.
- Record spatial-join version, geometry precision, and source dates. A public inventory record or spatial intersection is not proof of facility operation, service, withdrawal, or interconnection.
- Publish the formula and parameter source for each scenario. Make uncertainty/sensitivity outputs first-class, not footnotes.
- Protect restricted site, customer, utility, or telemetry data through a private deployment path; do not upload them to public GitHub or a public agent.

### Beta acceptance tests

- A selected site/scenario can be regenerated from its exported evidence packet on a clean environment.
- Unit tests cover unit conversion, time-basis conversion, geographic joins, missing-data states, and withdrawal-versus-consumption labels.
- A reviewer can identify every modeled input and its source without reading application source code.
- Public examples contain only public or synthetic data and state their evidence class.

## Experiment Passport and Commons integration

Extend the existing experiment manifest and evidence-report approach through adapters, not data duplication. A quantitative multimodal run should require:

- experiment/system metadata, geometry, fluid/material, operating conditions, and units;
- sensor locations, sampling/frame rates, clock/trigger chain, offset/drift, and synchronization uncertainty;
- calibration records, reduction equations, preprocessing configuration, and raw-to-derived lineage;
- declared labels as measured, derived, human-annotated, or model-derived;
- grouped train/validation/test rules that prevent leakage across runs, surfaces, heat paths, facilities, or datasets; and
- checkpoint/configuration/environment hashes, uncertainty declarations, and failure cases for model outputs.

The Passport should produce a machine-readable validation result and a human-readable evidence report. It should block a quantitative claim when essential time-alignment, calibration, or provenance declarations are unavailable rather than fabricating completeness.

## Thermal Workflow Navigator

The first agent should be a constrained workflow architect, not a general engineering chatbot. Its inputs should be a structured intake:

```text
physical objective -> system boundary -> geometry/fluid/material -> operating range
-> available data and instruments -> required output -> acceptable evidence level
```

Its outputs should be:

1. a physical-variable and measurement checklist;
2. compatible NED3 tools, datasets, and examples with license/access status;
3. an executable or inspectable workflow plan;
4. required missing metadata and out-of-domain warnings; and
5. an evidence-report template for the proposed result.

Tool execution should be opt-in, sandboxed, and reproducible. The agent must not present a repository listing, a synthetic benchmark, or a model prediction as validated facility or experimental evidence.

## Delivery sequence

| Window | Deliverables | Exit gate |
| --- | --- | --- |
| 0–45 days | Portfolio resource cards; cross-repository metadata convention; Water Atlas beta requirements and data dictionary; 6–10 user interviews. | Each priority product has a named user, supported decision, owner, canonical home, input/output contract, and evidence boundary. |
| 46–90 days | Water Atlas beta: versioned inventory, scenario engine, separate stress layers, evidence-packet export, tests, and public synthetic demonstration. | A clean-environment reproduction regenerates a selected public scenario from its export. |
| 91–135 days | Experiment Passport validator and first adapters for one BoilingLab/FlowLab case and one vision workflow. | Manifests and evidence reports validate deterministically; known incomplete records return actionable failures. |
| 136–180 days | Workflow Navigator pilot across the Atlas, Commons, and OpenDC-LCA. | Predeclared expert tasks show correct workflow routing, complete disclosure of missing inputs, and no unsupported claim escalation. |

## Portfolio measures

Track outcomes that demonstrate scientific and practical utility:

- time from a new user's question to a reproducible first result;
- fraction of reports with complete source/version/units/assumption records;
- number and type of missing-data or out-of-domain errors caught before interpretation;
- clean-environment reproduction rate for public examples;
- independently reproduced case studies; and
- user success on prespecified engineering/research tasks.

Avoid engagement metrics as the principal success criterion. A shorter session is better if it produces a more reproducible and appropriately bounded result.

## Governance and release rules

1. Preserve canonical homes and maintainer ownership; do not fork or consolidate projects merely for catalog consistency.
2. Treat public catalogs as discovery resources, not automatic redistribution permission for code, datasets, weights, telemetry, or commercial assets.
3. Publish a versioned release note and evidence boundary whenever an output-affecting assumption, model, source, dataset, or schema changes.
4. Keep private, sponsor-restricted, student-identifying, vendor-proprietary, and facility-operational material out of public repositories and public agents.
5. Require a reviewable test/evidence record before describing a workflow as validated, deployed, or decision-ready.

## Immediate next actions

1. Create issue templates for product requirements, evidence-boundary review, and reproducibility defects in the canonical repository selected for each product.
2. Draft the Water Atlas data dictionary and scenario schema in `Data-Center-Water-Research`.
3. Add a cross-repository resource-card schema to Thermal AI Commons, then register the first six canonical packages.
4. Select one public, synthetic, or rights-cleared Water Atlas example and one rights-cleared multimodal experiment as vertical-slice demonstrations.
