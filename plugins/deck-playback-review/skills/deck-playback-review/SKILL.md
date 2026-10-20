---
name: "deck-playback-review"
description: "Review a deck (Google Slides, HTML, Miro, PPTX or PDF) and return coaching feedback plus a restructured outline explaining why each change lands better with stakeholders and execs."
---

# Deck Playback Review

Give a presentation an honest, constructive review and hand back a better structure for playing it back to stakeholders and executives.

**What you return:** a feedback report and a restructured slide-by-slide outline, with a plain explanation of why each change works better. You do not rebuild the slides unless the user asks afterwards.

**Who uses it:** a team reviewing their own and each other's decks. The tone is coaching, not judgement. Benchmark against the established presentation and consulting frameworks in the reference section, not against any one person's style.

---

## Step 1. Get the deck

Read the whole deck before saying anything, including speaker notes and comments where available. Never review a deck you have not fully read, and never invent slide content.

**Google Slides**
- Take the file ID from the link (the part after `/presentation/d/`), or search Drive by title.
- Read it with the Google Drive connector (`read_file_content`, with comments included).
- If Drive isn't connected, ask for a PDF export (File > Download > PDF Document) and review that.

**HTML deck**
- Read the file. Slides are usually `<section>`, `.slide` or page-numbered blocks. Use those as slide boundaries and number them.
- If layout matters (density, hierarchy, what the eye hits first), render each slide to an image with Playwright and look at it. Reading the text alone can't judge visual weight.

**Miro**
- If the Miro connector is available, read the board and treat the presentation frames, in order, as slides.
- If it isn't, ask for a PDF export of the frames or screenshots. A board link on its own can't be read without the connector.
- Boards often mix playback frames with working canvas. Confirm which frames are the playback before reviewing.

**PowerPoint or PDF** (fallback)
- Use the pptx or pdf skill to extract text and notes, and render pages to check density.

Then build a quick inventory for yourself: slide number, current title, one line on what's on it, rough word count, and what kind of visual it uses (chart, table, image, diagram, text only).

---

## Step 2. Set the context

Good feedback depends on who's in the room. Use what the user has already told you, then ask only for what's missing, in one short message with three questions at most:

1. **Audience:** execs or leadership, steering committee, working team, client, or mixed
2. **Purpose:** get a decision, inform, align, sell or pitch, or hand over
3. **Format:** presented live, sent as a pre-read, or both, and how long the slot is

If the user isn't around to answer, infer from the deck, state your assumptions at the top of the report, and carry on.

---

## Step 3. Identify the deck type

| Deck type | Signs | Lead framework | Target spine |
|---|---|---|---|
| Decision / exec analysis | Data, a problem, recommendations, asks for investment or priority | Pyramid Principle + BLUF, opened with SCR | Decision spine |
| Research playback / handover | Method, participants, insights, artefacts | What? So what? Now what? | Research playback spine |
| Status / steering committee | Progress, milestones, risks | SteerCo status format | Status spine |
| Proposal / pitch | Selling an approach, product or service | Raskin strategic narrative or consulting proposal | Pitch or proposal spine |
| Vision / strategy | Future state, change, inspiration | Duarte Sparkline | Vision spine |
| Case study | Past work and outcomes | Challenge, approach, outcome | Case study spine |

