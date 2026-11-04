# CopyGPT

CopyGPT is a UX writing assistant demonstrated in [my Branch AI writing case study](https://olumideolusesi.com/work/ai-copywriting). It helps turn product context or an interface screenshot into a short, usable piece of interface copy.

## Behavior

The demo accepts text and optional image input, uses Claude with a structured JSON response schema, and returns one rewritten text item, a clarification question, or a request for human review. Its private context combines brand, market and component guidance. Missing context should lead to clarification rather than invented product details.

The service validates submitted inputs and model results. A quota store controls visitor, network and daily demo allowances. Provider requests have a deadline and are not retried automatically; admitted attempts count against the allowance, including provider failures.

## Implementation

- Next.js and React
- Anthropic SDK with text and screenshot input
- Structured output schema and response validation
- PostgreSQL-backed quota storage and visitor identity

## Source excerpts

- [Service orchestration](source/service.mjs)
- [Input and output contracts](source/contracts.mjs)

These are excerpts from the working portfolio application, not a complete standalone build. The private operating guide, reference bundle, runtime data, credentials, infrastructure modules and portfolio UI are excluded. The original imports are retained to show how these modules fit into the application.

The demo uses a model to generate copy; it does not autonomously update a product or perform transactions. Source inspection documents the implemented behavior, not an independent guarantee about the live deployment.
