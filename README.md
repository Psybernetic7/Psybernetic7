# Jishnu Sen

### Full-Stack Developer · MSc Computer Science

Full-stack developer in Turku, Finland, building web applications and ML systems, often implementing the underlying algorithms from scratch.

[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Psybernetic7)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/jishnu-sen)
[![Email](https://img.shields.io/badge/Email-6D4AFF?style=for-the-badge&logo=protonmail&logoColor=white)](mailto:jishsen@protonmail.com)

---

## About Me

I build full-stack web applications and machine learning systems, from Next.js/TypeScript products to Transformer models written from first principles in PyTorch. My work spans retrieval and RAG pipelines, real-time speech translation, and DevOps infrastructure on Kubernetes and AWS. I tend to implement core algorithms directly to understand them properly.

I hold an MSc in Computer Science from Åbo Akademi University, where my thesis surveyed large language models for code generation, and I have a background in research and data work as well. Currently open to full-stack, backend, and ML engineering roles as well as open-source collaborations. 

---

## Tech Stack

**Languages**

[![](https://skillicons.dev/icons?i=python,go,ts,js,bash)](https://skillicons.dev)

**Frontend**

[![](https://skillicons.dev/icons?i=react,nextjs,tailwind,html,css)](https://skillicons.dev)

**Backend & Data**

[![](https://skillicons.dev/icons?i=fastapi,postgres,appwrite,pytorch,sklearn)](https://skillicons.dev)

**DevOps & Tools**

[![](https://skillicons.dev/icons?i=docker,kubernetes,jenkins,ansible,aws,git,vercel,linux)](https://skillicons.dev)

Also: Streamlit, Shadcn/ui, React Hook Form, Zod, sqlc, goose, sentence-transformers, faster-whisper, Docker Compose, Argo CD.

---

## Featured Projects

### McKenna GPT — Character-Level Transformer Language Model
`Python` · `PyTorch` · `CUDA` · `yt-dlp` — [Repository](https://github.com/Psybernetic7/mckenna-gpt)

A 10.8M-parameter decoder-only Transformer implemented from first principles — scaled dot-product attention, multi-head attention, residual/LayerNorm blocks and causal masking written directly, without `nn.Transformer` or HuggingFace.

- End-to-end data pipeline sourcing 155 recorded talks from YouTube captions, reducing 189 MB of raw WebVTT to a 9.4 MB corpus via a custom word-overlap deduplicator
- Trained on GPU with AdamW: validation loss cut from 4.32 to 1.08 across 6 layers and 6 attention heads at 256-character context
- Best-validation checkpointing and train/validation gap monitoring to prevent overfitting on a small corpus
- Interactive CLI with temperature and top-k sampling

### Cloud File Storage & Management Platform
`Next.js 15` · `TypeScript` · `Appwrite` · `Tailwind` · `Vercel` — [Live Demo](https://cloud-storage-omega-five.vercel.app/sign-in) · [Repository](https://github.com/Psybernetic7/cloud-storage)

A full-stack cloud storage app where users securely upload, organize, search, and share files from a responsive interface built on the Next.js App Router.

- Passwordless email-OTP authentication via Appwrite Auth, removing password management entirely
- Per-file access control using a relational `files → users` ownership model with array-based sharing
- Real-time debounced search and flexible sorting (name, date, size) without a dedicated search service
- Storage dashboard with a Recharts radial chart breaking usage down by file category; drag-and-drop uploads up to 50 MB

### RAG Search Engine
`Python` · `sentence-transformers` · `cross-encoder` · `Google GenAI` · `NumPy` — [Repository](https://github.com/Psybernetic7/rag-search-engine)

A CLI search engine over a movie dataset implementing classic IR, neural retrieval, and retrieval-augmented generation end to end.

- BM25 built from the ranking formula up (`k1=1.5`, `b=0.75`) with Porter stemming and stopword removal
- Semantic search with `all-MiniLM-L6-v2` (384-dim) plus hybrid search using weighted fusion and Reciprocal Rank Fusion
- Three re-ranking strategies — per-document LLM scoring, batch JSON ranking, and a local `ms-marco-TinyBERT-L2-v2` cross-encoder — trading off latency, cost, and quality
- Evaluation harness computing precision@k, recall@k, and F1 against a hand-labelled golden dataset

### Finnish-to-English Live Speech Translator
`FastAPI` · `faster-whisper` · `MarianMT` · `WebSocket` — [Repository](https://github.com/Psybernetic7/finnish-translator)

A real-time speech translation web app that captures 16 kHz microphone audio in the browser and streams it to a FastAPI inference backend.

- Web Audio API `AudioWorklet` capture streamed over WebSocket for low-latency transcription
- faster-whisper large-v3-turbo for Finnish ASR and Helsinki-NLP MarianMT for translation, with automatic GPU/CPU detection and quantisation
- Flush protocol guaranteeing zero audio loss between recording sessions

---

## Currently Learning

- **HTTP from TCP** (Go) — implementing HTTP/1.1 from scratch on raw TCP sockets, bypassing `net/http`. Incremental state-machine request parsing is done; response writing, routing, and chunked encoding are in progress. [Repository](https://github.com/Psybernetic7/http-server)
- *Operating Systems: Three Easy Pieces* (Arpaci-Dusseau) and raytracing in C++.

---

## Links & Contact

- **GitHub:** [github.com/Psybernetic7](https://github.com/Psybernetic7)
- **LinkedIn:** [linkedin.com/in/jishnu-sen](https://www.linkedin.com/in/jishnu-sen)
- **Email:** [jishsen@protonmail.com](mailto:jishsen@protonmail.com)
- **Location:** Turku, Finland
