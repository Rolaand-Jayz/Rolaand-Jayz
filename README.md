# Rolaand Jayz
**Jeffrey Orr Jr. | Software QA, Technical Investigation & Linux/Video Engineering**

I investigate what software actually does, not just what it is supposed to do. My background combines enterprise IT support with independent software engineering and rigorous test work: reproducing failures, reading code and logs, isolating variables, challenging apparently successful results, and documenting findings so someone else can verify them.

My main areas are **manual and exploratory testing, evidence-based regression checks, C++/Python investigation, Linux, GPU/video pipelines, and AI-assisted engineering with independent validation**. I use AI tools to expand the scope of what I can work on, while retaining responsibility for requirements, technical decisions, testing, and acceptance.


**[QA case studies and sample test design →](QA_TEST_EVIDENCE.md)** — public evidence of defect investigation, failed hypotheses, test scope, and repeatable checks.

## Selected public work

### [Temporal Forge Player](https://github.com/Rolaand-Jayz/Temporal-Forge-Player) — closed FSR-era video-reconstruction research

A Linux C++/Vulkan/FFmpeg research project investigating how AMD FSR 4.1-style temporal reconstruction behaves on ordinary decoded video. The most relevant work is the **test methodology**: controlled experiments, source-cadence requirements, baseline comparisons, multi-frame evaluation, negative findings, and review of automated quality gates.

- Reopened a previously passing quality gate after visible lattice corruption appeared; retained and reclassified invalidated results.
- Used evidence from repeated experiments to close the FSR-centered approach in **September 2026** rather than claim a quality advantage that was not established.
- [Read the closure and evidence ledger](https://github.com/Rolaand-Jayz/Temporal-Forge-Player/blob/main/docs/closure/CLAIM_EVIDENCE_LEDGER.md).

### [AMD Video Enhancer (AMD-VE)](https://github.com/Rolaand-Jayz/AMD-VE) — Linux-first AMD video application

Experimental C++ application integrating FFmpeg, ROCm/HIP, MiGraphX, and Vulkan. Testing went beyond the application's UI into runtime dependencies, model execution, GPU behavior, benchmarking, fallback paths, and reproducible release documentation.

The investigations prompted **four submitted upstream MiGraphX optimization pull requests**: [#4707](https://github.com/ROCm/AMDMIGraphX/pull/4707), [#4708](https://github.com/ROCm/AMDMIGraphX/pull/4708), [#4709](https://github.com/ROCm/AMDMIGraphX/pull/4709), and [#4710](https://github.com/ROCm/AMDMIGraphX/pull/4710). Benchmarks are workload-specific; this is not a claim of universal speedup or upstream acceptance.

### [FSR 4.1 Static Reverse Engineering](https://github.com/Rolaand-Jayz/RE-of-FSR-4.1.0-Upscaling) — reproducible research

Analysis of shader passes, binary resources, dispatch structures, neural-weight data, and resource bindings using Python, C, disassembly, and comparison tools. The repository deliberately distinguishes **verified static facts, inferred behavior, and runtime behavior not yet observed**.

## Current private work

**ANVIL / FORGE:** ongoing from-scratch video-reconstruction R&D informed by the preceding research. The active repository is private; the public Temporal Forge repository remains available as an auditable record of the earlier experiment and the decision to pivot.

## How I approach quality

- **Start from observable behavior:** expected result, actual result, environment, reproduction steps, and evidence.
- **Test the affected scope:** inspect changes and dependencies; use normal, edge, negative, fallback, and regression scenarios as appropriate.
- **Isolate causes:** controlled comparisons, instrumentation, system logs, benchmarks, and cross-platform checks.
- **Verify independently:** visual inspection can overturn an automated PASS; compiling is not the same as fixing.
- **Document uncertainty:** retain failed tests, caveats, test conditions, and enough context for others to reproduce the result.

## Professional background & tools

- **Enterprise support:** Service Desk Analyst, Alpha Net Consulting LLC, through Capgemini for Progressive Insurance (April 2025–July 2026); Microsoft 365, application/hardware/access issues, BMC Remedy, incident resolution and escalation.
- **Customer operations:** Former ResultsCX team supervisor; led and coached teams of approximately 15–20+ agents.
- **Technical toolkit:** C++, Python scripting, JavaScript/Node familiarity, Bash, Git/GitHub, VS Code, Arch/CachyOS, Ubuntu Server, Windows, FFmpeg, Vulkan, ROCm/HIP, MiGraphX, Oracle Cloud, networking, and cross-browser diagnostics.
- **Certifications:** CompTIA A+, Azure Fundamentals (AZ-900), Azure AI Fundamentals (AI-900), Linux Essentials.

Interested in **manual/software QA, technical validation, video/application reliability, systems integration, and engineering roles where troubleshooting and empirical reasoning matter**.

[LinkedIn — Jeffrey Orr Jr.](https://www.linkedin.com/in/jeffreyorrjr)
