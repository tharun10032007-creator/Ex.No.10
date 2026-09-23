# Ex.No.10 – Content Creation (Reports, Articles, Case Studies, etc.) Using Prompt Patterns

## Aim

To demonstrate how various prompting techniques (query decomposition, decision-making, answer engineering, fact-check listing, tail generation, menu actions, and semantic filtering) can be employed to create content such as reports, articles, and case studies for a chosen engineering domain, using ChatGPT or similar models. The objective is to highlight how different prompt structures affect the content's quality, coherence, and structure.

## Engineering Domain Selected

**Agriculture**

## Selected Project

**AgriTwin – A Unified Multi-Crop Digital Twin for Explainable AI-Driven Crop Monitoring and Intelligent Farm Management**
*(Category: Smart Agriculture Advisor)*

AgriTwin builds a continuously updated virtual replica of a farm that monitors **multiple crop types simultaneously**, integrating IoT soil sensors, drone/satellite imagery, and weather data with AI models that predict irrigation needs, pest/disease outbreaks, and yield — while an **Explainable AI (XAI)** layer translates model outputs into plain-language justifications for farmers.

## Problem Statement

Farmers managing multi-crop farms currently lack a unified, real-time view of soil, canopy, and pest conditions across all their crop zones at once — most monitoring tools are single-crop or single-sensor solutions that don't talk to each other. In addition, existing AI-driven farm advisory systems tend to behave as "black boxes," issuing recommendations (e.g., "irrigate now" or "apply pesticide") without explaining the reasoning, which reduces farmer trust and adoption — especially among non-technical users in rural areas.

There is also a **content communication gap**: technical research on digital twins and explainable AI is rarely translated into farmer-facing reports, case studies, or educational articles that a cooperative, extension officer, or investor could actually read and act on.

This experiment addresses that gap by using structured prompt patterns to generate two forms of accessible content about the AgriTwin system: a **case study** documenting its real-world deployment, and an **educational article** explaining explainable AI in agriculture to a general audience.

## Selected Content Generation Scenarios (2 of the listed options)

1. **Case Study** — "AgriTwin: A Case Study in Multi-Crop Digital Twin Deployment"
2. **Article** — "Explainable AI in Agriculture: How Digital Twins Are Changing Farm Management"

## Prompt Patterns Used and How They Were Applied

| Pattern | Application in This Experiment |
|---|---|
| **Query Decomposition** | The broad request "write about AgriTwin" was broken into smaller sub-queries: background, architecture, deployment results, challenges, and farmer impact — each generated separately, then merged. |
| **Decision Making** | The model was asked to choose between two narrative angles for the case study ("technology-first" vs. "farmer-impact-first") and justify the choice before writing. |
| **Answer Engineering** | Detailed formatting instructions (headings, word limits, table use, audience level) were given to control structure and readability. |
| **Fact Check List** | The model was instructed to list every technical claim it planned to make (e.g., sensor types, XAI method, yield figures) before drafting, so each could be checked against the actual AgriTwin project description. |
| **Tail Generation** | After the initial case study draft, the model was asked to extend the narrative with a "lessons learned" and "future roadmap" section, deepening the analysis. |
| **Menu Actions** | The model was presented with multiple possible article angles (technical explainer, farmer testimonial style, policy-brief style) and asked to select and justify the best one for a general audience. |
| **Semantic Filter** | The model was instructed to rewrite the article in a specific tone (optimistic but balanced, non-jargon, accessible to non-technical readers) after the first technical draft. |

## Prompt Design and Iteration

### Content 1: Case Study – "AgriTwin: A Case Study in Multi-Crop Digital Twin Deployment"

#### Basic Prompt (First Draft)
```
Write a short case study about a digital twin system used for monitoring
multiple crops on a farm using AI.
```

**Sample Output (First Draft — abbreviated):**
> A farm implemented a digital twin system to monitor its crops using sensors and AI. The system tracked soil and weather data and gave recommendations to farmers. It helped detect problems early and improved yield. The project showed that digital twins can be useful for agriculture.

**Observation:** Generic, no specific facts, numbers, or structure — reads more like a summary than a case study.

#### Refined Prompt (Query Decomposition + Fact Check List)
```
Before writing, list the key factual claims you will make about the
following project, based only on the details provided:

Project: AgriTwin – A Unified Multi-Crop Digital Twin for Explainable
AI-Driven Crop Monitoring and Intelligent Farm Management.
Details: Four-layer architecture (data acquisition, synchronization,
AI-analytics, decision-support); monitors multiple crop zones (wheat,
maize, vegetables) simultaneously; uses IoT soil sensors, drone/satellite
imagery, CNN-based disease detection, LSTM-based yield prediction, and
an explainable AI (XAI) layer using SHAP-style feature importance.

Then write a 300-word case study covering: background, system
architecture, deployment scenario, results, and challenges.
```

