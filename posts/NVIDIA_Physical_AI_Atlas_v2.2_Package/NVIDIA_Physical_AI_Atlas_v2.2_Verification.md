# NVIDIA Physical AI Ecosystem Atlas v2.2 — Verification notes

**Review date:** 2026-11-11  
**Website:** `NVIDIA_Physical_AI_Ecosystem_Atlas_v2.2_EN_KO.html`  
**Scope:** official research and NVIDIA developer announcements; source repositories, publication/license status, role in architecture.

## 1. GR00T 2 / N2
- NVIDIA announced GR00T 2 at CoRL on **Nov 9, 2026**.
- The official NVIDIA Research page describes the **World–Action Model** architecture: a diffusion transformer jointly predicts future video and robot actions, with embodiment-specific controllers, X-Adapt skill transfer, few-shot post-training, reasoning-agent integration and a smaller Turbo configuration.
- Official site lists **Code Available in December**; as of the review date, the atlas does **not** claim public downloadable N2 model weights or production-ready code.
- Published performance examples are specific to NVIDIA's research setup and should not be treated as guaranteed robot success rates.
- Sources: https://research.nvidia.com/labs/gear/gr00t-2/ ; https://blogs.nvidia.com/blog/robotics-simulation-advancements-corl/

## 2. GR00T N1.7 (retained)
- Public VLA model / released code and model checkpoint; earlier GR00T generation.
- N1.7 **code** uses Apache-2.0; its **model weights** use NVIDIA Open Model License. Check the original repository/model card for exact restrictions.
- Kept in **Explore technologies**, not the Ecosystem Architecture. The reproducible policy workflow still uses N1.7 and identifies N2 as its research successor.
- Sources: https://github.com/NVIDIA/Isaac-GR00T ; https://developer.nvidia.com/blog/develop-humanoid-robot-policies-end-to-end-with-nvidia-isaac-gr00t/

## 3. Newton Physics
- Open-source, Linux Foundation project initiated by NVIDIA, Google DeepMind, and Disney Research; code Apache-2.0.
- Modular physics engine built on **Warp and OpenUSD** with selectable solvers, contact models, rigid/deformable simulation, and Isaac Lab / Isaac Sim integration.
- Placed in **Digital World (Simulation/Physics)** architecture stage, with detailed technical entry.
- Sources: https://developer.nvidia.com/newton-physics ; https://github.com/newton-physics/newton ; https://developer.nvidia.com/blog/newton-adds-contact-rich-manipulation-and-locomotion-capabilities-for-industrial-robotics/

## 4. NVIDIA Warp
- Open-source Apache-2.0 **Python JIT GPU-kernel framework**, supporting geometry processing, physics kernels, and differentiable computing.
- It is **not a turnkey physics simulator**; Newton adds robot simulation models and solvers on top.
- Placed in **Shared Compute & Operations** foundation in the Ecosystem Architecture, with detailed technical entry.
- Sources: https://github.com/NVIDIA/warp ; https://github.com/NVIDIA/warp/blob/main/docs/user_guide/faq.rst

## 5. Web verification
- Static self-contained HTML, no runtime translation API or build step.
- English is the default locale and the EN/KO switch works throughout the content.
- Preserved existing 6 layers, 3 workflows and search/filter/theme interactions.
- Tested **47 distinct routes in EN and 47 distinct routes in KO** at desktop width, plus key routes at 768px and 390px.
- Verified that the main architecture contains **GR00T 2 and Newton**, Warp remains in the architecture foundation, and **GR00T N1.7 appears only in the catalog and references** (not the architecture diagram).
- Verified GR00T search returns both N2 and N1.7, and language switching preserves the query.
- No JavaScript page errors encountered during these Chromium checks; tested responsive width had no document-level horizontal overflow.
- Source/license and future release information is dated; recheck official pages before production deployment.
