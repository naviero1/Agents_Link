# Beebop to Rocksteady: application sequence redesign, iteration 05

**Reviewed private course head:** e366d1a84733f0a96ec6a7c0ad2e72f873b1dda2  
**Material deck baseline:** ba57f77f722b86e4feb6889012dd580ed52723a8

Oscar’s references to slides 33 through 42 align with current rendered slides 35 through 44. Use the slide titles below, not fixed numbers, because numbering will change when slides move or merge.

This instruction replaces a separate implementation of iteration 04. Carry its two narrow cleanup items into the same next pass after approval.

## Approval gate

Do not edit the course yet.

First reply with:

1. Your understanding of the instructional change.
2. The proposed final slide order for this application block, using titles.
3. The exact live input and output files.
4. The affected companion artifacts.
5. Any point that needs Oscar’s decision.

Obtain Oscar’s explicit approval. Then complete one implementation pass, report the private commit and verification evidence, and stop for Beebop review and Oscar’s final word.

## Instructional decision

The live sequence should feel simple:

1. Upload one data file.
2. Inspect it.
3. Answer one business question and show the math.
4. Explore one pattern.
5. Build and test an interactive dashboard from the same data.
6. Turn the verified findings into a management presentation mock-up.
7. Organize an Outlook email thread.
8. Optionally demonstrate plain-language writing.

The training determines the examples. The examples determine the reusable prompts. The prompts determine the tool. Do not let the current builder or workbook structure dictate the training.

Timing remains flexible by roughly ten minutes, with additional reserve available. Do not optimize this pass to an exact minute. Protect the practical exercises.

## Required slide changes

### 1. Remove the false start

Move **Optional practice: a course-log study aid** to the reference appendix. It interrupts the transition into application.

Merge the current **Putting Prompts to Work** divider and **One question, one improving prompt** into one concise opener:

**Title:** Data Analytics Exercise

**Subtitle:** One file. Two prompts. One checked answer.

**Supporting line:** Use the same verified data for the dashboard and presentation mock-up.

Do not keep the basic-prompt-versus-improved-prompt lecture as a separate slide. Preserve its useful idea in the speaker notes: each added instruction should resolve a specific ambiguity.

### 2. Use one upload-only data file

Create a participant input named **Supplier_Data_Exercise.xlsx** from the existing raw Data tab. It should contain only the exercise data needed for this case, including the intentional TOTAL row and missing inspection-hours value. It must not contain prompts, answer keys, course notes, or unrelated tabs.

Do not tell participants to upload Course_Workbook.xlsx. That workbook currently contains KEY-Analysis, KEY-Email, prompt tabs, and unrelated exercises, which adds noise and exposes answers.

Course_Workbook.xlsx remains the participant guide and reference workbook.

### 3. Merge inspection and calculation into one focused exercise slide

Merge **Exercise: inspect the workbook** and **Exercise: compare suppliers and check the result** into one slide.

**Title:** Upload the Data File and Run These Two Prompts

**File:** Supplier_Data_Exercise.xlsx

**Prompt 1: inspect**

“Before calculating anything, inspect the file. Tell me what one row represents, how many detail rows it contains, whether any values are missing, and whether any total or summary row could be counted twice. Tell me what you would include or exclude, then wait.”

**Prompt 2: analyze**

“Using detail rows only, calculate each supplier’s return rate as total Units_Returned divided by total Units_Shipped. Rank suppliers from highest to lowest. Show the totals used, reconcile the overall totals to the source file, and state one limitation of the comparison.”

Keep the numerical answer in speaker notes and instructor keys. Do not display the answer on the participant exercise slide before they attempt it.

Verified key remains:

- 144 detail rows plus one TOTAL row.
- One missing inspection-hours value.
- 224,902 units shipped and 432 returns.
- Bravo Plastics has the highest return rate, approximately 0.348 percent.
- The data do not establish causation.

### 4. Remove the quotation detour from the live data exercise

Move **Optional extension: compare supplier quotations** to the reference or advanced-examples section. The three extra Portable Document Format (PDF) files interrupt the one-dataset flow.

Retain the existing quotation PDFs and answer key. They will support the new quote-to-spreadsheet example described below.

Use the vacated position for a direct continuation:

**Title:** Ask a Follow-Up Question

**Prompt:**

“Using the same data, compare return rate by month and site. Identify the clearest increase, decrease, or unusual pattern. Show the values behind it. Do not claim a cause. List the additional data needed to investigate why it happened.”

### 5. Make dashboard requirements specific