**Sample Output (Refined Draft — abbreviated):**
> **Fact list:** (1) four-layer architecture, (2) multi-crop zone monitoring, (3) CNN for disease detection, (4) LSTM for yield prediction, (5) SHAP-style explainability layer.
>
> **Case Study:** AgriTwin was deployed across a farm growing wheat, maize, and vegetables in adjacent zones. Its four-layer architecture synchronizes real-time sensor and imagery data with a virtual twin of each zone... [continues with architecture, deployment, results, and challenges sections]

**Observation:** Listing facts first noticeably reduced invented details and kept the case study grounded in the actual project architecture.

#### Advanced / Final Prompt (Decision Making + Answer Engineering + Tail Generation)
```
Two possible narrative angles are available for this case study:
(a) technology-first — leading with architecture and AI methods, or
(b) farmer-impact-first — leading with the on-the-ground outcome for
farmers and only then explaining the technology.

Choose the angle best suited for an audience of agricultural extension
officers and investors, and briefly justify your choice.

Then write the full case study (400-500 words) in this structure:
1. Background
2. System Overview
3. Deployment Scenario
4. Results and Impact
5. Challenges Faced
6. Lessons Learned
7. Future Roadmap

Use a professional, confident, but non-exaggerated tone. Present
key results in a table.
```

**Sample Output (Final Version — abbreviated):**
> **Chosen angle:** Farmer-impact-first, because extension officers and investors respond more strongly to demonstrated outcomes before technical depth.
>
> **1. Background:** Multi-crop farms often rely on single-crop monitoring tools that fail to capture cross-zone patterns... **2. System Overview:** AgriTwin's four layers — data acquisition, synchronization, AI-analytics, and decision-support — work together to... **3. Deployment Scenario:** Piloted across wheat, maize, and vegetable zones on one farm...
>
> | Metric | Before AgriTwin | After AgriTwin |
> |---|---|---|
> | Early pest detection | Reactive | Proactive, model-flagged |
> | Irrigation decisions | Manual, uniform | Zone-specific, data-driven |
> | Farmer trust in AI advice | Low (black-box) | Higher (explainable reasoning) |
>
> **5. Challenges Faced:** High computing cost, sensor data gaps... **6. Lessons Learned:** Explainability was the single biggest driver of farmer adoption... **7. Future Roadmap:** Lightweight edge-deployable models for low-connectivity rural areas.

**Observation:** Choosing a narrative angle before writing produced a case study with a clearer point of view; the tail-generation instruction (Lessons Learned + Future Roadmap) added depth beyond a simple results summary.

---

### Content 2: Article – "Explainable AI in Agriculture: How Digital Twins Are Changing Farm Management"

#### Basic Prompt (First Draft)
```
Write an article about explainable AI in agriculture.
```

**Sample Output (First Draft — abbreviated):**
> Explainable AI (XAI) is important in agriculture because it helps farmers understand AI decisions. Many AI systems are complex, and XAI makes them more transparent. This can improve trust and adoption of AI tools in farming.

**Observation:** Accurate but shallow, generic, and disconnected from any real system or example.

#### Refined Prompt (Menu Actions + Semantic Filter)
```
Here are three possible angles for this article:
(1) Technical explainer of XAI methods (SHAP, LIME) in agriculture
(2) Farmer-testimonial style, told through a fictional composite farmer's
    experience with a digital twin system
(3) Policy-brief style, aimed at agricultural policymakers

Select the angle best suited for a general undergraduate audience with
some technical background, and explain why.

Then write a 350-word article using that angle, referencing the AgriTwin
digital twin system as the central example. Use an optimistic but
balanced tone — acknowledge both benefits and current limitations.
Avoid heavy jargon; briefly explain any technical term on first use.
```

**Sample Output (Refined Draft — abbreviated):**
> **Chosen angle:** Technical explainer, lightly narrated — best balances depth and accessibility for an undergraduate audience already familiar with basic AI concepts.
>
> Modern farms increasingly rely on AI models to decide when to irrigate, which zones need pest treatment, and how much fertilizer to apply. But most of these models work as "black boxes" — they output a recommendation without saying why. Explainable AI (XAI) — techniques that make a model's reasoning visible to humans — is changing that. In systems like AgriTwin, a unified multi-crop digital twin, an XAI layer uses SHAP-style feature-importance scores to rank which sensor readings (soil moisture, NDVI trend, pest-detection confidence) most influenced a recommendation, then translates that ranking into a plain-language explanation a farmer can act on...
>
> XAI isn't a complete solution, though — it adds computational overhead, and translating complex model internals into truly simple language remains an open challenge...

**Observation:** Selecting an angle explicitly (menu actions) before drafting, followed by a tone-adjustment instruction (semantic filter), produced a more focused and appropriately pitched article than the generic first draft.

#### Final Version (After Semantic Filter Iteration)
```
Rewrite the article above, applying this semantic filter: make the tone
warmer and more narrative without losing technical accuracy — open with
a short relatable scenario before introducing the technical explanation.
```

