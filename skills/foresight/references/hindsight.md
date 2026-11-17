# Stress-testing with Hindsight

Hindsight collects forecasts that institutions publish (economic outlooks, technology trend lists, hype cycles, risk reports, scenario sets and more) and grades each one against what happened. Page: https://www.envisioning.com/hindsight. Data and rules: https://github.com/envisioning/hindsight.

## What a verdict means

Each claim gets one verdict: hit, partial, miss, unfalsifiable or ungradable, contested, or not due yet. Each kind of claim has its own test:

| Kind | Test |
| --- | --- |
| Numeric | Within 0.5 points (rates) or 10% (levels) of the actual value |
| Targets | Within 10% of the target figure by its date |
| Predictions | Came about by its date |
| Technology | Mainstream by its date |
| Studies | In use in its field, or on sale, by its date |
| Surveys | The panel's majority view came about |
| Trends | Kept, renamed or dropped by the publisher in later editions |
| Rankings | Risks that happened, events ranked high |
| Scenarios | Reality fell inside the scenario set |

Kinds are never mixed in one figure. Hit rates carry a 95% interval, widened by the audit error rate. Below 20 graded claims, Hindsight shows counts only. Hindsight puts publishers side by side and does not rank them. Read current numbers from the tools or the site. Do not copy them from memory.

## How to use it in a scan

For each timing claim that matters to the decision (for example "this technology will be mainstream within three years"):

1. Call `search_hindsight` with the subject. Without MCP, find the subject page under `/hindsight/subjects/<id>`.
2. Read what earlier forecasts said about the subject, when, and how they were graded.
3. Ask:
   - Did earlier forecasts place this subject too early, on time, or too late?
   - Was the subject dropped or renamed in later editions of a trend list?
   - Is your claim the same kind as the graded ones? A technology placement is tested differently from a numeric target.
4. Change the output if the record says so: move the horizon, widen it, or lower the reliability. Write down what you changed and why, with the claim permalinks.
5. If Hindsight has nothing on the subject, say so. Absence of graded forecasts is not evidence either way.

## Reporting

In the radar, add a "Hindsight check" section. For each checked claim: your original placement, what past forecasts said, their verdicts with links, and your final placement.

Do not present a publisher's hit rate as a ranking or as a reason to trust or dismiss one source. Use it as a base rate for that kind of claim.
