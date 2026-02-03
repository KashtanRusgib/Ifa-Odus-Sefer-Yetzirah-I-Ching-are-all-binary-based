# ABOUT.md: Ancient Systems Divination Simulator

## Project Overview

This project is a computational framework that maps three ancient mystical/divinatory traditions—Sefer Yetzirah (Jewish Kabbalah, focused on creation), I Ching (Chinese philosophy, focused on change), and Ifá Odus (Yoruba tradition, focused on probability)—to modern computer science (CS) concepts like binary encoding, data structures, algorithms, and information theory. It treats these systems as proto-computational models, simulating their processes for divination, comparative analysis, and epistemic exploration. Pioneered by Dr. Goldoval (@DoctorGoldOval) as the first known synthesis connecting all three traditions in the contexts of CS, probability, and epistemology, it highlights shared binary foundations (e.g., 32 paths ≈ 2^5, 64 hexagrams = 2^6, 256 Odus = 2^8) and inspires interdisciplinary insights, from AI ethics to quantum modeling.

The simulator enables users to query "latent spaces" of reality through an input-process-output paradigm, mirroring ancient oracles while incorporating epistemic weighting (viability scores for pattern "durability" via lemmas/causal links) and 3D visualizations. Built in Python with a Flask web app and CLI, it's designed for curiosity-driven exploration, not prediction—emphasizing fun, unity across cultures, and non-reductionist symbolism (e.g., symbols as dynamic operators, not static labels).

## Key Features

- **Divination Simulation**: Generate patterns/interpretations for each system or unified mode.
  - Sefer Yetzirah: Permutes letters/Sephirot for "creation" insights (e.g., golem-like sequence inscription).
  - I Ching: RNG-based hexagrams with changing lines for "change" guidance.
  - Ifá: 8-bit Odu casting with verses for "probability" advice.
- **Comparative Mapping**: Uses 65 NSM semantic primes as roots, with cultural encodings; bitwise operations (e.g., Hamming distance) for relational links between systems.
- **Epistemic Engine**: Biases results toward "durable" patterns (Tao-aligned, via viability scores, lemmas from CLI/searches); no steady states—models flux with time-crystal sims.
- **3D Visualization**: Nested Fibonacci spheres (inner: Sefer r=60 blue, middle: I Ching r=110 green, outer: Ifa r=170 gold) with uniform point distribution, causal link lines, and pulsing nodes on weights; rotatable for cycles.
- **Interfaces**:
  - CLI: `python src/main.py simulate --system all --query "your query" --lemmas 5 --mode ternary` for outputs/tables/graphs.
  - Web App: Flask at http://localhost:5000 with interactive form, 3D viz, metadata panels, and raycasting for details.
- **Extensions**: Ternary aspects (I Ching moving lines), Mars holiday param (annual "crack" for future-past bias), fractal overlays (optional ponerology).

## Architecture

Modular Python 3.12+ app with:
- **Core Modules**: SeferYetzirahModule, IChingModule, IfaModule (inherit DivinationEngine ABC for generate/interpret/map_to_physics/compute_viability/model_flux).
- **Utilities**: BinaryUtils (bit-to-symbol, combinations), GraphMapper (NetworkX knowledge graphs, visualize_toroid/knowledge_graph), Comparator (Pandas tables), EpistemicEngine (viability_score, mars_holiday_bias, time_crystal_model, bitwise_distance, ternary_extension, load_primitives).
- **Data Models**: Pydantic for SemioticPrimitive/SystemEncoding validation; primitives.json with 65 NSM primes mapped.
- **Frontend**: Flask app.py serving Three.js index.html for 3D spheres/points/links/pulsing; /coords endpoint exports data.
- **Testing**: 19 passing unit/integration tests (pytest) for generation, mappings, viz, etc.
- **Dependencies**: numpy, networkx, matplotlib, pandas, sympy, pydantic, flask (no installs needed in env).

Data flow: Query input → Pattern generation (RNG/permutations) → Interpretation (with epistemic bias) → Output (text/table/graph) + Viz export.

## Significance and Future Work

This project frames ancient oracles as early informational frameworks, prefiguring CS (e.g., binary as bits, permutations as recursion, Odus as bytes). It fosters cross-cultural innovation, like unified AI ethics (Kabbalah balance, I Ching harmony, Ifá indigenous binaries) or quantum simulations. Potential extensions: Real-time X searches for lemmas, torch ML for probabilistic models, expand to more primes/systems (e.g., Mesoamerican without base-13/20 creep).

Created by Dr. Goldoval (@DoctorGoldOval) as a curiosity-driven exploration of human unity through shared binary intuitions. Open to contributions—fork and PR!

For setup: See README.md. Run tests: `pytest`. Launch app: `python src/frontend/app.py`.
