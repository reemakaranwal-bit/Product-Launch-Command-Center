# Architecture Notes

## High-level flow
1. Stakeholder starts a voice conversation at the shared ElevenLabs entry point.
2. The workflow evaluates the caller's request.
3. LLM-condition routing selects the appropriate specialist path.
4. The relevant subagent responds using its scoped knowledge base.

## Specialist boundaries
- Technical Readiness: technical and operational launch-preparedness context.
- Marketing & GTM: go-to-market and marketing-readiness context.
- Executive Briefing: concise leadership-oriented summaries and decision context.

## Design considerations
- Keep each specialist's knowledge scope focused and current.
- Define clear routing conditions and test ambiguous or multi-intent requests.
- Provide a fallback path when intent is unclear or no specialist is appropriate.
- Evaluate routing accuracy separately from answer quality.
- Avoid placing confidential launch information in public knowledge sources.
- Monitor usage, latency, fallback behavior and user feedback before production use.

## Evaluation ideas
- Routing accuracy by stakeholder intent.
- Answer groundedness against the relevant knowledge base.
- Successful completion of representative stakeholder tasks.
- Rate of incorrect handoffs and fallback responses.
- User satisfaction and perceived usefulness.
