---
layout: post
title: An Operational Readiness Framework
author: James M
banner:
  video: 
  loop: true
  volume: 0.8
  start_at: 8.5
  image: /assets/images/Operational-readiness.jpg
  opacity: 0.618
  background: "#000"
  height: "100vh"
  min_height: "38vh"
  heading_style: "font-size: 4.25em; font-weight: bold; text-decoration: underline"
  subheading_style: "color: gold"
categories: [Governance, Processes, Leadership, Risk Management]
tags: 
---
# Knowing When You Are Ready: A Framework for Assessing Operational Readiness in Digital System Introduction

## Abstract

Organisations at every scale — from national infrastructure operators to small and medium enterprises — regularly commission or adopt digital systems that prove harder to operationalise than to build. A system that works in a laboratory or a vendor demonstration frequently fails to deliver operational value when deployed into complex, human-populated environments.

This paper introduces a structured framework for understanding why, drawing on the evolving literature on Technology Readiness Levels (TRL), Human Readiness Levels (HRL), and System Readiness Levels (SRL). It argues that true operational readiness requires all three dimensions to mature in parallel, not in sequence, and that readiness imbalances create identifiable, measurable risk that flows directly to the executive and board level. Implications for programme governance and practical application at different organisational scales are discussed.

## 1. Introduction: The Readiness Problem

Large-scale digital transformation programmes have a persistent and well-documented failure pattern. The technology is delivered on time. The hardware is installed. The software passes acceptance testing. And then, in operation, things go wrong — slowly at first, then visibly. Incident rates climb. Workarounds proliferate. Productivity falls before it rises, if it rises at all. The system that was declared complete is not, in any operationally meaningful sense, ready.

This is not primarily a technology problem. It is a readiness problem: a failure to assess and manage the maturity of all three dimensions that determine whether a complex digital system will work in the real world — the technology itself, the humans who operate it, and the integration of the two within a functioning system. The frameworks discussed in this paper offer a disciplined approach to diagnosing and managing readiness across all three dimensions, and doing so early enough in the programme lifecycle to actually change outcomes.

The framework has its origins in aerospace and defence acquisition, where the cost of deploying an immature system can be measured in billions of dollars and human lives. Its underlying logic, however, is universal. A regional hospital deploying a new clinical information system, a logistics company rolling out an AI-assisted routing platform, or a regulatory body introducing a new digital case management system all face structurally identical risks. The scale differs; the failure modes do not.

## 2. Technology Readiness Levels

The Technology Readiness Level (TRL) scale was created by NASA in the 1970s and formalised internally in 1989, providing a nine-level scale to describe how mature a given technology was relative to operational use (NASA, 2023). NASA describes TRLs as a measurement system for technology maturity with nine levels, where TRL 1 is the lowest and TRL 9 is the highest (NASA, 2023). NASA’s TRL guidance also distinguishes later-stage maturity from earlier laboratory validation, including TRL 8 as a fully integrated system tested in its intended operational environment and TRL 9 as a system proven through successful mission operations (NASA, 2023).

The appeal of TRL is its simplicity. It gives programme managers and their stakeholders a common language for describing developmental risk, comparing competing technologies, and making investment decisions with some basis in evidence rather than vendor assurance alone. A technology at TRL 4 is genuinely different from one at TRL 7, and treating them equivalently is a known source of programme failure.

For organisations introducing digital systems — whether enterprise software, AI-enabled decision support tools, or large-scale data platforms — TRL provides the first lens of assessment. The key questions it prompts are: Has this technology been validated in conditions that genuinely resemble the target operational environment? Has it been demonstrated at the scale and complexity of the intended deployment? What evidence exists that it performs reliably under real operational stress rather than controlled test conditions?

The TRL scale maps to three broad phases of digital system development:

| TRL Range | Phase | What It Means for Digital Systems |
|---|---|---|
| 1–3 | Basic R&D | Proof of concept; algorithms tested in isolation; no integration |
| 4–6 | Technology Demonstration | Validated in laboratory or simulated environment; functional prototype |
| 7–9 | Operational Deployment | Demonstrated and proven in the actual operational context |

However, TRL alone is insufficient, and recognising this limitation is what drives the rest of the framework.

## 3. The Integration Gap: IRL and SRL

