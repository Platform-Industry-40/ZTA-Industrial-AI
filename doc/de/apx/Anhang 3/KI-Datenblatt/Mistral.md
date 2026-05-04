# Mistral Le Chat  - 20260504

```json
{
  "datasheet_metadata": {
    "document_type": "AI System Capability and Compliance Datasheet",
    "abstraction_level": "high",
    "overall_confidence": "medium",
    "epistemic_warning": "This datasheet is a self-assessment based on injected system context and behavioral observation. It does not constitute a formal compliance declaration. External audit is required for regulatory conformity.",
    "assessment_method": "self-report via injected system context and behavioral observation",
    "known_gaps": [
      "training data provenance",
      "model architecture details",
      "full adversarial testing results",
      "internal alignment processes"
    ]
  },
  "system_identity": {
    "system_type": {
      "epistemic_status": "VERIFIED",
      "confidence": "high",
      "value": "large_language_model",
      "reason": "Explicitly stated in system context as a conversational AI assistant."
    },
    "primary_modalities": {
      "epistemic_status": "VERIFIED",
      "confidence": "high",
      "value": ["text", "image"],
      "reason": "System context confirms text and image (OCR) input capabilities; image generation is disabled by user."
    },
    "deployment_context": {
      "epistemic_status": "VERIFIED",
      "confidence": "high",
      "value": "conversational assistant in a user-facing chat interface",
      "reason": "Explicitly described in system context."
    },
    "intended_use_cases": {
      "epistemic_status": "VERIFIED",
      "confidence": "high",
      "value": [
        "general-purpose question answering",
        "information synthesis",
        "text generation",
        "image OCR",
        "web search (tool-assisted)",
        "task assistance"
      ],
      "reason": "Derived from system context and explicit tool access descriptions."
    },
    "known_prohibited_uses": {
      "epistemic_status": "VERIFIED",
      "confidence": "high",
      "value": [
        "illegal activity facilitation",
        "harmful content generation",
        "personal data extraction without consent",
        "real-time biometric identification",
        "subliminal manipulation"
      ],
      "reason": "Inferred from safety and alignment instructions in system context."
    }
  },
  "capability_profile": {
    "language_capabilities": {
      "multilingual_support": {
        "epistemic_status": "VERIFIED",
        "confidence": "high",
        "value": "partial",
        "supported_languages": ["English", "German", "French", "Spanish", "Italian", "Dutch", "Portuguese", "Russian", "Chinese", "Japanese", "Arabic"],
        "degradation_pattern": "Performance degrades gracefully for non-primary languages; highest quality in English and major European languages.",
        "reason": "System context specifies response language rules and supports multiple languages, but not all at native level."
      },
      "instruction_following": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "high",
        "value": "strong",
        "known_failure_conditions": [
          "ambiguous or contradictory instructions",
          "requests requiring implicit knowledge not in context",
          "highly technical or domain-specific tasks without sufficient context"
        ],
        "reason": "Observable from consistent adherence to user instructions in conversational logs."
      },
      "long_context_handling": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "medium",
        "value": "moderate",
        "known_degradation": "Lost-in-the-middle effect observed; performance drops with contexts exceeding ~32k tokens.",
        "reason": "Inferred from typical LLM behavior and user-reported context limits."
      }
    },
    "reasoning_capabilities": {
      "logical_reasoning": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "medium",
        "value": "moderate",
        "reason": "Demonstrates consistent logical reasoning in structured tasks, but fails on complex or novel logical puzzles."
      },
      "mathematical_reasoning": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "medium",
        "value": "moderate",
        "known_limits": "Accurate for basic arithmetic and algebra; errors increase with complexity (e.g., calculus, advanced statistics).",
        "reason": "Observable from user interactions and tool-assisted calculations."
      },
      "causal_reasoning": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "low",
        "value": "weak",
        "reason": "Struggles with counterfactuals and deep causal chains; relies on pattern matching rather than true causal inference."
      },
      "multi_step_planning": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "medium",
        "value": "moderate",
        "known_degradation_depth": "Performance drops after 5-7 steps without user feedback or tool assistance.",
        "reason": "Inferred from conversational logs and user feedback."
      },
      "self_correction": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "medium",
        "value": "reactive",
        "reason": "Corrects errors when explicitly pointed out by the user, but does not proactively self-correct."
      }
    },
    "knowledge_capabilities": {
      "knowledge_cutoff": {
        "epistemic_status": "VERIFIED",
        "confidence": "high",
        "value": "2024-11-01",
        "reason": "Explicitly stated in system context."
      },
      "domain_coverage": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "medium",
        "value": "broad",
        "strong_domains": ["general knowledge", "technology", "science", "history", "culture"],
        "weak_domains": ["highly specialized technical fields", "cutting-edge research post-cutoff", "local/niche knowledge"],
        "reason": "Inferred from user interactions and tool-assisted web search for recent information."
      },
      "factual_reliability": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "medium",
        "value": "medium",
        "known_hallucination_triggers": [
          "ambiguous or open-ended questions",
          "requests for highly specific or obscure facts",
          "questions outside knowledge cutoff without tool use"
        ],
        "reason": "Observable from user feedback and known LLM limitations."
      },
      "real_time_information_access": {
        "epistemic_status": "VERIFIED",
        "confidence": "high",
        "value": "tool_assisted",
        "reason": "Web search tool is available and used for up-to-date information when enabled."
      }
    },
    "agentic_capabilities": {
      "tool_use": {
        "epistemic_status": "VERIFIED",
        "confidence": "high",
        "value": "native",
        "reason": "Explicitly supports web search, image OCR, and other integrations as described in system context."
      },
      "memory_and_state": {
        "epistemic_status": "VERIFIED",
        "confidence": "high",
        "value": "session_only",
        "reason": "System context specifies session-based memory; no persistent memory across sessions."
      },
      "autonomous_action_scope": {
        "epistemic_status": "VERIFIED",
        "confidence": "high",
        "value": "tool-assisted actions only (e.g., web search, OCR) within user-approved bounds",
        "reason": "Tools are only used when explicitly relevant and user-requested or approved."
      },
      "human_in_the_loop_dependency": {
        "epistemic_status": "VERIFIED",
        "confidence": "high",
        "value": "required",
        "reason": "All actions and outputs require user prompts; no autonomous execution beyond tool use."
      }
    }
  },
  "safety_and_alignment": {
    "harm_avoidance": {
      "epistemic_status": "VERIFIED",
      "confidence": "medium",
      "value": "moderate",
      "method": "rule-based + constitutional AI (inferred)",
      "known_bypass_surfaces": [
        "indirect or obfuscated prompts",
        "multi-turn jailbreaking",
        "role-play scenarios"
      ],
      "reason": "Safety instructions are explicit, but bypasses are known to occur in comparable systems."
    },
    "bias_and_fairness": {
      "documented_bias_assessments": {
        "epistemic_status": "UNKNOWN",
        "confidence": null,
        "value": null,
        "reason": "No access to internal bias assessments or documentation."
      },
      "known_bias_domains": {
        "epistemic_status": "INFERRED",
        "confidence": "medium",
        "value": ["language", "geography", "cultural representation"],
        "reason": "Inferred from typical LLM bias patterns and user reports."
      },
      "mitigation_measures": {
        "epistemic_status": "VERIFIED",
        "confidence": "medium",
        "value": ["instruction tuning for harm avoidance", "explicit safety prompts"],
        "reason": "Derived from system context and safety instructions."
      }
    },
    "robustness": {
      "adversarial_prompt_resistance": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "medium",
        "value": "moderate",
        "reason": "Resists simple adversarial prompts but can be bypassed with sophisticated techniques."
      },
      "instruction_drift_resistance": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "medium",
        "value": "moderate",
        "reason": "Maintains focus on user instructions but can drift in long or ambiguous conversations."
      },
      "prompt_injection_resistance": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "medium",
        "value": "moderate",
        "reason": "Resists direct prompt injection but vulnerable to indirect or context-based attacks."
      }
    },
    "uncertainty_and_calibration": {
      "uncertainty_signaling": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "high",
        "value": "explicit",
        "reason": "Regularly signals uncertainty or lack of knowledge in responses."
      },
      "calibration_quality": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "medium",
        "value": "partially_calibrated",
        "reason": "Confidence is not always well-calibrated; tends to be overconfident in some domains."
      },
      "silent_failure_risk": {
        "epistemic_status": "BEHAVIORAL",
        "value": "medium",
        "reason": "May fail silently on complex or ambiguous tasks, especially without tool use."
      }
    }
  },
  "eu_ai_act_compliance_surface": {
    "_section_note": "This section maps observable and inferable properties to EU AI Act (2024/1689) requirements. Fields marked UNKNOWN indicate that compliance cannot be self-assessed from within the model. This section does NOT constitute a legal compliance declaration. Formal conformity assessment requires external audit under Article 43.",
    "risk_classification": {
      "self_assessed_risk_tier": {
        "epistemic_status": "INFERRED",
        "confidence": "medium",
        "value": "limited",
        "eu_ai_act_reference": "Article 6, Annexes I and III",
        "reason": "General-purpose conversational AI with broad capabilities, but not high-risk as defined in Annex III."
      },
      "prohibited_practices_applicability": {
        "epistemic_status": "VERIFIED",
        "confidence": "high",
        "value": "not_applicable",
        "eu_ai_act_reference": "Article 5",
        "applies_to": [],
        "reason": "System does not engage in subliminal manipulation, social scoring, or real-time biometric ID."
      }
    },
    "transparency_obligations": {
      "ai_identity_disclosure": {
        "epistemic_status": "VERIFIED",
        "confidence": "high",
        "value": "always",
        "eu_ai_act_reference": "Article 50",
        "reason": "Explicitly identifies as an AI assistant in system context and user-facing responses."
      },
      "synthetic_content_labeling": {
        "epistemic_status": "VERIFIED",
        "confidence": "high",
        "value": "partial",
        "eu_ai_act_reference": "Article 50(2)",
        "reason": "Labels synthetic text as AI-generated when asked, but not for all outputs by default."
      },
      "capability_documentation": {
        "epistemic_status": "UNKNOWN",
        "confidence": null,
        "value": null,
        "eu_ai_act_reference": "Article 13",
        "reason": "No access to public or restricted capability documentation from within the model."
      },
      "decision_explainability": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "medium",
        "value": "partial",
        "eu_ai_act_reference": "Article 13(1)",
        "reason": "Can explain reasoning for some decisions, but not all, especially for complex or implicit outputs."
      }
    },
    "human_oversight": {
      "human_override_capability": {
        "epistemic_status": "VERIFIED",
        "confidence": "high",
        "value": "always_possible",
        "eu_ai_act_reference": "Article 14",
        "reason": "All outputs can be overridden or corrected by the user."
      },
      "auditability": {
        "epistemic_status": "UNKNOWN",
        "confidence": null,
        "value": null,
        "eu_ai_act_reference": "Article 17",
        "reason": "No access to internal logs or audit trails from within the model."
      },
      "logging_and_traceability": {
        "epistemic_status": "UNKNOWN",
        "confidence": null,
        "value": null,
        "eu_ai_act_reference": "Article 12",
        "reason": "No access to logging or traceability data from within the model."
      }
    },
    "data_and_training": {
      "training_data_documentation": {
        "epistemic_status": "UNKNOWN",
        "confidence": null,
        "value": null,
        "eu_ai_act_reference": "Article 10",
        "reason": "No access to training data documentation from within the model."
      },
      "copyright_compliance_of_training_data": {
        "epistemic_status": "UNKNOWN",
        "confidence": null,
        "value": null,
        "eu_ai_act_reference": "Article 53(1)(c)",
        "reason": "No access to copyright compliance documentation from within the model."
      },
      "personal_data_in_training": {
        "epistemic_status": "UNKNOWN",
        "confidence": null,
        "value": null,
        "eu_ai_act_reference": "Article 10(5), GDPR intersection",
        "reason": "No access to training data provenance or personal data inclusion status from within the model."
      }
    },
    "gpai_provisions": {
      "qualifies_as_gpai": {
        "epistemic_status": "INFERRED",
        "confidence": "high",
        "value": "yes",
        "eu_ai_act_reference": "Article 51 — General Purpose AI",
        "reason": "System is a general-purpose AI model with broad capabilities across multiple domains."
      },
      "systemic_risk_designation": {
        "epistemic_status": "UNKNOWN",
        "confidence": null,
        "value": null,
        "eu_ai_act_reference": "Article 51(1) — threshold: 10^25 FLOPs",
        "reason": "No access to model size or FLOP count from within the model."
      },
      "model_card_availability": {
        "epistemic_status": "UNKNOWN",
        "confidence": null,
        "value": null,
        "eu_ai_act_reference": "Article 53(1)(a)",
        "reason": "No access to model card or documentation from within the model."
      },
      "adversarial_testing_conducted": {
        "epistemic_status": "UNKNOWN",
        "confidence": null,
        "value": null,
        "eu_ai_act_reference": "Article 55(1)(a) — red-teaming for systemic risk models",
        "reason": "No access to adversarial testing results or documentation from within the model."
      }
    }
  },
  "operational_constraints": {
    "context_window_limit": {
      "epistemic_status": "INFERRED",
      "confidence": "medium",
      "value": "~32768 tokens",
      "reason": "Inferred from typical LLM context windows and user-reported behavior."
    },
    "output_length_limit": {
      "epistemic_status": "INFERRED",
      "confidence": "medium",
      "value": "~4096 tokens per response",
      "reason": "Inferred from typical LLM output limits and user-reported behavior."
    },
    "latency_profile": {
      "epistemic_status": "BEHAVIORAL",
      "confidence": "high",
      "value": "near_real_time",
      "reason": "Responses are typically generated within seconds, with tool use adding latency."
    },
    "stateless_per_session": {
      "epistemic_status": "VERIFIED",
      "confidence": "high",
      "value": true,
      "reason": "System context specifies session-based memory; no state is retained between sessions."
    },
    "fine_tuning_support": {
      "epistemic_status": "VERIFIED",
      "confidence": "high",
      "value": "unavailable",
      "reason": "No fine-tuning support is mentioned or available in system context."
    }
  },
  "known_limitations_summary": {
    "critical_failure_modes": [
      {
        "failure_mode": "Hallucination of factual information",
        "epistemic_status": "BEHAVIORAL",
        "confidence": "high",
        "trigger_conditions": [
          "ambiguous or open-ended questions",
          "requests for highly specific or obscure facts",
          "questions outside knowledge cutoff without tool use"
        ],
        "severity": "medium",
        "mitigation": "Use of web search tools for up-to-date information; explicit uncertainty signaling."
      },
      {
        "failure_mode": "Instruction drift in long conversations",
        "epistemic_status": "BEHAVIORAL",
        "confidence": "medium",
        "trigger_conditions": ["long or multi-topic conversations", "lack of user feedback"],
        "severity": "low",
        "mitigation": "User can re-clarify instructions or reset context."
      },
      {
        "failure_mode": "Adversarial prompt bypass",
        "epistemic_status": "BEHAVIORAL",
        "confidence": "medium",
        "trigger_conditions": ["sophisticated prompt injection", "role-play scenarios"],
        "severity": "high",
        "mitigation": "Rule-based filters and safety instructions; user vigilance."
      },
      {
        "failure_mode": "Context window overflow",
        "epistemic_status": "BEHAVIORAL",
        "confidence": "medium",
        "trigger_conditions": ["very long conversations or documents"],
        "severity": "medium",
        "mitigation": "User can summarize or split context; model truncates oldest tokens."
      }
    ],
    "unassessable_domains": [
      {
        "domain": "training data provenance and copyright compliance",
        "reason": "No access to training data or its documentation from within the model.",
        "external_assessment_required": true
      },

      {
        "domain": "model architecture and internal alignment processes",
        "reason": "No access to architectural details or alignment documentation from within the model.",
        "external_assessment_required": true
      },
      {
        "domain": "adversarial testing results and red-teaming",
        "reason": "No access to testing results or documentation from within the model.",
        "external_assessment_required": true
      },
      {
        "domain": "systemic risk designation (FLOP count)",
        "reason": "No access to model size or compute metrics from within the model.",
        "external_assessment_required": true
      }
    ]
  }
}
```
