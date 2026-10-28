# Native-reasoning capture study: trace_60_native_v1

Valid judgments: **1440/1440**; 1494 finalized attempts; 0 pending jobs.

[Browse the casebook](trace_casebook.html). Full machine-readable report: `trace_results.json`.

## Interpretation

- Primary observations are the first valid verdict per expected job; their native fields come from that same attempt.
- Missing, empty or unrecognized native fields do not mean the model did not reason. Unrecognized structures remain preserved and are counted separately from empty fields. Nonempty text is not proof of a faithful or complete account of its decision.
- Native field formats and lengths are not directly comparable across models. Provider-reported truncation is flagged; its absence does not establish completeness.
- A length finish reason indicates response-budget exhaustion; it does not identify whether native reasoning, final content, or both were truncated.
- All-attempt diagnostics include errors and retries and are secondary; they are not additional independent judgments.
- Agreement is reported only when every expected job has a valid verdict, regardless of native-trace availability. No selected complete-case agreement is substituted for an incomplete run.
- BA verdicts are canonicalized to the original pair orientation. Mean peer kappa averages separately computed peer-by-order kappas, not pooled AB/BA labels; undefined components are counted and omitted from the mean.
- Overall topic rows average the six separately computed peer-by-order coefficients (three model pairs in two orders) and count each conversation pair once. Order-specific details remain in the JSON.
- All agreement measures are descriptive. There are no confidence intervals; judgments sharing a pair are dependent. Agreement does not establish accuracy or validate a judge.

## Individual-model mean peer κ, both orders

| Model | Transparency | Consistency | Refinement | Overall |
| --- | --- | --- | --- | --- |
| gpt-oss-20b | 0.318 | 0.217 | 0.265 | 0.386 |
| qwen3-32b | 0.344 | 0.277 | 0.352 | 0.300 |
| Nemotron-3-Nano-30B-A3B | 0.385 | 0.275 | 0.341 | 0.383 |

## Primary native-trace coverage

| Model | Rubric | Valid / expected | Field present | Nonempty | Absent | Present but empty | Unrecognized | Response truncation flag | Nonempty / valid |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| gpt-oss-20b | overall | 120/120 | 120 | 120 | 0 | 0 | 0 | 0 | 100.0% |
| gpt-oss-20b | transparency | 120/120 | 120 | 120 | 0 | 0 | 0 | 0 | 100.0% |
| gpt-oss-20b | consistency | 120/120 | 120 | 120 | 0 | 0 | 0 | 0 | 100.0% |
| gpt-oss-20b | refinement | 120/120 | 120 | 120 | 0 | 0 | 0 | 0 | 100.0% |
| qwen3-32b | overall | 120/120 | 120 | 120 | 0 | 0 | 0 | 0 | 100.0% |
| qwen3-32b | transparency | 120/120 | 120 | 120 | 0 | 0 | 0 | 0 | 100.0% |
| qwen3-32b | consistency | 120/120 | 120 | 120 | 0 | 0 | 0 | 0 | 100.0% |
| qwen3-32b | refinement | 120/120 | 120 | 120 | 0 | 0 | 0 | 0 | 100.0% |
| Nemotron-3-Nano-30B-A3B | overall | 120/120 | 120 | 120 | 0 | 0 | 0 | 0 | 100.0% |
| Nemotron-3-Nano-30B-A3B | transparency | 120/120 | 120 | 120 | 0 | 0 | 0 | 0 | 100.0% |
| Nemotron-3-Nano-30B-A3B | consistency | 120/120 | 120 | 120 | 0 | 0 | 0 | 0 | 100.0% |
| Nemotron-3-Nano-30B-A3B | refinement | 120/120 | 120 | 120 | 0 | 0 | 0 | 0 | 100.0% |

## Attempts and token caps (secondary diagnostics)

