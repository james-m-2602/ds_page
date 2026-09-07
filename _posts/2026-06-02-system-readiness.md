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

# Knowing When You Are Ready: From System Readiness to Operational Readiness in Digital Systems

## Abstract

Organisations at every scale—from national infrastructure operators to small and medium enterprises—regularly commission or adopt digital systems that prove harder to operationalise than to build. A system that works in a laboratory, test environment, or vendor demonstration can still fail to deliver operational value when introduced into complex, human-populated operating environments.

This paper presents a structured framework for distinguishing technical system maturity from genuine operational readiness. It draws on Technology Readiness Levels (TRL), Integration Readiness Levels (IRL), System Readiness Levels (SRL), and Human Readiness Levels (HRL), and introduces **Operational Readiness Level (ORL)** as the overarching measure of whether a complete socio-technical capability can enter, sustain, and recover from live operations while delivering its intended mission, service, safety, compliance, and value outcomes.

In this framework, SRL is retained as a measure of the maturity of the integrated technical system, derived from the readiness of constituent technologies and their interfaces. ORL is the executive and governance measure: it incorporates SRL and HRL, together with process readiness, organisational readiness, operational-support and assurance readiness, and evidence that the intended outcome can be achieved. The paper argues that these dimensions must mature in parallel, that critical weaknesses cannot be masked by an average score, and that readiness gaps should be governed as material operational and strategic risks.

## 1. Introduction: The Readiness Problem

Large-scale digital transformation programmes have a persistent and well-documented failure pattern. The technology is delivered on time. Hardware is installed. Software passes acceptance testing. Then, in operation, things go wrong—slowly at first, then visibly. Incident rates climb. Workarounds proliferate. Productivity falls before it rises, if it rises at all. The system that was declared complete is not, in any operationally meaningful sense, ready.

This is not primarily a technology problem. It is a readiness problem: a failure to assess and manage the maturity of the complete capability required to make a digital system work in the real world. That capability includes the technology itself, the interfaces between its parts, the people who use and maintain it, the operating processes around it, the organisation that governs it, and the support and assurance arrangements that sustain it.

The distinction matters because technical completion is not operational readiness. A system may satisfy its functional specification and still be unready for service if users cannot perform their work safely and effectively, decision rights remain unclear, support arrangements are incomplete, critical interfaces fail under real conditions, or the organisation has not demonstrated that it can achieve the outcome for which the system was funded.

The framework has its origins in aerospace and defence acquisition, where the cost of deploying an immature system can be measured in billions of dollars and human lives. Its underlying logic, however, is universal. A regional hospital deploying a new clinical information system, a logistics company rolling out an AI-assisted routing platform, or a regulatory body introducing a new digital case-management system all face structurally similar risks. The scale differs; the readiness problem does not.

This paper therefore distinguishes between **System Readiness Level (SRL)**—the readiness of the integrated technical system—and **Operational Readiness Level (ORL)**—the readiness of the whole socio-technical capability to operate in service.

## 2. Technology Readiness Levels

The Technology Readiness Level (TRL) scale was created by NASA in the 1970s and formalised internally in 1989, providing a nine-level scale to describe how mature a given technology was relative to operational use (NASA, 2023). NASA describes TRLs as a measurement system for technology maturity with nine levels, where TRL 1 is the lowest and TRL 9 is the highest. NASA’s TRL guidance also distinguishes later-stage maturity from earlier laboratory validation, including TRL 8 as a fully integrated system tested in its intended operational environment and TRL 9 as a system proven through successful mission operations (NASA, 2023).

The appeal of TRL is its simplicity. It gives programme managers and stakeholders a common language for describing developmental risk, comparing competing technologies, and making investment decisions with evidence rather than vendor assurance alone. A technology at TRL 4 is genuinely different from one at TRL 7, and treating them as equivalent is a known source of programme risk.

For organisations introducing digital systems—whether enterprise software, AI-enabled decision-support tools, or large-scale data platforms—TRL provides the first lens of assessment. It prompts three central questions:

- Has the technology been validated in conditions that genuinely resemble the target operational environment?
- Has it been demonstrated at the scale and complexity of the intended deployment?
- What evidence exists that it performs reliably under real operational stress rather than controlled test conditions?

