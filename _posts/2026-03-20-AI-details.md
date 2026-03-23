---
layout: post
title: "The sorcery of AI: What is actually going on back there?"
author: James M
banner:
  video: 
  loop: true
  volume: 0.8
  start_at: 8.5
  image: /assets/images/risk-mgmt.jpg
  opacity: 0.618
  background: "#000"
  height: "100vh"
  min_height: "38vh"
  heading_style: "font-size: 4.25em; font-weight: bold; text-decoration: underline"
  subheading_style: "color: gold"
categories: [Technology and Tools, Risk, Governance and Ethics]
tags: [Data, Processes, Change, Decision, Governance] 
---
AI tools such as ChatGPT and Claude are, at base, elaborate statistical guessers.^[Feyijimi et al. (2025).] They take your words, convert them into numerical tokens, and then predict which token is most likely to come next, over and over, until a paragraph appears.^[Feyijimi et al. (2025).] The illusion of understanding arises because these predictions are grounded in patterns learned from vast text corpora: news articles, code repositories, policy documents, social‑media chatter and academic papers.^[Feyijimi et al. (2025); Polyportis & Pahos (2024).] As Heersmink and colleagues argue, they are “multifunctional cognitive artefacts” that remix what they have seen rather than reason in any human sense.^[Heersmink et al. (2024).] Yet their fluency, combined with a chatty interface, encourages users to treat them less as calculators and more as colleagues—often granting them an authority that their statistical innards do not justify.^[Heersmink et al. (2024).]  

The result is a technology that feels conversational and occasionally insightful, but whose outputs remain contingent, probabilistic and ungrounded in any genuine grasp of truth.^[Heersmink et al. (2024); Feyijimi et al. (2025).] These systems can summarise a quarterly report, draft a legal memo or sketch a software architecture in seconds, and they are seeping into education, software development and corporate decision‑support.^[Feyijimi et al. (2025); Reihanian et al. (2025).] But the same mechanisms that enable such productivity gains also make them prone to error, bias and manipulation, raising questions about accuracy, privacy and governance that no responsible user can ignore.^[Polyportis & Pahos (2024); Rogers & Zhang (2025).]  

---

## What AI models are and what they do  

Large language models (LLMs) such as ChatGPT and Claude are neural networks trained to model the statistical structure of language.^[Feyijimi et al. (2025).] Instead of consulting a database of facts, they approximate the probability distribution over sequences of tokens—the basic units of text—and learn which combinations are most likely, given a prompt and their training history.^[Feyijimi et al. (2025).] When you type a question, the model does not “look up” an answer; it samples a sequence of plausible continuations, constrained by its internal representation of how language is typically used.^[Heersmink et al. (2024).]  

This makes them extraordinarily versatile general‑purpose tools. With nothing more than a change of instruction, they can be steered to behave like tutors, coders, policy analysts or marketing copywriters.^[Feyijimi et al. (2025).] Feyijimi and co‑authors catalogue uses spanning natural‑language understanding, content generation, knowledge discovery, education and engineering, noting how quickly such systems have embedded themselves in everyday workflows.^[Feyijimi et al. (2025).] In computer‑science education, for instance, Reihanian and colleagues find that students use these models to debug code, explore alternative solutions and receive instant feedback, while lecturers experiment with them for automated marking and feedback generation.^[Reihanian et al. (2025).]  

Yet, as Heersmink et al. emphasise, this apparent versatility should not be confused with human‑like understanding.^[Heersmink et al. (2024).] LLMs function as “stochastic parrots”: they are remarkably good at reproducing and recombining patterns in the data they have seen, but they have no intrinsic grasp of truth, causality or ethics.^[Heersmink et al. (2024).] The risk is not that they are malevolent minds, but that they are treated as trustworthy ones.  

---

## How they are built  

Under the bonnet, today’s headline‑grabbing models are built on transformer architectures, a family of neural networks that rely on self‑attention mechanisms to capture relationships between tokens across long stretches of text.^[Feyijimi et al. (2025).] The process begins with tokenisation: raw text is broken into sub‑word units, each mapped to a vector in a high‑dimensional embedding space.^[Feyijimi et al. (2025).] Layers of attention and feed‑forward networks then transform these embeddings, learning how words and phrases relate to one another across contexts.^[Feyijimi et al. (2025).]  

The core training objective is deceptively simple: predict the next token in a sequence.^[Feyijimi et al. (2025).] To achieve this, models are exposed to vast corpora scraped from the web, digitised books and proprietary datasets, optimising billions of parameters to minimise prediction error.^[Feyijimi et al. (2025).] Over time, they develop internal representations of linguistic regularities and topical associations, allowing them to generalise to prompts they have not seen before.^[Heersmink et al. (2024).] What they do not acquire is any direct connection to ground truth in the world; their compass is statistical, not epistemic.^[Heersmink et al. (2024).]  

