# Tri Bien

**Full-stack engineer with a backend and systems bent.** I build, then take apart. My best work starts with a small, inspectable reimplementation of something I rely on — a DI container, a GC workload, a JavaScript runtime — so I can reason about the real thing from its mechanics instead of its marketing. Then I ship it: production-minded apps, tests, CI, and demos you can actually click.

I care about the *why* behind a tool, the trade-offs at the boundary, and the difference between "it works" and "I know why it works."

- Email: [bienthanhtri@gmail.com](mailto:bienthanhtri@gmail.com)
- Portfolio of demos: [library](https://tribien.github.io/library/) · [trimbot](https://tribien.github.io/trimbot/) · [myblogs](https://tribien.github.io/myblogs/)

---

## What I work on

- **Systems & runtime depth** — JVM internals, memory and garbage collection, dependency-injection/IoC mechanics, dynamic proxies, language runtime semantics.
- **Full-stack delivery** — vanilla-JS and React PWAs, OAuth and cloud sync, offline-first service workers, Spring Boot services, CI/CD to GitHub Pages.
- **Applied ML & developer tooling** — in-browser LLM inference, CPU LoRA fine-tuning, speech-to-text, ffmpeg and desktop automation.

---

## Selected work

### Systems & runtime depth

These projects exist to make a hidden mechanism small enough to see.

- **[mini-di-container](https://github.com/TriBien/mini-di-container)** — A dependency-injection container written from scratch in Java 25. Annotation-based scanning, constructor and field injection, singleton/prototype scopes, `@PostConstruct`/`@PreDestroy` lifecycle, cycle detection over a construction stack, and proxy wrapping via JDK dynamic proxies and CGLIB. The README maps each toy feature back to the Spring infrastructure it explains. Built with Maven and JUnit 5, with a self-test runner.
  *Demonstrates: reflection, graph traversal, IoC/DI, lifecycle design, AOP proxies, API design.*

- **[jvm-memory-laboratory](https://github.com/TriBien/jvm-memory-laboratory)** — A hands-on lab for JVM memory behavior. Allocation storms under G1 vs ZGC, object layout and boxing with JOL, an intentional cache-retention bug diagnosed with heap dumps and GC-root analysis in Eclipse MAT, and GC tuning against pause goals. Ships a Spring Boot service with `/work` and `/cache` endpoints, a Python GC-log analyzer, `wrk` load tests, and Actuator/Prometheus metrics.
  *Demonstrates: GC/allocator reasoning, profiling and heap analysis, latency vs throughput trade-offs, load testing.*

- **[javascript-demo](https://github.com/TriBien/javascript-demo)** — A runtime lab notebook, not a syntax tour. Values vs references, closures, prototype chains, promises, and the microtask queue — each section moves from mental model → experiment → prediction → practical consequence.
  *Demonstrates: language semantics, event-loop reasoning, thinking in models.*

### Full-stack applications

- **[library](https://github.com/TriBien/library)** — A mobile-first reading library shipped as a static GitHub Pages site with **no build step and no framework**. Full-text search, per-book reading progress, theme and text-size preferences, and reading history — all synced across devices through the reader's own Google Drive `appDataFolder` via OAuth, with last-write-wins conflict resolution and a `localStorage` fallback before sign-in.
  *Demonstrates: vanilla-JS architecture, OAuth and REST integration, offline-first PWA, design tokens, GitHub Actions deploys.* — [live demo](https://tribien.github.io/library/)

- **[trimbot](https://github.com/TriBien/trimbot)** — A React 19 + Vite chat demo running an LLM entirely in the browser with WebLLM/WebGPU — no server, no API keys.
  *Demonstrates: modern React, browser GPU inference, static deployment.* — [live demo](https://tribien.github.io/trimbot/)

- **Offline-first PWA suite** — A set of small, installable apps built with plain JavaScript, service workers, and web manifests:
  [mymap](https://github.com/TriBien/mymap) (local mindmap) · [xtracker](https://github.com/TriBien/xtracker) (goal & streak tracking) · [deepSession](https://github.com/TriBien/deepSession) (deep-work session timer) · [leetcode-ranking](https://github.com/TriBien/leetcode-ranking) (company-wise practice explorer).
  *Demonstrates: repeatable app structure, offline caching, shipping small.*

### Applied ML & tooling

- **[mini-llm](https://github.com/TriBien/mini-llm)** — CPU-friendly fine-tuning of TinyLlama with LoRA (Hugging Face `transformers` + PEFT). Hash-tracked incremental dataset updates, resumable training, periodic snapshots that can be chatted with while training runs, and a small chat CLI.
  *Demonstrates: the full training loop, parameter-efficient fine-tuning, stateful pipelines.*

- **[transcriber](https://github.com/TriBien/transcriber)** — Audio/video transcription with `faster-whisper`, extracting audio with ffmpeg and running int8 `tiny.en` on CPU with VAD.
- **[gify](https://github.com/TriBien/gify)** — A Streamlit app that turns uploaded video into animated GIFs via ffmpeg. [Deployed on Streamlit Cloud](https://gifconverter.streamlit.app/).
- **[webcam-recorder](https://github.com/TriBien/webcam-recorder)** — One-click webcam capture into YouTube-Shorts-ready vertical MP4. A Tkinter GUI over a single ffmpeg shell engine, installed as a desktop launcher, with the trade-offs documented.

### Fundamentals & writing

- **[x35](https://github.com/TriBien/x35)** — Working notes on the ground floor: bits and bytes, two's complement, integer overflow, IEEE-754 floating point, decimal representations, endianness, and bit flags.
- **[algo](https://github.com/TriBien/algo)** — Java implementations of classic interview problems (graphs, intervals, DP, linked lists) with diagrams.
- **[myblogs](https://github.com/TriBien/myblogs)** — *First Principles*, a technical blog plus mastery roadmaps for frontend, backend, Java/Spring, and React.
- **[strategic-master-AI](https://github.com/TriBien/strategic-master-AI)** — A prioritized, tiered roadmap for learning applied AI/ML.

---

## How I approach engineering

- **Understand the mechanism, not just the API.** I reimplement a reduced version to expose the invariants a framework hides — then I know where it breaks.
- **Reason about trade-offs explicitly.** Pause goals trade against throughput; scopes trade against identity; a cache trades against retention. I try to name the axis before picking a point.
- **Prefer small, inspectable systems.** No build step where it isn't earning its keep, relative URLs, vendored dependencies, one source of truth for the tricky part.
- **Ship and verify.** Tests where they count, CI on push, live demos, and load/profiling evidence instead of assertions.

## Toolbox

**Languages** — Java · JavaScript/TypeScript · Python · SQL · Bash
**Backend & runtime** — Spring Boot · JVM/GC tuning · Maven · JUnit 5 · REST · OAuth
**Frontend** — React 19 · Vite · vanilla JS · PWA/service workers · CSS
**Data & infra** — Docker · GitHub Actions · GitHub Pages · Streamlit Cloud · Prometheus/Actuator
**ML** — PyTorch · Hugging Face Transformers · PEFT/LoRA · faster-whisper · WebLLM

---

Open to full-stack and senior/staff engineering roles. **bienthanhtri@gmail.com**