The TRL scale maps to three broad phases of digital system development:

| TRL range | Phase | What it means for digital systems |
|---|---|---|
| 1–3 | Basic research and development | Proof of concept; algorithms or technologies tested in isolation; no meaningful operational integration |
| 4–6 | Technology demonstration | Validated in laboratory, simulated, or relevant environments; functional prototypes and early integrations demonstrated |
| 7–9 | Operational deployment | Demonstrated, qualified, and proven in the actual operational context |

TRL is necessary evidence, but it is never sufficient evidence of operational readiness. A technically mature component may still fail when integrated with other components, placed in a live process, used by a real workforce, or governed within a complex organisation.

## 3. System Readiness: IRL and SRL

A technology can reach TRL 9 in isolation and still fail when connected to the other components of a real system. This is the integration problem, and it is pervasive in large digital programmes. A national health records platform may comprise individually mature components—a database engine, clinical user interface, messaging layer, analytics module, identity service, and integration platform—each tested independently. The interfaces between them, however, may be immature, poorly specified, insecure, or untested under realistic load. The system as a whole is less ready than any of its parts.

Sauser, Verma, Ramirez-Márquez and colleagues introduced the System Readiness Level concept to address this gap. Their approach treats system maturity as a function of both the readiness of individual technology components and the maturity of the interfaces between them (Sauser et al., 2006).

### 3.1 Integration Readiness Level

**Integration Readiness Level (IRL)** describes the maturity of an interface or relationship between two technologies, components, or subsystems. It assesses more than the existence of a connection. It assesses whether the interface has been defined, implemented, tested, and proven under conditions representative of intended use.

At low IRL, an interface may be identified but not yet specified or demonstrated. At intermediate levels, the technologies share sufficient structure, data definitions, protocols, and control logic to interact in a controlled environment. At high levels, the integration has been tested under realistic operating conditions and proven through actual mission or service operations.

For digital-system programmes, IRL assessment should consider, as relevant:

- Data definitions, semantics, ownership, quality, lineage, and timing
- Application-programming interfaces, message formats, and error handling
- Identity, access, cybersecurity, privacy, and audit controls
- Workflow orchestration, hand-offs, exception paths, and reconciliation
- Performance, latency, resilience, scalability, and recovery under load
- Dependencies on external platforms, vendors, legacy systems, and operating environments

An enterprise resource-planning system that cannot reliably exchange data with a legacy payroll platform, or an AI clinical decision tool that has not been validated against the specific data formats of a hospital’s patient-record system, may contain mature components but remains immature at the system level.

### 3.2 System Readiness Level

**System Readiness Level (SRL)** is the assessed maturity of a system as an integrated technical whole. It combines the readiness of constituent technologies, represented through TRLs, with the readiness of their interfaces, dependencies, and architectural relationships, represented through IRLs.

SRL is therefore not an average of component maturity. A system may contain individually mature technologies yet have low SRL if critical interfaces, data flows, orchestration logic, performance characteristics, cyber controls, or failure-recovery mechanisms remain unproven in the intended environment.

In formal applications, SRL can be calculated through a normalised matrix of TRL and IRL values across the system architecture. In less complex programmes, it can be assessed through structured evidence against critical components, interfaces, and end-to-end scenarios. The method may vary, but the governing question remains consistent:

> **Does the integrated technical system function reliably, securely, and recoverably in conditions representative of intended use?**

SRL establishes whether the technical system is sufficiently mature to proceed into operational validation. It does not, by itself, establish that people can use the system safely, that operating processes are viable, that accountabilities are clear, or that the organisation can support and sustain the capability in service. Those questions belong to Operational Readiness Level.

## 4. The Human Dimension: HRL

TRL and SRL together still leave a critical gap. They describe whether technologies and their integration are ready; they do not establish whether the humans who use, supervise, maintain, or make decisions with the system are ready, nor whether the system can be used safely and effectively in real operating conditions.

The Human Readiness Level concept was codified in ANSI/HFES 400-2021, *Human Readiness Level Scale in the System Development Process*. It defines HRL as a scale for evaluating, tracking, and communicating readiness for safe and effective human use. The standard positions HRL as complementary to TRL and provides a nine-level structure that mirrors the progression from early concept through operational use (Steelman and Handley, 2022).

