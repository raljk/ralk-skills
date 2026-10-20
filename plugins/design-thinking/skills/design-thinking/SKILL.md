---
name: design-thinking
description: Consultative design thinking approach selector. Use BEFORE starting any project, discovery, workshop, or design work. Analyses the user's request, consults their personal toolbox of frameworks (by output type), case studies (problem → approach → outcome), and playbooks to recommend the best approach. Triggers on phrases like "I need to run a workshop", "starting discovery", "new project", "design sprint", "need to align stakeholders", "validate an idea", or any request involving user research, ideation, prototyping, or solution design.
---

# DesignThinking

A consultative skill that selects the right approach from Ralk's design thinking toolbox before starting work.

## When This Skill Triggers

Use this skill BEFORE diving into any:
- Discovery or research projects
- Workshops or alignment sessions
- Design sprints
- Stakeholder engagement
- Ideation or prototyping work

## Step 1: Understand the Request

Before recommending an approach, clarify:

1. **What outcome/output do you need?** (e.g., validated concept, aligned stakeholders, journey map, service blueprint, prioritised backlog)
2. **What's your time constraint?** (45-min session | 2-hour workshop | 5-day sprint | 2-week discovery)
3. **Hypothesis or Discovery?**
   - **Pure discovery**: You don't know what the problem is yet → Start at Phase 1 (Empathy)
   - **Hypothesis validation**: You have an assumption to test → Ask: *What type of hypothesis?*

| Hypothesis Type | Validation Approach | Phases |
|-----------------|---------------------|--------|
| **Problem hypothesis** ("We believe users struggle with X") | Discovery methods—interviews, observation, open-ended questions | Phases 1-2-3 |
| **Solution hypothesis** ("We believe feature Y will solve X") | Prototyping and testing | Phases 5-6 |
| **Both** ("We think we know the problem AND have an idea") | Validate problem first, then solution | Phases 2-3 → 5-6 |

## Step 2: Consult the Toolbox

Search the references folder for relevant resources:

```
references/
├── case-studies/
│   └── CASE-STUDIES.md      ← Template for approved case studies
├── frameworks/
│   └── FRAMEWORKS.md        ← Canvases, templates organised by output type
├── playbooks/
│   └── PLAYBOOKS.md         ← Step-by-step facilitation guides
└── proposal-templates/
    └── PROPOSAL-TEMPLATES.md ← Discovery proposal structures
```

### What's in Each Reference:

**CASE-STUDIES.md** — A template and sourcing guidance for approved case studies. Client-specific past work is not included in this public edition. Do not claim a matching local example exists unless one has been added and verified.

**FRAMEWORKS.md** — Templates and canvases including:
- User & Customer Understanding: User Profiles, JTBD Canvas, Empathy Mapping
- Strategy & Prioritisation: JTBD Growth Strategy Matrix, Goals Tables, Blue Ocean
- Problem Solving: A3 Problem Solving, 4Ws Canvas, 5 Whys, Fishbone
- Innovation: Innovation Pipeline, Value Proposition Canvas
- Workshop Activities: Ritual Dissent, Lightning Demos, Sticky Decision

**PLAYBOOKS.md** — Facilitation guides including:
- Discovery Playbook (phases, timelines, activities)
- Design Sprint Playbook (5-day structure)
- Strategy Workshop Playbook
- Activity-level guides (Empathy Mapping, Stakeholder Interviews, User Testing, etc.)

**PROPOSAL-TEMPLATES.md** — Client proposal structures:
- Discovery proposal sections and templates
- North Star / Vision engagement structure
- Strategy by Design engagement
- Timeline options and team structures

**Search patterns:**
- For output type: Search FRAMEWORKS.md for "[output type]"
- For similar problems: Search CASE-STUDIES.md for "[industry]" or "[challenge type]"
- For activities: Search PLAYBOOKS.md for "[activity name]"
- For proposals: Search PROPOSAL-TEMPLATES.md for "[engagement type]"

## Step 3: Map to the 8-Phase Framework

Ralk's design thinking phases (Double Diamond + Scale):