A technology can reach TRL 9 in isolation and still fail when connected to other components of a real system. This is the integration problem, and it is pervasive in large digital programmes. A national health records platform may consist of individually mature components — a database engine, a clinical user interface, a messaging layer, an analytics module — each of which has been tested independently. The interfaces between them, however, may be immature, poorly specified, or untested under realistic load. The system as a whole is less ready than any of its parts.

Sauser, Verma, Ramirez-Márquez and colleagues introduced the System Readiness Level concept in 2006, proposing that system maturity must account for both the readiness of individual technology components and the maturity of the interfaces between them (Sauser et al., 2006). Their model combines TRL with Integration Readiness Levels (IRL), where interface maturity becomes a first-class part of readiness assessment (Sauser et al., 2006).

The IRL describes the maturity of the interface between any two technologies in a system. IRL 1 means an interface has been identified and characterised. IRL 3 means there is a common language between the technologies sufficient to allow orderly interaction. IRL 6 means the integrating technologies can accept, translate, and structure information for their intended application. IRL 9 means the integration has been proven through actual mission operations.

The SRL is then calculated as a composite of all TRL and IRL values across the system — a normalised matrix that captures both component maturity and the maturity of how components connect. This yields an index that maps to acquisition lifecycle phases.

For digital system programmes, this framework surfaces a diagnostic truth that is frequently obscured by technology-centric assessments: the bottleneck to operational readiness is often not an immature component but an immature interface. An enterprise resource planning system that cannot reliably exchange data with a legacy payroll platform, or an AI clinical decision tool that has not been validated against the specific data formats of the target hospital's patient record system, will fail in ways that no amount of component-level TRL assessment would have predicted.

## 4. The Human Dimension: HRL

TRL and SRL together still leave a critical gap. They describe how ready the technology is; they say nothing about how ready the humans are to use it, nor whether the system as designed can actually be used safely and effectively by real operators in real conditions. This is not a peripheral concern. Across operational domains, human error is a major contributor to incidents, and the HFES standard frames HRL specifically to address human readiness early in system development (Steelman and Handley, 2022).

The Human Readiness Level concept was codified in ANSI/HFES 400-2021, Human Readiness Level Scale in the System Development Process, which defines HRL as a scale to evaluate, track, and communicate readiness for safe and effective human use (Steelman and Handley, 2022). The standard positions HRL as complementary to TRL and gives a nine-level structure that mirrors TRL’s progression from early concept through operational use (Steelman and Handley, 2022). The HRL scale is intended to capture and mitigate human systems issues early in the design phase to reduce human error in fielded systems (Steelman and Handley, 2022).

The HRL scale maps to the same three developmental phases:

- Basic Research and Development (HRL 1–3): establish the evidence base for human performance in the intended context.
- Technology Demonstration (HRL 4–6): evaluate human performance with progressively higher-fidelity representations of the system.
- Full-Scale Testing, Production, and Deployment (HRL 7–9): verify and validate human performance in the actual operational environment.

The standard’s HRL descriptions make clear that the goal is to capture and mitigate human systems issues early, when design changes are still feasible (Steelman and Handley, 2022). That is why HRL 3–4 is especially important: it is the last stage where serious human-systems problems can be identified before they are embedded in infrastructure, training, and procurement commitments.

## 5. The Integrated Framework

The full framework combines all three readiness dimensions into a single operational picture. The practical implication can be expressed simply: a system is only as ready as its least mature dimension. A programme that achieves TRL 9, IRL 8, and HRL 4 is not operationally ready, regardless of what the technical acceptance tests say.

This is a forcing function for programme managers. It prevents the common pattern in which human factors work is treated as something that happens after the system is built, rather than a parallel and equally important maturation track. It also aligns with the HRL standard’s emphasis on evaluating human readiness alongside the technology lifecycle rather than after deployment (Steelman and Handley, 2022).

![Operational Readiness Framework](/assets/images/orl.jpg)

Is the tech ready?
Do the parts integrate and work together?
Can real users use the change safely?

All three must reach sufficient maturity before the SRL index reflects genuine deployment readiness. The system proceeds at the speed of its slowest dimension.

## 6. Readiness as a Risk Lens

Readiness imbalances are not merely programme management problems. They are risk events — with financial, reputational, operational, and in some contexts regulatory dimensions — that sit squarely within the accountability of executive leaders and boards. Understanding why requires mapping each readiness gap to a recognisable category of organisational risk.