**Sample Output (Final Version — abbreviated):**
> Picture a farmer checking a phone app one morning and seeing a simple message: "Zone 3 needs water — soil moisture is 18%, and no rain is expected for five days." No jargon, no black box — just a clear reason. That's the promise of explainable AI (XAI) in agriculture, and it's exactly what systems like AgriTwin are built to deliver...
> [continues into the technical explanation with the same core content, now framed narratively]

**Observation:** The semantic-filter rewrite kept every technical fact from the previous draft while substantially improving readability and engagement — demonstrating that tone and accuracy can be adjusted independently through iterative prompting.

## AI Output Evaluation

| Content | Version | Coherence | Creativity/Originality | Accuracy | Tone & Style | Overall |
|---|---|---|---|---|---|---|
| Case Study | Basic (First Draft) | Fair | Low | Fair (vague) | Generic | 5.5 / 10 |
| Case Study | Refined | Good | Moderate | Good (fact-checked) | Neutral | 7.5 / 10 |
| Case Study | Final (Advanced) | Excellent | Good | Excellent | Confident, professional | 9.2 / 10 |
| Article | Basic (First Draft) | Fair | Low | Good but shallow | Generic | 5 / 10 |
| Article | Refined (Menu + Filter) | Good | Good | Good | Appropriately pitched | 7.8 / 10 |
| Article | Final (Semantic Filter Rewrite) | Excellent | High | Good | Warm, narrative, accessible | 9.0 / 10 |

**Summary:** Across both content types, coherence and accuracy improved most sharply after introducing the **Fact Check List** and **Query Decomposition** patterns, while creativity and engagement improved most after **Menu Actions** and **Semantic Filtering** were applied. The **Decision Making** pattern was most valuable for giving the final case study a clear narrative point of view, and **Tail Generation** added meaningful depth (Lessons Learned, Future Roadmap) that basic prompts never produced on their own.

## Ethical Considerations

- **Accuracy of agronomic claims:** Any yield, water-saving, or pest-detection figures generated by the AI must be verified against real field data before publication — AI-generated statistics in a case study can be plausible-sounding but fabricated.
- **Avoiding overreliance on AI-generated farm advice:** Content describing AgriTwin's recommendations should make clear that outputs are decision-support, not a replacement for a qualified agronomist's judgment.
- **Transparency about AI-assisted authorship:** Reports, case studies, and articles generated with AI assistance should disclose that AI tools were used in drafting, especially where the content will inform real investment or extension decisions.
- **Bias in multi-crop recommendations:** Training data for the underlying pest/disease and yield models may underrepresent certain regions or crop varieties; content describing model performance should avoid overstating generalizability.
- **Data privacy:** Case studies referencing specific farms or cooperatives must anonymize or obtain consent for any sensor, yield, or financial data before publication.
- **Balanced narrative:** Articles on AI in agriculture should avoid both uncritical hype (overstating benefits) and unwarranted alarmism (job displacement narratives) — the semantic-filter step here was explicitly used to keep tone "optimistic but balanced."

## Final Presentation (Outline)

1. **Title Slide** — AgriTwin: Using Prompt Patterns to Generate Explainable Agricultural Content
2. **Problem Statement** — the multi-crop monitoring gap and the black-box trust problem
3. **Engineering Domain & Project Overview** — Agriculture / AgriTwin architecture recap (four-layer digital twin)
4. **Prompt Patterns Demonstrated** — one slide per pattern with a before/after prompt snippet
5. **Case Study Highlights** — key results table, chosen narrative angle, lessons learned
6. **Article Highlights** — chosen angle, tone evolution (technical → narrative)
7. **AI Output Evaluation Summary** — scoring table and key takeaways
8. **Ethical Considerations** — top 3 risks and mitigations
9. **Conclusion & Future Work** — extending the prompt-pattern approach to other content (FAQs, training materials, investor decks)
10. **Live Demonstration** — walkthrough of one prompt iteration live in ChatGPT, from basic to final version

## Deliverables

- **Complete Project Report** — this document, covering problem statement, prompt design, iteration, evaluation, and ethics
- **Prompt Repository** — the full set of basic, refined, and final prompts for both the case study and the article (see Prompt Design and Iteration section above), organized for reuse
- **Presentation** — slide deck following the outline above
- **Demonstration** — live or recorded walkthrough showing the case study/article prompts being run and refined in real time

## Conclusion

By applying structured prompt patterns — query decomposition, decision making, answer engineering, fact check listing, tail generation, menu actions, and semantic filtering — to the AgriTwin multi-crop digital twin project, this experiment produced a case study and an article that were significantly more coherent, accurate, and engaging than their basic-prompt counterparts. The experiment demonstrates that structured prompting can guide AI models like ChatGPT to create high-quality, domain-specific content for agricultural engineering communication, while ethical review remains essential to ensure factual accuracy, appropriate disclosure, and balanced framing before such content is used in real decision-making contexts.
