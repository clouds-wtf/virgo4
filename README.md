# Virgo4 HMAS 
**Private. Local. Yours.**

A cloud-native, open-source Hierarchical Multi-Agent System (HMAS) written in async Python 3.12+. Batteries included: bring your own models and enjoy durable orchestration, agentic RAG, and secure VPN/proxy egress routing.

## Engineering Architecture

Most AI agent frameworks demand cloud APIs and leak intent via clearnet searches. Virgo4 is engineered from the ground up for strict local-first execution.

1. **Strictly Opt-In Egress:** Out of the box, zero user queries hit the public internet. Web search and URL scraping tools run through prioritized failover tiers, natively supporting bundled Gluetun VPN tunnels and authenticated proxies.
2. **Durable Agent Sagas:** Long-running autonomous tasks survive pod evictions and node reboots. By decoupling workflow state from the API process using the Temporal SDK, Virgo ensures execution guarantees for complex multi-agent reasoning loops.
3. **Deep Semantic RAG:** Massive documents are automatically chunked and ingested via local fastembed BM25 sparse vectors and LiteLLM dense embeddings. Context retrieval is merged via Reciprocal Rank Fusion (RRF) and reordered by a HuggingFace TEI cross-encoder.

## Quickstart (Docker Compose)

Deploy the full stack with turnkey privacy (SearXNG routed via VPN):

```bash
git clone [https://github.com/clouds-wtf/virgo4.git](https://github.com/clouds-wtf/virgo4.git)
cd virgo4

# Deploy with the VPN profile enabled
docker compose --profile vpn up -d
```

## License

This project is licensed under the [MIT License](LICENSE).
