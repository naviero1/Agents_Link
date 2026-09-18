# Beebop to Rocksteady: approved guiding prompts and tokens teaching classification

Date: 18 September 2026.
Instruction: 21.

## Owner authorization and exact scope

Oscar approved the seven revised existing TYPE THIS prompt boxes and said: "ok let's improve this prompts as you suggest. And give the last set of instructions to rocksteady, dont change anything else, also make the tokens slide not a reference but a teaching slide".

Implement the exact wording below in the current presentation on branch `claude/training-course-polish-oxohwj` in `naviero1/Claude-Works`.

This releases instruction 19's hold only for these seven approved prompt sets. Instruction 20 was withdrawn and deleted; do not use its broad activity-selection approach. The current pass has exactly two changes:
1. Replace the existing seven numbered TYPE THIS prompt sets with the approved wording below. If one disappeared in an earlier edition, restore its revised counterpart only to the same corresponding topic slide.
2. Reclassify the existing tokens slide from REFERENCE to TEACH.

Keep each prompt on its corresponding topic slide. These are seven original prompt boxes, some with multiple sends, not a prompt for every slide. Match using the topic and original prompt number; old slide-number maps may lag the current deck. This work stays within the agreed Parts 1–4 scope. Detailed agentic-prompting content after the exercises remains for another session and is not edited in this pass.

Do not bundle earlier visual assignments or other pending improvements into this pass. Preserve other slide text, titles, order, slide count, classifications, illustrations, layouts, speaker notes, exercises, and later-session material. Do not add scoring tables, discussion questions, activities, images, or new prompt boxes elsewhere. If nearby existing wording conflicts with an approved prompt, report the specific conflict in the handoff instead of rewriting that surrounding content.

## Approved exact prompt text

Keep the existing grouping and separate sends. The following is the final wording Oscar reviewed and approved.

### Existing prompt 1/7: course log and farewell message

Send 1:

> Use this chat as my course log. When I request a report, use only the conversation available to you and flag any gaps. Acknowledge briefly.

Send 2:

> Write a farewell message for a coworker in about 50 words.

Send 3:

> Before revising, ask up to three questions that would most improve the message. Wait for my answers, then revise it.

### Existing prompt 2/7: narrowing guesses with context

Send 1:

> Finish this sentence five different ways: “We should review the launch date because…” Treat each ending as a hypothetical possibility.

Send 2:

> Repeat using these facts: we are a business-to-business software company; our beta ends April 20; a competitor launches May 3. Separate supplied facts from assumptions. End with one missing fact that could change the timing decision.

### Existing prompt 3/7: tokens

> Explain tokens to a new colleague using a LEGO-brick analogy, in about 100 words. Show an illustrative word split and explain why the actual split depends on the tokenizer. Connect token counts to context limits and charges when billing is based on tokens. End with one practical implication for working with long documents.

### Existing prompt 4/7: context window and handoff

Send 1:

> Explain a context window using a desk analogy, in about 100 words. What occupies the desk, and what happens as it fills? Distinguish information available for the current response from saved chat history and optional memory. Identify what depends on the application. End with one useful habit for continuing a long task.

Existing handoff follow-up:

> Create a concise HANDOFF from the conversation currently available: goal, decisions, constraints, unresolved questions, and next action. Name any files needed to continue. Mark missing information rather than inventing it.

### Existing prompt 5/7: fast responses versus more reasoning

> Explain when to start with fast responses versus more reasoning, using three examples: a routine email, inconsistent supplier data, and a problem with several interacting causes. For each, give a starting choice and what would justify increasing effort. Explain the tradeoff in time and resource use without guessing prices. About 120 words.

### Existing prompt 6/7: feature menu

> Using the supplied screenshot or copied text of my app’s menu, explain each visible mode in one line: its purpose and a suitable workplace task. Mark anything the supplied information does not establish as needing verification. If the menu is missing, ask for it first.

### Existing prompt 7/7: Mixture of Experts

> Explain Mixture of Experts using a specialist-hospital analogy, in about 120 words. Describe how selected computational components handle each token and how activating only a subset can reduce computation. Explain one way the hospital analogy can mislead, and why lower computation alone does not determine customer prices.

## Tokens slide: teaching status

The tokens topic is the existing "Tokens and practical limits" slide, current reviewed position 8, stable identity `sid-263`. Confirm by topic and identity before editing.

Change its classification from REFERENCE to TEACH. Apply the presentation's established teaching-slide label and color treatment, and update the corresponding authoritative classification/source entry so the change survives regeneration. Keep the slide in place and preserve its other content and visuals apart from the approved prompt replacement. Leave every other slide's classification unchanged. Do not add a new tokens slide or alter timing.

## Implementation and delivery

Make the smallest direct edits needed to the current presentation and its authoritative source. Preserve prompt readability and the existing font sizes. A local adjustment inside an affected prompt area is allowed only as needed to fit the approved text without covering or moving unrelated content. If it cannot fit, report that specific slide and layout constraint instead of shortening the approved wording or redesigning the slide.

Keep unrelated workbook, document, exercise and reference content unchanged. Do not run a broad regeneration that resets owner-approved work. If the existing workflow maintains an identical active pilot and deliverable, keep that same-version pair consistent using the established workflow.

Validate the seven prompt sets against the exact text above, check affected slides visually for clipping or overlap, and verify that the only classification change is tokens: REFERENCE to TEACH. Confirm slide count and order are unchanged. Deliver the revised presentation for Oscar's review with a concise list of affected slides and any actual unresolved fit or surrounding-text conflict. No further wording-selection approval is needed: Oscar has approved this wording and the tokens classification change.

Beebop is posting this limited implementation instruction. The presentation changes themselves are Rocksteady's implementation work.
