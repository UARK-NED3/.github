# NED³ Laboratory

The **NED³ Laboratory** at the University of Arkansas develops open software,
datasets, benchmarks, and educational resources for thermal-fluid systems,
multimodal sensing, and AI-enabled engineering research.

Our goal is practical reuse: a visitor should be able to identify a relevant
research task, understand the evidence and scope of a resource, and reproduce
an example before extending it to a new system.

> **Start here:** choose the resource by the task you need to perform. Each
> card identifies its canonical repository and maintenance home.

## Start here

| Research need | Resource | What it provides | Canonical home |
| --- | --- | --- | --- |
| Build a surrogate model from ANSYS Fluent results | [CFDTwin](https://github.com/UARK-NED3/CFDTwin) | Python API and desktop workflow for design of experiments, Fluent simulations, neural-network surrogate training, and analysis. | NED³-maintained |
| Reproduce or adapt pool-boiling experiment analysis | [BoilingLab](https://github.com/UARK-NED3/BoilingLab) | Experimental protocols, data-reduction documentation, analysis scripts, and example materials for pool-boiling research. | NED³-maintained |
| Develop fair multimodal boiling ML comparisons | [BoilingBench-Multimodal](https://github.com/UARK-NED3/BoilingBench-Multimodal) | A seed benchmark specification with tasks, metadata, split logic, leakage controls, and baseline expectations. | NED³-maintained |
| Find tools across data-center cooling scales | [Data Center Cooling Research Tools](https://github.com/UARK-NED3/Data-Center-Cooling-Research-Tools) | Curated, mechanism-to-facility research-tool and dataset hub. | NED³-maintained |
| Analyze and track vapor structures in boiling imagery | [BubbleID](https://github.com/cldunlap73/BubbleID) | Student-led canonical software for pool-boiling image segmentation, tracking, classification, and interface-dynamics analysis. | Student/collaborator-maintained |
| Learn machine learning through mechanical-engineering applications | [MEEG-54403](https://github.com/hanhuark/MEEG-54403) | Course notebooks and reproducible learning materials for mechanical engineers. | Han Hu personal account |

## Research paths

- **Software:** Start with [CFDTwin](https://github.com/UARK-NED3/CFDTwin) for
  CFD-surrogate workflows, or browse the [NED³ software
  catalog](https://ned3.uark.edu/software/).
- **Datasets and experimental workflows:** Start with
  [BoilingLab](https://github.com/UARK-NED3/BoilingLab),
  [FlowLab](https://github.com/UARK-NED3/FlowLab), and the [NED³ dataset
  catalog](https://ned3.uark.edu/datasets/). Check each repository for its
  specific access, licensing, and raw-data limitations.
- **Benchmarks:** Start with
  [BoilingBench-Multimodal](https://github.com/UARK-NED3/BoilingBench-Multimodal).
  It is currently a seed benchmark framework; public raw-data archives and
  release DOIs are prerequisites for a fully reusable benchmark release.
- **Education:** Start with [MEEG-54403](https://github.com/hanhuark/MEEG-54403)
  and the [NED³ software catalog](https://ned3.uark.edu/software/).

## Collaborator-maintained projects

NED³ research includes projects whose canonical repositories remain with the
student or collaborator who leads their development. We link to those sources
rather than duplicate or transfer them, preserving authorship, issue history,
and maintenance responsibility.

- [BubbleID](https://github.com/cldunlap73/BubbleID) — image-based boiling
  analysis.
- [SeqReg](https://github.com/cldunlap73/SeqReg) — sequence-regression
  software, including boiling heat-flux prediction applications.
- [IRISApp](https://github.com/BradenS-eng/IRISApp) — visualization for thermal
  imaging data from the Infra Red Imaging Station.

## Use, cite, and contribute

Please use each repository's license, citation guidance, and documented
limitations. For questions, bug reports, and feature proposals, use the issue
tracker or discussion channel specified by the canonical repository. For a
research collaboration or a question about the laboratory portfolio, visit
[NED³](https://ned3.uark.edu/) or contact [Han Hu](https://engineering.uark.edu/mechanical-engineering/faculty/uid/hanhu/name/Han+Hu/).

---

**Maintenance labels:** “NED³-maintained” identifies repositories owned and
maintained by the UARK-NED3 organization. “Student/collaborator-maintained” and
“Han Hu personal account” identify external canonical homes; their inclusion
does not transfer ownership or maintenance responsibility to the organization.
