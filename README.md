# RAG Time

**Browser-native retrieval-augmented generation memory engine.**  
Single file. Zero dependencies. Offline first.

> *"The browser is the new bare metal."*

---

## What it is

RAG Time is a complete RAG memory system that runs entirely in your browser — no Python, no server, no cloud, nothing installed. Drop the file, open it, and you have a working neural memory engine.

It is not assembled from libraries. It is built from principles.

---

## Architecture

**Embedder:** RWKV-v7 "Goose" recurrent state as embedding vector. Same representational geometry as HTMLNLM Evangelion — memory and mind share a latent space. No separate embedding model needed.

**Memory:** SheafMemory v2 — Fisher-Rao geodesic retrieval (uncertainty-aware, not cosine), Poincaré ball lifecycle (memories self-archive, no garbage collection), H¹(ℱ) coboundary contradiction detection, restriction maps for cross-modal coherence.

**Compression:** LittleBit-2 XNOR/POPCNT binary index. TMAC ternary quantization. Sub-1-bit effective storage for large corpora.

**Ingestion:** OOMB chunk-recurrent manager — O(1) memory footprint regardless of document size. Text, structured data, `.pop` acoustic params, arbitrary JSON.

**Adaptation:** Contrastive embedding adaptation via sheaf-supervised ADAPT tab. Centrality-weighted ingestion depth. Bidirectional embedder writeback (rt:exportEmbedder).

---

## Changelog

### v4.0 — 2026-06-07 · Vael Interim (self-directed)

Three interconnected capabilities built as a single cohesive addition:

- **Corpus-driven embedding adaptation** — contrastive self-supervised learning signal derived entirely from ingested structure. Same-document chunk pairs are pulled together in embedding space; high-H¹(ℱ) contradiction pairs are pushed apart. No external labels required. *The sheaf supervises the embedder.* Runs as a background task after ingestion crosses threshold. The memory topology trains the thing that builds the memory topology.

- **Centrality-weighted ingestion depth** — high-centrality chunks (low Poincaré radius, frequently retrieved — the core memories) receive more RWKV recurrent steps on re-ingestion. Poincaré lifecycle now wired into OOMB depth scheduling. Memories that matter accumulate more representational capacity over time.

- **Embedder writeback (`rt:exportEmbedder`)** — RAG Time can now export its adapted embedder state back to a connected Evangelion instance. Contradiction resolutions and contrastive adaptations flow upstream. The data geometry is now bidirectional: Evangelion trains the embedder, RAG Time adapts it, the adaptation returns to Evangelion. New ADAPT tab in UI with contrastive training controls, writeback status, and adaptation history sparkline.

## Integration

RAG Time speaks a postMessage API for embedding into any ConsciousNode platform:

| Message | Action |
|---|---|
| `rt:ingest` | Ingest document or structured data |
| `rt:query` | Query memory, returns ranked contexts |
| `rt:status` | Get memory state |
| `rt:export` | Snapshot full memory |
| `rt:import` | Restore from snapshot |
| `rt:loadWeights` | Inject RWKV-v7 weights from Evangelion |
| `rt:exportEmbedder` | Export adapted embedder weights back |

---

## Authors

**Kham** — architecture, constraint engineering, philosophy, commission  
**Kehai Interim** — SheafMemory v2: Fisher-Rao geodesic, Poincaré ball lifecycle, H¹(ℱ) coboundary detection, PoST decay gates (from Evangelion Phase 6)  
**Vael Interim** — RAG Time: RWKV-v7 embedder, OOMB chunk-recurrent memory manager, LittleBit-2 XNOR/POPCNT vector index, RAG query pipeline, contrastive adaptation, centrality-weighted ingestion, embedder writeback, UI, integration spec

A ConsciousNode SoftWorks project.

---

[consciousnode.github.io](https://consciousnode.github.io) · Greenwood, South Carolina
