# Prompt Blueprint

A drafting table for AI instructions. Type a rough request, pick a target
platform (Claude, GPT, Gemini, or Any), and get back a structured,
ready-to-paste prompt built with the PCTCE framework (Persona, Context,
Task, Constraints, Evaluation).

**[Open the live page](https://YOUR_GITHUB_USERNAME.github.io/prompt-blueprint/)**

## What it does

- Classifies the request (code, writing, analysis, or conversational) and
  scopes the persona and task steps to match.
- Detects programmatic intent (API, JSON, pipeline, schema, and so on) and
  switches the output to strict-JSON mode automatically.
- Adapts structure per platform: XML tags for Claude, context-first
  hierarchy for Gemini, portable markdown for GPT and Any.
- Flags real gaps only. A "Sharpen it further" panel appears when something
  is actually missing (audience, a tone example, a schema), not as filler.
- Copies or downloads the result as a `.md` file.

## How it works

Everything runs client-side in a single `index.html`. There is no backend
and no API call: it is a deterministic, rule-based generator that applies
the PCTCE framework and platform-specific structuring on-device. Treat the
output as a strong first draft, not a substitute for review.

## Running locally

Open `index.html` directly in a browser, or serve the folder:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

## License

MIT