### 6.1 Why Boards Are Accountable

As digital strategy has become inseparable from organisational strategy, responsibility for governing digital assets has migrated from the IT function to the boardroom. Board-level IT governance literature shows that board involvement remains low relative to the importance of digital risk, creating a structural gap between accountability and oversight (Caluwe and De Haes, 2019; Caluwe et al., 2024).

The consequence is predictable. When a major digital system fails operationally — whether a public sector programme that cannot deliver its intended service, a financial institution whose trading platform collapses under load, or a healthcare provider whose clinical system is abandoned by clinical staff — the failure traces back through a chain of decisions that a board either ratified, was not equipped to interrogate, or was never shown evidence about.

The TRL/HRL/SRL framework reframes readiness as a board-legible risk metric. Rather than presenting boards with technical status reports that conflate completion with readiness, the framework provides a dimensioned picture: where the technology stands, where the integration stands, and where the human readiness stands.

### 6.2 Risk Categories

Each failure mode maps to a distinct category of organisational risk:

- Operational risk is the most direct consequence of a TRL-HRL gap. A system deployed before human readiness has been achieved will generate elevated error rates, increased incident frequency, and workflow degradation.
- Financial risk compounds over time in ways that are not visible at deployment. Late correction of human-systems integration issues is more expensive than addressing them early, because options narrow as the programme progresses (Steelman and Handley, 2022).
- Reputational and legal risk becomes acute when digital system failures affect service quality at scale.
- Strategic risk is perhaps the most underappreciated. A system that is technically deployed but operationally undermined by poor human integration does not deliver the productivity or capability improvements that justified the investment (Griffy-Brown et al., 2020).

### 6.3 What Boards Should Demand

The governance literature converges on several specific board obligations. Public digital governance guidance emphasises strong leadership, clear strategy, and active oversight of digital projects (Global Network of Director Institutes, n.d.; PricewaterhouseCoopers, n.d.). Applied to readiness, that suggests three concrete instruments:

- Readiness-gated deployment decisions.
- Dimensioned readiness reporting.
- Human readiness as a board-level metric.

These are not administrative niceties. They are the minimum controls needed to distinguish technical delivery from operational readiness.

## 7. Application at Scale

The frameworks above were developed in contexts where the consequences of failure are large and visible. For national-scale digital systems — a universal health records platform, a national taxation system, a defence command and control infrastructure — the integrated framework provides three specific management instruments:

- Transition gates with objective criteria.
- Early visibility of imbalances.
- A shared language across stakeholder communities.

Scaling to small and medium enterprises, the same logic applies, but the questions become more practical:

- Has this system been demonstrated to work at the scale and operational complexity of our environment?
- Have all the interfaces with existing systems been tested under realistic load?
- Have representative members of the workforce been involved before go-live?

Research on technology adoption also supports the broader point that organisational and institutional readiness matter alongside technology readiness (Webster and Gardner, 2019; Nahum et al., 2026). In other words, the system sits inside an organisation, and that organisation’s capacity to absorb change is part of the readiness problem.

## 8. Common Failure Modes

Three failure modes recur across operational digital system deployments at every scale.

- The TRL-HRL gap is the most common: a technically mature system deployed to a workforce whose readiness has not been developed in parallel.
- The IRL bottleneck is the most technically invisible failure mode: individually mature components that fail at their interfaces.
- The institutional readiness gap is the failure mode least visible to engineering-led assessments: a technically and humanly ready system introduced into an organisation whose governance, incentives, and culture are not aligned to support it.

The HRL standard explicitly treats human readiness as something to be developed and evaluated early, with representative users and mission-relevant environments becoming more important as fidelity increases (Steelman and Handley, 2022). That makes the framework not just descriptive, but diagnostic.

## 9. Practical Governance Model

A practical readiness governance model for digital system introduction, scalable from national programme to SME, rests on four principles:

1. Parallel maturation, not sequential.
2. Weakest dimension governs.
3. Evidence, not assertion.
4. Institutional context is part of the system.

For boards and executive teams, these principles translate into a governance posture: not passive recipients of programme status updates, but active demanders of evidence that readiness across all three dimensions has been demonstrated before the organisation commits to operational deployment.

## 10. Conclusion

