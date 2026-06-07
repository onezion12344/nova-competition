# NOVA Project: Metacognitive Branching Narrative — Scope & Framework

## 1. Scope Definition

### What we are building

A **branching narrative game** (interactive digital narrative) that trains the player's **metacognitive awareness** — the ability to notice, reflect on, and adjust one's own cognitive processes when encountering information.

### What we are NOT building

- ❌ A fact-checking tool
- ❌ A bias detector for external text (already exists: BiasChecker)
- ❌ A quiz-based educational module
- ❌ A persuasion or "correction" engine

### Core insight

Existing inoculation games (Bad News, Go Viral!) teach players to *recognize manipulation techniques in others' content*. Our game goes one step deeper: it teaches players to *recognize their own cognitive shortcuts when they themselves fall for them*.

The mechanism: **narrative transportation → cognitive inflection point → self-reflection**.

---

## 2. Theoretical Architecture

### Layer 1: Core Framework (总框架)

These papers define the *problem* and the *mechanism*. Everything else hangs off them.

```
                    ┌──────────────────────────────┐
                    │  Metacognition & Reasoning    │
                    │  Errors Framework             │
                    │  (Pennycook 2022)             │
                    │  "Why do people fall for it?"  │
                    └──────────────┬───────────────┘
                                   │
              ┌────────────────────┼────────────────────┐
              │                    │                    │
    ┌─────────▼────────┐  ┌───────▼────────┐  ┌───────▼──────────┐
    │ Narrative        │  │ Inoculation    │  │ Cognitive        │
    │ Transportation   │  │ Theory         │  │ Flexibility      │
    │ (Green & Brock   │  │ (Roozenbeek &  │  │ (Spiro et al.    │
    │  2000)           │  │  van der Linden│  │  2013)           │
    │                  │  │  2019)         │  │                  │
    │ How stories      │  │ Pre-exposure   │  │ Switching        │
    │ bypass critical  │  │ builds         │  │ perspectives     │
    │ thinking         │  │ resistance     │  │ builds cognitive │
    └─────────┬────────┘  └───────┬────────┘  │ resilience       │
              │                    │           └───────┬──────────┘
              └────────────────────┼────────────────────┘
                                   │
                    ┌──────────────▼───────────────┐
                    │  STUDY: Metacognitive         │
                    │  Branching Narrative Game     │
                    │  (Our project)                │
                    └──────────────────────────────┘
```

### Core Papers (must cite)

| # | Paper | Role in our framework |
|---|-------|----------------------|
| C1 | **Pennycook (2022)** — A framework for understanding reasoning errors | Defines WHY people fail — the cognitive taxonomy we design game traps around |
| C2 | **Roozenbeek & van der Linden (2019)** — Fake news game confers psychological resistance | Establishes that game-based inoculation WORKS. Our baseline to surpass (from recognition → metacognition) |
| C3 | **Green & Brock (2000)** — Transportation theory | Explains WHY stories work for persuasion AND why we need "exit moments" for reflection |
| C4 | **Spiro et al. (2013)** — Cognitive flexibility theory | Theoretical basis for why perspective-switching builds deeper understanding |

### Layer 2: Branching Frameworks (分支框架)

These translate the core framework into *game design*.

| # | Paper | Role in our game design |
|---|-------|------------------------|
| B1 | **Pitt, Youngblood & Haahr (2025)** — Designing for Ideological Flexibility in an Educational IDN | 🔥 Direct blueprint. Multi-perspective branching narrative + MKO scaffolding + cognitive inflection points. We adapt their methodology to metacognition domain |
| B2 | **Modirrousta-Galian et al. (2023)** — Inductive learning + gamification for news veracity | Shows inductive (discovery-based) > deductive (taught). Our game uses inductive: players discover their biases through consequences, not lectures |
| B3 | **Orosz et al. (2023)** — Prosocial fake news intervention with durable effects | Evidence for durable effects (not just immediate). Important for our claim that metacognitive training has lasting impact |
| B4 | **Kerwer & Rosman (2020)** — Epistemic beliefs affect intervention efficacy | Explains individual differences. Supports our design choice: the game adapts to player's epistemic style through branching |
| B5 | **Cabrera & Cabrera (2015/2022)** — DSRP Theory | Distinctions/Systems/Relationships/Perspectives. The cognitive framework Pitt (2025) used. We use as game state system skeleton |

