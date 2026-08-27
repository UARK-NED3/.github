# NED³ Laboratory

![Illustration of the NED³ research ecosystem: thermal-fluid experiments and
simulation become multimodal datasets, software, and benchmarkable engineering
models.](../assets/ned3-research-ecosystem.png)

The **NED³ Laboratory** at the University of Arkansas develops reusable
research objects for thermal-fluid systems, multimodal sensing, and AI-enabled
engineering: open software, datasets, benchmarks, and educational workflows.

**Choose a path:** [use software](#software) · [find and cite
datasets](#datasets) · [explore benchmarks](#benchmarks) · [learn or
contribute](#methods-and-education)

> **Canonical-home principle:** NED³ links to the repository or archive that
> maintains each resource. Some are NED³-maintained; others remain with the
> student or collaborator who leads their development, preserving authorship,
> issue history, and maintenance responsibility.

## Flagship AI-for-thermal ecosystem

The NED³ flagship platform is [Thermal AI Commons](https://github.com/UARK-NED3/Thermal-AI-Commons), an interoperability hub for trustworthy AI in boiling, thermal-fluid, and energy systems. It connects versioned datasets, physics-aware processing, computer-vision feature extraction, and temporal-learning tools without merging their repositories or changing their licenses.

```text
BoilingBench-Multimodal → BoilingLab → BubbleID/BubbleID-Flow → SeqReg
                                  ↘ Thermal AI Commons evidence reports
```

Use the Commons for shared data contracts, synchronization/provenance records,
benchmark splits, compatibility pinning, and reproducible evidence reports.
Use each component's canonical repository for installation, issues, releases,
and scientific limitations.

### Start here

| Research need | Resource | Current role |
| --- | --- | --- |
| Start an AI-for-thermal workflow | [Thermal AI Commons](https://github.com/UARK-NED3/Thermal-AI-Commons) | Flagship interoperability hub for datasets, processing tools, model adapters, and leakage-safe evaluation. |
| Build and assess a CFD surrogate model | [CFDTwin](https://github.com/UARK-NED3/CFDTwin) | Released Python/GUI workflow for DOE, Fluent simulations, surrogate training, and analysis. |
| Reproduce or extend pool-boiling analysis | [BoilingLab](https://github.com/UARK-NED3/BoilingLab) | Experimental protocols, data-reduction guidance, scripts, and example materials. |
| Develop fair thermal-ML comparisons | [BoilingBench-Multimodal](https://github.com/UARK-NED3/BoilingBench-Multimodal) | Seed benchmark framework with task definitions, split logic, and leakage controls. |
| Find data-center cooling tools by research task | [Data Center Cooling Research Tools](https://github.com/UARK-NED3/Data-Center-Cooling-Research-Tools) | Curated discovery hub from mechanisms through facility operation. |
| Analyze single- and two-phase liquid-cooling experiments | [FlowLab](https://github.com/UARK-NED3/FlowLab) | Experimental protocols, multimodal collection guidance, and analysis notebooks. |
| Screen cooling life-cycle impacts | [OpenDC-LCA](https://github.com/UARK-NED3/OpenDC-LCA) | Open, physics-informed life-cycle-analysis workflow for data-center cooling. |

## Software

Start with [CFDTwin](https://github.com/UARK-NED3/CFDTwin) for Fluent-based
surrogate models, then browse the [NED³ software catalog](https://ned3.uark.edu/software/)
for the broader portfolio. Every repository states its own installation path,
license, citation guidance, and limitations.

## Datasets

**NED³ datasets are archived and cited on their canonical DOI-hosting
platforms—not duplicated in GitHub.** Use the [NED³ dataset
registry](https://ned3.uark.edu/datasets/) to find a dataset by physical
system, modality, or NED³ identifier, then follow its DOI/archive link for
download, license, version, and citation metadata.

The registry connects datasets to their linked papers and software, including
[BubbleID](https://github.com/cldunlap73/BubbleID) and
[SeqReg](https://github.com/cldunlap73/SeqReg). Check the individual archive
record for access conditions and the authoritative citation.

## Benchmarks

[BoilingBench-Multimodal](https://github.com/UARK-NED3/BoilingBench-Multimodal)
is the flagship boiling dataset and benchmark entry point. It specifies tasks,
metadata, split rules, baseline expectations, and contribution mechanisms; its
public Lite snapshot is distributed through Hugging Face and archived on
[Zenodo](https://doi.org/10.5281/zenodo.22131859). The [Thermal AI
Commons](https://github.com/UARK-NED3/Thermal-AI-Commons) repository provides
the cross-component contracts and evidence workflow.

## Methods and education

- [MEEG-54403](https://github.com/hanhuark/MEEG-54403) — machine-learning
  learning materials for mechanical engineers (Han Hu personal account).
- [Mechanical Engineering Research Skill](https://github.com/hanhuark/mechanical-engineering-research-skill)
  — an AI-assisted workflow for evidence-aware thermal-fluid research, data
  analysis, technical writing, and proposal development (Han Hu personal
  account).
- The [open ecosystem paper](https://arxiv.org/abs/2605.23037) explains how
  NED³ datasets and software support reproducible AI-enabled thermal-fluid
  research.

## Collaborator-maintained projects

- [BubbleID](https://github.com/cldunlap73/BubbleID) — pool-boiling image
  segmentation, tracking, classification, and interface-dynamics analysis.
- [SeqReg](https://github.com/cldunlap73/SeqReg) — sequence-regression
  software, including boiling heat-flux prediction applications.
- [IRISApp](https://github.com/BradenS-eng/IRISApp) — desktop analysis and
  data-collection software for infrared imaging experiments.

## Use, cite, and contribute

Use the license, citation guidance, and documented limitations supplied by the
canonical repository or archive. Direct questions, bug reports, and feature
proposals to its issue tracker or documented support channel. For research
collaboration or a question about the laboratory portfolio, visit
[NED³](https://ned3.uark.edu/) or contact [Han Hu](https://engineering.uark.edu/mechanical-engineering/faculty/uid/hanhu/name/Han+Hu/).
