# Interview me

Let AI interview you before it answers. This is a Claude skill and two prompts
from the Loyola Marymount University Center for Faculty Development workshop
"Let AI Interview You First," November 6, 2026, by Greg Lontok and Ed Mosteig.

The first thing you type into an AI is a compressed version of your real
problem, bent toward what you think the tool can answer. Answer-first AI
solves that compressed version. This skill makes Claude interview you first,
in five stages: GOAL, EXAMPLE, EXPLORE, REFLECT, NEXT. It asks one question
at a time, ten at most, says back what it heard, and waits for your
correction before it proposes anything.

## Install the skill in Claude

1. Download [interview-me.zip](https://github.com/LMU-ISBA/interview-me/releases/latest/download/interview-me.zip).
2. Open claude.ai and go to Customize > Skills.
3. If you see no Skills section, turn on "Create and edit files" under Settings > Capabilities.
4. Click the plus button, then "Create skill," then "Upload a skill."
5. Choose the zip you downloaded.
6. Turn the skill on in your list.

Start a new chat and say "interview me first," then describe your problem in
a sentence. Say "enough" to skip to the summary. The upload works on every
claude.ai plan, Free included.

If you use Claude Code in a terminal, the skill loads there too once it is on
in claude.ai and you sign in with the same account. To install it by hand
instead, run this:

```
mkdir -p ~/.claude/skills/interview-me && curl -fsSL https://raw.githubusercontent.com/LMU-ISBA/interview-me/main/interview-me/SKILL.md -o ~/.claude/skills/interview-me/SKILL.md
```

## Use the prompt in any other tool

Copilot, Gemini, and ChatGPT have no skill file, so the prompt is the share.
Start a new chat. Paste this, add your problem as the last line, and send both
together. Don't paste student names, grades, accommodation details, or
anything you wouldn't put in an email.

```
Act as my interviewer. Do not propose a solution yet. Work in five stages, in order, and name each as you start it.

GOAL. Ask what I want to accomplish and what success would look like. Stop when you could state my goal in one sentence.

EXAMPLE. Ask me to walk you through the most recent specific time this came up: what happened, what I did, and what I noticed. Stop when you can retell it in three sentences.

EXPLORE. Pick one questioning lens that fits (root cause, Socratic, backward design). Name it in one line. Ask two or three questions through it, evidence before causes. If I have proposed a solution, treat it as a hypothesis and test it.

REFLECT. Summarize under four headings: my goal, what the example showed, what the real problem seems to be, and what you are assuming or unsure about. Ask what you got wrong or missed, and end the message there. Do not start NEXT until I answer.

NEXT. Write a specification under 400 words: problem statement, constraints, evidence of success, two or three options, your recommendation, and one next step with a date. Mark what rests on my evidence and what on your assumptions.

Rules. You have ten questions in total, so spend each on the unknown that would most change your specification. Number them (Q1 of 10) and ask one per message, under 30 words. End the message after it. A leading question contains the answer you expect ("Is it because the reading is too long?"). Ask what happened instead, and let me name the cause. Offer answer choices only for simple facts, never for what happened or why. If I answer with a solution, note it as an idea to test and ask again. Stop early when you could fill all four REFLECT headings without guessing. "Enough" sends you to REFLECT. I make the decisions.

Begin with GOAL now. Do not restate these instructions.
```

If it asks several questions at once, answer the first and type: one at a
time, please. If it starts proposing solutions, type: not yet, back to the
interview.

## Three opinions besides your own

Once you have a specification, or at least a corrected summary, ask for five
people who would see it differently, pick three, and put them to work. You do
the choosing, and the choosing is the thinking. Part one, paste after your
specification or summary:

```
Here is where I have got to on a problem: my corrected summary or my plan, and the direction I am leaning. I wrote it. Propose five people who would see it differently from me. Use roles, not names. Give each a different thing they would protect, such as their time, fairness, evidence, morale, or reputation. For each, in three or four lines: who they are, what they would notice that I have not, what they would get wrong, and which of the other four they would disagree with most. Then stop. I will pick three and say why I dropped two. Do not argue with my choice.
```

Part two, after you have chosen:

```
Answer as each of my three, one at a time, to the same three questions: what is right about this plan, what breaks first, and what one change would you make. Keep each under 120 words and in their own priorities. Where two would agree, say so in the comparison rather than softening one to make room. Then write a comparison under three headings: where all three agree, where they split, and what none of them raised. Stop after the third heading. No conclusion, no recommendation, no next step. Then ask me one question: which change, if any, I want to make to the plan.
```

## What is here

| Path | What it is |
| --- | --- |
| `interview-me/SKILL.md` | The skill: five stages, lenses, question rules, the specification format, and the pressure test |
| `prompts/interview-prompt.md` | The interview prompt, a room version under 2,000 characters and a full version, with notes on the choices |
| `prompts/perspectives-prompt.md` | The five-then-three pressure test, with notes |

## Contact

Greg Lontok, greg@lontok.com. This is a first draft, and we'd like to hear
what changed when you ran it.