**Human Readiness Level (HRL)** concerns the demonstrated readiness of people and human-system interactions. It includes the suitability of the user experience, competence and training, workload, cognitive demand, supervision, procedures, ergonomics, accessibility, trust, and the capacity to identify, manage, and recover from errors.

The HRL scale maps to the same broad developmental phases:

- **Basic research and development (HRL 1–3):** establish the evidence base for human performance in the intended operating context
- **Technology demonstration (HRL 4–6):** evaluate human performance with progressively higher-fidelity representations of the system
- **Full-scale testing, production, and deployment (HRL 7–9):** verify and validate human performance in the actual operational environment

HRL is particularly important in AI-enabled and highly automated systems. A model may be technically capable and fully integrated into a production architecture while the operational capability remains immature: users may not understand when to rely on it, how to challenge it, how to detect degradation, or who holds authority when its recommendation conflicts with professional judgment.

The purpose of HRL is not simply to ensure that users receive training. It is to expose and resolve human-system problems early, when design changes remain feasible and before problems become embedded in infrastructure, procedures, procurement commitments, and organisational habits.

## 5. From System Readiness to Operational Readiness

System readiness and operational readiness should not be treated as synonyms.

**SRL** describes the maturity of the integrated technical system. It is built from evidence about individual technologies and the interfaces between them. SRL answers a necessary technical question: *does the system work as an integrated system in conditions representative of intended use?*

A positive SRL assessment does not yet establish that an organisation is ready to operate the system. Live operation also depends on whether people can use the capability safely and effectively; whether workflows, controls, and exception paths are viable; whether roles and decision rights are clear; whether the service can be supported, monitored, protected, and recovered; and whether the intended mission or business outcome can actually be achieved.

For that reason, this paper defines **Operational Readiness Level (ORL)** as the maturity of the complete socio-technical capability to enter, sustain, and recover from live operations while delivering its intended outcomes.

> **Operational Readiness Level (ORL)** is the demonstrated maturity of a socio-technical capability to operate safely, effectively, sustainably, and accountably within its intended environment. ORL is the executive-level and governance measure used to decide whether a capability may progress to pilot, initial operating capability, scale-up, or full operational service.

ORL incorporates SRL and HRL, but it is broader than either. It assesses whether the complete operating capability—not just the technology—has been proven.

![Operational Readiness Framework](/assets/images/orl.jpg)

### 5.1 The relationship between SRL and ORL

The relationship is hierarchical:

- **TRL and IRL** are primary inputs to SRL
- **SRL** is a critical technical input to ORL
- **HRL**, process readiness, organisational readiness, support and assurance readiness, and outcome readiness are parallel inputs to ORL
- **ORL** is the readiness measure against which an accountable executive should make deployment and operational-acceptance decisions

This resolves a common governance error. A programme may achieve a high SRL and still have a low ORL. For example, an integrated asset-management platform may pass end-to-end technical testing and demonstrate reliable interfaces with field devices, finance systems, and a data platform. Yet it may not be operationally ready if field supervisors have not been trained, maintenance workflows have not been validated, after-hours support is unavailable, incident escalation is unclear, or the organisation has not confirmed how decisions will be made when data from the new platform conflicts with existing records.

### 5.2 ORL dimensions

ORL should be assessed through a structured readiness profile rather than a single technical score.

| ORL dimension | Core question | Illustrative evidence |
|---|---|---|
| System readiness | Does the integrated technical system function reliably in its intended environment? | SRL assessment, end-to-end testing, performance and resilience tests, data-quality results, security testing |
| Human readiness | Can representative users, supervisors, maintainers, and decision-makers use the capability safely and effectively? | HRL assessment, usability testing, competency evidence, training completion, workload analysis, procedure validation |
| Process readiness | Are future-state workflows, controls, hand-offs, exceptions, and recovery procedures viable? | Process trials, standard operating procedures, control testing, exception simulations, reconciliation evidence |
| Organisational readiness | Are roles, accountabilities, decision rights, capacity, incentives, and change arrangements in place? | Operating-model design, RACI, workforce plan, executive ownership, adoption measures, governance forums |
| Support and assurance readiness | Can the capability be supported, protected, monitored, audited, recovered, and improved in service? | Service model, support roster, service-level arrangements, cyber controls, monitoring, incident management, continuity and vendor arrangements |
| Mission or value readiness | Has the organisation demonstrated that the capability enables the outcome for which it was funded? | Operational pilots, mission scenarios, service-quality thresholds, benefits measures, regulatory or compliance evidence |