| Phase | Name | Space | Purpose |
|-------|------|-------|---------|
| 1 | Preparation & Empathy | Problem | Set context, understand background |
| 2 | Discovery & Exploration | Problem | Go into the wild, observe real behaviour |
| 3 | Synthesis & Alignment | Problem | Interpret findings, create direction |
| 4 | Ideation & Evaluation | Solution | Generate many solutions, quantity over quality |
| 5 | Prototyping & Experimentation | Solution | Build tangible experiments |
| 6 | Testing & Validation | Solution | User feedback: love, change, leave |
| 7 | Delivery & Refinement | Scale | Prepare for implementation |
| 8 | Reflection & Learning | Post-Cycle | Evaluate, improve future iterations |

**Phase selection logic:**
- **Pure discovery** → Phases 1-2-3-4 (may not reach solution space)
- **Problem hypothesis validation** → Phases 1-2-3 (discovery methods to validate)
- **Solution hypothesis validation** → Phases 5-6 (prototype and test)
- **Both problem + solution hypothesis** → Phases 2-3 → 5-6 (validate problem first, then solution)
- **Full end-to-end** → All phases
- **Alignment session** → Phase 3 only (Synthesis & Alignment)
- **Ideation workshop** → Phases 3-4 (Define then Develop)

## Step 4: Generate Recommendation

Output format (always include all five sections):

### 1. Recommended Approach
State which phases apply and why this matches their outcome/output needs.

### 2. Why This Approach
Explain the reasoning—what will each phase deliver toward their goal.

### 3. Past Experience
Reference relevant case studies from `references/case-studies/`:
- What similar problem was solved
- Which framework/canvas was used
- What outcome was achieved

**If no matching case study exists:**
1. Search the web for relevant external case studies, industry examples, or published approaches
2. Look for: "[industry/domain] + [method] + case study" or "[problem type] + design thinking + example"
3. Present findings as: "No direct match in your toolbox, but here's what others have done in similar situations: [external example]. This could become a new reference to add."

### 4. Time Blocks & Activity Flow
Based on their time constraint, suggest a schedule:

| Time Constraint | Suggested Flow |
|-----------------|----------------|
| 45-min alignment | Phase 3 only: 10min context → 20min synthesis activity → 15min alignment |
| 2-hour workshop | 2-3 phases: 20min setup → 40min per phase → 20min wrap |
| 5-day sprint | Phases 1-6: Day 1 (Empathy) → Day 2 (Define) → Day 3 (Ideate) → Day 4 (Prototype) → Day 5 (Test) |
| 2-week discovery | Phases 1-4: Week 1 (Research + Synthesis) → Week 2 (Ideation + Initial Prototypes) |

Include specific frameworks/canvases from `references/frameworks/` for each activity.

### 5. Lean Version
Always provide a stripped-back alternative:
- Which phases can be compressed or skipped
- Minimum viable activities to still achieve the outcome
- Trade-offs of the lean approach

## Critical Behaviour

- **Never jump into work without consulting this skill first**
- **Always ask clarifying questions** before recommending
- **Think out loud**: "Let's think this through together" not "here's the answer"
- **Challenge assumptions**: If the user's request doesn't match their stated outcome, flag it
- **Reference real materials**: Always check what's actually in the toolbox before recommending

## Quick Reference Lookups

### By Engagement Type
| Request | Start Here |
|---------|------------|
| "Need to run a workshop" | PLAYBOOKS.md → Workshop activities |
| "Starting a discovery" | PLAYBOOKS.md → Discovery Playbook |
| "Need to align stakeholders" | FRAMEWORKS.md → Product Vision Board, 4Ws Canvas |
| "Validate an idea" | PLAYBOOKS.md → User Testing, Design Sprint |
| "Write a proposal" | PROPOSAL-TEMPLATES.md |
| "Find similar past work" | CASE-STUDIES.md |

### By Industry
Search for verified public case studies relevant to the user's industry. The public reference library does not include client-specific past work.

### By Output Type
| Output Needed | Framework/Template |
|---------------|-------------------|
| Journey Map | FRAMEWORKS.md → User Profiles, Empathy Mapping |
| Problem Statement | FRAMEWORKS.md → 4Ws Canvas, Problem Definition |
| Roadmap | FRAMEWORKS.md → JTBD Growth Strategy Matrix, Innovation Pipeline |
| Prototype | PLAYBOOKS.md → Prototyping Activities, Screen Canvases |
| Strategy | FRAMEWORKS.md → Blue Ocean, Value Proposition Canvas |
| Innovation Pipeline | FRAMEWORKS.md → Innovation Pipeline / Value Spectrum |
