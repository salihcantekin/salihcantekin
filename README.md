<div align="center">

# Salih Cantekin

**Lead Developer · Software Architect · Microsoft MVP**

Building high-performance .NET systems, scalable cloud architectures, and open-source developer tools.

<p>
  <a href="https://higgs.digital"><img src="https://img.shields.io/badge/HiggsDigital-Enterprise%20Consulting-0891B2?style=flat-square" alt="HiggsDigital" /></a>
  <a href="https://dometrain.com/author/salih-cantekin/"><img src="https://img.shields.io/badge/Dometrain-Course%20Instructor-7C3AED?style=flat-square" alt="Dometrain Instructor" /></a>
  <img src="https://img.shields.io/badge/Microsoft-MVP-0078D4?style=flat-square&logo=microsoft&logoColor=white" alt="Microsoft MVP" />
  <a href="https://ruviodb.com"><img src="https://img.shields.io/badge/Creator%20of-Ruvio-DE5833?style=flat-square&logo=rust&logoColor=white" alt="Creator of Ruvio" /></a>
  <img src="https://img.shields.io/badge/Focus-Performance%20%26%20Architecture-1E293B?style=flat-square" alt="Focus" />
</p>

<p>
  <a href="https://linkedin.com/in/salih-cantekin">LinkedIn</a> ·
  <a href="https://salihcantekin.com">Blog</a> ·
  <a href="https://www.youtube.com/@SalihCantekin">YouTube</a> ·
  <a href="mailto:salihcantekin@gmail.com">Email</a>
</p>

</div>

---

## Currently Building: Ruvio

<table>
<tr>
<td valign="top">

### [Ruvio](https://ruviodb.com) — a Redis-compatible in-memory server, written in Rust

Ruvio speaks the Redis protocol (RESP), so `redis-cli` and existing Redis clients just connect. It aims to replace a separate cache, lock service and delay queue with a single process.

- **287 commands across 21 families** — strings, hashes, lists, sets, sorted sets, streams, JSON, geo, bitmaps, HyperLogLog, Bloom filters and more
- **Built-in coordination primitives** — leases with fencing tokens, semaphores, rate limits, stampede-free cache fill, conditional writes, change feeds and delayed stream entries
- **Shard-owned architecture** — each shard owns its keys, with no locks on the hot path
- **Choose your durability** — `always`, `everysec`, `snapshot` or `memory`, picked at startup
- **Official clients** for Rust, C#/.NET, Go, Java, Python and Node.js

<p>
  <a href="https://ruviodb.com"><b>Website</b></a> ·
  <a href="https://ruviodb.com/docs/commands/">Commands</a> ·
  <a href="https://ruviodb.com/docs/resilience/">Durability &amp; WAL</a> ·
  <a href="https://ruviodb.com/benchmarks/">Benchmarks</a> ·
  <a href="https://github.com/salihcantekin/ruvio"><b>GitHub</b></a>
</p>

<p>
  <img src="https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white" alt="Rust" />
  <img src="https://img.shields.io/badge/Redis%20protocol-compatible-DC382D?style=flat-square&logo=redis&logoColor=white" alt="Redis compatible" />
  <img src="https://img.shields.io/badge/Server-AGPL--3.0-1E293B?style=flat-square" alt="Server AGPL-3.0" />
  <img src="https://img.shields.io/badge/Clients-MIT-1E293B?style=flat-square" alt="Clients MIT" />
  <a href="https://github.com/salihcantekin/ruvio/stargazers"><img src="https://img.shields.io/github/stars/salihcantekin/ruvio?style=flat-square&logo=github&label=Stars" alt="GitHub stars" /></a>
</p>

</td>
</tr>
</table>