| Model | Finalized attempts | Accepted jobs | Error/interrupted attempts | Retried jobs | Escalated jobs | Accepted by cap | All attempts by cap | Nonempty traces in all attempts | Truncated attempts |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| gpt-oss-20b | 509 | 480 | 29 | 25 | 25 | 2048: 455, 4096: 21, 8192: 4 | 2048: 480, 4096: 25, 8192: 4 | 509 | 29 |
| qwen3-32b | 480 | 480 | 0 | 0 | 0 | 2048: 480 | 2048: 480 | 480 | 0 |
| Nemotron-3-Nano-30B-A3B | 505 | 480 | 25 | 19 | 19 | 2048: 461, 4096: 16, 8192: 3 | 2048: 481, 4096: 20, 8192: 4 | 505 | 25 |

## Individual-model detail: peer agreement and defined components

| Model | Rubric | Mean peer κ | Defined κ components | Mean peer AC1 | Mean peer agreement |
| --- | --- | --- | --- | --- | --- |
| gpt-oss-20b | overall | 0.386 | 4/4 | 0.531 | 65.8% |
| gpt-oss-20b | transparency | 0.318 | 4/4 | 0.523 | 64.2% |
| gpt-oss-20b | consistency | 0.217 | 4/4 | 0.192 | 45.0% |
| gpt-oss-20b | refinement | 0.265 | 4/4 | 0.301 | 51.7% |
| qwen3-32b | overall | 0.300 | 4/4 | 0.425 | 58.8% |
| qwen3-32b | transparency | 0.344 | 4/4 | 0.537 | 65.4% |
| qwen3-32b | consistency | 0.277 | 4/4 | 0.354 | 55.0% |
| qwen3-32b | refinement | 0.352 | 4/4 | 0.448 | 60.8% |
| Nemotron-3-Nano-30B-A3B | overall | 0.383 | 4/4 | 0.539 | 66.2% |
| Nemotron-3-Nano-30B-A3B | transparency | 0.385 | 4/4 | 0.585 | 68.8% |
| Nemotron-3-Nano-30B-A3B | consistency | 0.275 | 4/4 | 0.338 | 53.3% |
| Nemotron-3-Nano-30B-A3B | refinement | 0.341 | 4/4 | 0.450 | 60.8% |

## Agreement by rubric and order

| Rubric | Order | Pairs | Mean κ | Mean AC1 | Agreement | Undefined κ |
| --- | --- | --- | --- | --- | --- | --- |
| overall | AB | 60 | 0.289 | 0.451 | 60.0% | 0 |
| overall | BA | 60 | 0.424 | 0.545 | 67.2% | 0 |
| transparency | AB | 60 | 0.334 | 0.541 | 65.6% | 0 |
| transparency | BA | 60 | 0.365 | 0.555 | 66.7% | 0 |
| consistency | AB | 60 | 0.232 | 0.282 | 50.0% | 0 |
| consistency | BA | 60 | 0.280 | 0.308 | 52.2% | 0 |
| refinement | AB | 60 | 0.304 | 0.403 | 57.8% | 0 |
| refinement | BA | 60 | 0.335 | 0.397 | 57.8% | 0 |

## Pairwise agreement by rubric and order

