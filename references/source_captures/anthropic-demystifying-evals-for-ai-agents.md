<!-- generated-by: copy_writer_agent.runtime_sync -->
# Anthropic - "Demystifying evals for AI agents"

- URL: https://www.anthropic.com/engineering/demystifying-evals-for-ai-agents
- Source role: supporting_source
- Linked sections: Production Challenges, Guardrails, Future Outlook (evaluation maturity), Recommendations, Future Outlook, Research Directions
- Why this source matters: Detailed engineering guidance on designing, running, and maintaining evaluations for agents; includes definitions (eval harness, transcript, graders), practical grader taxonomy, pass@k/pass^k metrics, and a step-by-step roadmap from zero to a robust eval practice.
- Reliability tier: strong-secondary (primary engineering guidance from a major model/provider; authoritative about best practices and internal learnings but reflective of Anthropic's practices)
- Date accessed: 2026-03-18

## Evidence extracted
- Definitions and taxonomy (task, trial, grader types, transcript, harness) (Support: Article defines evaluation components and ties them to practical implementation choices)
- Grader taxonomy and recommended use (code-based, model-based, human) (Support: Article provides tables and examples of grader strengths/weaknesses and recommends hybrid approaches)
- pass@k and pass^k distinctions for non-deterministic agents (Support: Article explains metrics and their product implications (consistency vs. any-success))
- Roadmap to adopt evals (collect tasks, write unambiguous tasks, build harness, graders, maintain over time) (Support: Stepwise guidance and examples from Anthropic internal practice)

## Open questions
- How easily can smaller teams adopt Anthropic's entire eval roadmap? Which parts give most leverage early?
- Cost of running large eval suites frequently for high-throughput agent workloads.

## Draft implications
- Anthropic's guidance makes clear that mature harness engineering will center on eval-harnesses, transcript capture, grader calibration, and continuous monitoring. Teams should prioritize small, high-impact eval suites early, then scale.