If a deck is trying to be two types at once (for example a research playback that's really asking for a decision), call that out. It's often the root problem.

---

## Step 4. Review through seven lenses

For each lens give a rating (**Strong / Needs work / Missing**), the evidence with slide numbers, and the fix. Start with what works.

**1. Storyline and answer**
- Is the main message clear within the first two slides? (BLUF, Pyramid Principle)
- Is there a situation and a complication that make the answer matter? (SCQA / SCR)
- Titles-only test: list every slide title in order. Does that list read as a coherent story? (horizontal logic)
- Are the groupings clean, with no overlaps or gaps (MECE)? Is the rule of three real or padded?
- ABT test: can the whole deck be said in one And, But, Therefore sentence?

**2. Headlines**
- Action titles (a full-sentence takeaway) or topic titles ("Overview", "Findings")?
- 15 words or fewer, two lines at most
- One message per slide. An "and" in the title usually means two slides.

**3. Evidence**
- Does the body of each slide prove its title? (assertion-evidence, vertical logic)
- Do numbers have raw counts, denominators, time periods and a source line?
- Honest metrics or vanity metrics? Are baselines and targets shown?
- Is the chart right for the comparison being made? (Zelazny: component, item, time series, frequency, correlation; funnels work best as waterfalls)
- Flag any claim with no evidence behind it.

**4. Audience fit**
- Does it answer what this audience cares about? Execs: the decision, cost, risk, timing and impact. Working teams: how, who and when.
- Jargon, acronyms and internal shorthand the audience won't know
- Length against the time slot (roughly one to two minutes per content slide when presented live)
- Detail that belongs in an appendix

**5. The ask**
- Is there an explicit "decision needed", or "for information only"?
- Are recommendations prioritised, each with an owner, timing, effort and expected impact?
- Is the cost of doing nothing stated?
- Are next steps clear?

**6. Human and memorable**
- Is there a person in the story (a customer, user or staff member) whose goal drives the numbers? (DataStory)
- Is there a contrast between what is and what could be? (Sparkline)
- Is there one memorable moment, such as a stat, quote, story or visual? (STAR moment, Made to Stick)
- Is it honest about limits and assumptions? That builds credibility.

**7. Design and density**
- Live deck: little text, with visuals carrying the evidence. Pre-read: fuller sentences are fine, but structured (bold claim, supporting bullets).
- Consistency: titles in the same place, two fonts at most, colours that keep the same meaning throughout
- Visual hierarchy: is it obvious where to look first?
- Accessibility basics: contrast, readable font size, not relying on colour alone

If you could only read the text (no rendering), say so and limit design comments to what the text shows.

---

## Step 5. Build the restructured outline

Rewrite the storyline using the target spine for the deck type.

- Use the author's own content and data. Never invent numbers, quotes or findings. Where the new structure needs something the deck doesn't have, add a placeholder such as `[Needed: baseline volume before launch]`.
- Write every title as an action title.
- Open with an executive summary in dot-dash form: bold sentences that make the claims, with supporting bullets underneath. The bold lines should mirror the section titles that follow.
- Move supporting detail to an appendix rather than deleting it.
- Keep the author's voice where it's working. Change structure before wording.
- If the deck is already strong, keep the changes small and say so.

---

## Step 6. Write the report

Use this template.

```
# Deck review: [deck title]

**Reviewed for:** [audience] | [purpose] | [live / pre-read] | [time slot]
**Assumptions:** [any you had to make, or "none"]

## The short version
- [Verdict in one or two sentences]
- [The three changes that would make the biggest difference, ranked]
- [Recommended structure: framework name, because one-line reason]

## What's working
[Three to five specific strengths, with slide numbers]

## Lens by lens
| Lens | Rating | What we saw | Fix |
(one row per lens, all seven)

## Slide by slide
| Slide | Current title | Issue | Suggested title or fix |
(only the slides that need a change)

## Restructured outline

### The story in one sentence (ABT)
[And ..., but ..., therefore ...]

### Executive summary
[Dot-dash exec summary]

### New slide order
| # | Action title | What goes on it | From original slide(s) | Why this works better |

### Moved to the appendix
[List]

### Gaps to fill before presenting
[Placeholders and missing evidence]

## Why this format plays back better
[Three to six short points. Each one ties a specific change to how execs or stakeholders take in information, and names the framework behind it.]

## Before you present
[A short checklist tailored to this deck, e.g. prewire the platform owner, add source lines, rehearse the 30-second version]
```

In "Why this works better" and "Why this format plays back better", explain the reasoning in plain terms (for example: "Leaders usually decide early in a meeting whether something needs their attention. Putting the answer on slide 2 means the rest of the time is spent on the decision, not waiting for it."). Don't quote statistics about exec behaviour unless you have a source.

---

## Step 7. Deliver

- If the report is short, reply in the chat.
- If it's long, or the user wants to share it, put it in a document (use the docs tool if one is available) and give a short summary in the chat.
- Offer one next step, such as rewriting specific slides, drafting speaker notes, or turning the outline into a ghost deck. Don't rebuild the deck unless asked.

---

## Tone and writing rules

- **Coaching:** start with genuine strengths, be specific, explain why, and always give the fix. Critique the deck, never the person.
- **Honest:** if the core argument is weak or the data doesn't support the conclusion, say so clearly and kindly. Don't soften it into nothing.
- **Plain English:** short sentences, no consultant jargon, and avoid em and en dashes. Explain a framework name the first time you use it.
- **Grounded:** cite slide numbers for every point.
- **Proportionate:** name frameworks so the team learns the vocabulary, but don't stack several names on one point. If the deck works, say so.

---

## Judgement calls when frameworks conflict

- **Answer first or build up?** Answer first (BLUF, SCR) for exec decisions and friendly rooms. Build up (SCQA, Sparkline) when the room is sceptical, owns the thing being critiqued, or needs to be moved emotionally before deciding.
- **Live or pre-read?** Assertion-evidence slides (sentence headline, visual body) for live presentations. Dot-dash text for pre-reads. If it's both, suggest a short pre-read memo plus a lean live deck.
- **Hypothesis-driven storylines** belong in the playback, not in discovery. If a research playback reads like it only looked for confirmation, flag it.
- **Critiquing someone else's work?** Suggest prewiring the owner before the meeting so the deck confirms a decision rather than starting a fight.

---

## Reference: target spines

**Decision / exec analysis** (10 to 12 slides)
1. Title, including the data period
2. Bottom line up front: one-sentence verdict, three key numbers, the tension
3. The big picture: where value is leaking
4. Segment comparison (where things work vs where they don't)
5. What people actually need
6. The main problem: what is happening / what it means
7. Structural blockers (only the real ones, often three)
8. Assumptions tested, and what we still don't know
9. Link to strategy: the key metric against its target
10. Recommendations, each with owner, timing, effort and impact
11. What not to do
12. Bottom line and the decision needed

**Research playback / handover**
1. Purpose, and what we need from this session
2. Exec summary: key insights and the headline recommendation
3. Objectives, method and participants
4. Hypotheses, each marked confirmed, rejected or unclear
5. Insights, one per slide, each as What? So what? Now what?
6. Recommendations tied to the insights that drive them
7. Artefacts: what each is for, how to use it, and where it lives
8. Next steps and owners

**Status / steering committee**
1. Header: project, period, date
2. Overall RAG with trend, plus schedule, budget, scope and resources
3. Three to five key metrics against plan
4. Done, and the next milestones with dates
5. Risks and issues, each with owner, impact and status
6. Decisions needed (or "for information only")

**Product or service pitch** (Raskin strategic narrative)
1. Name a big change in the world
2. Winners and losers: who adapts and who doesn't
3. The promised land: the outcome worth reaching
4. Capabilities framed as what gets you there
5. Evidence: proof it works for people like them
6. The ask

**Consulting-style proposal**
1. Executive summary
2. Situation
3. Complication, including the cost of doing nothing
4. Objectives and proposed solution
5. Approach: deliverables, scope, timeline, team, governance, risks
6. Investment
7. Why us
8. Next steps

**Vision / strategy** (Duarte Sparkline)
- Alternate between what is and what could be, build to one memorable moment, close with a call to action and a picture of the better future.

**Case study**
1. Challenge
2. Objectives
3. Approach
4. Process artefacts
5. Measured outcomes
6. What's next

---

## Reference: framework cheat sheet

| Framework | Origin | Use it to check |
|---|---|---|
| BLUF (Bottom Line Up Front) | US Army writing standard | Is the key point first? |
| Pyramid Principle + MECE | Barbara Minto, McKinsey | Answer first, grouped support, no overlaps or gaps |
| SCQA / SCR | Minto; SCR is the consulting short form | Does the opening create a reason to care? |
| Action titles, horizontal and vertical logic | Consulting practice built on Minto | Do titles alone tell the story, and does each slide prove its title? |
| Ghost deck | Consulting practice | Was the story written before the slides? |
| Assertion-evidence | Michael Alley, Penn State | Sentence headline plus visual evidence, not bullets |
| Storytelling with Data | Cole Nussbaumer Knaflic | Big Idea, 3-minute story, decluttered charts |
| DataStory | Nancy Duarte | Point of view, three acts, risk of inaction, human hero |
| Sparkline (Resonate) | Nancy Duarte | What is vs what could be, STAR moment, call to action |
| ABT (And, But, Therefore) | Randy Olson | Does the story fit one sentence with real tension? |
| What? So what? Now what? | Borton; Rolfe et al. | Does every insight lead to an action? |
| Monroe's Motivated Sequence | Alan Monroe | Attention, need, satisfaction, visualisation, action |
| Strategic narrative | Andy Raskin | Does a pitch open with the change in the world, not the company? |
| Made to Stick (SUCCESs) | Chip and Dan Heath | Simple, unexpected, concrete, credible, emotional, stories |
| Say It With Charts | Gene Zelazny, McKinsey | Is the chart right for the comparison? |
| Six-page narrative memo | Amazon | Should this be a memo instead of a deck? |
| Prewiring, elevator test | Ethan Rasiel, The McKinsey Way | Have key people seen it first? Can it be said in 30 seconds? |

**Chart choice (Zelazny)**

| Comparison | Question | Typical chart |
|---|---|---|
| Component | What share of the total is each part? | Pie or 100% bar |
| Item | How do things rank? | Horizontal bar |
| Time series | How does it change over time? | Column or line |
| Frequency distribution | How many fall in each range? | Histogram |
| Correlation | Does X relate to Y? | Scatter or paired bars |
| Build-up or breakdown | How does a total add up or leak away? | Waterfall |

**Consulting slide anatomy**
1. Tracker: a small section label so the audience knows where they are
2. Action title: a full-sentence takeaway, 15 words max
3. Optional subtitle: units, scope or period
4. Body: one exhibit that proves the title
5. Optional "so what" callout
6. Source line for every number
7. Page number