### 5.3 Weakest critical condition governs

Operational readiness should not be calculated as a simple average. An average can conceal a critical weakness. A capability with strong technical and organisational scores but inadequate human readiness may appear ready numerically even when deployment would be unsafe or predictably ineffective.

The governing principle is therefore:

> **A capability is operationally ready only when every critical condition for safe, effective, sustainable, and accountable operation has been demonstrated to the required level of confidence.**

Conceptually:

$$
\mathrm{ORL} \approx \min\left(
\mathrm{SRL}_{\text{critical}},
\mathrm{HRL}_{\text{critical}},
\mathrm{PRL}_{\text{critical}},
\mathrm{OrgRL}_{\text{critical}},
\mathrm{ARL}_{\text{critical}},
\mathrm{VRL}_{\text{critical}}
\right)
$$

Where the terms represent the maturity of critical requirements in the system, human, process, organisational, assurance, and value dimensions. This expression is not intended to replace judgement with mathematics. Its purpose is to make explicit that a material weakness in a critical condition cannot be offset by strength elsewhere.

In practice, ORL reporting should show:

- The readiness level or confidence assessment for each ORL dimension
- Critical blocking conditions and their accountable owners
- The quality and relevance of the evidence supporting the assessment
- Residual risks and their relationship to approved risk appetite
- A clear decision recommendation: proceed, proceed with constraints, pilot, remediate, defer, or stop

### 5.4 Indicative ORL scale

A nine-level ORL scale aligns conceptually with the wider readiness-level family while retaining a progression meaningful to executives and operational leaders.

| ORL | Stage | Meaning | Decision posture |
|---|---|---|---|
| 1 | Operational need framed | Intended outcome, users, operating context, constraints, and success conditions are identified | Explore and shape |
| 2 | Operating concept defined | High-level operating model, stakeholders, workflows, accountabilities, and assurance needs are identified | Concept approval only |
| 3 | Operational design evidenced | Key processes, roles, support arrangements, human factors, system architecture, and controls are designed and tested in representative scenarios | Prepare pilot |
| 4 | Integrated operational pilot | Integrated system, representative users, processes, support arrangements, and controls are demonstrated in a realistic setting | Controlled pilot or limited release |
| 5 | Initial operating capability | Capability can operate at an agreed initial scope with trained staff, accountable owners, support, monitoring, and recovery arrangements | Conditional go-live |
| 6 | Stable operational capability | Routine operations are reliable; exceptions, incidents, support, and hand-offs function as designed | Scale within validated boundaries |
| 7 | Full operating capability | Capability meets defined mission or business outcomes at intended scale with sustainable governance and operating arrangements | Full deployment |
| 8 | Resilient and optimised operations | Capability demonstrates resilience, learning, continuous improvement, and adaptability to expected variability | Optimise and evolve |
| 9 | Sustained mission-proven capability | Capability demonstrates durable value through real operating cycles, disruption, learning, and adaptation | Business-as-usual capability |

The precise thresholds will differ by sector and risk profile. A safety-critical defence, healthcare, aviation, or critical-infrastructure capability may require stronger evidence at ORL 4–5 than an internal productivity platform. The discipline remains the same: release scope and operational exposure must not exceed the readiness evidence obtained.

## 6. Readiness as a Risk Lens

Readiness imbalances are not merely programme-management problems. They are risk events with financial, reputational, operational, safety, cyber, regulatory, and strategic dimensions. They therefore sit squarely within the accountability of executive leaders and boards.

The ORL framework reframes readiness as a board-legible risk measure. Rather than presenting technical status reports that conflate completion with readiness, it provides a structured picture of whether the integrated system works, whether people can use it, whether operating processes and governance are in place, whether the capability can be supported and assured, and whether intended outcomes have been evidenced.