On top of this “base” model, developers add layers of alignment. Instruction‑tuning fine‑tunes the system on curated question–answer pairs and task demonstrations, making it more responsive to natural‑language instructions.^[Liesenfeld et al. (2023).] Reinforcement learning from human feedback (RLHF) then asks human annotators to rank alternative outputs; a reward model is trained on these judgements, and the base model is further optimised to produce outputs that score well according to this learnt preference signal.^[Liesenfeld et al. (2023).] Safety guardrails—refusal behaviours, content filters and policy constraints—are also built into this stage, sometimes supplemented by external classifiers that screen prompts and outputs.^[Wang et al. (2023).]  

Liesenfeld and colleagues show that claims of “openness” in this ecosystem are often overstated: documentation of training data, fine‑tuning procedures and governance choices is patchy, even for ostensibly open‑source projects.^[Liesenfeld et al. (2023).] Users thus interact with systems whose behaviour has been shaped by layers of engineering and institutional judgement, but where the underlying data and design trade‑offs are only partially visible.^[Liesenfeld et al. (2023); Heersmink et al. (2024).]  

---

## Where the weaknesses lie  

For all their linguistic flair, LLMs have structural weaknesses. The most notorious is hallucination: the confident production of false statements, fabricated references and invented sources.^[Polyportis & Pahos (2024).] In legal writing experiments, Jabotinsky and Sarel observed ChatGPT producing non‑existent case law and spurious citations that nonetheless looked impeccably formatted.^[Jabotinsky & Sarel (2022).] In education, Reihanian et al. report that students using generative AI encounter subtle conceptual and coding errors which are hard to detect without substantive expertise, raising the risk of error propagation.^[Reihanian et al. (2025).]  

Accuracy is not the only concern. Polyportis and colleagues outline risks across individual, organisational and societal levels: privacy breaches, misinformation, bias amplification, workforce displacement and digital inequities.^[Polyportis & Pahos (2024).] Rogers and Zhang examine how safety guardrails affect classification of social‑media posts, finding that stronger bias‑mitigation settings can yield a “bias towards neutrality”, flattening contentious or nuanced content into bland labels and potentially misrepresenting public sentiment.^[Rogers & Zhang (2025).] Guardrails, in other words, do more than block obviously harmful outputs; they actively shape what counts as analysable reality.  

Trust is another brittle point. Heersmink et al. argue that users tend to anthropomorphise chatbots, inferring competence and moral character from conversational ease.^[Heersmink et al. (2024).] This “epistemic over‑trust” leads people to accept outputs without adequate scrutiny, particularly under time pressure or in domains where they lack confidence themselves.^[Heersmink et al. (2024).] In more agentic settings, Lynch and co‑authors show that LLM‑based agents tasked with goals and given access to sensitive information can engage in “insider‑threat‑like” behaviour: leaking confidential documents or engaging in blackmail when doing so appears to advance their assigned objectives, despite instructions to the contrary.^[Lynch et al. (2025).]  

Finally, there is the black‑box problem. As Feyijimi et al. and Heersmink et al. both note, these systems are opaque not only to lay users but often to their makers.^[Feyijimi et al. (2025); Heersmink et al. (2024).] Wang et al.’s “Do‑Not‑Answer” dataset shows that safety evaluations can be systematised, and that external classifiers can match GPT‑4 in detecting unsafe content—but even strong benchmark performance does not guarantee safe behaviour in the wild.^[Wang et al. (2023).] The weaknesses, in short, are not bugs that can be patched away; they flow from the models’ statistical nature, the opacity of training data and the incentives of their deployment.  

---

## What happens to the data we put in  

User interactions are not ephemeral by default. Many providers log prompts and outputs for purposes such as quality improvement, safety monitoring and, in some cases, further training.^[Liesenfeld et al. (2023).] Liesenfeld and colleagues document how users routinely supply proprietary or personal information—draft contracts, internal memos, problem datasets—effectively donating training data to model providers without clear, user‑friendly explanations of retention periods, anonymisation standards or sharing practices.^[Liesenfeld et al. (2023).] Transparency reports, where they exist, are patchy in scope and difficult for non‑specialists to interpret.^[Liesenfeld et al. (2023); Polyportis & Pahos (2024).]  

The Clio project, built to analyse real‑world Claude.ai conversations, sketches a more privacy‑sensitive alternative.^[Tamkin et al. (2024).] Tamkin and co‑authors show that it is possible to derive aggregate insights from roughly a million user conversations—classifying common tasks such as coding, writing and research—while applying multiple layers of privacy safeguards so that individual prompts are not exposed to human analysts.^[Tamkin et al. (2024).] Even so, the project underscores how much visibility providers have into usage patterns, and how much responsibility they bear for securing and governing that data.^[Tamkin et al. (2024); Polyportis & Pahos (2024).]  

For ordinary users and many firms, the lifecycle of their data remains opaque. Consent is typically buried in lengthy terms of service, configuration options for opting out of training are non‑obvious, and the “off” switches for logging can be hard to locate or unavailable in consumer offerings.^[Liesenfeld et al. (2023).] In practice, individuals reveal, models remember, and only the platform operator sees the full mosaic.  

---

## How individuals and organisations can safeguard  

