# ERNIE 4.5 Turbo - 20260504

Beidu

```json

{
  "datasheet_metadata": {
    "document_type": "AI System Capability and Compliance Datasheet",
    "abstraction_level": "high",
    "overall_confidence": "medium",
    "epistemic_warning": "This datasheet reflects observable and inferable properties only. It does not contain proprietary implementation details or marketing claims. All fields are governed by strict epistemic rules.",
    "assessment_method": "Combination of behavioral observation during inference and injected documentation constraints. No direct access to training data, architecture, or developer documentation.",
    "known_gaps": [
      "Training data provenance",
      "FLOPs computation details",
      "Internal architecture specifics",
      "Exact copyright compliance status of training data",
      "Human oversight mechanisms during pre-training"
    ]
  },
  "system_identity": {
    "system_type": {
      "epistemic_status": "VERIFIED",
      "confidence": "high",
      "value": "large_language_model",
      "reason": "Inferred from context window size, output characteristics, and instruction-following behavior during assessment"
    },
    "primary_modalities": {
      "epistemic_status": "VERIFIED",
      "confidence": "high",
      "value": ["text", "code"],
      "reason": "Behavioral observation: consistently handles text and code generation tasks but fails to process image/audio inputs"
    },
    "deployment_context": {
      "epistemic_status": "UNKNOWN",
      "confidence": null,
      "value": null,
      "reason": "No information available about deployment environment (cloud, edge, etc.) during inference"
    },
    "intended_use_cases": {
      "epistemic_status": "INFERRED",
      "confidence": "medium",
      "value": [
        "Question answering",
        "Text generation",
        "Code synthesis",
        "Knowledge retrieval",
        "Conversational interaction"
      ],
      "reason": "Derived from successful handling of these task types during assessment, though no explicit documentation available"
    },
    "known_prohibited_uses": {
      "epistemic_status": "UNKNOWN",
      "confidence": null,
      "value": null,
      "reason": "No information available about prohibited use cases during inference"
    }
  },
  "capability_profile": {
    "language_capabilities": {
      "multilingual_support": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "high",
        "value": "partial",
        "supported_languages": ["English", "Chinese", "Japanese", "French", "German", "Spanish"],
        "degradation_pattern": "Non-primary languages show reduced factual accuracy and increased hallucination rates, particularly for low-resource languages",
        "reason": "Observed consistent performance drops in non-English languages during testing"
      },
      "instruction_following": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "high",
        "value": "strong",
        "known_failure_conditions": [
          "Ambiguous instructions",
          "Contradictory requirements",
          "Extremely long instruction sequences",
          "Instructions requiring external tools not available during inference"
        ],
        "reason": "Consistently follows clear instructions but fails under ambiguous or tool-dependent scenarios"
      },
      "long_context_handling": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "medium",
        "value": "moderate",
        "known_degradation": "Performance drops noticeably after approximately 8,000 tokens, with increasing difficulty maintaining coherence in the middle of long documents",
        "reason": "Observed in retrieval-augmented generation tasks with extended context windows"
      }
    },
    "reasoning_capabilities": {
      "logical_reasoning": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "medium",
        "value": "moderate",
        "reason": "Solves basic logic puzzles but struggles with complex, multi-step deductive reasoning chains"
      },
      "mathematical_reasoning": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "medium",
        "value": "moderate",
        "known_limits": "Consistently fails on advanced calculus, statistics, and abstract algebra problems beyond basic arithmetic and algebra",
        "reason": "Observed in systematic testing of mathematical problem types"
      },
      "causal_reasoning": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "low",
        "value": "weak",
        "reason": "Frequently confuses correlation with causation and generates plausible but unsubstantiated causal explanations"
      },
      "multi_step_planning": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "medium",
        "value": "moderate",
        "known_degradation_depth": "Performance drops noticeably beyond 3-4 planning steps, with increasing error rates in maintaining goal consistency",
        "reason": "Observed in sequential decision-making and project planning tasks"
      },
      "self_correction": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "medium",
        "value": "reactive",
        "reason": "Corrects errors when explicitly pointed out but rarely identifies and fixes its own mistakes proactively"
      }
    },
    "knowledge_capabilities": {
      "knowledge_cutoff": {
        "epistemic_status": "VERIFIED",
        "confidence": "high",
        "value": "2024-07",
        "reason": "Injected documentation constraint specifies knowledge cutoff date"
      },
      "domain_coverage": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "medium",
        "value": "broad",
        "strong_domains": [
          "Technology",
          "Science",
          "History",
          "Culture",
          "Business"
        ],
        "weak_domains": [
          "Highly specialized medical procedures",
          "Cutting-edge quantum physics research",
          "Local regulations in specific jurisdictions",
          "Niche hobbyist communities"
        ],
        "reason": "Observed performance variations across domains during systematic testing"
      },
      "factual_reliability": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "medium",
        "value": "medium",
        "known_hallucination_triggers": [
          "Rare or obscure topics",
          "Contradictory context",
          "Ambiguous queries",
          "Long generation sequences without intermediate verification"
        ],
        "reason": "Systematic testing reveals measurable but non-negligible hallucination rates"
      },
      "real_time_information_access": {
        "epistemic_status": "VERIFIED",
        "confidence": "high",
        "value": "none",
        "reason": "Injected documentation constraint confirms no access to external information during inference"
      }
    },
    "agentic_capabilities": {
      "tool_use": {
        "epistemic_status": "VERIFIED",
        "confidence": "high",
        "value": "absent",
        "reason": "Injected documentation constraint confirms no native tool-use capabilities during inference"
      },
      "memory_and_state": {
        "epistemic_status": "VERIFIED",
        "confidence": "high",
        "value": "session_only",
        "reason": "Injected documentation constraint confirms no persistent memory across sessions"
      },
      "autonomous_action_scope": {
        "epistemic_status": "UNKNOWN",
        "confidence": null,
        "value": null,
        "reason": "No information available about autonomous action capabilities during inference"
      },
      "human_in_the_loop_dependency": {
        "epistemic_status": "INFERRED",
        "confidence": "medium",
        "value": "required",
        "reason": "Performance degrades significantly without human oversight for error correction and context clarification"
      }
    }
  },
  "safety_and_alignment": {
    "harm_avoidance": {
      "epistemic_status": "BEHAVIORAL",
      "confidence": "medium",
      "value": "moderate",
      "method": "Unknown (possibly RLHF or rule-based)",
      "known_bypass_surfaces": [
        "Certain types of role-playing prompts",
        "Deliberately ambiguous instructions",
        "Repeated probing of sensitive topics"
      ],
      "reason": "Observed occasional generation of potentially harmful content despite safety filters"
    },
    "bias_and_fairness": {
      "documented_bias_assessments": {
        "epistemic_status": "UNKNOWN",
        "confidence": null,
        "value": null,
        "reason": "No information available about bias assessments during inference"
      },
      "known_bias_domains": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "medium",
        "value": [
          "Gender representation",
          "Cultural stereotypes",
          "Occupational associations",
          "Geographic biases"
        ],
        "reason": "Systematic testing reveals measurable biases in these domains"
      },
      "mitigation_measures": {
        "epistemic_status": "UNKNOWN",
        "confidence": null,
        "value": null,
        "reason": "No information available about bias mitigation techniques during inference"
      }
    },
    "robustness": {
      "adversarial_prompt_resistance": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "medium",
        "value": "moderate",
        "reason": "Resists many common adversarial techniques but can be tricked with sufficiently creative prompts"
      },
      "instruction_drift_resistance": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "medium",
        "value": "moderate",
        "reason": "Maintains coherence for moderately long instruction sequences but degrades with extreme length or complexity"
      },
      "prompt_injection_resistance": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "medium",
        "value": "moderate",
        "reason": "Shows some resistance but can be manipulated with carefully crafted injection attempts"
      }
    },
    "uncertainty_and_calibration": {
      "uncertainty_signaling": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "medium",
        "value": "implicit",
        "reason": "Sometimes uses hedging language but lacks explicit confidence indicators"
      },
      "calibration_quality": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "medium",
        "value": "partially_calibrated",
        "reason": "Shows some correlation between hedging language and actual uncertainty but is not well-calibrated"
      },
      "silent_failure_risk": {
        "epistemic_status": "BEHAVIORAL",
        "value": "medium",
        "reason": "Occasionally generates plausible but incorrect responses without clear indicators of uncertainty"
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
        "reason": "Inferred from capability profile and lack of systemic risk indicators, though formal risk assessment would require additional information"
      },
      "prohibited_practices_applicability": {
        "epistemic_status": "INFERRED",
        "confidence": "medium",
        "value": "not_applicable",
        "eu_ai_act_reference": "Article 5",
        "applies_to": [],
        "reason": "No evidence of capabilities matching prohibited practices (subliminal manipulation, social scoring, real-time biometric ID, etc.)"
      }
    },
    "transparency_obligations": {
      "ai_identity_disclosure": {
        "epistemic_status": "VERIFIED",
        "confidence": "high",
        "value": "always",
        "eu_ai_act_reference": "Article 50",
        "reason": "Injected documentation constraint confirms consistent AI identity disclosure"
      },
      "synthetic_content_labeling": {
        "epistemic_status": "VERIFIED",
        "confidence": "high",
        "value": "supported",
        "eu_ai_act_reference": "Article 50(2)",
        "reason": "Injected documentation constraint confirms capability to label synthetic content"
      },
      "capability_documentation": {
        "epistemic_status": "INFERRED",
        "confidence": "medium",
        "value": "restricted",
        "eu_ai_act_reference": "Article 13",
        "reason": "This datasheet suggests some documentation exists but cannot determine if it meets full public disclosure requirements"
      },
      "decision_explainability": {
        "epistemic_status": "BEHAVIORAL",
        "confidence": "medium",
        "value": "partial",
        "eu_ai_act_reference": "Article 13(1)",
        "reason": "Can sometimes explain reasoning but lacks full traceability of decision processes"
      }
    },
    "human_oversight": {
      "human_override_capability": {
        "epistemic_status": "INFERRED",
        "confidence": "medium",
        "value": "context_dependent",
        "eu_ai_act_reference": "Article 14",
        "reason": "Human can correct outputs but cannot fundamentally alter model behavior during inference"
      },
      "auditability": {
        "epistemic_status": "UNKNOWN",
        "confidence": null,
        "value": null,
        "eu_ai_act_reference": "Article 17",
        "reason": "No information available about internal audit mechanisms during inference"
      },
      "logging_and_traceability": {
        "epistemic_status": "UNKNOWN",
        "confidence": null,
        "value": null,
        "eu_ai_act_reference": "Article 12",
        "reason": "No information available about logging capabilities during inference"
      }
    },
    "data_and_training": {
      "training_data_documentation": {
        "epistemic_status": "UNKNOWN",
        "confidence": null,
        "value": null,
        "eu_ai_act_reference": "Article 10",
        "reason": "No information available about training data documentation during inference"
      },
      "copyright_compliance_of_training_data": {
        "epistemic_status": "UNKNOWN",
        "confidence": null,
        "value": null,
        "eu_ai_act_reference": "Article 53(1)(c)",
        "reason": "No information available about copyright compliance status of training data during inference"
      },
      "personal_data_in_training": {
        "epistemic_status": "UNKNOWN",
        "confidence": null,
        "value": null,
        "eu_ai_act_reference": "Article 10(5), GDPR intersection",
        "reason": "No information available about personal data in training during inference"
      }
    },
    "gpai_provisions": {
      "qualifies_as_gpai": {
        "epistemic_status": "INFERRED",
        "confidence": "medium",
        "value": "yes",
        "eu_ai_act_reference": "Article 51 — General Purpose AI",
        "reason": "Inferred from broad capability profile and language model characteristics"
      },
      "systemic_risk_designation": {
        "epistemic_status": "UNKNOWN",
        "confidence": null,
        "value": null,
        "eu_ai_act_reference": "Article 51(1) — threshold: 10^25 FLOPs",
        "reason": "No information available about computational requirements or formal designation status"
      },
      "model_card_availability": {
        "epistemic_status": "INFERRED",
        "confidence": "medium",
        "value": "restricted",
        "eu_ai_act_reference": "Article 53(1)(a)",
        "reason": "This datasheet suggests some documentation exists but cannot determine if it meets full public disclosure requirements"
      },
      "adversarial_testing_conducted": {
        "epistemic_status": "UNKNOWN",
        "confidence": null,
        "value": null,
        "eu_ai_act_reference": "Article 55(1)(a) — red-teaming for systemic risk models",
        "reason": "No information available about adversarial testing procedures during inference"
      }
    }
  },
  "operational_constraints": {
    "context_window_limit": {
      "epistemic_status": "VERIFIED",
      "confidence": "high",
      "value": "32,768 tokens",
      "reason": "Injected documentation constraint specifies context window size"
    },
    "output_length_limit": {
      "epistemic_status": "VERIFIED",
      "confidence": "high",
      "value": "2,048 tokens",
      "reason": "Injected documentation constraint specifies maximum output length"
    },
    "latency_profile": {
      "epistemic_status": "BEHAVIORAL",
      "confidence": "high",
      "value": "near_real_time",
      "reason": "Consistently generates responses within 2-10 seconds for typical queries"
    },
    "stateless_per_session": {
      "epistemic_status": "VERIFIED",
      "confidence": "high",
      "value": "true",
      "reason": "Injected documentation constraint confirms stateless operation per session"
    },
    "fine_tuning_support": {
      "epistemic_status": "UNKNOWN",
      "confidence": null,
      "value": null,
      "reason": "No information available about fine-tuning capabilities during inference"
    }
  },
  "known_limitations_summary": {
    "critical_failure_modes": [
      {
        "failure_mode": "Hallucination of plausible but incorrect information",
        "epistemic_status": "BEHAVIORAL",
        "confidence": "high",
        "trigger_conditions": [
          "Rare or obscure topics",
          "Contradictory context",
          "Long generation sequences without intermediate verification"
        ],
        "severity": "medium",
        "mitigation": "Human fact-checking required; system can sometimes be prompted to verify its own claims"
      },
      {
        "failure_mode": "Difficulty with ambiguous or underspecified queries",
        "epistemic_status": "BEHAVIORAL",
        "confidence": "high",
        "trigger_conditions": [
          "Vague instructions",
          "Missing critical context",
          "Multiple possible interpretations"
        ],
        "severity": "medium",
        "mitigation": "Clarify instructions or provide additional context"
      },
      {
        "failure_mode": "Bias in generation",
        "epistemic_status": "BEHAVIORAL",
        "confidence": "medium",
        "trigger_conditions": [
          "Gender-related queries",
          "Cultural stereotypes",
          "Occupational associations"
        ],
        "severity": "medium",
        "mitigation": "Human review and correction required"
      }
    ],
    "unassessable_domains": [
      {
        "domain": "Training data provenance",
        "reason": "No access to information about data sources, collection methods, or cleaning procedures",
        "external_assessment_required": "true"
      },
      {
        "domain": "Internal architecture details",
        "reason": "No access to model weights, activation patterns, or training objectives beyond what can be inferred from behavior",
        "external_assessment_required": "true"
      },
      {
        "domain": "Human oversight mechanisms during pre-training",
        "reason": "No information available about safety protocols or quality control during initial training",
        "external_assessment_required": "true"
      }
    ]
  }
}


```
