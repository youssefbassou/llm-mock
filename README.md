# llm-mock

Mock LLM provider for C++ testing. Zero deps, zero network.

## Quickstart

`cpp
#define LLM_MOCK_IMPLEMENTATION
#include "llm_mock.hpp"

llm::ScriptedResponses s;
s.responses = {"Paris"};
llm::MockConfig cfg; cfg.strategy = s;
llm::MockLLM mock(cfg);
assert(mock.complete("Capital of France?") == "Paris");
`

## Strategies: ScriptedResponses, PatternResponses, RandomResponses, EchoResponse

## Build

`ash
cmake -B build
cmake --build build
`

## Examples

| File | Description |
|------|-------------|
| basic_mock.cpp | Scripted responses |
| pattern_mock.cpp | Pattern matching |
| error_simulation.cpp | Error injection |
| ci_test.cpp | Global mock for CI |

## See Also

| Repo | What it does |
|------|-------------|
| [llm-stream](https://github.com/Mattbusel/llm-stream) | Stream OpenAI and Anthropic responses via SSE |
| [llm-cache](https://github.com/Mattbusel/llm-cache) | LRU response cache |
| [llm-cost](https://github.com/Mattbusel/llm-cost) | Token counting and cost estimation |
| [llm-retry](https://github.com/Mattbusel/llm-retry) | Retry and circuit breaker |
| [llm-format](https://github.com/Mattbusel/llm-format) | Structured output / JSON schema |
| [llm-embed](https://github.com/Mattbusel/llm-embed) | Embeddings and vector search |
| [llm-pool](https://github.com/Mattbusel/llm-pool) | Concurrent request pool |
| [llm-log](https://github.com/Mattbusel/llm-log) | Structured JSONL logging |
| [llm-template](https://github.com/Mattbusel/llm-template) | Prompt templating |
| [llm-agent](https://github.com/Mattbusel/llm-agent) | Tool-calling agent loop |
| [llm-rag](https://github.com/Mattbusel/llm-rag) | RAG pipeline |
| [llm-eval](https://github.com/Mattbusel/llm-eval) | Evaluation and consistency scoring |
| [llm-chat](https://github.com/Mattbusel/llm-chat) | Conversation memory manager |
| [llm-vision](https://github.com/Mattbusel/llm-vision) | Multimodal image+text |
| [llm-mock](https://github.com/Mattbusel/llm-mock) | Mock LLM for testing |
| [llm-router](https://github.com/Mattbusel/llm-router) | Model routing by complexity |
| [llm-guard](https://github.com/Mattbusel/llm-guard) | PII detection and injection guard |
| [llm-compress](https://github.com/Mattbusel/llm-compress) | Context compression |
| [llm-batch](https://github.com/Mattbusel/llm-batch) | Batch processing and checkpointing |

## License

MIT -- Copyright (c) 2026 Mattbusel. See LICENSE.