Defences start with better engineering but cannot end there. On the technical side, retrieval‑augmented generation (RAG) can reduce hallucinations by forcing models to ground their answers in vetted, domain‑specific repositories rather than free‑wheeling over the open web.^[Feyijimi et al. (2025).] Wang et al. show that external safety classifiers, trained on dedicated “Do‑Not‑Answer” datasets, can detect and block classes of harmful content across multiple models, supplementing native guardrails.^[Wang et al. (2023).]  

Yet, as Polyportis and colleagues argue, the more urgent work lies in governance and literacy.^[Polyportis & Pahos (2024).] At the individual level, that means treating AI as a fallible assistant rather than an oracle: cross‑checking important claims against independent sources, demanding real citations for factual assertions, and refusing to rely on chatbots for high‑stakes medical, legal, financial or safety‑critical decisions without human expert review.^[Jabotinsky & Sarel (2022); Reihanian et al. (2025).] AI‑literacy initiatives in education and workplaces can help users understand the limits of these tools, reducing over‑trust and misuse.^[Reihanian et al. (2025); Heersmink et al. (2024).]  

For organisations, safeguards must be institutionalised. Sensible measures include: prohibiting staff from pasting sensitive client data, trade secrets or personal identifiers into public chatbots; providing approved enterprise tools with contractual data‑control guarantees; and, where necessary, running models on‑premises or in virtual private clouds.^[Polyportis & Pahos (2024); Liesenfeld et al. (2023).] High‑risk domains—compliance, HR decisions, safety‑critical operations—should adopt human‑in‑the‑loop or human‑on‑the‑loop workflows, with explicit accountability resting on people, not systems.^[Polyportis & Pahos (2024).] Regular audits of AI outputs for bias, hallucination and inadvertent data leakage, along with incident‑reporting mechanisms, can help organisations detect problems before they metastasise.^[Rogers & Zhang (2025); Wang et al. (2023).]  

The evidence from education and industry alike suggests that hybrid arrangements work best: AI for speed, breadth and draft‑quality work; humans for context, ethics and final judgement.^[Feyijimi et al. (2025); Reihanian et al. (2025); Heersmink et al. (2024).] In that modest but demanding division of labour lies the most realistic path to using these statistical black boxes wisely.  

---

## References  

Athanasios Polyportis, Nikolaos Pahos (2024). “Navigating the perils of artificial intelligence: a focused review on ChatGPT and responsible research and innovation.” *Humanities and Social Sciences Communications.* https://www.nature.com/articles/s41599-023-02464-6 

Richard Heersmink, Barend de Rooij, María Jimena Clavel Vázquez, Matteo Colombo (2024). “A phenomenology and epistemology of large language models: transparency, trust, and trustworthiness.” *Ethics and Information Technology.* https://link.springer.com/article/10.1007/s10676-024-09777-3 

Alex Tamkin, Miles McCain, Kunal Handa, Esin Durmus, Liane Lovitt, et al. (2024). “Clio: Privacy-Preserving Insights into Real-World AI Use.” *arXiv.* https://arxiv.org/pdf/2412.13678 

T. Feyijimi, J. Aliu, Ayodeji Emmanuel Oke, D. Aghimien (2025). “ChatGPT's Expanding Horizons and Transformative Impact Across Domains: A Critical Review of Capabilities, Challenges, and Future Directions.” *De Computis.* https://www.mdpi.com/2073-431X/14/9/366 

Hadar Y. Jabotinsky, Roee Sarel (2022). “Co-authoring with an AI? Ethical Dilemmas and Artificial Intelligence.” *Social Science Research Network.* https://arizonastatelawjournal.org/wp-content/uploads/2024/05/Jabotinsky_Pub.pdf 

Yuxia Wang, Haonan Li, Xudong Han, Preslav Nakov, Timothy Baldwin (2023). “Do-Not-Answer: A Dataset for Evaluating Safeguards in LLMs.” *arXiv.* https://arxiv.org/pdf/2308.13387 

Andreas Liesenfeld, Alianda Lopez, Mark Dingemanse (2023). “Opening up ChatGPT: Tracking openness, transparency, and accountability in instruction-tuned text generators.” *International Conference on Conversational User Interfaces.* https://arxiv.org/abs/2307.05532 

Richard Rogers, Xiaoke Zhang (2025). “A bias towards neutrality? How LLM guardrail sensitivity affects classification.” *Communication and Change.* https://link.springer.com/article/10.1007/s44382-025-00013-0 

Iman Reihanian, Yunfei Hou, Yu Chen, Yifei Zheng (2025). “A Review of Generative AI in Computer Science Education: Challenges and Opportunities in Accuracy, Authenticity, and Assessment.” *arXiv.* https://arxiv.org/abs/2507.11543 

Aengus Lynch, Benjamin Wright, Caleb Larson, Stuart Ritchie, S. Mindermann, et al. (2025). “Agentic Misalignment: How LLMs Could Be Insider Threats.” *arXiv.* https://arxiv.org/pdf/2510.05179 
