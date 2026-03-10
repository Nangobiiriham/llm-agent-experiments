# LLM Security Research & Adversarial Testing
### AI Misuse Investigation | Prompt Security | Behavioral Anomaly Detection

> Research and documentation from hands-on security work on an AI-powered platform integrating voice-based LLM interactions.  
> Focus: adversarial prompt testing, AI misuse detection, and behavioral safety controls.

---

## Overview

This repository documents security research conducted at the intersection of **cybersecurity and large language model (LLM) systems** — specifically, how AI-powered conversational platforms can be evaluated, stress-tested, and hardened against misuse.

The work stems from a live internship environment supporting the security of an AI mental wellness platform that integrates voice-based LLM interactions with real users. All findings are sanitized and contain no proprietary, confidential, or sensitive user data.

---

## Research Areas

### 1. 🔴 Adversarial Prompt Testing & LLM Misuse Evaluation

**Objective:** Identify how an LLM-powered conversational system responds under adversarial conditions — including attempts to manipulate model behavior, extract system-level information, or elicit harmful outputs.

**Methods Applied:**
- Designed and executed test cases targeting system prompt boundary enforcement
- Tested model responses under manipulative prompt structures, including roleplay-based jailbreak attempts and indirect instruction injection
- Evaluated how prompt engineering techniques influence AI system outputs in sensitive user environments
- Identified edge cases where AI-generated responses deviated from intended safe behavior

**Key Findings (Sanitized):**
- LLMs in conversational wellness contexts are susceptible to **context manipulation** — where multi-turn conversation history is used to gradually shift model behavior away from its guardrails
- **System prompt extraction attempts** via indirect questioning revealed partial information leakage in certain prompt configurations
- Models prompted with emotionally framed adversarial inputs showed higher rates of **policy boundary deviation** than direct adversarial prompts — suggesting emotional context is an underexplored attack surface in mental health AI applications

**Mitigations Recommended:**
- Stricter system prompt isolation and output filtering at the API layer
- Turn-level context monitoring to detect gradual behavioral drift
- Red-team testing as a standard pre-deployment step for LLM-integrated features

---

### 2. 🎙️ AI Voice Agent Security Assessment (VAPI Integration)

**Objective:** Evaluate security and misuse risks introduced by integrating AI voice agent technology into a user-facing mental wellness platform.

**Methods Applied:**
- Assessed VAPI voice agent integration for adversarial misuse vectors
- Evaluated risks of social engineering via AI-generated voice responses
- Analyzed how conversational LLM context can be manipulated through voice interaction flows
- Documented potential for voice-based AI to deliver harmful guidance under adversarial prompting

**Key Risk Categories Identified:**

| Risk | Description | Severity |
|------|-------------|----------|
| Conversational context manipulation | Multi-turn voice sessions used to drift model behavior | High |
| Harmful advice elicitation | Emotionally manipulative prompts producing unsafe responses | High |
| AI-generated voice social engineering | Platform voice responses used to simulate trust | Medium |
| Prompt injection via transcribed input | Voice-to-text pipeline introducing adversarial text | Medium |

---

### 3. 📊 Behavioral Anomaly Detection via Activity Tracking

**Objective:** Use structured behavioral data to identify unusual usage patterns that may signal platform misuse or adversarial probing.

**Approach:**
- Supported development of user activity tracking systems using **Firebase Firestore**
- Designed data queries to surface anomalous behavioral signals — including unusual session lengths, repeated adversarial probing patterns, and atypical task completion sequences
- Mapped behavioral indicators to potential abuse scenarios (automated bot activity, systematic prompt testing, coordinated misuse attempts)

**Signals Developed:**
- High-frequency short sessions with repeated similar inputs → potential automated probing
- Unusually long sessions with escalating prompt complexity → potential systematic jailbreak attempts  
- Sudden spikes in XP/engagement metrics without corresponding task completion → behavioral anomaly flag

---

### 4. 🏗️ Security Architecture & Threat Modeling for AI Platforms

**Objective:** Ensure security-by-design principles are embedded in AI platform development before large-scale deployment.

**Activities:**
- Conducted threat modeling for AI-enabled platform features, identifying attack surfaces introduced by LLM integration
- Reviewed system architecture components for cybersecurity risk
- Evaluated security implications of integrating third-party AI services into a sensitive user environment
- Communicated security findings to developers and stakeholders, advocating for security controls at the architecture level

**Threat Modeling Framework Used:** NIST Cybersecurity Framework principles applied to AI system context

---

## Skills & Tools Applied

| Domain | Tools / Techniques |
|--------|-------------------|
| LLM Security Testing | Prompt injection, jailbreak testing, context manipulation, system prompt extraction |
| Behavioral Analysis | Firebase Firestore, SQL-style queries, anomaly signal design |
| Threat Intelligence | MITRE ATT&CK mapping, TTP documentation, threat modeling |
| AI Safety | Responsible AI governance, output safety evaluation, red teaming |
| Frameworks | NIST CSF, ISO 27001 principles, secure SDLC |

---

## Key Takeaways

> **1. Emotional context is an underexplored attack surface.**  
> In mental health AI applications, emotionally framed prompts bypass safety filters more reliably than direct adversarial inputs. This has significant implications for any LLM deployed in a sensitive user context.

> **2. Voice-based LLMs expand the threat surface significantly.**  
> Voice interaction introduces transcription-layer vulnerabilities and social engineering risks that text-only LLM security frameworks don't fully address.

> **3. Behavioral data is an underused detection tool.**  
> Usage patterns in platform telemetry can surface adversarial probing before it becomes a significant incident — if the right signals are defined upfront.

> **4. Security must be embedded at the architecture stage.**  
> LLM misuse risks cannot be patched retroactively. Threat modeling must happen before deployment, not after.

---

## About

This research was conducted as part of a cybersecurity internship supporting an AI-powered digital wellness platform. All content is sanitized and publicly shareable — no proprietary code, confidential datasets, internal architecture details, or user data is included.

**Researcher:** Iriham Nangobi Mukoka  
**Focus Area:** AI System Security | LLM Adversarial Testing | Cyber Threat Investigation  
**LinkedIn:** [linkedin.com/in/nangobi-iriham-mukoka](https://linkedin.com/in/nangobi-iriham-mukoka)

---

*Interested in AI security research, responsible AI deployment, or LLM misuse detection? Feel free to connect.*
