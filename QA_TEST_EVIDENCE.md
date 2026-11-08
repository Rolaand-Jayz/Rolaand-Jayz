# Software QA & Validation — Public Evidence Portfolio

**Jeffrey Orr Jr. (Rolaand Jayz)** | [GitHub profile](https://github.com/Rolaand-Jayz) | [LinkedIn](https://www.linkedin.com/in/jeffreyorrjr)

This is an index of **independent engineering and test work**, not a claim of salaried QA employment. It links to public technical evidence and includes a clearly marked *illustrative test case* derived from an existing software contract.

## Case study 1 — A false-positive quality gate

**System:** [Temporal Forge Player](https://github.com/Rolaand-Jayz/Temporal-Forge-Player), experimental Linux C++/Vulkan/FFmpeg temporal video reconstruction.

**Problem:** A prior automated quality gate reported PASS, but a later visual review identified periodic lattice corruption in the rendered output.

**QA response:** The apparent PASS was challenged; affected experimental evidence was treated as historical/invalidated rather than promoted as proof of quality. The defect was reopened for targeted investigation.

**What this demonstrates:** Independent visual inspection, regression skepticism, controlled evidence handling, and the ability to reject attractive green metrics when observable behavior contradicts them.

**Primary evidence:** [Closure claim/evidence ledger](https://github.com/Rolaand-Jayz/Temporal-Forge-Player/blob/main/docs/closure/CLAIM_EVIDENCE_LEDGER.md) and [lattice corruption diagnostic](https://github.com/Rolaand-Jayz/Temporal-Forge-Player/blob/main/docs/LATTICE_CORRUPTION_DIAGNOSTIC.md).

## Case study 2 — A hypothesis that did not pass

**Question:** Would more accurate motion estimation materially improve FSR-style reconstruction of finished video?

**Approach:** Controlled comparisons of motion input strategies and temporal outcomes against matched controls, with source resolution and other inputs constrained as appropriate to the test campaign.

**Result:** The published 288-key multi-frame campaign did **not** establish repeatable quality gains from improved motion across the tested scope. This is not a proof that motion is useless in all architectures; it is a reason not to promote this specific approach without evidence.

**What this demonstrates:** Hypothesis-driven testing, explicit scope, reproducibility, handling of negative findings, and a willingness to revise an implementation strategy based on data.

**Primary evidence:** [Motion campaign ledger](https://github.com/Rolaand-Jayz/Temporal-Forge-Player/blob/main/benchmarks/quality_sweeps/MOTION_CAMPAIGN.md) and [project closure decision](https://github.com/Rolaand-Jayz/Temporal-Forge-Player/blob/main/docs/closure/FSR41_FINAL_ADJUDICATION_20260915.md).

## Case study 3 — Cross-browser user issue isolation

**Observed defect:** YouTube watch history failed to update in Firefox, while the same account recorded history in Zen and Brave.

**Manual investigation:** Compared the same user workflow across browsers, excluded account-wide history being off, then isolated a suspected browser-extension condition.

**Observed resolution:** With uBlock disabled in Firefox, watch history saved again.

**What this demonstrates:** Reproducing a user-visible issue, comparison against known-good environments, selecting a low-risk discriminating test, and confirming recovery. This was an informal personal troubleshooting case, not a formal browser regression project.

## Case study 4 — Performance change without overclaiming

**System:** [AMD Video Enhancer](https://github.com/Rolaand-Jayz/AMD-VE) / MiGraphX inference on AMD hardware.

**Focus:** Investigating a GPU execution bottleneck, changing launch geometry, and comparing a specific isolated workload against an identified preceding baseline.

**Observed:** Public documentation reports an approximately 11.80 ms to 8.31 ms result for a specified FP16 gfx1100 workload. This is **workload-specific**, not proof of an across-the-board 30% application speedup.

**Review artifacts:** Four [submitted MiGraphX PRs](https://github.com/ROCm/AMDMIGraphX/pulls?q=author%3ARolaand-Jayz), documented benchmarking caveats, and [AMD-VE validation documentation](https://github.com/Rolaand-Jayz/AMD-VE/blob/main/docs/VALIDATION_AND_EVIDENCE.md). Submission is not the same as merging.

## Illustrative manual test case — preserving source cadence

*This is a portfolio test-case example derived from Temporal Forge's published contract; it is not represented as a verbatim historical test record or a fresh execution result.*

| Field | Example |
|---|---|
| ID | VID-CADENCE-001 |
| Target | Video output pipeline |
| Objective | Verify one decoded source frame corresponds to one displayed reconstructed frame |
| Preconditions | Known sample with verified frame count, frame timestamps, and frame rate; supported GPU/backend |
| Steps | (1) Record source frame count, PTS and cadence. (2) Run the configured output path. (3) Capture emitted frame count and timestamps. (4) Compare source/output sequences. (5) Repeat after resizing output window and when falling back to spatial scaling. |
| Expected | Output preserves source frame count and timestamps; window resizing changes presentation, not source cadence; unavailable experimental backend reports fallback rather than silently claiming success. |
| Report if failed | Source/configuration, build revision, backend, output mode, exact mismatch, reproduction command, logs, sample frames, and expected versus actual result |
| Evidence status | Example procedure; **not newly executed for this portfolio entry** |

## My test habits

1. Inspect code/configuration changes and identify affected behavior.
2. Write an observable expectation and a reproducible test procedure.
3. Check the normal path, boundary conditions, negative controls, and fallback behavior.
4. Compare with a versioned baseline; distinguish an isolated result from a general claim.
5. Use logs/traces and visual inspection when numeric metrics are incomplete.
6. Retain failed tests, limitations, and enough provenance for independent review.

**Relevant tools:** Git/GitHub, C++, Python analysis, Bash, VS Code, Linux, FFmpeg, Vulkan, ROCm/HIP, MiGraphX, browser comparisons, system monitoring, and structured documentation.