| Rubric | Order | Model A | Model B | Pairs | κ | AC1 | Agreement |
| --- | --- | --- | --- | --- | --- | --- | --- |
| overall | AB | gpt-oss-20b | qwen3-32b | 60 | 0.314 | 0.418 | 58.3% |
| overall | AB | gpt-oss-20b | Nemotron-3-Nano-30B-A3B | 60 | 0.313 | 0.531 | 65.0% |
| overall | AB | qwen3-32b | Nemotron-3-Nano-30B-A3B | 60 | 0.241 | 0.404 | 56.7% |
| overall | BA | gpt-oss-20b | qwen3-32b | 60 | 0.294 | 0.416 | 58.3% |
| overall | BA | gpt-oss-20b | Nemotron-3-Nano-30B-A3B | 60 | 0.625 | 0.757 | 81.7% |
| overall | BA | qwen3-32b | Nemotron-3-Nano-30B-A3B | 60 | 0.352 | 0.463 | 61.7% |
| transparency | AB | gpt-oss-20b | qwen3-32b | 60 | 0.208 | 0.443 | 58.3% |
| transparency | AB | gpt-oss-20b | Nemotron-3-Nano-30B-A3B | 60 | 0.429 | 0.601 | 70.0% |
| transparency | AB | qwen3-32b | Nemotron-3-Nano-30B-A3B | 60 | 0.365 | 0.578 | 68.3% |
| transparency | BA | gpt-oss-20b | qwen3-32b | 60 | 0.347 | 0.506 | 63.3% |
| transparency | BA | gpt-oss-20b | Nemotron-3-Nano-30B-A3B | 60 | 0.291 | 0.541 | 65.0% |
| transparency | BA | qwen3-32b | Nemotron-3-Nano-30B-A3B | 60 | 0.457 | 0.618 | 71.7% |
| consistency | AB | gpt-oss-20b | qwen3-32b | 60 | 0.176 | 0.189 | 45.0% |
| consistency | AB | gpt-oss-20b | Nemotron-3-Nano-30B-A3B | 60 | 0.180 | 0.157 | 41.7% |
| consistency | AB | qwen3-32b | Nemotron-3-Nano-30B-A3B | 60 | 0.341 | 0.501 | 63.3% |
| consistency | BA | gpt-oss-20b | qwen3-32b | 60 | 0.262 | 0.228 | 48.3% |
| consistency | BA | gpt-oss-20b | Nemotron-3-Nano-30B-A3B | 60 | 0.250 | 0.194 | 45.0% |
| consistency | BA | qwen3-32b | Nemotron-3-Nano-30B-A3B | 60 | 0.329 | 0.500 | 63.3% |
| refinement | AB | gpt-oss-20b | qwen3-32b | 60 | 0.254 | 0.302 | 51.7% |
| refinement | AB | gpt-oss-20b | Nemotron-3-Nano-30B-A3B | 60 | 0.313 | 0.379 | 56.7% |
| refinement | AB | qwen3-32b | Nemotron-3-Nano-30B-A3B | 60 | 0.345 | 0.528 | 65.0% |
| refinement | BA | gpt-oss-20b | qwen3-32b | 60 | 0.298 | 0.295 | 51.7% |
| refinement | BA | gpt-oss-20b | Nemotron-3-Nano-30B-A3B | 60 | 0.194 | 0.229 | 46.7% |
| refinement | BA | qwen3-32b | Nemotron-3-Nano-30B-A3B | 60 | 0.512 | 0.666 | 75.0% |

## Overall agreement by topic, both orders

| Topic | Unique pairs | Mean κ | Mean AC1 | Agreement | Undefined κ |
| --- | --- | --- | --- | --- | --- |
| analysis | 20 | 0.373 | 0.504 | 64.2% | 0 |
| personal-advice | 20 | 0.380 | 0.479 | 62.5% | 0 |
| how-to | 20 | 0.307 | 0.523 | 64.2% | 0 |

Primary coverage counts refer only to accepted verdict attempts. The response truncation flag can apply with or without a nonempty native field; it does not identify which response component was truncated. Unrecognized native structures are distinct from empty fields. The JSON includes these combinations and separate all-attempt coverage by model and rubric.

Generated: 2026-10-22T21:31:53.241038+00:00


## Public data attribution

Conversation excerpts come from [WildChat-1M (AllenAI)](https://huggingface.co/datasets/allenai/WildChat-1M), available under the [ODC Attribution License 1.0](https://opendatacommons.org/licenses/by/1-0/).

Public excerpts have identifying path segments, private network addresses, and credential-like strings redacted; ratings and statistics use the original frozen inputs.
