# DESIGN.md — Lucky Streak?

**ID:** 24B0387 · **P3** Multi-agent collaborative learning · **T6** Probability: is a "lucky streak" real? (Cl. 9–10) · **L5** Anxious repeat learner · **C4** 10-minute sessions

## D1 · Problem
Students can use *P = favourable/total*, yet still believe a streak changes the next toss: "tails is due" (**gambler's fallacy**) or "she's winning, so she'll surely win again" (**hot hand**). Textbooks never test this belief, and an anxious learner who failed once avoids the topic. In this app, three AI agents disagree about a streak; the learner settles it with coin-toss evidence, all in one calm 10-minute session.

**Scope:** the claim is tested for **independent tosses of a fair coin (or die)**. Real-world streaks such as a batsman in form can involve changing skill or conditions; that is a different question, and the app says so.

**Learning outcomes**
- **LO1:** *Predict* that P(heads) after any streak is still 1/2, and *explain* this with independence.
- **LO2:** *Compute* a sequence's probability by multiplying, and *compare* sequences (each exact sequence of 4 tosses = 1/16).
- **LO3:** *Use* simulation evidence, including sample variation, to *judge* conflicting claims.

**Context:** at home in the evening, on her own Android phone; 10 minutes, possibly interrupted.

## D2 · Persona
**Kavya Deshmukh, 15, Class 10, Pune (Maharashtra State Board, English medium; Marathi at home).** Father runs a small hardware shop; mother is a homemaker. She goes to group tuition three evenings a week.

- **History:** scored 9/25 in the probability unit test and must re-sit it. Her teacher returned the paper in front of the class. Since then she says "I'm just bad at maths".
- **Learning gaps:**
  - **Knows:** fractions, %, and P = favourable/total for a single coin or die.
  - **Gap 1:** has never met *independence*; thinks of past results as "affecting" the next one.
  - **Gap 2:** adds probabilities instead of multiplying (says P(HH) = 1/2 + 1/2, or "1/3 because there are 3 outcomes: HH, HT, TT").
  - **Gap 3:** has never seen data vary; one surprising result convinces her.
- **Misconceptions:**
  - **M1, gambler's fallacy:** "After a run of heads, tails is due." This comes from cricket tosses ("we'll win it this time").
  - **M2, hot hand:** "A winning streak guarantees, or makes more likely, another win." This comes from the idea that a player "in form" will keep winning.
- **When confused:** she doesn't ask. She guesses the first option that "sounds right", or freezes and closes the app. She re-reads long text without taking it in, and copies a classmate's answer instead of trying.
- **Anxiety triggers:**
  - red crosses and "Wrong!";
  - visible countdown timers;
  - being compared with others;
  - a wall of formulas;
  - being asked to explain out loud in front of people.
- **Confidence issues:**
  - She under-rates herself even when she is right ("I was just guessing").
  - When a guess happens to be right she becomes over-sure, then crashes on the next question.
  - Once she has decided she is "bad at it" she stops trying.
- **Preferred learning style:**
  - learns by *seeing it happen* and short worked examples;
  - prefers everyday Indian contexts (cricket toss, Ludo, the mela);
  - short sentences, one idea at a time;
  - private practice, where nobody watches her mistakes;
  - likes being *asked her opinion* rather than told.
- **Device / time:** her own low-cost Android phone (shared data pack); about 10 minutes after tuition, often interrupted by family.
- **Motivation:** pass the re-sit without embarrassment; she wants to feel in control.

**How each trait shapes the app**
| Kavya's trait | App feature |
|---|---|
| Gap 1: no idea of independence | The Challenger voices her belief; she tests it in the coin lab; the Teacher's explanation is "the coin has no memory" |
| Gap 2: adds instead of multiplying, the "3 outcomes" error | Numeric task with targeted feedback for 1/2 and for 1/3, plus a hint to list HH, HT, TH, TT |
| Gap 3: trusts a single result | Repeated lab batches, a 50% theory line and a "normal range" band that shows how small samples jump around |
| M1 or M2 | The **explicit diagnosis** picks a different explanation, example, follow-up question and hints for each |
| Guesses or freezes when confused | **Adaptive hints:** a one-tap hint tailored to her diagnosis; 2 tries, then a model answer, so she is never stuck |
| Doesn't ask for help | Agents step in on their own: after a wrong lab verdict the Evaluator nudges; after a second, the Teacher walks her through it |
| Triggers: red crosses, "Wrong!", comparison | **Supportive feedback:** "Not yet", "very common idea", no red, no ranking, nothing graded; feedback quotes her *own* lab data |
| Trigger: countdown timer | The clock shows time *used* ("m:ss of 10:00"), in calm wording; going over is "fine, finish calmly" |
| Trigger: wall of formulas | One idea per screen; formulas only as 1/2 × 1/2; short sentences |
| Under-confident even when right | One-tap confidence check; "You felt you were guessing, but you reasoned correctly. Trust it" |
| Over-sure after a lucky guess | Calibration message in the summary when confidence > post-test result |
| Likes being asked, not told | **Agent interaction:** she is the judge of the Teacher vs Challenger disagreement, not a listener |
| Anxious in front of others | Private, single-learner app; the Challenger is told to "keep it gentle" when she says she is worried |
| "Bad at maths" self-image | **Assessment:** the pre-test has no feedback, then the summary shows her own pre → post gain on matched items |
| Interrupted by family | Pause & save on every screen; "Welcome back, continue from Stage N" |
| Low-cost phone, limited data | Phone-first layout, large tap targets, no images or video, works offline except the optional AI check |

## D3 · Content: six timed stages = exactly 10:00
Welcome, Pause, About and Summary are **supporting screens and are not timed**.

| # | Stage | Budget | What happens |
|---|---|---|---|
| 1 | Check-in + pre-test | 1:30 | Feeling (worried / unsure / okay), then 3 items with no feedback (scenario A) |
| 2 | Agents disagree | 1:30 | Challenger vs Teacher on the learner's own pre-test answer; the Evaluator hands the decision to the learner |
| 3 | Coin lab | 2:00 | Repeated batches; P(H right after HHH) vs the theoretical 50%; variation range; the learner's verdict |
| 4 | Diagnosis + practice | 2:30 | The explicit diagnosis selects the explanation, example, follow-up and hints; then 3 tasks |
| 5 | Post-test | 1:30 | 3 items in **new scenarios** (scenario B), mirroring the pre-test |
| 6 | Reflect | 1:00 | Confidence, then a personalised summary showing pre → post |
| | **Total** | **10:00** | |

**Pre-test (scenario A)** vs **post-test (scenario B)**, matched item by item:
| Probes | Pre-test | Post-test |
|---|---|---|
| M1 / M2 diagnosis | Riya's coin: 5 heads, so P(next H)? | A Ludo die: three 6s, so P(next 6)? |
| M2 "guarantee" / M1 "luck turns" | Arjun lost the toss 4 times, so P(he wins next)? | Sana won the toss 4 matches in a row and the coach says she's guaranteed to win the next, so P? |
| LO2 sequences | HHHH vs HTTH (4 tosses)? | TTTTTT vs TTHTHH (6 tosses)? |

**Diagnosis → different explanation, example, follow-up and hints**
| | M1: gambler's fallacy | M2: hot hand | None |
|---|---|---|---|
| Explanation | The coin doesn't keep score or "owe" tails; the share of heads nears 50% by *dilution*, not payback | A win never makes the next more likely, and a streak never guarantees one | Independence transfers to any memoryless device |
| Example | 5 extra heads in 1,000 tosses = 0.5%; a captain who lost 5 tosses still has 1/2 | Your lab: heads after HHH was about 50% | A die has no memory: still 1/6 |
| Follow-up | 8 heads, then how many tails expected in the next 2? → **1** | Priya won 3 tosses, "sure to win the 4th"? → **1/2** | A die after three 6s? → **1/6** |

**Practice** (hint, 2 tries, then the model answer):
1. The tailored follow-up (above).
2. **Numeric:** P(HH)? → **1/4**. Feedback for 1/2 ("multiply") and for 1/3 ("there are 4 outcomes").
3. **Explain (free text, AI-checked):** "I lost 5 times, so my luck must turn."
   - **Model answer:** "Each toss is independent; still 1/2."
   - **Rubric (0–2):** 1 point for independence, 1 point for 1/2; 0 if it endorses "due" or "luck".

**Coin lab:** the learner runs repeated batches (10 / 100 / 1000). Every time **HHH occurs**, the app records the next toss.
- **Shown per batch and in total:** P(H | after HHH), compared with the **theoretical 50%**.
- **Normal range for chance variation:** 50% ± 98/√n percentage points (n = number of HHH occurrences, roughly 95%).
- **The message:** small batches jump around; more data settles near 50%; a gap inside the range is just chance.
- **Also shown:** streaks are normal. P(a run of 5+ heads in 100 tosses) ≈ 81%, computed exactly.

## Agents (P3): collaboration through shared notes
The agents share one **notes board**: feeling, diagnosis, lab result, wrong verdicts and hints used. Each reads it before speaking, and every influenced message shows **"↳ using X's note"**:
1. **Teacher → Challenger** "anxious learner": the Challenger uses a gentle version of the challenge.
2. **Evaluator → Teacher** diagnosis: chooses the explanation, example, follow-up question and hints.
3. **Evaluator → Teacher** lab result: practice feedback quotes the learner's *own* lab percentage.
4. **Evaluator → Challenger** verdict and evidence: the Challenger concedes using the learner's data.
5. **Challenger → Evaluator** concession: the summary records the resolved disagreement.

**Disagreement → decision → resolution:**
1. The Challenger argues the learner's pre-test idea (labelled "Challenge: I might be wrong").
2. The Teacher disagrees.
3. The Evaluator: "Don't pick the louder voice; test it."
4. The learner runs the lab and **chooses** who the evidence supports.
5. A wrong verdict gets a nudge to look at the number, not the answer; a second gets a worked explanation.
6. The losing agent concedes, citing the data.

## D4 · App
- **Stack:** Vite + React + TypeScript (Vite starter template, no UI library); a Vercel function `/api/agent`; `localStorage` for saving.
- **C4, visible in the app:**
  - a clock "m:ss of 10:00" counting active time in stages 1–6 only;
  - stage chips with budgets;
  - **Pause & save** and "Welcome back, continue from Stage N";
  - the summary shows "completed in m:ss of 10:00".
- **ID 24B0387** appears in every footer and on the About screen.

## D6 · AI
- **What it does:** the Evaluator scores practice Task 3 using an LLM via `/api/agent`. It receives the question, rubric, M1/M2 definitions and the answer, and returns JSON `{score, misconception, feedback}`.
- **Checks before display:**
  - schema and enum values;
  - a length limit;
  - banned claims (e.g. "is due");
  - a cross-check with the rule-based rubric.
- **Fallback:** a labelled rule-based Evaluator.
- **Maths and dialogue:** the maths is computed in code; the dialogue is scripted and personalised from the notes board.

## D7 · Rationale
- **Cognitive conflict leads to conceptual change:** the learner's own idea is voiced by the Challenger and tested with evidence.
- **Inquiry with sampling variation:** the learner produces the evidence and learns to read it.
- **Scaffolding (ZPD):** a diagnosis-specific hint → 2 tries → model answer.
- **Cognitive Load Theory:** one idea per screen, short sentences.
- **Anxiety (affective filter):**
  - "not yet" instead of red crosses;
  - mistakes called "very common";
  - no countdown pressure; nothing graded;
  - calibration feedback that builds self-efficacy.
- **C4:** a fixed 6-stage micro-lesson of exactly 10:00, with pause and resume.

## D8 · Evaluation
| Outcome | Evidence | Success |
|---|---|---|
| LO1 | Post-test items 1–2 + follow-up | Post-test items 1–2 correct |
| LO2 | Practice numeric + post-test item 3 | Both correct |
| LO3 | Lab verdict + explanation (0–2) | Correct verdict and a score ≥ 1 |
| Conceptual gain | Pre-test vs post-test (0–3 each, matched items) | Post > pre, or both 3/3; M1/M2 answers disappear |
| Confidence | Before vs after | Rises, and matches the post-test |
| C4 | Active time | ≥ 80% finish in ≤ 10:00 |

**Logged (exportable JSON):** pre- and post-test answers; each answer with attempts, hints and misconception tag; confidence; lab batches; verdicts; notes-board changes; time per stage; pauses; agent messages.