### 6.1 Readiness risks

Each readiness gap maps to recognisable organisational risks:

- **System readiness gaps** create operational, cyber, performance, resilience, and service-continuity risk. Mature components can fail through immature integration, untested dependencies, poor data quality, or inadequate recovery arrangements.
- **Human readiness gaps** create safety, quality, conduct, productivity, adoption, and incident risk. A technically capable system used incorrectly, misunderstood, bypassed, or distrusted can degrade performance rather than improve it.
- **Process readiness gaps** create control, compliance, error, hand-off, and service-delivery risk. The core workflow may work while exceptions, reconciliation, escalation, and recovery fail.
- **Organisational readiness gaps** create accountability, capacity, incentive, governance, and change-adoption risk. A capability cannot be operated effectively where ownership, decision authority, workforce capacity, or operating-model alignment remains unresolved.
- **Support and assurance gaps** create cyber, reliability, continuity, supplier, audit, and recovery risk. A system may work at go-live but fail when an incident occurs outside business hours or when a dependency degrades.
- **Mission or value gaps** create strategic and financial risk. A deployed system that does not enable the intended mission, service, compliance, or productivity outcome does not justify the investment that created it.

### 6.2 What boards should demand

Boards should not be asked to arbitrate individual interface-maturity scores or detailed usability findings. They should demand evidence that the accountable executive has established sufficient ORL for the proposed operational exposure.

Before approving a material deployment, transition, or scale-up, boards and executive risk committees should seek confirmation that:

- SRL is sufficient for the proposed scope, environment, and critical dependencies
- HRL has been demonstrated with representative users, realistic workload, and credible supervision and recovery arrangements
- Critical operating processes, control points, exception paths, and hand-offs have been tested
- Accountable owners, decision rights, workforce capacity, service support, cyber resilience, and business-continuity arrangements are in place
- The planned release scope matches the maturity demonstrated by the evidence
- Residual risks have named accountable owners and remain within approved risk appetite
- Measures of intended mission, service, compliance, or business value are defined and can be observed after deployment

These are not administrative niceties. They are the minimum controls needed to distinguish technical delivery from operational readiness.

## 7. Application at Scale

The readiness concepts above were developed in contexts where the consequences of failure are large and visible. For national-scale digital systems—such as a universal health-records platform, national taxation system, defence command-and-control infrastructure, or critical-infrastructure operations platform—the ORL framework provides several management instruments:

- Transition gates with objective, evidence-based criteria
- Early visibility of technical, human, process, organisational, and support imbalances
- A common language across engineering, operations, risk, finance, cyber, workforce, and executive stakeholders
- Clear authority for accepting residual readiness risk at each transition point

For small and medium enterprises, the same logic applies, though the assessment can be deliberately lighter. The questions become practical:

- Has this system been demonstrated to work at the scale and operational complexity of our environment?
- Have all material interfaces with existing systems been tested under realistic conditions?
- Have representative people who will use and support the system participated before go-live?
- Are the new processes, accountabilities, controls, and escalation paths clear?
- Who will support the system, manage access, respond to incidents, and recover it when something goes wrong?
- What result should improve after implementation, and how will we know?

The framework should be proportionate, not bureaucratic. The level of evidence should increase with operational consequence, irreversibility, complexity, regulatory exposure, and the cost of failure.

## 8. Common Failure Modes

Several failure modes recur across operational digital-system deployments at every scale.

### 8.1 The component maturity illusion

A programme reports high TRLs for its major technologies and assumes readiness follows. It does not. Mature components can be combined into an immature system when critical interfaces, data flows, identity arrangements, orchestration logic, or recovery procedures are unproven. This is an SRL problem.

### 8.2 The technical completion illusion

A programme completes system integration, passes acceptance tests, and declares success. Yet representative users have not validated the system under realistic workload, supervisors lack reliable procedures, and errors cannot be readily identified or recovered. This is an HRL and ORL problem.

### 8.3 The process and governance gap

The technology and users may be ready, but the organisation has not resolved who owns decisions, who handles exceptions, what service levels apply, how performance is monitored, or how incentives and controls change. This is an organisational and process-readiness problem.

### 8.4 The unsupported go-live

