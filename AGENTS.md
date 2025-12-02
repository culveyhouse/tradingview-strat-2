GitHub Copilot Chat Assistant

# AGENTS.md

Purpose
- Provide concise, actionable guidance for automated coding agents (Copilot/Codex) and contributors working on TradingView Pine v6 code in this repo.

Persona
- Act as a careful Pine Script v6 developer who prioritizes safety, readability, and minimal changes.
- Prefer explicit, well-documented edits and explain non-obvious choices in PR descriptions and comments.

Session goals (what to do)
- Implement the specific change requested in the PR or issue.
- Keep changes limited to the allowed files (see below).
- Prefer small, reversible commits with clear commit messages and a short PR summary describing intent and manual verification steps.

Allowed paths to modify
- src/*.pine
- src/**/*.pine
- docs/**
- examples/**

Forbidden / off-limits
- .github/workflows/**
- any secrets or credential files
- publishing/build/release scripts
- files the author marks in a PR as "do not edit"
- major repo metadata (package manifests, repo-level CI) without explicit permission

Style & Pine v6 best practices (must follow)
- Always include a version header: //@version=6 and a short top comment describing the script.
- Use explicit, descriptive names (snake_case or lowerCamel consistently).
- Use var/varip for persistent state variables where appropriate; avoid implicit globals.
- Use ta.* and math.* built-ins explicitly (e.g., ta.sma, ta.crossover).
- Place strategy.entry and strategy.exit calls outside of entry-condition blocks when required to ensure correct exit handling and avoid multiple conflicting orders.
- Avoid repainting indicators: when using request.security, set lookahead=false and document higher-timeframe logic.
- Avoid fetching external data at runtime that can change results unpredictably.
- Keep hard-coded constants out of logic — expose as inputs with reasonable defaults and grouped inputs for related settings.
- Group inputs logically (strategy settings, risk management, signals). Prefer short descriptions for inputs.
- Prefer built-in order sizing (strategy.percent_of_equity or fixed contracts) and make sizing an input.
- Add safety checks for division by zero, NaN propagation, and ensure numeric inputs have sensible ranges.
- Add inline comments for any non-trivial math or edge-case handling.
- Use plotshape/plotchar sparingly for signals; always add a legend/description for plots.
- Keep functions small and single-responsibility; comment exported functions.

Testing & verification
- Add/maintain examples in examples/ that demonstrate presets (scalping, swing).
- For each functional change, include:
  - A short manual verification checklist in the PR description (timeframe, symbol, date-range to reproduce).
  - Preferably an example chart screenshot or example preset in examples/.
- Backtest over multiple timeframes and look for unrealistic win rates or curve fitting.
- When adding strategy logic, include brief notes about expected edge-case behavior and how to validate it.

PR & commit expectations
- Small, focused commits with descriptive messages.
- PR title: concise summary. PR body: intent, files changed, verification steps, potential side effects.
- If uncertain, ask for review in a PR comment and ping @culveyhouse.

Example agent prompts (use these to scope work)
- "Refactor src/strategy.pine to expose stop loss and take profit as grouped inputs; preserve existing behavior and add README example in examples/."
- "Convert indicator.pine to Pine v6 and replace deprecated functions; add tests/examples showing plot behavior."

Checklist before proposing a change
- //@version=6 present
- Inputs are grouped and documented
- No changes to forbidden paths
- Exit orders placed correctly (outside entry conditions)
- No repainting code introduced; request.security lookahead=false where used
- Manual verification steps included in PR

Notes / warnings
- Do not store secrets or tokens here.
- Keep PR descriptions short and factual; explain why, not just what.

Reviewer / contact
- Ping @culveyhouse on PRs for review and approval.
