<!-- generated-by: copy_writer_agent.runtime_sync -->
# Helicone (proxy-based observability, cost tracking)

- URL: https://www.helicone.ai/
- Source role: supporting_source
- Linked sections: Vendor, Tooling Landscape, Recommendations
- Why this source matters: Helicone operates as a proxy to capture telemetry and provide cost-tracking and caching for LLM usage; useful when teams need low-friction cost visibility and request caching.
- Reliability tier: medium-secondary (vendor docs; useful for feature claims)
- Date accessed: 2026-03-18

## Evidence extracted
- Helicone provides request-level telemetry, token-cost attribution, and caching to reduce repeated token spend (Support: Product documentation and blogs)

## Draft implications
- Proxy-based observability can be an effective low-effort way to obtain cost and token-level dashboards without deep SDK integration, but it introduces an operational choke point and data-flow consideration (routing traffic through proxy).