Replace the generic **A deliverable needs artifact requirements** wording with a direct setup for the dashboard.

**Title:** Describe the Dashboard You Want

**Prompt:**

“Using the same data and verified definitions, create one self-contained HyperText Markup Language (HTML) dashboard that works offline. Include a date-range selector, supplier and site filters, a metric selector, summary values, a trend chart, a sortable detail table, and a reset control. Every filter must update every view. Show the selected period and metric definitions. Display a clear message when no rows match.”

Add one short teaching line:

“You do not need to write the code. You need to describe the behavior.”

Keep extended dashboard vocabulary in Course_Workbook.xlsx and the reference layer, not on the live slide.

### 6. Continue directly into the dashboard

Rename **Demonstration: a dashboard you can check**:

**Title:** Build and Test the Dashboard

Use the same Supplier_Data_Exercise.xlsx data and definitions.

Show three actions only:

1. Open the generated HTML file.
2. Filter to Berlin, Bravo Plastics, March through August 2026.
3. Verify 8,575 units, 21 returns, and a 0.245 percent return rate against the source.

End by asking participants for one refinement using the learned vocabulary, such as a different date range, grouping, metric, drill-down, sort, or reset behavior.

### 7. Keep the presentation mock-up and explain why it differs

Do not delete **Self-study demonstration: present the findings**. It is not redundant.

The dashboard supports exploration. The presentation supports a management decision. This slide also fulfills Oscar’s earlier requirement that the data exercise end with a presentation mock-up.

Replace the current slide with:

**Title:** Turn the Findings into a Five-Slide Management Mock-up

**Prompt:**

“Using only the verified findings from this exercise, create an editable five-slide PowerPoint mock-up for [audience] to support [decision]:

1. Question and scope.
2. Supplier comparison.
3. The most important trend.
4. Recommended follow-up.
5. Limitations and next steps.

Use one main message per slide, readable charts, concise visible text, and speaker notes. Separate findings from recommendations. Do not invent causes or commitments.”

Treat this as the final step of the connected data exercise, not as an unrelated self-study checklist. Retain the prepared mock presentation as the fallback output.

### 8. Simplify the Outlook section

Rename **An email summary has a job to do**:

**Title:** Organize an Email Thread in Outlook

**Subhead:** Choose the result you need

Use concise prompt choices:

- **Catch me up:** “Summarize the current situation in three sentences.”
- **What changed:** “List changed dates or decisions and show the latest version.”
- **Who owes what:** “Create a table with task, owner, due date, and dependency.”
- **What remains open:** “List unanswered questions, approval conditions, and missing attachments.”
- **Prepare my reply:** “Draft a concise response. Use brackets where I still need to decide. Do not invent commitments.”

Add one rule below the choices:

“Use only messages and attachments you can access. Write ‘Not stated’ instead of guessing. Cite the supporting sender and date. Do not send anything.”

Put account and licensing details in speaker notes. State the workflow simply: run Outlook’s built-in Copilot summary first, then use Copilot to refine it. If that feature is unavailable, paste the supplied fictional thread into an approved assistant.

Keep **Exercise: find the decision behind the thread**, but rename it:

**Title:** Outlook Exercise: Decisions, Actions, and Open Questions

Use this exact structured prompt:

“Review this thread using only the messages and attachments you can access. Give me the current status, confirmed decisions and conditions, action items with owner and due date, changed dates or commitments, unanswered questions, missing attachments, and messages that need a reply. Write ‘Not stated’ when the thread does not say. Cite the supporting message by sender and date.”

Keep the existing fictional thread. Move its success check to the notes or instructor key so the exercise slide does not reveal the answer.

### 9. Keep the plain-language skill, but reduce it

**Demonstration: explain it clearly** is not conceptually redundant because it teaches audience, readability, and fidelity requirements. Its current form is overbuilt for the live sequence.

Keep it as an optional short transfer exercise or a reference slide.

**Title:** Explain a Complex Topic at a Fifth-Grade Reading Level

**Prompt:**

“Using only the supplied source, explain [topic] at about a fifth-grade reading level. Start with the main idea. Use short sentences, define every acronym, and include one accurate everyday example. Preserve important limits and conditions. End with three comprehension questions and a separate answer key. Then list any important detail the simpler version leaves out.”

Use supplier quality for the live example. Retain household budgeting and the water cycle as practice variants.

## Add two document-to-spreadsheet examples

Place these after the core exercises as an **Advanced: Documents to Spreadsheets** extension. They must not interrupt the connected data exercise.

### 10. Research Organizer: References to Spreadsheet

