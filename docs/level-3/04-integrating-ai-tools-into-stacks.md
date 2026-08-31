# 04 · Integrating AI Tools into Existing Software Stacks

Beyond using an AI tool through its own interface, teams often need it
woven into existing systems — via APIs, plugins, or middleware. This
module covers the architectural and operational considerations that differ
from standalone tool use.

## 1. Integration patterns

| Pattern | Description | Typical use |
|---|---|---|
| Direct API call | Your application calls the AI provider's API directly | Custom features embedded in your own product |
| Middleware/gateway | Requests route through an internal layer that adds logging, rate limiting, and policy enforcement | Organizations with multiple teams/apps needing consistent governance |
| Plugin/extension | A pre-built connector into an existing tool (IDE, CRM, docs platform) | Fast adoption with limited customization |
| Embedded vendor widget | A vendor's AI feature embedded via iframe/SDK inside your product | Fastest to ship, least control over behavior and data flow |

## 2. Architectural considerations

| Consideration | Why it matters |
|---|---|
| Latency budget | AI calls are typically much slower than traditional API calls; design UX and timeouts accordingly |
| Rate limits and quotas | Provider-side limits can throttle your application under load; plan fallback behavior |
| Error handling | Model outputs can be malformed, refused, or low-confidence; the integration must handle all three gracefully |
| Versioning | Underlying models change over time; pin versions where reproducibility matters, and test before accepting auto-updates |
| Observability | Log inputs/outputs (respecting data policy) so failures are diagnosable, not just visible as "AI feature is being weird" |
| Cost attribution | Usage-based billing needs per-feature or per-team cost tracking, or costs become impossible to attribute later |

## 3. A gateway/middleware checklist for larger orgs

| Function | Why centralize it |
|---|---|
| Policy enforcement (data classification checks) | Consistent enforcement across every team's integration, not per-team discretion |
| Centralized logging and audit trail | Needed for the incident process and governance (Module 7) |
| Rate limiting and cost caps | Prevents one team's runaway usage from affecting shared budget or provider quotas |
| Model/vendor abstraction | Lets you swap providers later without every downstream team rewriting integration code |
| Centralized key management | Avoids scattering API credentials across many codebases with inconsistent security practices |

## 4. Common integration failure modes

| Failure | Cause | Fix |
|---|---|---|
| Silent degraded UX under provider outage | No fallback path when the AI call fails or times out | Design a graceful degradation (cached response, "unavailable" state, or non-AI fallback) for every AI-dependent feature |
| Cost blowout | Usage scaled with product growth without cost monitoring | Build cost dashboards and caps before wide release, not after the first surprising invoice |
| Untracked model drift | Provider updates the underlying model; feature behavior changes without your team having decided that | Pin model versions where behavior stability matters; test before opting into updates |
| Data policy violation via integration | An engineer's API call passes more context/fields than the approved use case | Enforce field-level scoping at the integration layer, not just as a written guideline |

## 5. Build vs. buy considerations

| Factor | Favors build (direct API/custom integration) | Favors buy (plugin/vendor widget) |
|---|---|---|
| Customization need | High — very specific workflow requirements | Low — a standard use case a vendor already solves well |
| Engineering capacity | Available and it's a differentiating feature | Limited, or this isn't a differentiating capability |
| Time to value | Can absorb weeks of integration work | Needs to ship fast |
| Long-term cost control | Volume high enough that a direct integration pays off | Volume too low to justify custom build/maintenance cost |

## Worked example

A SaaS company wants an AI-powered search feature in their product. Direct
API integration lets them control latency, cache common queries to reduce
cost, and enforce that only public-facing product data (never customer
account data) is sent to the model — via a middleware layer the platform
team already runs for governance. They pin the model version after
testing, set a per-team cost cap in the gateway, and build a fallback to
traditional keyword search if the AI call times out, so a provider outage
degrades the feature rather than breaking it.

## Exercise

Pick a feature or workflow where your team might integrate an AI tool
directly into a software stack rather than using it via its own interface.
Choose an integration pattern from section 1, and write out how you'd
handle at least three of the architectural considerations in section 2
(latency, error handling, and cost attribution, at minimum).