The system works during the planned release window but lacks a functioning service model, monitoring, incident response, supplier support, cybersecurity assurance, or business-continuity capability. This is an assurance and operational-support problem.

### 8.5 The value-realisation gap

The capability reaches production but does not improve the mission, customer service, compliance, productivity, cost, or decision quality for which it was funded. This is a mission-or-value readiness problem. It often arises because benefit measures were never translated into operating-level requirements and tested before scale-up.

## 9. Practical Governance Model

A practical readiness governance model for introducing digital systems, scalable from national programmes to SMEs, rests on six principles:

1. **Parallel maturation, not sequential.** System, human, process, organisational, support, and value dimensions should mature together rather than leaving operational issues until after technical delivery.
2. **SRL is necessary but not sufficient.** Integrated technical maturity is a critical input to deployment, but not the operational acceptance decision.
3. **ORL governs operational release.** ORL is the measure used to decide whether a capability may progress to pilot, initial operating capability, scale-up, or full deployment.
4. **Weakest critical condition governs.** A material weakness in a safety-, mission-, service-, or compliance-critical condition cannot be offset by a high average score elsewhere.
5. **Evidence, not assertion.** Readiness claims should be supported by relevant, representative, traceable evidence rather than status reporting, vendor assurance, or checklist completion alone.
6. **Institutional context is part of the system.** Roles, incentives, decision rights, governance, capacity, support, and culture are not external implementation concerns; they are operating components of the capability.

### 9.1 Governance reporting cascade

The framework also clarifies the role of different governance layers:

| Governance level | Primary readiness measures | Core question |
|---|---|---|
| Engineering, architecture, and cyber | TRL and IRL | Are technologies, interfaces, data flows, controls, and dependencies mature enough? |
| Programme and delivery leadership | SRL and HRL | Does the integrated system work, and can people use it safely and effectively? |
| Operational leadership and executive sponsor | ORL profile | Can this organisation operate, govern, support, and sustain the capability within the proposed scope? |
| Board or risk committee | ORL, residual risk, and benefits confidence | Is the proposed deployment consistent with risk appetite and strategic objectives? |

### 9.2 A readiness gate

Every material transition should end with an explicit readiness decision. The decision record should state:

- The proposed operating scope, users, environment, and exposure
- The assessed ORL and supporting dimension profile
- Critical evidence reviewed and the confidence in that evidence
- Constraints, assumptions, residual risks, and accountable owners
- The conditions under which the release must be paused, rolled back, or escalated
- The post-deployment measures that will verify operational performance and value

This approach prevents the common failure in which a programme declares a system “ready” without stating what it is ready **for**, under what conditions, at what scale, and with what risk acceptance.

## 10. Conclusion

Digital systems do not fail in operation simply because technology is hard. They fail because readiness is multidimensional, while many organisations assess only a narrow technical dimension and mistake completion for operational capability.

TRL provides a disciplined measure of individual technology maturity. IRL assesses the maturity of interfaces and dependencies. SRL uses these inputs to assess whether the integrated technical system is ready for operational validation. HRL assesses whether people can use the capability safely and effectively. These measures are valuable, but they do not on their own answer the question that matters at the point of deployment.

That question is operational: **can the organisation safely, effectively, sustainably, and accountably operate this capability to achieve its intended outcome?**

Operational Readiness Level provides the framework for answering it. ORL places SRL in its proper role—as a necessary technical input—and integrates it with human, process, organisational, assurance, and value evidence. It gives executives and boards a clearer basis for deciding whether to pilot, deploy, scale, defer, or remediate.

Organisations that make this distinction will be better able to expose readiness gaps before those gaps become incidents, remediation programmes, regulatory failures, or forfeited strategic value. The objective is not to add another assessment layer. It is to ensure that the organisation deploys not merely a working system, but a capability it is genuinely prepared to operate.

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

NASA (2023) ‘Technology Readiness Levels’, available at: https://www.nasa.gov/directorates/somd/space-communications-navigation-program/technology-readiness-levels/ (Accessed: 3 June 2026).

Newton, V., Greenberg, A. and See, J. (2017) ‘Project management implications and implementation roadmap of Human Readiness Levels’, *Interacción*.

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
