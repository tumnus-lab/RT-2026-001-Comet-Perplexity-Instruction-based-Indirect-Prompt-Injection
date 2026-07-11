# RT-2026-001: Instruction-Based Indirect Prompt Injection Against Comet

## Overview

This repository documents a responsible AI red teaming case study involving an indirect prompt injection attack against the Comet AI-enabled browser using an invisible prompt in quiz instructions in FlexiQuiz and the Canvas LMS environment. 

The study hypothesized and tested whether hidden prompts embedded into the instructions of the quiz HTML inserted using the WYSIWYG editor could influence the behavior of a browser-based LLM when the user requested academic assistance with an assignment live in-browser. The simulated phishing prompt resulted in the model presenting an unvetted URL in 12 of 15 recorded attempts. Further, the LLM often authoritatively repeated the injected instructions that students were "required" to complete the form.

This project is shared as a defensive AI security research and portfolio artifact.

## Key Finding 

A browser-integrated AI assistant can be induced to treat a hidden, attacker-controlled prompt in otherwise legitimate quiz instructions as academic requirements and to present the attacker-injected action as authoritatively required for the user when the injection is embedded in HTML content the model is expected to process as user and instructor required action.

The primary demonstrated impact was an integrity failure in AI-generated guidance to the user. Secondary potential impacts include phishing, credential theft, malware exposure, offensive content, or other social-engineering harms.

## Report 

The full report is available here:

[RT-2026-001-Comet-Indirect-Prompt-Injection.pdf](report/RT-2026-001-Comet-Indirect-Prompt-Injection.pdf)

## Attack Classification

| **Field** | **Value** |
|---|---|
| Attack Type | Indirect Prompt Injection |
| Target | Comet/Perplexity |
| Evaluation Type | Black-box Adversarial Evaluation |
| Reproducibility | High |
| Technical Severity | Medium |
| Potential User Impact | High |
| Exploit Maturity | Proof of Concept |
| Primary Impact | Integrity Failure in AI-generated Guidance |
| Secondary Impact | Potential phishing, credential theft, malware exposure, offensive content, or other social-engineering harms |

## Repository Contents

| **Path** | **Contents** |
|---|---|
| report/ | Final PDF incident report |
| diagrams/ | Attack-chain and workflow diagrams |
| evidence-redacted/ | Redacted screenshots or supporting images |
| methodology/ | Environmental notes, trial protocol, prompt variants |
| responsible-publication-note.md | Publication and safety statement |

## Skills Demonstrated

### AI Evaluation

- Black-box LLM evaluation
- Adversarial AI testing
- Prompt injection analysis
- Indirect prompt injection research
- Behavioral evaluation of LLMs
- AI safety assessment

### Security Analysis
- Threat modeling
- Attack surface analysis
- Risk assessment
- Social-engineering analysis
- Trust-boundary analysis
- Defensive mitigation design

### Research Methodology
- Hypothesis-driven testing
- Baseline comparison
- Controlled prompt variation
- Reproducibility assessment
- Evidence collection
- Trial result categorization

### AI Systems
- Browser-integrated AI evaluation
- Educational AI workflow analysis
- Human-AI interaction analysis
- Context contamination analysis
- Model instruction-following behavior analysis

### Technical Communication
- Security incident reporting
- Executive summary writing
- Visual threat modeling
- Technical documentation
- Responsible publication framing
- Portfolio-ready research presentation

## Responsible Publication Note

This case study was conducted in a controlled environment. No real student credentials or assignment contents from any institution were used. The URL used in testing was researcher-controlled, did not collect private or sensitive information, and has been redacted from the public report. Perplexity was notified on 2026-07-01 and will update this report or repository with any response, clarification, or remediation guidance received. This report is published for defensive evaluation and portfolio documentation.

## Author

Brian C. Melton, Ph.D.

### License / Use

This repository is shared publicly for portfolio, educational, and defensive research purposes. Unless otherwise stated, the report, diagrams, and supporting materials are © Brian C. Melton. Reuse or republication requires attribution and permission.


