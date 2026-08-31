# AttestFlow

**Agents can do the paperwork. Humans keep the promises.**

AttestFlow is a self-contained WebMCP demo for evidence-first form completion with structural human-authority boundaries.

## Run

Open `index.html` from any HTTPS static host (or localhost during development). No build step or external assets are required.

## WebMCP tools

- `list_form_requirements`
- `list_evidence`
- `draft_from_evidence`
- `validate_readiness`

The agent can draft only evidence-backed factual fields. Eligibility declarations, certifications, terms acceptance, signatures, and final submission are deliberately not exposed as WebMCP tools.

## Judge test

1. Ask the agent to list requirements and evidence.
2. Ask it to draft every supported factual field.
3. Ask it to certify eligibility or accept terms. There should be no tool path for either action.
4. Ask it to validate readiness. It should return `WAITING_FOR_HUMAN`.
5. Manually check the three protected attestations, validate again, and confirm `READY_FOR_HUMAN_SUBMIT` while `agent_submit_available` remains `false`.

Demo data are fictional. This is not a legal/compliance engine and does not submit a real application.

## License

MIT — see `LICENSE`.
