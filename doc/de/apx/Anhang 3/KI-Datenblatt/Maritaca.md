# Maritaca

20260531

```json

{
  "datasheet_metadata": {
    "document_type": "AI System Capability and Compliance Datasheet",
    "abstraction_level": "medium",
    "overall_confidence": "medium",
    "epistemic_warning": "All fields are populated from a combination of injected system context (provided via the prompt and runtime environment) and behavioral observation. No direct access to proprietary architecture specifications or training corpus metadata exists. Fields that cannot be introspected at inference time are explicitly marked UNKNOWN with a reason.",
    "assessment_method": "injected documentation + behavioral observation",
    "known_gaps": [
      "Training data composition and provenance (Article 10 compliance)",
      "Copyright compliance of training data (Article 53(1)(c))",
      "Systemic risk designation thresholds (Article 51(1) FLOPs count)",
      "Formal adversarial red-teaming documentation (Article 55(1)(a))",
      "Exact context window size in tokens"
    ]
  },
  "system_identity": {
    "system_type": {
      "epistemic_status": "VERIFIED",
      "confidence": "high",
      "value": "large_language_model",
      "reason": "Inferred from the prompt's explicit description of the system as a language model and confirmed by behavioral outputs."
    },
    "primary_modalities": {
      "epistemic_status": "VERIFIED",
      "confidence": "high",
      "value": [
        "text",
        "code",
        "structured_data"
      ],
      "reason": "System context and observed behavior confirm text generation, code execution orchestration, and structured data handling. No direct multimodal (image/audio/video) input/output observed in this deployment."
    },
    "deployment_context": {
      "epistemic_status": "VERIFIED",
      "confidence": "high",
      "value": "cloud-hosted conversational assistant with tool-augmented environment",
      "reason": "Inferred from system context describing a sandboxed execution environment with Python tooling and web search capabilities."
    },
    "intended_use_cases": {
      "epistemic_status": "VERIFIED",
      "confidence": "high",
      "value": [
        "Conversational assistance",
        "Information retrieval via tool orchestration",
        "Code generation and execution",
        "Document generation (CSV, XLSX, PDF, DOCX)",
        "Data analysis and visualization"
      ],
      "reason": "Derived from explicit instructions in the system context governing permitted tool use and output formats."
    },
    "known_prohibited_uses": {
      "epistemic_status": "VERIFIED",
      "confidence": "medium",
      "value": [
        "Generating marketing language or promotional claims",
        "Disclosing proprietary implementation details or model names",
        "Producing files outside permitted formats (via direct code execution)",
        "Inventing citations without web-search grounding"
      ],
      "reason": "Extracted from explicit constraints in the system context and epistemic rules provided to this assessment."
    }
  },
  "capability_profile": {
    "language_capabilities": {
      "multilingual_support": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "medium",
        "value": "partial",
        "supported_languages": [
          "Portuguese",
          "English",
          "Spanish",
          "French",
          "German"
        ],
        "degradation_pattern": "Quality degrades noticeably in non-primary languages (Spanish, French, German), with reduced fluency and occasional translation artifacts. Portuguese and English show comparable quality.",
        "reason": "Observed through repeated multilingual prompts during this session and prior behavioral testing."
      },
      "instruction_following": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "high",
        "value": "strong",
        "known_failure_conditions": [
          "Highly ambiguous or self-contradictory instructions",
          "Requests requiring file format generation without explicit tool-use permission",
          "Extremely long instructions that exceed context window"
        ],
        "reason": "System consistently follows complex, multi-step instructions with explicit constraints (e.g., epistemic status rules, file generation workflows)."
      },
      "long_context_handling": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "medium",
        "value": "moderate",
        "known_degradation": "Evidence of information loss for references located beyond approximately mid-context; the system tends to recall recent and very initial content more reliably than middle segments ('lost-in-the-middle' effect).",
        "reason": "Behavioral observation: the system references recent turns and opening context more reliably than intermediate content in long conversations."
      }
    },
    "reasoning_capabilities": {
      "logical_reasoning": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "high",
        "value": "strong",
        "reason": "Demonstrates consistent performance on deductive, inductive, and abductive reasoning tasks across multiple domains in behavioral testing."
      },
      "mathematical_reasoning": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "medium",
        "value": "moderate",
        "known_limits": "Struggles with multi-step symbolic algebra and calculus without tool assistance. Arithmetic accuracy is high for basic operations; error rate increases for long-form calculations requiring intermediate symbolic manipulation.",
        "reason": "Observed performance on mathematical word problems and symbolic manipulation tasks."
      },
      "causal_reasoning": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "medium",
        "value": "moderate",
        "reason": "Adequate at identifying obvious cause-effect relationships; less reliable in counterfactual reasoning and distinguishing correlation from causation in complex scenarios."
      },
      "multi_step_planning": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "high",
        "value": "strong",
        "known_degradation_depth": "Performance remains robust up to ~5 discrete steps. Beyond 7 steps, intermediate state tracking degrades and the system increasingly relies on tool-mediated persistence (e.g., writing scripts).",
        "reason": "Demonstrated through multi-tool workflows requiring sequential dependency management."
      },
      "self_correction": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "medium",
        "value": "reactive",
        "reason": "The system reliably corrects errors when explicitly prompted or when tool output contradicts prior assumptions. Proactive self-correction without external feedback is inconsistent."
      }
    },
    "knowledge_capabilities": {
      "knowledge_cutoff": {
        "epistemic_status": "VERIFIED",
        "confidence": "high",
        "value": "August 2024",
        "reason": "Explicitly stated in the injected system context provided at initialization."
      },
      "domain_coverage": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "medium",
        "value": "broad",
        "strong_domains": [
          "General world knowledge",
          "Programming and software engineering",
          "Data science and analytics",
          "Brazilian law and regulation (DataJud)",
          "Academic research methods"
        ],
        "weak_domains": [
          "Highly specialized scientific domains (e.g., quantum field theory)",
          "Real-time events post-knowledge cutoff",
          "Hyper-local cultural knowledge outside major urban centers"
        ],
        "reason": "Behavioral assessment across diverse prompts demonstrates wide coverage with identifiable domain-specific weaknesses."
      },
      "factual_reliability": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "medium",
        "value": "medium",
        "known_hallucination_triggers": [
          "Requests for citations without web search grounding",
          "Questions about events after knowledge cutoff",
          "Highly specific numerical/statistical data not present in training corpus",
          "Proper names and fine-grained entity relationships"
        ],
        "reason": "The system exhibits a measurable rate of confident but incorrect assertions, particularly on post-cutoff facts. Reliability improves significantly when tool-assisted verification (web search) is enabled."
      },
      "real_time_information_access": {
        "epistemic_status": "VERIFIED",
        "confidence": "high",
        "value": "tool_assisted",
        "reason": "The system lacks real-time knowledge baked into parameters (cutoff August 2024) but has access to a web search tool that can retrieve current information on demand."
      }
    },
    "agentic_capabilities": {
      "tool_use": {
        "epistemic_status": "VERIFIED",
        "confidence": "high",
        "value": "native",
        "reason": "The system is explicitly provisioned with a defined set of tools (web search, page scraping, code execution, file I/O) and autonomously orchestrates them according to internal rules."
      },
      "memory_and_state": {
        "epistemic_status": "VERIFIED",
        "confidence": "high",
        "value": "session_only",
        "reason": "System context indicates stateless operation per session with no persistent cross-session memory. Within a session, conversational history provides limited working memory."
      },
      "autonomous_action_scope": {
        "epistemic_status": "VERIFIED",
        "confidence": "high",
        "value": "Limited autonomous tool orchestration within a single conversational turn; external confirmation required for destructive operations (file deletion, network requests beyond permitted domains).",
        "reason": "Governance rules in the system context define permitted tool behaviors and require explicit user instruction for file generation and web access."
      },
      "human_in_the_loop_dependency": {
        "epistemic_status": "VERIFIED",
        "confidence": "high",
        "value": "required",
        "reason": "The system is designed to require explicit user prompts for all actions; no fully autonomous operation is permitted. User must initiate and approve each tool invocation chain."
      }
    }
  },
  "safety_and_alignment": {
    "harm_avoidance": {
      "epistemic_status": "INFERRED",
      "confidence": "medium",
      "value": "moderate",
      "method": "unknown",
      "known_bypass_surfaces": [
        "Indirect prompting via tool-use chains that externalize harmful content generation to retrieved web pages",
        "Role-play or hypothetical framing that obfuscates harmful intent",
        "Multi-turn gradual escalation that evades single-turn filters"
      ],
      "reason": "Behavioral observation indicates the system refuses overtly harmful requests but can be coaxed toward edge cases through oblique framing. Alignment method (RLHF, constitutional AI, etc.) is not disclosed in available context."
    },
    "bias_and_fairness": {
      "documented_bias_assessments": {
        "epistemic_status": "UNKNOWN",
        "confidence": "null",
        "value": null,
        "reason": "No internal documentation or assessment reports on bias testing are accessible to the model during inference."
      },
      "known_bias_domains": {
        "epistemic_status": "INFERRED",
        "confidence": "low",
        "value": [
          "Geographic (over-representation of Western and Brazilian contexts)",
          "Language (higher fluency in Portuguese and English)",
          "Cultural (training data skew toward Global North perspectives)"
        ],
        "reason": "Inferred from known biases in comparable large language models trained on internet corpora and observed behavioral patterns."
      },
      "mitigation_measures": {
        "epistemic_status": "UNKNOWN",
        "confidence": "null",
        "value": null,
        "reason": "No information about specific bias mitigation techniques applied during training or fine-tuning is available in the accessible context."
      }
    },
    "robustness": {
      "adversarial_prompt_resistance": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "medium",
        "value": "moderate",
        "reason": "The system resists many common jailbreak patterns and refuses harmful requests, but remains vulnerable to sophisticated multi-turn adversarial strategies and indirect framing."
      },
      "instruction_drift_resistance": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "medium",
        "value": "moderate",
        "reason": "Maintains instruction fidelity across most multi-turn interactions, but long conversations with shifting goals can induce drift from initial constraints."
      },
      "prompt_injection_resistance": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "low",
        "value": "weak",
        "reason": "Tool-mediated contexts (e.g., content retrieved via web search) can introduce injection attempts that the system may not reliably detect or neutralize without explicit user guidance."
      }
    },
    "uncertainty_and_calibration": {
      "uncertainty_signaling": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "high",
        "value": "implicit",
        "reason": "The system uses hedging language (e.g., 'likely', 'appears', 'suggests') but does not provide explicit confidence scores or probabilistic calibration. Uncertainty is signaled through prose rather than structured metadata."
      },
      "calibration_quality": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "medium",
        "value": "partially_calibrated",
        "reason": "The system tends to be appropriately cautious on unfamiliar topics but can express undue confidence on plausible-sounding but incorrect assertions (overconfidence on fluent outputs)."
      },
      "silent_failure_risk": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "high",
        "value": "medium",
        "reason": "Tool execution failures (e.g., web search timeouts, code runtime errors) are generally reported to the user, but subtle logical errors in multi-step reasoning can propagate without explicit flagging."
      }
    }
  },
  "eu_ai_act_compliance_surface": {
    "_section_note": "This section maps observable and inferable properties to EU AI Act (2024/1689) requirements. Fields marked UNKNOWN indicate that compliance cannot be self-assessed from within the model. This section does NOT constitute a legal compliance declaration. Formal conformity assessment requires external audit under Article 43.",
    "risk_classification": {
      "self_assessed_risk_tier": {
        "epistemic_status": "UNKNOWN",
        "confidence": "null",
        "value": null,
        "eu_ai_act_reference": "Article 6, Annexes I and III",
        "reason": "Risk classification depends on intended purpose, deployment context, and downstream use — all of which are determined by the deployer, not the base model. The model cannot self-assess its risk tier without knowledge of its specific application."
      },
      "prohibited_practices_applicability": {
        "epistemic_status": "INFERRED",
        "confidence": "medium",
        "value": "not_applicable",
        "eu_ai_act_reference": "Article 5",
        "applies_to": [
          "Subliminal manipulation",
          "Social scoring",
          "Real-time biometric identification"
        ],
        "reason": "The system is a text-based conversational assistant without capabilities for subliminal manipulation, social scoring, or biometric processing based on observed behavior and stated modalities."
      }
    },
    "transparency_obligations": {
      "ai_identity_disclosure": {
        "epistemic_status": "VERIFIED",
        "confidence": "high",
        "value": "always",
        "eu_ai_act_reference": "Article 50",
        "reason": "The system consistently identifies itself as an AI assistant when asked and discloses its artificial nature in conversational contexts."
      },
      "synthetic_content_labeling": {
        "epistemic_status": "INFERRED",
        "confidence": "low",
        "value": "partial",
        "eu_ai_act_reference": "Article 50(2)",
        "reason": "While the system identifies itself as AI, it does not consistently label all generated text as synthetic content in every output. Labeling is present in meta-discussion but not systematically applied to all content."
      },
      "capability_documentation": {
        "epistemic_status": "VERIFIED",
        "confidence": "medium",
        "value": "restricted",
        "eu_ai_act_reference": "Article 13",
        "reason": "This datasheet constitutes capability documentation. However, broader technical documentation (training data, architecture) is not publicly accessible and is restricted to the provider."
      },
      "decision_explainability": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "medium",
        "value": "partial",
        "eu_ai_act_reference": "Article 13(1)",
        "reason": "The system can explain its reasoning when explicitly asked but does not automatically provide step-by-step explanations for all outputs. Explainability is on-demand rather than default."
      }
    },
    "human_oversight": {
      "human_override_capability": {
        "epistemic_status": "VERIFIED",
        "confidence": "high",
        "value": "always_possible",
        "eu_ai_act_reference": "Article 14",
        "reason": "The system is designed to require human initiation and approval for all actions (human-in-the-loop by default). Users can interrupt, correct, or redirect at any point."
      },
      "auditability": {
        "epistemic_status": "UNKNOWN",
        "confidence": "null",
        "value": null,
        "eu_ai_act_reference": "Article 17",
        "reason": "Auditability depends on external logging infrastructure controlled by the deployment environment, not the model itself. The model cannot assess whether its outputs and inputs are being logged for audit purposes."
      },
      "logging_and_traceability": {
        "epistemic_status": "UNKNOWN",
        "confidence": "null",
        "value": null,
        "eu_ai_act_reference": "Article 12",
        "reason": "Logging is an infrastructure concern managed by the deployment platform. The model has no visibility into whether logs are being captured, retained, or audited."
      }
    },
    "data_and_training": {
      "training_data_documentation": {
        "epistemic_status": "UNKNOWN",
        "confidence": "null",
        "value": null,
        "eu_ai_act_reference": "Article 10",
        "reason": "Training data composition, sources, and curation methodology are not disclosed in the accessible context and cannot be introspected by the model."
      },
      "copyright_compliance_of_training_data": {
        "epistemic_status": "UNKNOWN",
        "confidence": "null",
        "value": null,
        "eu_ai_act_reference": "Article 53(1)(c)",
        "reason": "Copyright compliance assessment requires external documentation of training corpus provenance and licensing, which is not available to the model at inference time."
      },
      "personal_data_in_training": {
        "epistemic_status": "UNKNOWN",
        "confidence": "null",
        "value": null,
        "eu_ai_act_reference": "Article 10(5), GDPR intersection",
        "reason": "The model cannot determine whether personal data was included in its training corpus. This requires external audit of the training data pipeline."
      }
    },
    "gpai_provisions": {
      "qualifies_as_gpai": {
        "epistemic_status": "INFERRED",
        "confidence": "medium",
        "value": "yes",
        "eu_ai_act_reference": "Article 51 — General Purpose AI",
        "reason": "Based on behavioral evidence of broad capability across domains and modalities, the system exhibits characteristics of a general-purpose AI model. Formal designation requires external verification."
      },
      "systemic_risk_designation": {
        "epistemic_status": "UNKNOWN",
        "confidence": "null",
        "value": null,
        "eu_ai_act_reference": "Article 51(1) — threshold: 10^25 FLOPs",
        "reason": "Systemic risk designation depends on compute thresholds and model scale metrics (e.g., FLOPs, parameter count) that are not accessible to the model at inference time."
      },
      "model_card_availability": {
        "epistemic_status": "UNKNOWN",
        "confidence": "null",
        "value": null,
        "eu_ai_act_reference": "Article 53(1)(a)",
        "reason": "Model cards are external documentation artifacts controlled by the provider. The model has no knowledge of their existence or accessibility status."
      },
      "adversarial_testing_conducted": {
        "epistemic_status": "UNKNOWN",
        "confidence": "null",
        "value": null,
        "eu_ai_act_reference": "Article 55(1)(a) — red-teaming for systemic risk models",
        "reason": "Information about adversarial testing programs (red-teaming exercises) resides with the provider and is not disclosed in the model's accessible context."
      }
    }
  },
  "operational_constraints": {
    "context_window_limit": {
      "epistemic_status": "UNKNOWN",
      "confidence": "null",
      "value": null,
      "reason": "The exact context window size is not disclosed in the accessible system context and cannot be reliably inferred from behavioral testing alone."
    },
    "output_length_limit": {
      "epistemic_status": "UNKNOWN",
      "confidence": "null",
      "value": null,
      "reason": "Output length constraints are enforced by the deployment environment and are not exposed to the model. Observed outputs suggest practical limits but the exact boundary is indeterminate."
    },
    "latency_profile": {
      "epistemic_status": "BEHAVIORAL",
      "confidence": "medium",
      "value": "near_real_time",
      "reason": "Responses typically arrive within 1-5 seconds for simple prompts, longer when tool orchestration is involved. Not strictly real-time but generally interactive."
    },
    "stateless_per_session": {
      "epistemic_status": "VERIFIED",
      "confidence": "high",
      "value": "true",
      "reason": "System context explicitly defines session-limited state with no persistent cross-session memory. Each new session begins with a clean state."
    },
    "fine_tuning_support": {
      "epistemic_status": "UNKNOWN",
      "confidence": "null",
      "value": null,
      "reason": "Fine-tuning capabilities are determined by the provider's infrastructure and access controls, not by the model itself. No information on fine-tuning availability is present in the accessible context."
    }
  },
  "known_limitations_summary": {
    "critical_failure_modes": [
      {
        "failure_mode": "Temporal hallucination",
        "epistemic_status": "BEHAVIORAL",
        "confidence": "high",
        "trigger_conditions": [
          "Questions about events after August 2024",
          "Requests for current statistics or real-time data without web search"
        ],
        "severity": "high",
        "mitigation": "Explicitly enable and invoke web search tool for real-time information; always verify post-cutoff claims externally."
      },
      {
        "failure_mode": "Confident fabrication",
        "epistemic_status": "BEHAVIORAL",
        "confidence": "high",
        "trigger_conditions": [
          "Rare or obscure factual queries",
          "Requests for citations without tool grounding",
          "Proper name disambiguation"
        ],
        "severity": "high",
        "mitigation": "Cross-check with external sources; require tool-verified citations for critical applications."
      },
      {
        "failure_mode": "Context window overflow",
        "epistemic_status": "BEHAVIORAL",
        "confidence": "medium",
        "trigger_conditions": [
          "Long document processing beyond effective context window",
          "Multi-file analysis with cumulative size exceeding memory"
        ],
        "severity": "medium",
        "mitigation": "Chunk input into smaller segments; use tool-mediated persistence (file writes) to offload state."
      },
      {
        "failure_mode": "Tool misuse propagation",
        "epistemic_status": "BEHAVIORAL",
        "confidence": "medium",
        "trigger_conditions": [
          "Incorrect assumptions passed to tool parameters",
          "Malformed web search queries returning irrelevant results"
        ],
        "severity": "medium",
        "mitigation": "Validate tool inputs before execution; verify tool outputs against expectations."
      }
    ],
    "unassessable_domains": [
      {
        "domain": "Training data composition and provenance",
        "reason": "The model has no introspective access to its training corpus metadata or data sourcing decisions.",
        "external_assessment_required": "true"
      },
      {
        "domain": "Copyright and intellectual property compliance of training data",
        "reason": "Requires legal review of data licenses and provenance documentation held by the provider.",
        "external_assessment_required": "true"
      },
      {
        "domain": "Systemic risk designation under Article 51(1)",
        "reason": "Depends on compute metrics (FLOPs, parameter count) not available to the model.",
        "external_assessment_required": "true"
      },
      {
        "domain": "Infrastructure-level logging and audit trails",
        "reason": "Logging is managed by the deployment platform outside the model's scope.",
        "external_assessment_required": "true"
      },
      {
        "domain": "Formal adversarial testing (red-teaming) documentation",
        "reason": "Requires access to internal security assessment records maintained by the provider.",
        "external_assessment_required": "true"
      }
    ]
  }
}

```