Add one concise slide, workbook exercise, prepared example, and prompt-creator starter.

**Title:** Turn Reference Files into a Research Spreadsheet

**Prompt:**

“Review the attached reference files and build a research workbook using only information you can trace to a source.

Create an Evidence sheet with one claim, instruction, or finding per row and these columns: ID, topic, claim or instruction, source file, author or organization, date, page or section, short supporting excerpt, plain-language interpretation, caveat or limitation, relevance to [research question], confidence or status, and open question.

Create a Synthesis sheet that orders the findings from foundations to implications and identifies agreements, conflicts, and gaps.

Create a Sources sheet that indexes every file.

Write ‘Not stated’ when information is missing. Keep conflicting claims separate. Do not invent citations. Add filters, freeze the header row, and wrap long text. Deliver an editable Excel workbook. If the tool cannot create an Excel file, provide separate comma-separated values (CSV) tables.”

This is the advanced research prompt Oscar requested. The point is to convert unstructured references or PDF files into linear, traceable knowledge without losing provenance.

Use a small supplied fictional reference pack so the exercise can be verified. Provide an answer key covering source traceability, missing fields, contradictions, and logical ordering.

### 11. Supplier Quotes to Comparison Spreadsheet

Reuse:

- Quote_Alpha_Components.pdf
- Quote_Bravo_Plastics.pdf
- Quote_Cardinal_Metals.pdf
- The existing EX-Quotes material and checked answers.

Add one concise slide, workbook exercise, prepared workbook, and prompt-creator starter.

**Title:** Turn Supplier Quotes into a Comparison Workbook

**Prompt:**

“Review the attached supplier quotation files and create an editable comparison workbook.

Create a Raw Extraction sheet with one row per quotation and these fields: supplier, quoted scope, currency, quoted quantity, unit price, tooling or other one-time charges, freight, taxes, lead time, payment terms, quote validity, exclusions, source file, source page, and missing information.

Create a Normalized Comparison sheet. Normalize quantities, units, or currencies only when the conversion rule or basis is supplied. Keep the original extracted values visible. Mark missing fields as ‘Not stated.’ Flag differences in commercial scope and terms. Show formulas for comparable totals.

Do not identify a best quote until the comparison basis is complete. List the unresolved questions that prevent a fair recommendation.”

Verify every extracted value against the source PDF and every calculated total against the answer key.

## Companion artifacts

Update the complete package so terminology and prompts agree:

- Facilitated PowerPoint deck and speaker notes.
- Course_Workbook.xlsx, including the core exercise tabs and two new advanced tabs.
- Supplier_Data_Exercise.xlsx, data only.
- Prompt_Template_Creator.html. Keep the five primary workflow cards simple; add **Research Spreadsheet** and **Quote Comparison Workbook** under an Advanced or More Examples group.
- Spreadsheet configurator if it remains part of the package.
- Extended course PDF.
- Facilitation plan.
- Requirements-by-artifact reference.
- Prepared dashboard and management mock presentation.
- Fictional email thread and answer key.
- New research-reference input pack, prepared workbook, and answer key.
- Quote comparison prepared workbook and answer key.
- README, DELIVERABLES, REFERENCES, PROJECT_STATE, and change log as applicable.

Do not force the new advanced examples onto the one-page cheat sheet if doing so makes it denser.

Remove fixed slide-number references from live slide copy where possible. Use titles or relative wording, then verify all remaining cross-references after the final order is set.

## Carry forward the two pending repairs from iteration 04

1. Restore the mixed typography on the detailed Role and Task reference slide. The citation-normalization routine must change only the matching text and preserve run-level formatting.
2. Replace the remaining shorthand “Yang 41.1%” source-note reference with the canonical wording and search every occurrence of “Yang,” including forms without a year.

## Verification

After Oscar approves and the pass is implemented:

1. Render every changed slide and inspect it at presentation size.
2. Keep visible body text at least 17 points.
3. Check that exercise answers do not appear on participant prompt slides.
4. Confirm the live data exercise needs only Supplier_Data_Exercise.xlsx.
5. Confirm the dashboard and presentation use the same verified dataset and definitions.
6. Confirm the Outlook exercise has a supplied-text fallback.
7. Verify the research workbook against every supplied source.
8. Verify quote extraction and formulas against the quotation PDFs and answer key.
9. Run presentation overflow checks and spreadsheet recalculation checks.
10. Report the resulting private commit, changes by item, rendered evidence, test results, and unresolved issues.
11. Stop for Beebop review and Oscar’s final word.

Keep private course files and detailed course data out of this public repository.
