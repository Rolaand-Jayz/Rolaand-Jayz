# Rolaand Jayz
**Rolaand Jayz | IT Support & Troubleshooting · AI-Directed Development, QA & Validation · Linux**

I investigate what software actually does, not just what it is supposed to do. My background combines enterprise IT support with independent, AI-directed software R&D and rigorous test work: reproducing failures, reading logs, isolating variables, challenging apparently successful results, and documenting findings so someone else can verify them.

**How I build:** I am not a trained programmer, and I don't write code by hand. My projects are built by AI coding agents (Claude Code, ChatGPT/Codex, GitHub Copilot) working under my direction. My part is the part that decides whether the work is any good: defining the objective and requirements, choosing between technical approaches, structuring the agents' context, testing the results, rejecting work that only *looks* finished, and deciding what ships. Every project below is evidence of that process — including the ones that ended in a documented "no."

**[QA case studies and sample test design →](QA_TEST_EVIDENCE.md)** — public evidence of defect investigation, failed hypotheses, test scope, and repeatable checks.

## Selected public work

### [RJW Redux](https://github.com/Rolaand-Jayz/RJW-Redux) and [Promptitect](https://github.com/Rolaand-Jayz/RJW-Redux/blob/main/design/PROMPTITECT_ENGINEERING_SPEC_2026-09-26.md): how I direct AI agents
RJW Redux is the public record of my method for directing AI agents. It grew out of RJW-IDD (started September 2025) by finding where the method broke on real projects and changing it. It now has separate components: context curation (CCE), Promptitect, an independent Evaluator, and an adversarial Tribunal. The dated history is kept, so the evolution can be checked instead of taken on trust.

Promptitect is the system behind everything else here. It started in 2025 as a family of specialist GPTs that turn an idea into an executable specification and route the work, and it is now growing into my own agent harness. It's built around the habits I've used since March 2025: self-critique on every response, independent evaluation, and audits that don't close until three consecutive clean passes. Core rule: *a worker saying it is finished is not evidence that the objective was achieved.*

### [Temporal Forge Player](https://github.com/Rolaand-Jayz/Temporal-Forge-Player) — closed video-reconstruction research
A Linux C++/Vulkan/FFmpeg research project testing how AMD FSR 4.1-style temporal reconstruction behaves on ordinary decoded video. The most relevant part is the **test methodology**: controlled experiments, source-cadence requirements, baseline comparisons, multi-frame evaluation, negative findings, and review of automated quality gates.

- Reopened a previously passing quality gate after visible lattice corruption appeared; retained and reclassified invalidated results.
- Closed the FSR-centered approach in **September 2026** on the evidence, rather than claim a quality advantage that was not established. → [Closure and evidence ledger](https://github.com/Rolaand-Jayz/Temporal-Forge-Player/blob/main/docs/closure/CLAIM_EVIDENCE_LEDGER.md)
- Successor work continues in [New Forge](https://github.com/Rolaand-Jayz/New-Forge) (public) and ANVIL (private).

### [New Forge / FORGE](https://github.com/Rolaand-Jayz/New-Forge) — the successor, with first results
After closing the FSR approach, I commissioned a new reconstruction stage, FORGE: a lanczos3 base plus a small correction network and an evidence-gated temporal path, with its pass/fail gates written down before any tuning. On scenes held out from tuning it passes its quality gate: **+0.585 dB on clean input and +0.414 dB on compressed (CRF 23) input over lanczos3**. On noisy input it measures +4.858 dB, but that gain is mostly denoising, not recovered detail. The whole stage takes 9.77 ms per 4K frame on an RX 7900 GRE. The same record states what still fails: frame-to-frame stability on noisy input. Real 4K60 playback is not yet measured.

- The FORGE code, the hand-built weights, and the gate scripts that produced these numbers are public, so the results can be checked against the code. → [Code](https://github.com/Rolaand-Jayz/New-Forge/tree/main/implementations/forge) · [Results record](https://github.com/Rolaand-Jayz/New-Forge/blob/main/docs/results/2026-11-17-forge-protected-scene-confirm.md)

### [AMD Video Enhancer (AMD-VE)](https://github.com/Rolaand-Jayz/AMD-VE) — Linux-first AMD video application
Experimental C++ application integrating FFmpeg, ROCm/HIP, MiGraphX, and Vulkan. Testing went beyond the UI into runtime dependencies, model execution, GPU behavior, benchmarking, fallback paths, and reproducible release documentation.

The investigations produced **four upstream MiGraphX optimization pull requests** to AMD's ROCm project — [#4707](https://github.com/ROCm/AMDMIGraphX/pull/4707), [#4708](https://github.com/ROCm/AMDMIGraphX/pull/4708), [#4709](https://github.com/ROCm/AMDMIGraphX/pull/4709), [#4710](https://github.com/ROCm/AMDMIGraphX/pull/4710) — one approved by a maintainer, the others in review. Benchmarks are workload-specific; this is not a claim of universal speedup or merged code.

### [FSR 4.1 Static Reverse Engineering](https://github.com/Rolaand-Jayz/RE-of-FSR-4.1.0-Upscaling) — reproducible research
Analysis of shader passes, binary resources, dispatch structures, neural-weight data, and resource bindings with disassembly and comparison tooling. The repository deliberately separates **verified static facts, inferred behavior, and runtime behavior not yet observed**.

## How I approach quality

- **Start from observable behavior:** expected result, actual result, environment, reproduction steps, evidence.
- **Test the affected scope:** normal, edge, negative, fallback, and regression scenarios as appropriate.
- **Isolate causes:** controlled comparisons, instrumentation, system logs, benchmarks, cross-platform checks.
- **Verify independently:** visual inspection can overturn an automated PASS; compiling is not the same as fixing; an agent reporting "done" is not the same as done.
- **Document uncertainty:** keep failed tests, caveats, test conditions, and enough context for others to reproduce the result.

## Professional background

- **Certifications:** CompTIA A+, Microsoft Azure Fundamentals (AZ-900), Azure AI Fundamentals (AI-900), Linux Essentials. IT Security & Administration program, MyComputerCareer (2024).

## Tools

- **I use directly:** Linux (Arch/CachyOS, Ubuntu Server), Windows, Git/GitHub, VS Code, the command line, FFmpeg, BMC Remedy, Microsoft 365, Oracle Cloud, networking and cross-browser diagnostics.
- **AI development:** Claude Code, ChatGPT / Codex, GitHub Copilot — multi-agent workflows, context curation, independent evaluation.
- **Stacks my projects use (built by agents under my direction):** C++, Python, Vulkan, ROCm/HIP, MiGraphX, Qt/QML.

Open to **IT support and service desk, application and product support, software QA and technical validation, AI red teaming and model evaluation, and other roles where troubleshooting and evidence-based reasoning matter.** Remote.

