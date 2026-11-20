# Product Launch Command Center | Multi-Agent Voice AI

A multi-agent voice AI system built with **ElevenLabs Conversational AI Workflow Builder**. It provides stakeholders with one voice entry point and routes each request to the relevant launch specialist.

## 🎙️ Try the live demo

**[Open the Product Launch Command Center voice agent](https://elevenlabs.io/app/talk-to?agent_id=agent_0201m7erf8ygec9bv5fkpn1y76j7)**

The demo opens in ElevenLabs. Microphone permission may be required.

## Problem

Product launches involve stakeholders with different information needs. Technical teams need readiness context, marketing teams need go-to-market information, and executives need concise briefings. A single general-purpose assistant may not provide the right depth or framing for every audience.

## Solution

1. A stakeholder starts a conversation through one voice entry point.
2. The workflow evaluates the request using LLM-condition routing.
3. The conversation is directed to the relevant specialist subagent.
4. Each specialist uses its own scoped knowledge base to respond within its domain.

## Specialist agents

| Specialist | Intended scope |
|---|---|
| **Technical Readiness** | Technical launch-preparedness questions and operational context |
| **Marketing & GTM** | Go-to-market, campaign, positioning and marketing-readiness questions |
| **Executive Briefing** | Concise leadership briefings and launch decision context |

The exact scope and behavior depend on the instructions and knowledge configured for each subagent.

## Architecture

```text
Stakeholder
    |
Single ElevenLabs Voice Entry Point
    |
Workflow Orchestration
    |
LLM-condition Routing
    |
    +-------------------+-------------------+
    |                   |                   |
Technical Readiness  Marketing & GTM  Executive Briefing
Subagent             Subagent         Subagent
    |                   |                   |
Scoped knowledge    Scoped knowledge Scoped knowledge
base                base             base
```

## Technology and concepts

- ElevenLabs Conversational AI and Workflow Builder
- Voice-based conversational interface
- Multi-agent orchestration and subagent nodes
- LLM-condition routing
- Scoped knowledge bases

## Product thinking

This prototype explores how a shared conversational entry point can reduce the effort required for stakeholders to find the right launch information. It demonstrates the importance of matching an agent's scope, context and response style to the user's role and intent.

Potential evaluation measures for a future iteration:
- Correct specialist-routing rate
- Successful task completion by stakeholder intent
- Answer relevance and groundedness
- Escalation or fallback rate
- User satisfaction and time to find information

These are proposed evaluation measures, not measured results from this prototype.

## Repository contents

```text
product-launch-command-center/
├── index.html
├── README.md
└── docs/
    └── architecture.md
```

## Publish with GitHub Pages

1. Push this repository to GitHub.
2. Open **Settings → Pages**.
3. Under **Build and deployment**, select **Deploy from a branch**.
4. Choose the `main` branch and `/ (root)`, then save.
5. Use the published Pages URL as your public project page.

## Notes

- This is an independent portfolio prototype, not a production launch-management system.
- The live voice experience is hosted by ElevenLabs; this repository contains the project page and documentation.
- Do not add API keys, private credentials, unpublished knowledge-base files or sensitive launch information to this public repository.