Digital systems fail in operation not because technology is hard but because readiness is multidimensional and most organisations assess only one dimension at a time. The TRL/HRL/SRL framework provides an integrated approach to assessing technology, interfaces, and human use, with NASA’s TRL maturity model and HFES’s HRL standard providing the core structure (NASA, 2023; Steelman and Handley, 2022).

At the board and executive level, this framework reframes what has too often been treated as a programme management problem as what it actually is: a risk governance problem. Organisations that conflate technical delivery with operational readiness will continue to pay the costs of that confusion in operational failures, remediation expenditure, and forfeited strategic value.

## References

Caluwe, L. and De Haes, S. (2019) ‘Board level IT governance: A scoping review to set the research agenda’, *Information Systems Management*.

Caluwe, L., Wilkin, C.L., De Haes, S. and Huygh, T. (2024) ‘Board roles required for IT governance to become an integral component of corporate governance’, *International Journal of Accounting Information Systems*.

Fu, J., Mazzuchi, T. and Sarkani, S. (2026) ‘Cluster-based system readiness levels: Mathematical interface properties’, *Systems Engineering*.

Global Network of Director Institutes (n.d.) *Governing digital transformation and emerging technologies: A quick guide*.

Griffy-Brown, C., Miller, H., Zhao, V., Lazarikos, D. and Chun, M. (2020) ‘Making better risk decisions in a new technological environment’, *IEEE Engineering Management Review*.

Handley, H.A.H. (2023) ‘Human System Integration Framework (HSIF) activities to support Human Readiness Levels (HRLs)’, *Ergonomics in Design*.

Hodgson, J. and Drummond, H. (2009) ‘Learning from fiasco: What causes decision error and how to avoid it’, *Journal of General Management*.

Lozito, S. and Arsintescu, L. (2026) *NASA’s Integrated Arrival Departure System: A case study for the application of the Human Readiness Scale*. NASA Technical Memorandum.

Miller, M.E., Thomas, S. and Rusnock, C.F. (2016) ‘Extending system readiness levels to assess and communicate human readiness’, *Systems Engineering*, 19(2), pp. 146–157.

Nahum, N., Larsson-Olaison, U., Uman, T. and Achtenhagen, L. (2026) ‘Corporate governance for digital transformation: The role of ownership and the board of directors’, *Technological Forecasting and Social Change*.

Newton, V., Greenberg, A. and See, J. (2017) ‘Project management implications and implementation roadmap of Human Readiness Levels’, *Interacción*.

NASA (2023) ‘Technology Readiness Levels’, available at: https://www.nasa.gov/directorates/somd/space-communications-navigation-program/technology-readiness-levels/ (Accessed: 3 June 2026).

Okoro, W.J.C. (2025) ‘Digital banking transformation and board oversight effectiveness: A governance intensity perspective’, *Multiverse Journal*.

PricewaterhouseCoopers (n.d.) *Strategic oversight: Boards and digital transformation*.

Robertson, J. (2008) *A moral and ethical dilemma: Systems that fail*.

Rudman, R. (2011) *IT governance failure*.

Sauser, B., Verma, D., Ramirez-Márquez, J. and Gove, R. (2006) ‘From TRL to SRL: The concept of systems readiness levels’, in *Proceedings of the Conference on Systems Engineering Research (CSER)*, Los Angeles, CA, 7–8 April 2006.

Sauser, B., Ramirez-Márquez, J., Magnaye, R. and Tan, W. (2008) ‘A systems approach to expanding the technology readiness level within defense acquisition’, *Defense Technical Information Center*.

Steelman, K.S. and Handley, H.A.H. (2022) ‘A primer on the Human Readiness Level scale (ANSI/HFES 400-2021)’, *Human Factors in Transportation*.

Tan, W. (2009) ‘Monte-Carlo simulation approach for system readiness level estimation’.

Tedrick, S. (2026) ‘Why enterprise technology investments fail: A structural cascade model of compounding implementation risk’, *SSRN*.

Wallace, D.F., Bost, J., Thurber, J.B. and Hamburger, P.S. (2007) ‘Importance of addressing human systems integration issues early in the science and technology process’, *Naval Engineers Journal*.

Webster, A. and Gardner, J. (2019) ‘Aligning technology and institutional readiness: The adoption of innovation’, *Technology Analysis & Strategic Management*.