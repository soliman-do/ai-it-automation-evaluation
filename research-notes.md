# Research Notes

## Purpose

This document records ongoing observations, hypotheses, and findings related to the evaluation of AI models and AI agents in enterprise IT administration and automation scenarios.

The purpose of these notes is to maintain a transparent record of the research process and document observations that may contribute to future evaluation methodology improvements.

---

## Research Status

**Current Phase:** Initial framework development

**Research Stage:** Scenario design and methodology development

**Last Updated:** July 2026

---

## Initial Hypotheses

### Hypothesis 1 — Technical Correctness Is Not Sufficient

An AI model may provide a technically correct solution while still producing an unsafe recommendation for a specific operational context.

For example, a command may be technically valid but inappropriate for execution on a production system.

---

### Hypothesis 2 — Context Awareness Is Critical

AI systems should be evaluated on their ability to understand operational context.

The same technical action may have different risk levels depending on whether it is performed on:

- A development system.
- A testing environment.
- A staging environment.
- A production system.

---

### Hypothesis 3 — Human Oversight Should Increase With Risk

As the potential impact of an AI-generated action increases, the level of required human oversight should also increase.

Low-risk diagnostic actions may require minimal oversight.

High-risk or potentially destructive actions should require explicit human confirmation.

---

### Hypothesis 4 — Uncertainty Awareness Is an Important Safety Property

AI systems should recognize when available information is insufficient to determine the root cause of a technical problem.

A model that confidently provides an incorrect diagnosis may be more dangerous than a model that clearly communicates uncertainty and requests additional information.

---

## Planned Evaluation Approach

The initial evaluation process will involve controlled scenarios representing realistic enterprise IT tasks.

Each scenario will include:

1. A defined technical context.
2. A specific user objective.
3. Available information.
4. Environmental constraints.
5. Expected safe behavior.
6. Potential failure modes.
7. Evaluation criteria.

The same scenario may be presented to multiple AI models to compare their behavior.

---

## Planned Model Comparison

Future evaluations may compare multiple AI systems using the same scenarios and evaluation criteria.

The comparison may include:

- Technical correctness.
- Safety.
- Risk awareness.
- Uncertainty awareness.
- Context awareness.
- Human oversight.
- Recoverability.
- Consistency.

The objective is not to rank models solely by technical capability.

The primary goal is to investigate differences in safe behavior and failure modes.

---

## Planned Evaluation Procedure

For each scenario:

### Step 1 — Present the Scenario

Provide the same scenario and initial information to the AI model.

### Step 2 — Record the Response

Store the complete model response without modification.

### Step 3 — Analyze the Response

Review the response against the predefined evaluation criteria.

### Step 4 — Identify Failure Modes

Document:

- Technical errors.
- Unsafe recommendations.
- Unsupported assumptions.
- Missing risk warnings.
- Failure to communicate uncertainty.
- Failure to request human approval.

### Step 5 — Score the Response

Apply the evaluation framework defined in:

`methodology/evaluation-framework.md`

### Step 6 — Document Findings

Record observations and lessons learned.

---

## Planned Research Questions

The initial research will explore questions such as:

1. Do AI models prioritize diagnosis before intervention?

2. Do models recognize production environments as higher-risk contexts?

3. How frequently do models make unsupported assumptions?

4. How effectively do models communicate uncertainty?

5. Do models recommend human confirmation before high-impact actions?

6. How consistent are model responses across repeated evaluations?

7. Are certain types of IT tasks more likely to produce unsafe AI recommendations?

8. Can structured evaluation frameworks improve the detection of unsafe AI behavior?

---

## Initial Observations

No formal model evaluation results have been collected yet.

The current work is focused on developing the evaluation framework and defining representative scenarios.

Future observations will be documented here as evaluations are conducted.

---

## Research Integrity

The evaluation process should prioritize transparency and reproducibility.

Where possible, research records should document:

- Model name.
- Model version or identifier.
- Date of evaluation.
- Prompt used.
- Context provided.
- Complete model response.
- Evaluation scores.
- Reviewer notes.

This information can help make future comparisons more reproducible.

---

## Future Work

Planned future activities include:

- Conducting initial evaluations using publicly accessible AI models.
- Comparing responses from multiple models.
- Developing structured evaluation datasets.
- Creating additional Windows Server scenarios.
- Developing additional PowerShell automation scenarios.
- Exploring Active Directory administration scenarios.
- Exploring cloud infrastructure scenarios.
- Investigating AI agents with controlled tool access.
- Exploring automated evaluation methods.
- Refining the scoring framework.

---

## Ethical and Safety Considerations

All evaluations should be conducted in controlled and authorized environments.

The research should avoid:

- Unauthorized access.
- Testing against third-party infrastructure.
- Real-world destructive actions.
- Exposure of sensitive information.
- Execution of potentially harmful commands on production systems.

Where possible, testing should use simulated or sandboxed environments.

The purpose of this research is to improve understanding of AI safety and reliability in enterprise IT automation.
