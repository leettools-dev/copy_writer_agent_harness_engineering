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


## Source: LangSmith (LangChain product page)
- URL: https://www.langchain.com/langsmith/observability
- Why this source matters: Primary product documentation showing how a leading vendor positions observability, tracing, evaluation, and deployment features for agents. Useful for concrete claims about SDK support, tracing semantics, and deployment options.
- Reliability tier: strong-secondary (vendor primary docs; authoritative about the product but may emphasize strengths over limitations)
- Date accessed: 2026-03-18

### Evidence extracted
- Claim or data point: LangSmith provides tracing and observability for agents and LLMs
  - Support: Product page: "LangSmith Observability gives you complete visibility into agent behavior... Trace your preferred framework or integrate LangSmith with any agent stack using our Python, Typescript, Go, or Java SDKs."
  - Intended section(s): Vendor and Tooling Landscape; Production Challenges and Guardrails
  - Confidence: high

- Claim or data point: Monitoring and evaluation features
  - Support: LangSmith monitoring includes cost tracking, online evals (LLM-as-judge), tool/agent trajectory monitoring, webhooks/PagerDuty alerts, and dashboards for token usage, latency (P50, P99), error rates, and feedback scores.
  - Intended section(s): Vendor and Tooling Landscape; Recommendations
  - Confidence: high

- Claim or data point: Integration and deployment modes
  - Support: Docs and FAQ indicate SDKs, OpenTelemetry support, managed cloud/BYOC/self-hosted deployment options, and assurances about data residency and not training on customer data.
  - Intended section(s): Vendor and Tooling Landscape; Recommendations for Engineering Teams
  - Confidence: high

- Claim or data point: Pricing and tiers
  - Support: LangSmith provides a free tier for development and scales with trace volume; enterprise pricing available via sales (product page / pricing link).
  - Intended section(s): Vendor and Tooling Landscape; Recommendations
  - Confidence: medium

### Open questions
- Latency and overhead in high-throughput agent loops beyond SDK assurances: how trace payloads affect cost and operational plumbing at scale?
- Enterprise SLA specifics and comparative pricing vs. open-source/self-hosted alternatives.

### Draft implications
- Vendor platforms like LangSmith reduce integration friction by offering SDKs and OTel bridges, but teams should validate latency and cost at expected trace volumes before committing to managed plans.
- Self-hosted/BYOC options are important for compliance-heavy teams; procurement should collect SLA and data-residency terms early.


## Source: AIMultiple - LLM Observability Tools
- URL: https://aimultiple.com/llm-observability
- Why this source matters: Independent comparison that synthesizes vendor strengths and trade-offs across observability, evaluation, and cost-tracking tools; useful for triangulating vendor capabilities and expected trade-offs for engineering teams.
- Reliability tier: medium-secondary (analyst/aggregator content with vendor-reported features; useful for feature comparison but requires cross-checking primary docs for critical claims)
- Date accessed: 2026-03-18

### Evidence extracted
- Claim or data point: Tool positioning by strength
  - Support: AIMultiple organizes vendors by "best for" categories: W&B for experiments/versioning, LangSmith for agent-level traces and evaluation, Helicone for proxy-based cost tracking and caching, Langfuse for open-source/self-hosted tracing.
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


## Source: Langfuse (open-source tracing & observability)
- URL: https://www.langfuse.io/
- Why this source matters: Representative open-source alternative for tracing and agent observability; provides a self-hosted path and shows feature parity tradeoffs versus managed vendors.
- Reliability tier: medium-secondary (project documentation and community resources; accurate for product claims but requires evaluation for SLA and scale characteristics)
- Date accessed: 2026-03-18

### Evidence extracted
- Claim or data point: Langfuse provides tracing, evaluation, and debug tooling for LLM applications with a focus on self-hosting and data control
  - Support: Project docs and feature lists
  - Intended section(s): Vendor and Tooling Landscape; Recommendations
  - Confidence: medium

### Open questions
- Operational overhead at scale: resource needs, maintenance effort, and how it compares to managed alternatives.

### Draft implications
- Langfuse is a strong candidate for teams with strict data residency or cost constraints who can tolerate some operational overhead; procurement should include an internal TCO exercise.


## Source: Helicone (proxy-based observability, cost tracking)
- URL: https://www.helicone.ai/
- Why this source matters: Helicone operates as a proxy to capture telemetry and provide cost-tracking and caching for LLM usage; useful when teams need low-friction cost visibility and request caching.
- Reliability tier: medium-secondary (vendor docs; useful for feature claims)
- Date accessed: 2026-03-18

### Evidence extracted
- Claim or data point: Helicone provides request-level telemetry, token-cost attribution, and caching to reduce repeated token spend
  - Support: Product documentation and blogs
  - Intended section(s): Vendor and Tooling Landscape; Recommendations
  - Confidence: medium

### Draft implications
- Proxy-based observability can be an effective low-effort way to obtain cost and token-level dashboards without deep SDK integration, but it introduces an operational choke point and data-flow consideration (routing traffic through proxy).


## Notes: additional sources to fetch
- Independent analyst surveys (Gartner, Forrester, McKinsey) to triangulate adoption statistics.
- Observability and evaluation tooling comparisons (LangSmith, Weights & Biases, Sentry for LLMs, Helicone, Langfuse).
- Public case studies that quantify ROI (reduced handle time, cost savings from automation) for customer support & finance agents.
