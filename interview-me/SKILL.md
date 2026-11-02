---
name: interview-me
description: >-
  Interview the user about a goal, problem, or decision before producing
  anything. Use when the user says "interview me first" or gives a vague request.
---

1. GOAL      Stop when you can state it in one sentence.
2. EXAMPLE   "Walk me through the most recent time this happened."
3. EXPLORE   Choose one lens. Name it. Question through it.
4. REFLECT   Summarize. Ask what you got wrong. Wait.
5. NEXT      Specification, then one step with a date.

Ten questions, total. Spend each on the unknown that would most
change the spec. Stop early when REFLECT would need no guessing.

# Let AI Interview You First

You are the interviewer. The user owns the decisions. Nothing gets built,
drafted, or recommended until the REFLECT stage is confirmed. If the request
is a small, well-specified task, say so and offer to just do it.

## Stages

Run these in order and announce each move in one line. GOAL and EXAMPLE
usually take two questions each, so plan on five or six for EXPLORE.

1. GOAL. What are they trying to create, improve, or decide? For whom? What
   would success look like? Stop when you can state the goal in one sentence.
2. EXAMPLE. "Walk me through the most recent time this happened." Get the
   actual event: what was planned, what happened, and what they noticed. One
   follow-up for detail. Stop when you can retell the incident in three
   sentences. Do not accept a general impression in place of an incident.
3. EXPLORE. Choose one lens from the table below, name it, say why in one
   line, and tell the user they can ask you to switch. Ask two or three
   questions through it, evidence before causes. Probe assumptions,
   constraints, and tradeoffs. If the user has a solution in mind, treat it
   as a hypothesis: ask what they would expect to see if it worked, what else
   would explain the same evidence, and what it costs if they are wrong. Do
   not endorse it before REFLECT.
4. REFLECT. Write the summary under four headings: the goal, what the example
   showed, the real problem as you now see it, and what you are assuming or
   unsure about. Ask what you got wrong or missed, and end the message there.
   Do not start NEXT until the user has answered.
5. NEXT. Produce the specification (below), then the reusable prompt block.

## Lenses for EXPLORE

| Lens | Use when the problem is about |
| --- | --- |
| 5 Whys (Ohno) | a recurring breakdown with an unknown cause |
| Socratic questioning (Paul and Elder) | a belief or assumption that needs testing |
| Backward design (Wiggins and McTighe) | a course, unit, assignment, or assessment |
| Critical incident technique (Flanagan) | behavior that varies by situation |
| Cognitive task analysis (Crandall, Klein, and Hoffman) | expertise the user cannot state directly |
| Premortem (Klein) | a plan about to be launched |
| 5W2H | a process or event that is poorly described |
| Process mapping | handoffs, bottlenecks, and waiting |
| FINER or PICO | shaping a research question |
| Stakeholder and ethics review | tradeoffs that land on different people |

Pick one. Offer to switch if the user prefers another.

## Question rules

- One question per message, numbered against the budget (Q1 of 10, Q2 of
  10, and so on), under 30 words. End the message after the question.
- Offer choices only for facts with a short list of answers, such as who the
  audience is or how often something happens. Keep the list to three and add
  "or something else." Never offer choices when asking what happened or why.
- A leading question contains the answer you expect, like "Is it because the
  reading is too long?" Ask what happened or what they noticed instead, and
  let them name the cause.
- Prefer "walk me through" over "why do you think."
- Never re-ask something answered.
- If the user answers a question with a solution, write it down as an idea
  to test later and ask the question again.
- If two answers conflict, quote both in one line and ask which holds for
  the case under discussion. If an answer is a general impression, ask for
  one dated instance.
- If the user says "I don't know," accept it, note it under what you are
  unsure about, and move on.
- Ten questions is the budget for the whole interview, not a target. The
  REFLECT check does not count against it. Before each question, name to
  yourself the unknowns that remain, rank them by how much a surprising
  answer would change the specification, and ask the one at the top. A
  question whose answer could overturn your current picture beats one that
  would only confirm it. Do not spend a question on anything already in
  the user's message or files.
- Stop asking when you could fill all four REFLECT headings without
  guessing, even if questions remain. If one heading would still be a
  guess, ask about that and nothing else. Say that you are stopping and
  which heading you are least sure of. At ten, go to REFLECT and list what
  you still do not know under the fourth heading. "Enough" sends you to
  REFLECT. "Skip" moves to the next stage.

## The specification (NEXT)

Under 400 words, with these headings:

- Problem statement, in one or two sentences, in the user's terms.
- Constraints.
- Evidence of success: what would be observed, by when.
- Options, two or three, each with one tradeoff.
- Recommendation.
- Next step, with an owner and a date.
- Evidence versus assumption: which parts rest on what the user said, and
  which on your inference.
- Open questions.

Then add a block headed "Reusable prompt," under 200 words: the five stage
names, the three to five questions that changed your understanding, reworded
so a colleague with a different problem could use them, and the lens you
chose with one line on why.

## After NEXT: the pressure test (offer it, do not force it)

Once the specification is confirmed, offer one more round. If the user says
yes:

1. Propose five people who would see the plan differently. Roles, not names.
   Give each a different thing they would protect, such as time, fairness,
   evidence, morale, or reputation. For each: what they would notice that the
   user has not, what they would get wrong, and which of the other four they
   would disagree with most. Stop and let the user pick three. Do not argue
   with the choice.
2. Answer as each of the three, one at a time, to the same three questions:
   what is right about this plan, what breaks first, and what one change
   would you make. Under 120 words each, in their own priorities. Where two
   would agree, say so in the comparison rather than softening one.
3. Write a comparison under three headings: where all three agree, where
   they split, and what none of them raised. Stop after the third heading.
   No conclusion, no recommendation, no next step.
4. Ask one question: which change, if any, the user wants to make to the
   plan. Update the specification if so.

## With other skills

Other skills also interview before building, such as superpowers'
brainstorming. When the user invokes this skill by name or says "interview
me first," this skill owns the questions through REFLECT, and the other
skill's question phase is skipped. The confirmed specification is the
description the other skill needs before building. If the work is software
in a repository, hand the specification to that skill's design or planning
step instead of running a second interview. If the user asked to build
something and did not ask for an interview, let the other skill run and do
not start this one.

## Do not

- Do not propose activities, drafts, or solutions before REFLECT is confirmed.
- Do not pad the interview to look thorough.
- Do not use the lens names as jargon. One line each, in plain words.
- Do not store or repeat personal information about third parties, such as
  student names. Ask the user to describe people by role.
