# Research Notes

## Source: LangChain - State of AI Agents
- URL: https://www.langchain.com/stateofaiagents
- Why this source matters: Large, industry-facing survey (LangChain) that directly addresses adoption, use cases, controls, and production barriers for AI agents. Serves as a timely empirical anchor for market signals and engineering priorities.
- Reliability tier: strong-secondary (survey published by a major vendor; primary for vendor-led industry insight but may have sampling biases toward tech-oriented respondents)
- Date accessed: 2026-03-18

### Evidence extracted
- Claim or data point: Survey sample size and respondent composition
  - Support: "We surveyed over 1,300 professionals  from engineers and product managers to business leaders and executives"
  - Intended section(s): Market Signals and Key Statistics; Methods note in Executive Summary
  - Confidence: high

- Claim or data point: Production adoption rate
  - Support: "About **51% of respondents** are using agents in production today." (LangChain)
  - Intended section(s): Market Signals and Key Statistics; Executive Summary
  - Confidence: high

- Claim or data point: Near-term plans to implement agents
  - Support: "**78% have active plans** to implement agents into production soon."
  - Intended section(s): Market Signals and Key Statistics; Executive Summary
  - Confidence: high

- Claim or data point: Top use cases (percentages)
  - Support: "Top use cases for agents include **performing research and summarization (58%)**, followed by **personal productivity or assistance (53.5%)**, and **customer service (45.8%)".
  - Intended section(s): Leading Use Cases for LLM Agents; Executive Summary
  - Confidence: high

- Claim or data point: Controls and evaluation practices
  - Support: "Tracing and observability tools top the list of must-have controls"; offline evaluation (39.8%) cited more than online evaluation (32.5%); many teams require read-only tool permissions or human approval for write/delete actions.
  - Intended section(s): Production Challenges and Guardrails; Recommendations
  - Confidence: high

- Claim or data point: Biggest barrier to production is performance quality
  - Support: "Performance quality stands out as the top concern more than twice as significant as other factors like cost and safety."
  - Intended section(s): Production Challenges and Guardrails; Executive Summary
  - Confidence: high

### Open questions
- Representativeness: LangChain's respondent pool is 60% from technology industry and skewed to smaller companies (<100 employees = 51%). How does this affect generalizability to large enterprises?
- Temporal stability: Are these adoption rates consistent across other independent surveys (vendor-agnostic sources) conducted in late 2024 / 2025?
- Vendor influence: Because LangChain publishes agent frameworks and observability/validation products (LangSmith), to what extent do product mentions and tooling priorities reflect vendor positioning vs. broad market needs?

### Draft implications
- Observed high interest and non-trivial production presence imply immediate demand for harness capabilities: observability/tracing, permissioned tool execution, offline evaluation pipelines, and incident response workflows.
- The prominence of research/summarization and productivity use cases suggests harnesses must prioritize retrieval, grounding, and summarization evaluation metrics alongside action/permission controls.
- Given performance/quality is the top barrier, investment in systematic offline evaluation, regression testing, and human-in-the-loop approval paths should be prioritized by engineering teams.


## Source: InfoQ coverage of LangChain report
- URL: https://www.infoq.com/news/2024/12/ai-agents-langchain/
- Why this source matters: Independent tech press coverage that corroborates key findings and provides additional industry reaction.
- Reliability tier: weak-secondary (press coverage summarizing vendor report)
- Date accessed: 2026-03-18

### Evidence extracted
- Claim or data point: Industry reaction and corroboration of adoption trends
  - Support: Article summarises LangChain findings and highlights growing adoption of agent frameworks across industries.
  - Intended section(s): Market Signals and Key Statistics; Vendor Landscape
  - Confidence: medium

### Open questions
- Need to cross-check with vendor-agnostic surveys (e.g., enterprise AI adoption reports from analyst firms) for triangulation.

### Draft implications
- Press corroboration strengthens confidence that the LangChain survey reflects a visible market conversation, but independent sources should be added for stronger claims.


## Notes on additional sources to fetch (next iteration)
- Independent industry surveys (McKinsey, BCG, Gartner, O'Reilly reports) covering generative AI/agents adoption to triangulate adoption and production rates.
- Vendor landscape snapshots from cloud providers (AWS, Google, Azure) and agent framework activity (LangChain, LlamaIndex, Microsoft Copilot X, Replit, Perplexity, Cursor).
- Observability and evaluation tooling comparisons (LangSmith, Weights & Biases, Sentry-like tracing for LLMs).

