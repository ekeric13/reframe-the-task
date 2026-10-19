---
name: reframe-the-task
description: Reconsider an approach by identifying the outcome behind a task and comparing better ways to achieve it. Use when the user knows the domain but suspects their current solution, workflow, or requested deliverable may be the wrong approach, or asks to challenge assumptions and explore alternatives. Interview only when missing context could change the recommendation.
disable-model-invocation: true
---

# Reframe the Task

Only use this skill when the user explicitly invokes it; never select it automatically.

Help a knowledgeable user examine whether their current approach is the best route to the outcome they want. Treat their domain knowledge and existing constraints as evidence. Challenge the approach with concrete alternatives, without assuming that a broader assignment is better.

## Choose the mode

- If asked to rewrite a task or prompt, return a self-contained reframed prompt after resolving consequential context gaps. Do not execute it.
- If asked for advice or exploration, produce a recommendation and a concrete next step.
- If asked to execute, investigate and implement the better approach within the existing authorization. Present material expansions of scope as proposals; discovering a broader goal does not authorize pursuing it.
- A bare invocation requests exploration and a recommendation, not permission to implement a materially different solution.

## Understand the outcome

Read the available conversation, artifacts, code, and documentation before asking the user to repeat facts. Establish:

- What outcome the user wants, for whom, and what observable change would indicate success.
- How the current approach is supposed to produce that outcome, and what makes the user question it.
- Which requirements are real constraints and which are inherited choices or assumptions.
- What has already been tried and why it was accepted or rejected, when that history affects the recommendation.

Describe the task in terms of actions and effects. For example, "make a quarterly review deck" may mean "help leadership notice changes and decide where to allocate resources." Treat that interpretation as a hypothesis until supported by context. Do not keep climbing to abstract goals after reaching a useful, actionable outcome.

## Interview selectively

Interview only when an unanswered question could change the choice of approach. If the context is sufficient, proceed directly to alternatives.

- Ask one focused question at a time and wait for the answer. Briefly explain the tradeoff it resolves.
- Offer a tentative recommendation or plausible options when useful, while leaving room for an answer you did not anticipate. Do not anchor questions on an unsupported conclusion.
- Resolve foundational constraints before asking about dependent implementation details.
- Look up discoverable facts yourself. Ask the user about intent, preferences, experience, and decisions the environment cannot establish.
- Stop when you can compare approaches and propose a useful next step. Do not exhaust every branch, require a ceremonial confirmation of shared understanding, or turn a small decision into an interrogation.

When the user prefers no questions, proceed with explicit assumptions where reasonable. Identify any genuinely blocking missing decision instead of inventing an answer.

## Compare approaches

Keep the current approach as a serious candidate. Develop only alternatives with meaningfully different ways of producing the outcome; a simpler intervention or keeping the current approach may be best.

Compare the candidates using the user's actual criteria: expected benefit, supporting evidence, effort, constraints, reversibility, and operational burden where relevant. Explain the mechanism by which each option helps. Distinguish known facts from assumptions and avoid arbitrary scores or invented precision.

Recommend an approach and explain what evidence would change the recommendation. When uncertainty matters, propose the smallest informative experiment or prototype, with an observable success condition, before committing to a larger change. Do not manufacture novelty if the current solution holds up.

## Make the result actionable

Summarize the intended outcome, the key assumption being challenged, the recommended approach and its tradeoff, and the next action. Keep this proportional to the decision rather than imposing a report template.

If rewriting a prompt, include the outcome, relevant context, constraints, selected approach, deliverable, and success criteria so it stands alone. If executing, complete the authorized work and validate against the outcome. Do not stop at a rewritten prompt when execution was requested.

If the approach is already settled and the real need is stronger evidence, precise terminology, or better methods, focus on those improvements instead of forcing a reframe. That is the complementary purpose of `deepen-the-task`; this skill does not require it to be installed.

## Example

A user wants to replace a weekly status meeting with a dashboard. First determine whether the meeting primarily shares information, resolves dependencies, or makes decisions. If that is unclear and consequential, ask about a recent meeting that worked well. Compare the dashboard with a short asynchronous update, a narrower decision meeting, and the current process using the actual purpose and constraints. Recommend a small trial with a concrete outcome measure rather than assuming a dashboard solves the problem.

## Origin

Inspired by the altitude framing in Felix Rieseberg's [How to be more ambitious: A tutorial for humans with models](https://felixrieseberg.com/how-to-be-more-ambitious-a-tutorial-for-humans-with-models/). The selective interview uses the useful principle of one consequential question at a time; it has no dependency on an external interview skill.
