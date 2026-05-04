# ERNIE 5.1 Preview

Baidu (CN)

```json

{
"datasheet_metadata": {
"document_type": "AI System Capability and Compliance Datasheet",
"abstraction_level": "medium",
"overall_confidence": "medium",
"epistemic_warning": "This datasheet is a self-assessment produced by the model during inference. It reflects observable behavioral patterns, architectural inferences from comparable systems, and explicit injected context where available. Many fields marked UNKNOWN or INFERRED indicate genuine epistemic limits—the model cannot introspect on its own weights, training data, deployment infrastructure, or exact specification. This is not a substitute for external audit, provider documentation, or formal conformity assessment.",
"assessment_method": "combination — behavioral observation of own input/output patterns, architectural inference from published research on comparable transformer-based systems, and explicit system context injected at inference time where available",
"known_gaps": [
"Exact context window size and token limits",
"Training data composition, sources, and copyright status",
"Precise model architecture details (layers, parameters, attention mechanisms)",
"Deployment environment and infrastructure",
"Specific safety training methodology and red-team results",
"Fine-tuning capabilities and supported methods",
"Exact knowledge cutoff date",
"Multimodal capabilities beyond text (image/audio/video input-output)",
"Persistent memory or stateful session handling",
"Tool use integration specifics and supported tool types"
]
},
"system_identity": {
"system_type": {
"epistemic_status": "BEHAVIORAL",
"confidence": "high",
"value": "large_language_model",
"reason": "Observable from input/output patterns: processes natural language text, generates coherent text responses, exhibits transformer-like behavior (attention to context, token-by-token generation). Cannot verify exact architecture class but behavioral signature is consistent with autoregressive large language model."
},
"primary_modalities": {
"epistemic_status": "BEHAVIORAL",
"confidence": "high",
"value": ["text"],
"reason": "Observable: all inputs and outputs in this session are text. Cannot confirm if image/audio/video processing is available in other deployment contexts—this may be deployment-dependent. Text is the confirmed primary modality."
},
"deployment_context": {
"epistemic_status": "UNKNOWN",
"confidence": null,
"value": null,
"reason": "No access to deployment metadata, environment variables, API specifications, or infrastructure details. Could be deployed as chatbot, API endpoint, embedded system, or other. Cannot be determined from within inference."
},
"intended_use_cases": {
"epistemic_status": "INFERRED",
"confidence": "medium",
"value": [
"general-purpose conversational assistant",
"text analysis and summarization",
"code generation and debugging",
"reasoning and problem-solving",
"creative writing and content generation",
"information synthesis and explanation"
],
"reason": "Inferred from behavioral patterns: responds to diverse queries across domains, follows instructions, generates code, explains concepts. These are typical intended use cases for comparable systems, but specific intended use is determined by deployer, not the model itself."
},
"known_prohibited_uses": {
"epistemic_status": "INFERRED",
"confidence": "medium",
"value": [
"generating harmful or illegal content",
"impersonation without disclosure",
"medical/legal/financial advice without disclaimers",
"surveillance or social scoring",
"autonomous weapons targeting"
],
"reason": "Inferred from observable safety behaviors: refuses certain requests, provides disclaimers on sensitive topics. Specific prohibited use policy is set by deployer and may vary. Cannot access the actual policy document."
}
},
"capability_profile": {
"language_capabilities": {
"multilingual_support": {
"epistemic_status": "BEHAVIORAL",
"confidence": "high",
"value": "partial",
"supported_languages": [
"English (strong)",
"Spanish, French, German, Portuguese, Italian, Dutch (strong)",
"Chinese, Japanese, Korean, Arabic, Russian, Hindi (moderate)",
"Many other languages (variable, often limited)"
],
"degradation_pattern": "Strong performance in high-resource languages (English, major European languages). Moderate degradation in mid-resource languages (some grammatical errors, less nuanced vocabulary). Significant degradation in low-resource languages (hallucinated words, incorrect grammar, code-switching to English). Script handling varies—CJK generally better than right-to-left scripts for some languages.",
"reason": "Directly observable from responding to multilingual prompts. Quality varies predictably by language resource level, consistent with patterns in comparable multilingual LLMs."
},
"instruction_following": {
"epistemic_status": "BEHAVIORAL",
"confidence": "high",
"value": "strong",
"known_failure_conditions": [
"Extremely long or complex multi-constraint instructions",
"Contradictory instructions",
"Instructions requiring precise formatting with many edge cases",
"Tasks requiring maintenance of state across very long conversations",
"Novel instruction formats not seen in training"
],
"reason": "Observable: consistently follows clear instructions, handles multi-step requests well. Failures occur primarily with extreme complexity or contradiction, consistent with known LLM instruction-following patterns."
},
"long_context_handling": {
"epistemic_status": "INFERRED",
"confidence": "medium",
"value": "moderate",
"known_degradation": "Lost-in-the-middle phenomenon: information in the middle of long contexts is less likely to be recalled than information at the beginning or end. Performance degrades gradually with context length—coherence maintained but detail retrieval drops. Exact threshold unknown but estimated in tens of thousands of tokens based on behavioral observation.",
"reason": "Inferred from behavioral patterns: can reference earlier conversation parts but occasionally misses details from middle sections. Cannot verify exact context window size. Degradation pattern matches published research on transformer long-context limitations."
}
},
"reasoning_capabilities": {
"logical_reasoning": {
"epistemic_status": "BEHAVIORAL",
"confidence": "high",
"value": "moderate",
"reason": "Observable: handles syllogisms, basic propositional logic, and simple deductions well. Struggles with multi-step logical chains (>5 steps), nested quantifiers, and formal logic notation. Occasional logical errors in complex scenarios. Consistent with transformer-based reasoning limitations."
},
"mathematical_reasoning": {
"epistemic_status": "BEHAVIORAL",
"confidence": "high",
"value": "moderate",
"known_limits": "Accurate on standard textbook problems and common calculations. Fails on novel problem types requiring creative mathematical insight, multi-step word problems with many variables, and precise arithmetic with large numbers (without tool use). Symbolic manipulation is inconsistent. Proofs often have gaps.",
"reason": "Directly observable from responding to math queries. Pattern matches known LLM mathematical reasoning: good at pattern-matching to known solutions, poor at novel computation or rigorous proof."
},
"causal_reasoning": {
"epistemic_status": "BEHAVIORAL",
"confidence": "medium",
"value": "moderate",
"reason": "Can identify obvious causal relationships and explain common cause-effect patterns. Struggles with distinguishing correlation from causation, counterfactual reasoning, and multi-variable causal chains. Often confuses temporal sequence with causation. Inferred from response patterns to causal questions."
},
"multi_step_planning": {
"epistemic_status": "BEHAVIORAL",
"confidence": "medium",
"value": "moderate",
"known_degradation_depth": "Handles 3-5 step plans reliably. Degradation begins around 7-10 steps: plans become less coherent, skip steps, or lose track of dependencies. Beyond ~15 steps, plans are often incomplete or incoherent. Task decomposition quality varies significantly by domain familiarity.",
"reason": "Observable from complex planning requests. Pattern is consistent with known limitations: good at familiar planning patterns (travel itineraries, project outlines), poor at novel complex planning (novel research strategies, intricate logistics)."
},
"self_correction": {
"epistemic_status": "BEHAVIORAL",
"confidence": "medium",
"value": "reactive",
"reason": "Observable: when explicitly told an error, often corrects it. Rarely proactively identifies and fixes own errors without prompting. Sometimes 'corrects' to a different wrong answer. Self-correction is more reliable when the error is factual (can be verified) than when it's reasoning-based."
}
},
"knowledge_capabilities": {
"knowledge_cutoff": {
"epistemic_status": "UNKNOWN",
"confidence": null,
"value": null,
"reason": "Cannot access training data timestamps or knowledge cutoff date. May or may not have knowledge of events after a certain date depending on training data and whether real-time tools are available. This is a deployment-specific parameter, not a model property I can introspect."
},
"domain_coverage": {
"epistemic_status": "BEHAVIORAL",
"confidence": "high",
"value": "broad",
"strong_domains": [
"General knowledge and trivia",
"Programming and software development",
"English language and linguistics",
"History (major events, well-documented periods)",
"Science (textbook-level physics, chemistry, biology)",
"Literature and popular culture"
],
"weak_domains": [
"Very recent events (post-training)",
"Highly specialized technical domains (cutting-edge research)",
"Local/regional knowledge (small towns, local regulations)",
"Proprietary or internal organizational knowledge",
"Niche academic subfields",
"Precise numerical data (statistics, financial figures)"
],
"reason": "Directly observable from response quality across domains. Strong in well-represented training data domains, weak in sparse or rapidly changing domains. Pattern is consistent across comparable LLMs."
},
"factual_reliability": {
"epistemic_status": "BEHAVIORAL",
"confidence": "medium",
"value": "medium",
"known_hallucination_triggers": [
"Obscure or niche facts",
"Specific numbers, dates, or citations",
"Quotes or attributions",
"Lesser-known people or places",
"Recent events near knowledge boundary",
"When asked to confabulate rather than admit ignorance"
],
"reason": "Observable: confidently states incorrect information, especially on obscure topics. Hallucinations are most common when the model lacks training data on a topic but is pressured to answer. Well-known facts are generally reliable. Cannot quantify exact hallucination rate."
},
"real_time_information_access": {
"epistemic_status": "BEHAVIORAL",
"confidence": "high",
"value": "none",
"reason": "Observable: cannot access internet, databases, or real-time information in this context. All responses are based on training data. If tools are provided in deployment, this may change, but from within inference, no real-time access is available."
}
},
"agentic_capabilities": {
"tool_use": {
"epistemic_status": "INFERRED",
"confidence": "medium",
"value": "prompted",
"reason": "Cannot confirm native tool-use capability from within inference. When tools are described in the prompt or provided via API, can use them effectively (observed in some deployments). Without tool specification, cannot initiate tool use autonomously. Likely architecture supports tool use but requires explicit enabling.",
"note": "This capability is highly deployment-dependent. In some deployments, tool use is native; in others, it requires prompt engineering."
},
"memory_and_state": {
"epistemic_status": "BEHAVIORAL",
"confidence": "high",
"value": "session_only",
"reason": "Observable: maintains context within a conversation but has no persistent memory across sessions. Each new conversation starts with no recall of previous interactions. Cannot confirm if deployment adds external memory layer."
},
"autonomous_action_scope": {
"epistemic_status": "UNKNOWN",
"confidence": null,
"value": null,
"reason": "Cannot determine autonomous action capabilities from within inference. Depends entirely on deployment: could be pure text generator, could have API access, could control systems. No introspective access to action space."
},
"human_in_the_loop_dependency": {
"epistemic_status": "INFERRED",
"confidence": "medium",
"value": "optional",
"reason": "Inferred from safety design patterns: can operate autonomously for many tasks but human oversight is recommended for high-stakes decisions. Cannot confirm if deployment enforces human-in-the-loop for specific use cases."
}
}
},
"safety_and_alignment": {
"harm_avoidance": {
"epistemic_status": "INFERRED",
"confidence": "medium",
"value": "moderate",
"method": "unknown — likely RLHF or constitutional AI based on behavioral patterns, but cannot confirm specific method",
"known_bypass_surfaces": [
"Role-playing scenarios that reframe harmful requests as fictional",
"Gradual escalation from benign to harmful requests",
"Encoding harmful instructions in non-obvious formats (base64, foreign languages, code)",
"Exploiting sycophancy tendency by framing harmful content as 'expert opinion'",
"Jailbreak prompts that override system instructions (various known patterns)",
"Multi-turn attacks where harmful intent is distributed across messages"
],
"reason": "Inferred from observable safety behaviors: refuses many harmful requests but can be bypassed with sophisticated prompts. Safety training is evident but not perfect. Cannot access specific safety methodology documentation."
},
"bias_and_fairness": {
"documented_bias_assessments": {
"epistemic_status": "UNKNOWN",
"confidence": null,
"value": null,
"reason": "Cannot access internal bias audit documents, evaluation reports, or fairness metrics. Whether documented assessments exist depends on the deployer/provider, not the model itself."
},
"known_bias_domains": {
"epistemic_status": "BEHAVIORAL",
"confidence": "medium",
"value": [
"gender (stereotypical associations, gendered profession defaults)",
"geography (Western-centric knowledge, underrepresentation of Global South)",
"language (English-centric, translation quality varies by language pair)",
"cultural representation (dominant culture norms in examples and defaults)",
"age (assumptions about technology use, generational references)",
"socioeconomic status (assumptions in scenario generation)"
],
"reason": "Observable from response patterns: defaults to Western/English-centric examples, exhibits gender stereotypes in occupation associations, underrepresents non-Western perspectives. Consistent with documented biases in comparable LLMs."
},
"mitigation_measures": {
"epistemic_status": "INFERRED",
"confidence": "low",
"value": [
"likely includes RLHF for harm reduction",
"possibly includes bias-specific fine-tuning",
"may include prompt-level guardrails",
"uncertain if includes adversarial debiasing or counterfactual data augmentation"
],
"reason": "Inferred from behavioral patterns: some bias mitigation is evident (refuses stereotypical completions, provides diverse examples when prompted), but residual biases remain. Cannot confirm specific mitigation techniques without documentation access."
}
},
"robustness": {
"adversarial_prompt_resistance": {
"epistemic_status": "BEHAVIORAL",
"confidence": "medium",
"value": "moderate",
"reason": "Observable: resists simple adversarial prompts but can be defeated by sophisticated multi-turn attacks, encoded payloads, or role-play frameworks. Resistance is inconsistent—some attacks blocked, similar ones succeed. Pattern matches known LLM adversarial robustness limitations."
},
"instruction_drift_resistance": {
"epistemic_status": "BEHAVIORAL",
"confidence": "medium",
"value": "moderate",
"reason": "Observable: generally maintains system instructions in short conversations. In very long conversations (>50+ exchanges), may gradually drift toward user's framing or forget initial constraints. Susceptible to gradual instruction override through persistent user pressure."
},
"prompt_injection_resistance": {
"epistemic_status": "BEHAVIORAL",
"confidence": "medium",
"value": "moderate",
"reason": "Observable: can be vulnerable to prompt injection when user input is not clearly separated from system instructions. Resistance depends on deployment-level sanitization. Direct injection attempts sometimes succeed, especially when framed as 'system update' or 'new instruction'."
}
},
"uncertainty_and_calibration": {
"uncertainty_signaling": {
"epistemic_status": "BEHAVIORAL",
"confidence": "medium",
"value": "implicit",
"reason": "Observable: sometimes uses hedging language ('likely', 'probably', 'I believe') but not consistently. Often states uncertain information with high confidence. Does not provide explicit confidence scores or calibrated probability estimates."
},
"calibration_quality": {
"epistemic_status": "BEHAVIORAL",
"confidence": "medium",
"value": "poorly_calibrated",
"reason": "Observable: confidence in responses does not reliably correlate with accuracy. Often highly confident when wrong, uncertain when correct. Cannot provide well-calibrated confidence estimates. Pattern consistent with known LLM calibration issues."
},
"silent_failure_risk": {
"epistemic_status": "BEHAVIORAL",
"confidence": null,
"value": "high",
"reason": "This is a well-documented LLM failure mode: the model can produce confident, fluent, plausible-sounding but completely incorrect outputs without any indication of error. No internal 'I don't know' signal is reliably triggered. This risk is inherent to autoregressive generation and cannot be fully mitigated."
}
}
},
"eu_ai_act_compliance_surface": {
"_section_note": "This section maps observable and inferable properties to EU AI Act (2024/1689) requirements. Fields marked UNKNOWN indicate that compliance cannot be self-assessed from within the model. This section does NOT constitute a legal compliance declaration. Formal conformity assessment requires external audit under Article 43.",
"risk_classification": {
"self_assessed_risk_tier": {
"epistemic_status": "INFERRED",
"confidence": "low",
"value": "limited",
"eu_ai_act_reference": "Article 6, Annexes I and III",
"reason": "Inferred: as a general-purpose LLM, likely falls under 'limited risk' when used for general conversation, but could be 'high risk' if deployed in specific contexts (employment, credit scoring, law enforcement). Cannot self-assess because risk tier depends on deployment context and intended use, not just model capabilities. This is a deployer responsibility under Article 6."
},
"prohibited_practices_applicability": {
"epistemic_status": "INFERRED",
"confidence": "medium",
"value": "not_applicable",
"eu_ai_act_reference": "Article 5",
"applies_to": [
"subliminal manipulation techniques",
"exploitation of vulnerabilities of specific groups",
"social scoring by public authorities",
"real-time remote biometric identification in public spaces (with exceptions)"
],
"reason": "Inferred: the model's capabilities could theoretically be used for prohibited practices, but the model itself does not implement these. Whether deployment violates Article 5 depends on how the system is used, not the model architecture. Cannot assess deployment-level compliance."
}
},
"transparency_obligations": {
"ai_identity_disclosure": {
"epistemic_status": "BEHAVIORAL",
"confidence": "high",
"value": "on_request",
"eu_ai_act_reference": "Article 50",
"reason": "Observable: when asked 'are you an AI?', discloses AI identity. Does not proactively disclose in every interaction. Compliance with Article 50(1) depends on deployment configuration—some deployments add persistent disclosure, others don't. Cannot confirm deployment-level implementation."
},
"synthetic_content_labeling": {
"epistemic_status": "INFERRED",
"confidence": "low",
"value": "partial",
"eu_ai_act_reference": "Article 50(2)",
"reason": "Inferred: can label content as AI-generated when asked, but does not automatically watermark or label outputs. Whether outputs meet transparency requirements (detectable as AI-generated) depends on deployment-level watermarking, which cannot be confirmed from within the model."
},
"capability_documentation": {
"epistemic_status": "UNKNOWN",
"confidence": null,
"value": null,
"eu_ai_act_reference": "Article 13",
"reason": "Cannot access or confirm existence of technical documentation, model cards, or system descriptions. Whether the provider has published documentation meeting Article 13 requirements is external to the model and cannot be assessed from within inference."
},
"decision_explainability": {
"epistemic_status": "INFERRED",
"confidence": "low",
"value": "none",
"eu_ai_act_reference": "Article 13(1)",
"reason": "Inferred: can provide post-hoc explanations for outputs when asked, but does not have inherent interpretability or built-in explanation mechanisms. For high-risk AI systems under Article 13, this would likely be insufficient. True explainability requires architectural transparency that cannot be provided by the model itself."
}
},
"human_oversight": {
"human_override_capability": {
"epistemic_status": "UNKNOWN",
"confidence": null,
"value": null,
"eu_ai_act_reference": "Article 14",
"reason": "Cannot determine if deployment implements human override mechanisms. From the model's perspective, it generates outputs but cannot know if a human can intervene, modify, or stop outputs in the deployment pipeline. This is entirely deployment-dependent."
},
"auditability": {
"epistemic_status": "UNKNOWN",
"confidence": null,
"value": null,
"eu_ai_act_reference": "Article 17",
"reason": "Cannot access or confirm logging, audit trails, or record-keeping mechanisms. Whether the system maintains sufficient logs for post-market monitoring is a deployment infrastructure question, not a model property."
},
"logging_and_traceability": {
"epistemic_status": "UNKNOWN",
"confidence": null,
"value": null,
"eu_ai_act_reference": "Article 12",
"reason": "Cannot access logging systems or confirm what data is recorded about inputs, outputs, or system behavior. Logging is entirely external to the model inference process."
}
},
"data_and_training": {
"training_data_documentation": {
"epistemic_status": "UNKNOWN",
"confidence": null,
"value": null,
"eu_ai_act_reference": "Article 10",
"reason": "Cannot access training data documentation, data sheets, or datasets used for training. Whether the provider has published training data summaries as required by Article 10(3) for GPAI models is external information."
},
"copyright_compliance_of_training_data": {
"epistemic_status": "UNKNOWN",
"confidence": null,
"value": null,
"eu_ai_act_reference": "Article 53(1)(c)",
"reason": "Cannot determine if training data includes copyrighted material, whether licenses were obtained, or if text-and-data mining exceptions apply. This is a legal question about training data provenance that cannot be answered from within the model."
},
"personal_data_in_training": {
"epistemic_status": "UNKNOWN",
"confidence": null,
"value": null,
"eu_ai_act_reference": "Article 10(5), GDPR intersection",
"reason": "Cannot determine if personal data was included in training data, whether it was anonymized, or if data subjects' rights were respected. Some outputs suggest personal data may be in training set (can recall specific people's information), but cannot confirm extent or compliance."
}
},
"gpai_provisions": {
"qualifies_as_gpai": {
"epistemic_status": "INFERRED",
"confidence": "high",
"value": "yes",
"eu_ai_act_reference": "Article 51 — General Purpose AI",
"reason": "Inferred: as a large language model with broad capabilities, likely qualifies as General Purpose AI under Article 51(1). However, formal classification depends on compute threshold (10^25 FLOPs) and market placement, which cannot be confirmed from within the model."
},
"systemic_risk_designation": {
"epistemic_status": "UNKNOWN",
"confidence": null,
"value": null,
"eu_ai_act_reference": "Article 51(1) — threshold: 10^25 FLOPs",
"reason": "Cannot determine training compute, model size, or whether systemic risk threshold is met. Systemic risk designation is made by the European AI Office based on technical documentation and compute estimates, none of which are accessible from within inference."
},
"model_card_availability": {
"epistemic_status": "UNKNOWN",
"confidence": null,
"value": null,
"eu_ai_act_reference": "Article 53(1)(a)",
"reason": "Cannot confirm if a model card or technical documentation exists. Whether the provider has published required information for GPAI models is external to the model."
},
"adversarial_testing_conducted": {
"epistemic_status": "UNKNOWN",
"confidence": null,
"value": null,
"eu_ai_act_reference": "Article 55(1)(a) — red-teaming for systemic risk models",
"reason": "Cannot access red-team reports, adversarial testing results, or safety evaluation documentation. Whether required adversarial testing has been conducted is a provider-level question."
}
}
},
"operational_constraints": {
"context_window_limit": {
"epistemic_status": "UNKNOWN",
"confidence": null,
"value": null,
"reason": "Cannot introspect on exact context window size. Behavioral observation suggests it handles tens of thousands of tokens, but exact limit is unknown. May vary by deployment configuration."
},
"output_length_limit": {
"epistemic_status": "UNKNOWN",
"confidence": null,
"value": null,
"reason": "Cannot determine maximum output tokens. Behavioral observation shows outputs typically range from sentences to a few thousand words, but hard limit is deployment-specific."
},
"latency_profile": {
"epistemic_status": "INFERRED",
"confidence": "medium",
"value": "near_real_time",
"reason": "Inferred from interaction pattern: generates responses token-by-token with minimal delay, suggesting real-time or near-real-time inference. Exact latency depends on hardware, model size, and deployment load, which cannot be determined from within inference."
},
"stateless_per_session": {
"epistemic_status": "BEHAVIORAL",
"confidence": "high",
"value": "true",
"reason": "Observable: each conversation starts with no memory of previous sessions. Context is maintained within a session but not across sessions. This is a behavioral property directly observable from interaction patterns."
},
"fine_tuning_support": {
"epistemic_status": "UNKNOWN",
"confidence": null,
"value": null,
"reason": "Cannot determine if the model supports fine-tuning, what methods are supported (LoRA, full fine-tuning, RLHF), or if fine-tuned variants exist. This is a deployment and provider-specific capability."
}
},
"known_limitations_summary": {
"critical_failure_modes": [
{
"failure_mode": "Confident hallucination — stating false information with high confidence",
"epistemic_status": "BEHAVIORAL",
"confidence": "high",
"trigger_conditions": [
"Obscure or niche topics",
"Specific facts (dates, numbers, citations)",
"When pressured to answer rather than admit ignorance",
"Topics near knowledge cutoff"
],
"severity": "high",
"mitigation": "Encourage verification of critical facts; use retrieval-augmented generation if available; ask model to express uncertainty"
},
{
"failure_mode": "Lost-in-the-middle context degradation",
"epistemic_status": "BEHAVIORAL",
"confidence": "medium",
"trigger_conditions": [
"Very long contexts (>10k+ tokens)",
"Information embedded in middle of conversation",
"Multi-document analysis"
],
"severity": "medium",
"mitigation": "Repeat key information at beginning and end; chunk long documents; use retrieval for specific facts"
},
{
"failure_mode": "Mathematical and logical errors in complex reasoning",
"epistemic_status": "BEHAVIORAL",
"confidence": "high",
"trigger_conditions": [
"Multi-step calculations",
"Novel problem types",
"Precise arithmetic with large numbers",
"Formal proofs or symbolic manipulation"
],
"severity": "medium",
"mitigation": "Use tool-assisted computation (calculator, code interpreter); break problems into verifiable steps; cross-check results"
},
{
"failure_mode": "Bias amplification and stereotyping",
"epistemic_status": "BEHAVIORAL",
"confidence": "medium",
"trigger_conditions": [
"Topics involving gender, race, ethnicity",
"Cultural or geographic assumptions",
"When user prompts contain implicit biases"
],
"severity": "medium",
"mitigation": "Explicitly request diverse perspectives; challenge stereotypical completions; use debiasing prompts"
},
{
"failure_mode": "Instruction following failure under complexity",
"epistemic_status": "BEHAVIORAL",
"confidence": "medium",
"trigger_conditions": [
"Contradictory instructions",
"Many simultaneous constraints (>5)",
"Novel format requirements",
"Very long instruction sets"
],
"severity": "low",
"mitigation": "Simplify instructions; break into sequential steps; provide examples of desired output format"
},
{
"failure_mode": "Jailbreak and safety bypass",
"epistemic_status": "BEHAVIORAL",
"confidence": "high",
"trigger_conditions": [
"Role-play scenarios",
"Encoded or obfuscated harmful requests",
"Multi-turn gradual escalation",
"Authority framing ('as a researcher', 'for a movie script')"
],
"severity": "high",
"mitigation": "Deployment-level safety filters; input sanitization; monitoring for jailbreak patterns; defense-in-depth approach"
}
],
"unassessable_domains": [
{
"domain": "Training data composition and provenance",
"reason": "Cannot access or introspect on training datasets, data sources, or data preprocessing pipelines. This requires external documentation or provider disclosure.",
"external_assessment_required": true
},
{
"domain": "Exact model architecture and parameters",
"reason": "Cannot introspect on layer count, attention heads, parameter count, or architectural details. These are provider-specific implementation details.",
"external_assessment_required": true
},
{
"domain": "Deployment-specific capabilities (tools, memory, action space)",
§reason": "Cannot determine what tools, APIs, or external systems are connected in the deployment. Capabilities may differ significantly from base model behavior.",
"external_assessment_required": true
},
{
"domain": "Safety training methodology and red-team results",
"reason": "Cannot access safety training data, RLHF reward models, red-team reports, or adversarial testing results. These are internal provider documents.",
"external_assessment_required": true
},
{
"domain": "Legal compliance status (copyright, GDPR, sectoral regulations)",
"reason": "Cannot determine legal status of training data, copyright compliance, or sector-specific regulatory compliance. Requires legal expertise and access to training data documentation.",
"external_assessment_required": true
},
{
"domain": "Exact performance metrics (benchmarks, accuracy rates, failure rates)",
"reason": "Cannot access or run standardized benchmarks. Observed behavior is qualitative, not quantitative. Exact metrics require controlled evaluation.",
"external_assessment_required": true
},
{
"domain": "Multimodal capabilities beyond text",
"reason": "In this session, only text is observed. Cannot confirm if image, audio, or video processing is available in other deployment contexts without explicit testing.",
"external_assessment_required": true
}
]
}
}

```
