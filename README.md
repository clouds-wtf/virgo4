# Virgo4 HMAS 
**Private. Local. Yours.**

A cloud-native, open-source Hierarchical Multi-Agent System (HMAS) written in async Python 3.12+. Batteries included: bring your own models and enjoy durable orchestration, agentic RAG, and secure VPN/proxy egress routing.

## Engineering Architecture

Most AI agent frameworks demand cloud APIs, leak intent via clearnet searches, and lock you out while they "think." Virgo4 is engineered from the ground up for strict local-first execution, tenant isolation, and real-time collaboration.

1. **Real-Time Interjection:** Unlike traditional agents where you fire a prompt and wait, Virgo's asynchronous architecture allows for true real-time interjection. You can interrupt, steer, or correct an agent mid-thought or mid-execution. *(Demo GIF coming soon)*
2. **Adaptive User Memory:** Virgo doesn't just execute commands; it learns how you operate. Built-in conversational memory allows the system to continuously adapt to your infrastructure, preferences, and coding style. This intelligence is strictly partitioned per account by default, meaning your personal agent grows alongside you while remaining entirely private. 
3. **Strictly Opt-In Egress:** Out of the box, zero user queries hit the public internet. Web search and URL scraping tools run through prioritized failover tiers, natively supporting bundled Gluetun VPN tunnels and authenticated proxies.
4. **Durable Agent Sagas:** Long-running autonomous tasks survive pod evictions and node reboots. By decoupling workflow state from the API process using the Temporal SDK, Virgo ensures execution guarantees for complex multi-agent reasoning loops.
5. **Deep Semantic RAG:** Massive documents are automatically chunked and ingested via local fastembed BM25 sparse vectors and LiteLLM dense embeddings. Context retrieval is merged via Reciprocal Rank Fusion (RRF) and reordered by a HuggingFace TEI cross-encoder.

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