### Layer 3: Design Methodology (参考论文)

| # | Paper | What we borrow |
|---|-------|---------------|
| D1 | **The Twine Project** | Pedagogical method: the *act of creating* branching narrative as metacognitive training. We apply this to our game's *authoring pipeline* |
| D2 | **Gee (2003)** — What video games teach us about learning | Identity + reflection loop design principles |
| D3 | **Rozenblit & Keil (2002)** — Illusion of explanatory depth | The specific cognitive bias we build our first game scene around ("you think you understand this, but do you?") |
| D4 | **Shaffer (2006)** — Epistemic games | Epistemic frame design: the player adopts a professional identity (editor/analyst) and thinks within that frame |

---

## 3. From Framework to Game: The Fusion

### How the theories fuse into game mechanics

| Game Mechanic | Derived From | How it works |
|---------------|-------------|--------------|
| **Branching choices with hidden consequences** | Green & Brock (transportation) × Pennycook (reasoning errors) | Player is immersed in a realistic scenario; makes choices; the game does NOT immediately reveal whether the choice was biased. The consequence unfolds naturally 3-5 scenes later |
| **Cognitive Inflection Points** | Pitt et al. (2025) — Dhwani8 | At specific narrative nodes, an NPC-mentor asks: "Why did you choose that?" Player must articulate reasoning. This is the metacognitive moment |
| **State system: Cognitive Flexibility Index** | Cabrera (DSRP) × Spiro (cognitive flexibility) | Game tracks: perspective-switching frequency, consistency of reasoning, willingness to revise. NOT right/wrong score |
| **Inductive discovery** | Modirrousta-Galian et al. (2023) | Player is never told "this is confirmation bias." They experience being in an information bubble, then the bubble breaks. They discover the pattern |
| **Post-game cognitive portrait** | Kerwer & Rosman (2020) | Instead of a score: "You tend to trust authority figures without checking. You changed your mind twice. You never questioned your first source." — a mirror, not a grade |
| **Inoculation layer** | Roozenbeek & van der Linden (2019) | After the experience, the game explicitly names the cognitive patterns the player exhibited. This is the "vaccine" — active inoculation after passive experience |

### Player journey (one session, ~20 minutes)

```
Scene 1: Immersion
  Player receives 3 pieces of conflicting info
  Makes intuitive choice about which to trust
  ↓
Scene 2-4: Consequence unfolding
  Story continues. Player sees consequences of Scene 1 choice
  No judgment, no "you're wrong"
  ↓
Scene 5: Cognitive Inflection Point (Dhwani moment)
  NPC-mentor: "So, why did you trust that source?"
  Player reflects and explains
  ↓
Scene 6-8: Perspective switch
  Player sees the same events from another stakeholder's view
  Original choice looks different now
  ↓
Scene 9: Meta-moment
  "Here's what you did. Here's what you didn't consider."
  Cognitive portrait generated
  ↓
Debrief: Inoculation
  "The pattern you just experienced is called X."
  "Next time you encounter this, you'll notice it."
```

---

## 4. Next Steps

1. ✅ Scope narrowed
2. [ ] Write full literature review (this doc → expanded with detailed citations)
3. [ ] Write methodology section (game design based on the fusion above)
4. [ ] Design first scene prototype (test the Dhwani moment)
5. [ ] Write paper
6. [ ] Build game using story-to-game pipeline

---

*Last updated: 2026-06-08*