**Published benchmark highlights** (self-reported, Redis 8.10.2 as the baseline — [methodology and caveats](https://ruviodb.com/benchmarks/)):

| Setup | Throughput vs. Redis | Memory vs. Redis |
|-------|----------------------|------------------|
| Apple M4 Pro, single shard | **1.25×** geometric mean over 60 commands | **26% less** |
| AMD EPYC 2 vCPU (KVM), single shard | **1.09×** geometric mean over 60 commands | **19% less** |
| 8 shards vs. 8-node Redis Cluster (Azure, pipeline 16) | **1.13×** geometric mean over 59 commands | 0.94× of cluster total |

Peak: **29M GET/s** on 8 shards (pipeline 64). Ratios vary by command and host — see the benchmark page for the full picture.

**Try it:**

```bash
docker run -p 6379:6379 salihcantekin/ruvio:linux
redis-cli ping
```

---

## About

I help teams design and deliver **enterprise-grade .NET software** — from performance-critical backends to cloud-native architectures on Azure. My work spans consulting through [Higgs Digital](https://higgs.digital), open-source libraries used in production, and technical education for developers who want to go beyond CRUD.

**What I bring to the table:**

| Area | Focus |
|------|--------|
| **Performance** | Zero-allocation patterns, profiling, SIMD, memory-mapped I/O, source generators |
| **Architecture** | Microservices, CQRS, event-driven systems, domain modeling, modernization |
| **Cloud** | Azure, CI/CD, observability, cost optimization, production reliability |
| **Systems** | Rust, in-memory databases ([Ruvio](https://ruviodb.com)), GPU-accelerated tooling, cross-platform desktop utilities |

---

## Teaching on Dometrain

<a href="https://dometrain.com/course/from-zero-to-hero-1-billion-row-performance-challenge-in-dotnet/?refer=salih-cantekin&promo=github-readme">
  <img align="right" width="220" src="https://assets.dometrain.com/cdn-cgi/image/width=358,quality=70/from-zero-to-hero-1-billion-row-performance-challenge-in-dotnet/thumbnail-d716b179f36241eb8fea79d9c1562d1b.jpeg" alt="1 Billion Row Performance Challenge in .NET" />
</a>

### [From Zero to Hero: 1 Billion Row Performance Challenge in .NET](https://dometrain.com/course/from-zero-to-hero-1-billion-row-performance-challenge-in-dotnet/?refer=salih-cantekin&promo=github-readme)

A hands-on performance engineering course on **[Dometrain](https://dometrain.com/author/salih-cantekin/)**. Starting from a naive file-read implementation, we refactor step by step into a solution that is **hundreds of times faster** — the same mindset behind the famous 1 Billion Row Challenge, applied to modern .NET.

**You will work through:**

- Performance profiling, allocation analysis, and baseline measurement
- Streaming I/O, buffering, and disk-level concepts
- Multi-threading, `Amdahl's Law`, and race-condition-safe aggregation
- Memory-mapped files, unsafe code, and custom parsers
- SIMD, pipelining, and a custom hash table built for raw speed

<p>
  <a href="https://dometrain.com/course/from-zero-to-hero-1-billion-row-performance-challenge-in-dotnet/"><b>View course on Dometrain →</b></a>
</p>

<br clear="right" />

---

<a href="https://dometrain.com/course/from-zero-to-hero-garbage-collection-in-dotnet/?refer=salih-cantekin&promo=github">
  <img align="right" width="220" src="https://assets.dometrain.com/cdn-cgi/image/width=358,quality=70/from-zero-to-hero-garbage-collection-in-dotnet/thumbnail-b9bd65b2fb384490a67baf799cd9e648.jpeg" alt="From Zero to Hero: Garbage Collection in .NET" />
</a>

### [From Zero to Hero: Garbage Collection in .NET](https://dometrain.com/course/from-zero-to-hero-garbage-collection-in-dotnet/?refer=salih-cantekin&promo=github)

A deep-dive course on **[Dometrain](https://dometrain.com/author/salih-cantekin/)** exploring the inner workings of .NET garbage collection. Understand how GC decisions impact your application's performance, memory usage, and latency — and learn practical patterns to write GC-friendly code.

**You will learn:**

- Generational GC model, heap structure, and collection phases
- GC modes: Workstation, Server, and Tiered Compilation effects
- Allocation pressure, promotion rates, and heap fragmentation
- Pinning, unmanaged memory, and GC suspension impacts
- Profiling GC behavior and optimization techniques

<p>
  <a href="https://dometrain.com/course/from-zero-to-hero-garbage-collection-in-dotnet/?refer=salih-cantekin&promo=github"><b>View course on Dometrain →</b></a>
</p>

<br clear="right" />

---

## Featured Open Source

<table>
<tr>
<td width="33%" valign="top">

### [UnionRailway](https://github.com/salihcantekin/UnionRailway)

Type-safe error handling for C# with Railway Oriented Programming, RFC 7807 Problem Details, and ASP.NET Core / EF Core integrations.

`C#` `NuGet` `ASP.NET Core`

<br>

[Website](https://salihcantekin.github.io/UnionRailway/) · [GitHub](https://github.com/salihcantekin/UnionRailway)

</td>
<td width="33%" valign="top">

### [Space](https://github.com/salihcantekin/Space)

Source-generator powered mediator and messaging framework for .NET. Zero runtime reflection, compile-time routing, extensible pipelines.

`C#` `Source Generator` `CQRS`

<br>

[Website](https://salihcantekin.github.io/Space/) · [GitHub](https://github.com/salihcantekin/Space)

</td>
<td width="33%" valign="top">

### [RustFrame](https://github.com/salihcantekin/RustFrame)

Privacy-focused, cross-platform screen region sharing. GPU-accelerated capture for video calls without exposing your full desktop.

`Rust` `Tauri` `Cross-Platform`

<br>

[Website](https://salihcantekin.github.io/RustFrame/) · [GitHub](https://github.com/salihcantekin/RustFrame) · [Download](https://github.com/salihcantekin/RustFrame/releases/latest)

</td>
</tr>
</table>

**Also:** [Ruvio](https://github.com/salihcantekin/ruvio) · [InputReader](https://github.com/salihcantekin/InputReader) · [TechBuddy.Extensions](https://github.com/TechBuddyTR/TechBuddy.Extensions)

---

## Expertise

```
Languages & Runtimes     C# · .NET 8/9/11 · Rust · T-SQL
Backend & APIs           ASP.NET Core · Blazor · Minimal APIs · gRPC
Data & Messaging         EF Core · PostgreSQL · Redis · Ruvio · RabbitMQ
Architecture             DDD · CQRS · Microservices · Event-Driven Design
Cloud & Delivery         Azure · Docker · GitHub Actions · App Insights
Performance              Source Generators · SIMD · Memory-mapped I/O · Benchmarking
```

**Happy to discuss:** .NET performance tuning · system design · Azure architecture · microservice boundaries · source generators · Rust interop

---

## Latest Writing

<!-- BLOG_POSTS:START -->
- [Medium articles](https://medium.com/@salihcantekin) — .NET internals, architecture, and performance
<!-- BLOG_POSTS:END -->

---

## Latest Videos

<!-- YOUTUBE:START -->
- [YouTube channel](https://www.youtube.com/@SalihCantekin) — .NET, system design, and software engineering deep dives
<!-- YOUTUBE:END -->

---

## Connect

<p>
  <a href="https://linkedin.com/in/salih-cantekin"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
  <a href="https://twitter.com/salihcantekin"><img alt="X" src="https://img.shields.io/badge/X-000000?style=for-the-badge&logo=x&logoColor=white" /></a>
  <a href="https://www.youtube.com/@SalihCantekin"><img alt="YouTube" src="https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white" /></a>
  <a href="https://medium.com/@salihcantekin"><img alt="Medium" src="https://img.shields.io/badge/Medium-12100E?style=for-the-badge&logo=medium&logoColor=white" /></a>
  <a href="https://higgs.digital"><img alt="Higgs Digital" src="https://img.shields.io/badge/Higgs%20Digital-higgs.digital-0891B2?style=for-the-badge" /></a>
  <a href="mailto:salihcantekin@gmail.com"><img alt="Email" src="https://img.shields.io/badge/Email-salihcantekin%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white" /></a>
</p>

---

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=salihcantekin&show_icons=true&theme=dark&hide_border=true&include_all_commits=true&count_private=true" height="150" alt="GitHub Stats" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=salihcantekin&layout=compact&theme=dark&hide_border=true&langs_count=6" height="150" alt="Top Languages" />
</p>

<p align="center">
  <sub>Open to collaboration, consulting, and interesting engineering problems.</sub>
</p>
