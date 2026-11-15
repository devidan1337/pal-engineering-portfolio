# Read-only retrieval and human-reviewed agent handoff

**Outcome** A dedicated Hermes profile exposed one candidate-search tool. I measured input-token use on a controlled query and verified that Codex could use a retrieved excerpt to make a documented engineering decision.

## What I built and checked

The search adapter limits scope to an approved candidate catalog. It checks the returned bytes against their recorded integrity and returns source references with a candidate-only authority label. I checked the actual tool schema after runtime discovery to verify the profile exposed only the search tool.

## Controlled measurement

| Metric | Baseline | Coding context off |
| --- | ---: | ---: |
| Input tokens | 7,611 | 6,151 |
| Output tokens | 292 | 292 |
| Main model requests | 2 | 2 |
| Candidate-search invocations | 1 | 1 |

Input fell by 1,460 tokens, or about 19%, on this matched comparison. Both runs preserved the same four source destinations, six line references, and authority label. This measurement describes one query pair.

## Documentation handoff

Hermes retrieved a criterion about recording source and destination zones for network tests. Codex applied it to the [July DNS investigation](segmented-network-dns.md) and checked the tracked log. The entry identified the source and described the destinations, while some zone labels remained implicit. Codex recommended keeping the entry because the source evidence could not establish the missing labels. The decision was reviewable through the query, excerpt, and tracked citations.
