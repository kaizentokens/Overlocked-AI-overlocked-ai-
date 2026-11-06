# Overlocked AI (`overlocked-ai`)

> **"To 'overlock' your AI tools means moving from being a passive consumer to an active hacker — tuning the engine rather than just reading the output."**

[License: MIT](https://www.google.com/search?q=LICENSE)
[](https://www.python.org/)
[](#architecture)
[](#)

---

## ⚡ Manifesto & Philosophy

Most users treat Large Language Models like an opaque black box:
$$\text{Input} \longrightarrow \boxed{\text{Black Box LLM}} \longrightarrow \text{Output}$$

To the passive consumer, an LLM is a conversational chatbot. To the hacker, an LLM is a **stochastic inference engine governed by multidimensional latent spaces, activation vectors, and next-token probability distributions**.

Inspired by foundational exploit and logic libraries like [`yaklang/hack-skills`](https://github.com/yaklang/hack-skills.git), **Overlocked AI** is a universal framework and middleware layer that deconstructs, intercepts, and supercharges LLM interactions. It treats AI as raw hardware requiring precision timing, parametric overclocking, and tactical gadget injection.

```
       +-------------------------------------------------------------+
       |                     RAW USER PROMPT                         |
       +-------------------------------------------------------------+
                                      |
                                      v
       +-------------------------------------------------------------+
       |               OVERLOCKED INJECTION ENGINE                   |
       |  - Latent Deconstruction & Dimensionality Conditioning     |
       |  - Gadget Wrapping (Role Hijacking, CoT Verification)       |
       |  - Dynamic Temperature & Top-p Latent Jitter                |
       +-------------------------------------------------------------+
                                      |
                                      v
       +-------------------------------------------------------------+
       |                  TARGET LLM / INFERENCE                     |
       |       (OpenAI / Anthropic / Gemini / Local Ollama)          |
       +-------------------------------------------------------------+
                                      |
                                      v
       +-------------------------------------------------------------+
       |                RECURSIVE CRITIQUE & SYNTHESIS               |
       |       Pass 1: Raw Output -> Adversarial Critique            |
       |       Pass 2: Targeted Edge Tightening                      |
       |       Pass 3: Synthesized Final Execution                   |
       +-------------------------------------------------------------+
                                      |
                                      v
                          OVERLOCKED OUTPUT
```

---

## 🔬 Core Pillars

### 1. Reverse Engineering the AI Engine
Before you can overlock a system, you must expose its internal mechanics:
* **Token Dynamics & Logits:** LLMs do not "think"; they compute transition probabilities over vocabulary token spaces. Generic inputs land in high-probability, high-entropy clichéd basins.
* **Latent Space Steering:** By injecting precise syntactic gadgets and semantic constraints, you steer activation vectors away from default median outputs toward high-performance latent sub-manifolds.
* **Boundary & Guardrail Probing:** Mapping the exact perimeter where system instructions collide with raw completion dynamics allows surgical bypass of conversational molasses and artificial conversational padding.

### 2. The Gadget Architecture
A **gadget** is an isolated, modular prompt-wrapper or structural transform injected into the model pipeline. Rather than issuing a bare query, gadgets wrap prompts with operational logic:
* **Recursive Optimizer:** Enforces iterative self-critique loops before finalizing outputs ($Output_{n} = f(Critique(Output_{n-1})) $).
* **Chain-of-Thought (CoT) Verification:** Forces structured topological step decomposition and premise validation.
* **Role Hijacker:** Conditions model tone, vocabulary, and deductive stance into hyper-specialized execution modes (e.g. Hemingway prose, ruthless red-team auditor, systems kernel architect).
* **Boundary Prober:** Strips corporate boilerplate, pleasantries, and hedging, forcing high signal-to-noise ratio output.

### 3. Universal Skill Injection Layer
You can't retrain closed frontier models on the fly, but you can wrap them in a **universal middleware interceptor**. `overlocked-ai` hooks into standard LLM client libraries (`openai`, `anthropic`, `google-genai`, `ollama`) and injects overlocked gadgets seamlessly into every transaction.

### 4. The 3 Levels of AI Mastery
1. **Level 1: The Prompt Architect** — Moves past prose sentences into hierarchical meta-prompt structures, schema enforcement, and zero-shot latent constraints.
2. **Level 2: The Recursive Loop Engineer** — Rejects first-draft mediocrity. Automates multi-pass critique cycles that tighten reasoning, eliminate passive voice, and verify factual assertions.
3. **Level 3: Multi-Agent Orchestration** — Synchronizes heterogeneous models across specialized roles (e.g., DeepSeek/Claude for formal reasoning, GPT-4o for synthesis, local specialized models for fast critique).

---

## 🛠️ Repository Layout

```
overlocked-ai/
├── overlock/
│   ├── __init__.py            # Package root & exports
│   ├── engine.py              # Overlock Engine core runner & lifecycle
│   ├── middleware.py          # Universal API Interceptor & wrapper
│   ├── orchestrator.py        # Multi-model synchronous orchestration
│   ├── cli.py                 # Command-line interface (`overlock`)
│   └── gadgets/               # Modular skill gadget library
│       ├── __init__.py
│       ├── base.py            # BaseGadget interface
│       ├── recursive_loop.py  # Recursive critique & refinement loop
│       ├── chain_of_thought.py# Step-by-step reasoning amplifier
│       ├── role_hijacker.py   # Latent persona & constraint steering
│       ├── deconstructor.py   # Token/latent deconstruction analyzer
│       └── boundary_probe.py  # Anti-fluff & guardrail pressure probe
├── examples/
│   ├── 01_basic_overlock.py   # Single-turn gadget injection demo
│   ├── 02_recursive_refine.py # 3-stage iterative self-refinement
│   └── 03_multi_agent.py      # Multi-model red-team / blue-team pipeline
├── tests/
│   └── test_engine.py         # Unit tests for engine & gadget registry
├── pyproject.toml             # Modern packaging spec
├── LICENSE                    # MIT License
└── README.md                  # System architecture & documentation
```

---

## 🚀 Quickstart

### Installation

```bash
# Clone the repository
git clone https://github.com/overlocked/overlocked-ai.git
cd overlocked-ai

# Install in editable mode
pip install -e .
```

### CLI Usage

```bash
# Basic run with Role Hijacker and Recursive Optimization
overlock run "Analyze the vulnerabilities of JWT token storage in localStorage" \
    --gadget role_hijacker \
    --role "Offensive Security Lead" \
    --gadget recursive_loop \
    --passes 3

# Deconstruct an prompt into latent tokens and structural constraints
overlock deconstruct "Draft a microservices architecture migration plan"

# Anti-Fluff Boundary Probe mode
overlock probe "Explain transformer self-attention mechanisms" --anti-fluff
```

### Python API Usage

```python
from overlock.engine import OverlockEngine
from overlock.gadgets.role_hijacker import RoleHijacker
from overlock.gadgets.recursive_loop import RecursiveLoop
from overlock.gadgets.chain_of_thought import ChainOfThought

# Initialize Overlock Engine
engine = OverlockEngine()

# Register desired gadgets
engine.add_gadget(RoleHijacker(role="High-Performance Systems Engineer", constraints=["Zero boilerplate", "Include algorithmic complexity"]))
engine.add_gadget(ChainOfThought(depth=3))
engine.add_gadget(RecursiveLoop(max_passes=2))

# Execute Overlocked transformation
prompt = "Design a lock-free ring buffer in C++20"
overlocked_prompt = engine.prepare_prompt(prompt)

print(overlocked_prompt)
```

---

## 🧩 Built-in Gadgets

| Gadget | Type | Function |
| :--- | :--- | :--- |
| `RoleHijacker` | Latent Steering | Injects authoritative personas and strict linguistic constraints to bypass generic conversational tropes. |
| `RecursiveLoop` | Execution Flow | Implements automated multi-pass self-critique: Draft $\to$ Critique $\to$ Refine. |
| `ChainOfThought` | Cognitive Amplifier | Deconstructs complex inquiries into strict premise dependencies and verification gates. |
| `BoundaryProbe` | Guardrail Audit | Strips sycophancy, hedges, disclaimers, and conversational filler. |
| `Deconstructor` | Analysis | Inspects prompt token entropy and highlights failure points before API transmission. |

---

## ⚡ The Overlocked Workflow in Action

| Standard Prompting | Overlocked Execution |
| :--- | :--- |
| *"Write me a story about a cat."* | **Input:** *"Write me a story about a cat"*<br>**Injected Gadgets:** `[Role: Hemingway]` `[Constraint: Zero adjectives in draft 1]` `[RecursiveLoop: 3 passes]`<br>**Result:** Lean, muscular, rhythmic prose engineered down to the syllable. |
| *"How do I optimize SQL queries?"* | **Input:** *"How do I optimize SQL queries?"*<br>**Injected Gadgets:** `[CoT: Explain plan tree]` `[BoundaryProbe: No intro/outro]` `[Critique: B-Tree vs LSM tradeoffs]`<br>**Result:** Surgical, execution-plan-level architectural breakdown. |

---

## 🤝 Contributing

Contributions to the Gadget Registry are welcome:
1. Fork the repository
2. Create a feature branch (`git checkout -b gadget/dynamic-entropy`)
3. Add your gadget under `overlock/gadgets/` inheriting from `BaseGadget`
4. Add unit test coverage under `tests/`
5. Submit a Pull Request

---

## 📜 License

MIT License. See [LICENSE](https://www.google.com/search?q=LICENSE) for details.
