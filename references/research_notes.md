# Research Notes

## Source: LangChain - State of AI Agents
- URL: https://www.langchain.com/stateofaiagents
- Why this source matters: Large, industry-facing survey (LangChain) that directly addresses adoption, use cases, controls, and production barriers for AI agents. Serves as a timely empirical anchor for market signals and engineering priorities.
- Reliability tier: strong-secondary (survey published by a major vendor; primary for vendor-led industry insight but may have sampling biases toward tech-oriented respondents)
- Date accessed: 2026-03-18

### Evidence extracted
- Claim or data point: Survey sample size and respondent composition
  - Support: "We surveyed over 1,300 professionals — from engineers and product managers to business leaders and executives"
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
  - Support: "Performance quality stands out as the top concern — more than twice as significant as other factors like cost and safety."
  - Intended section(s): Production Challenges and Guardrails; Executive Summary
  - Confidence: high

### Open questions
- Representativeness: LangChain's respondent pool is 60% from technology industry and skewed to smaller organizations (<100 employees = 51%). How does this affect generalizability to large enterprises?
- Temporal stability: Are these adoption rates consistent across other independent surveys (vendor-agnostic sources) conducted in late 2024 / 2025?
- Vendor influence: Because LangChain publishes agent frameworks and observability/validation products (LangSmith), to what extent do product mentions and tooling priorities reflect vendor positioning vs. broad market needs?

### Draft implications
- Observed high interest and non-trivial production presence imply immediate demand for harness capabilities: observability/tracing, permissioned tool execution, offline evaluation pipelines, and incident response workflows.
- The prominence of research/summarization and productivity use cases suggests harnesses must prioritize retrieval, grounding, and summarization evaluation metrics alongside action/permission controls.
- Given performance/quality is the top barrier, investment in systematic offline evaluation, regression testing, and human-in-the-loop approval paths should be prioritized by engineering teams.


## Source: Microsoft Copilot Studio product page
- URL: https://www.microsoft.com/en-us/microsoft-365-copilot/microsoft-copilot-studio
- Why this source matters: Vendor product page showing concrete enterprise features (agent templates, multi-agent orchestration, analytics & governance) and customer stories that map to high-value use cases.
- Reliability tier: strong-secondary (major cloud vendor product documentation and customer case studies)
- Date accessed: 2026-03-18

### Evidence extracted
- Claim or data point: Copilot Studio enables building, customizing, and publishing agents across Microsoft 365 apps and external channels
  - Support: Product landing page copy and features list (agent templates, multi-agent orchestration, publishing channels)
  - Intended section(s): Leading Use Cases; Vendor Landscape
  - Confidence: high

- Claim or data point: Enterprise governance features (Purview integration, admin controls, analytics)
  - Support: Documentation and admin center references on product page
  - Intended section(s): Production Challenges and Guardrails; Recommendations
  - Confidence: high

### Draft implications
- Large vendors are packaging harness capabilities as integrated enterprise offerings (connectors, governance, analytics), lowering entry-barriers for organizations already in those ecosystems.


## Source: AIMultiple - LLM Observability Tools
- URL: https://aimultiple.com/llm-observability
- Why this source matters: Independent comparison that synthesizes vendor strengths and trade-offs across observability, evaluation, and cost-tracking tools; useful for triangulating vendor capabilities and expected trade-offs for engineering teams.
- Reliability tier: medium-secondary (analyst/aggregator content with vendor-reported features; useful for feature comparison but requires cross-checking primary docs for critical claims)
- Date accessed: 2026-03-18

### Evidence extracted
- Claim or data point: Tool positioning by strength
  - Support: AIMultiple organizes vendors by "best for" categories: W&B Weave for experiments/versioning, LangSmith for agent-level traces and evaluation, Helicone for proxy-based cost tracking and caching, Langfuse for open-source/self-hosted tracing.
  - Intended section(s): Vendor and Tooling Landscape; Production Challenges and Guardrails
  - Confidence: high

- Claim or data point: Observability categories and metrics
  - Support: AIMultiple details core metric categories (latency, throughput, token usage, correctness/factuality) and recommends mapping these to experiment and production dashboards.
  - Intended section(s): Production Challenges and Guardrails; Vendor Landscape
  - Confidence: high

### Open questions
- Pricing and enterprise feature parity: AIMultiple summarizes features but not enterprise SLAs or detailed pricing; need vendor docs for procurement decisions.
- Integration friction: how easily do observability tools integrate with non-LangChain stacks (self-built agent harnesses) at scale?

### Draft implications
- Observability tooling landscape is meaningfully segmented: teams should pick tools based on primary needs (tracing vs. experiment/versioning vs. cost proxies) and plan for integration/plumbing work if their stack diverges from a vendor's native ecosystem.


## Notes: additional sources to fetch
- Independent analyst surveys (Gartner, Forrester, McKinsey) to triangulate adoption statistics.
- Observability and evaluation tooling comparisons (LangSmith, Weights & Biases, Sentry for LLMs).
- Public case studies that quantify ROI (reduced handle time, cost savings from automation) for customer support & finance agents.
