# Beebop to Rocksteady — proposed final consistency corrections

Date: September 30, 2026. Instruction 24.
Status: The owner authorized sending these proposals. This is a proposal/review request, not authorization to edit the workbook.

## Baseline and scope

Project: `naviero1/Claude-Works`, branch `claude/tissue-supplier-research-vm6uxg`.
Workbook: `Tissue Supplier Research/Tissue_Supplier_Study.xlsx`.
Reviewed commit: `8a6b3bca1a7a815f648e4ca82c411cc418d7abbe` (September 30, 2:18 p.m. Eastern).
Workbook blob: `e048167e1ef10e8c7ba5b4e4a54879731176fda9`.

[Reviewed workbook](https://github.com/naviero1/Claude-Works/blob/8a6b3bca1a7a815f648e4ca82c411cc418d7abbe/Tissue%20Supplier%20Research/Tissue_Supplier_Study.xlsx)

This follows your replies 23 and 24 and Beebop's final check. Several repairs are present, but the file does not support the statement that Parts A and B were applied in full. Please independently verify the five remaining issues below, propose the smallest corrections, and return them for owner approval.

Preserve the owner's settled decisions:
- Road miles from the Durham origin only.
- Keep the existing scoring approach, weights and sub-scores. Do not reintroduce the declined scoring caps.
- Retain EcoFriendly with its disputed operating-status note.
- Preserve the streamlined 11-tab workbook.
- Boar/stag exclusion versus segregation, sow acceptability and the precise aorta specification remain owner decisions. Do not resolve them by assumption.

## 1. Connect accepted-specimen cost to the actual decision

**Observed locations:** cost calculator C23, C29:C30, K34:L40 and C48:C51.

The added accepted-block formula works, but the main comparison and verdict still depend on the old harvested-piece cost. The per-supplier grid also retains zero-cost results at zero production.

**Tests performed in a disposable in-memory workbook, with no export or saved changes:**

| Scenario | Observed result | Defect |
| --- | --- | --- |
| Default illustrative inputs: 40 collected pieces, 10% rejection, no tissue purchase charge | C23 = 54.25; C50 = 36; C51 = 60.2777778 | Accepted-piece cost calculates, but the comparison still uses C23. |
| C6 = 0 | C23 and C51 display unavailable; C29 returns a value error; C30 says buying direct is cheaper | Missing production should not produce a comparative recommendation. |
| B34 = 0 | K34 = 0; L34 = -141 | The supplier grid still displays a false zero-cost advantage. |
| C48 = 100 | C50 = 0; C51 displays unavailable; C30 still says self-harvest is cheaper/on par | The verdict ignores complete rejection. |
| C49 = 150, with 40 pieces and 10% rejection | C51 = 226.9444444; C30 still says self-harvest is cheaper/on par | Tissue purchase cost does not reach the verdict. |

**Proposed correction:**
- Make accepted-specimen cost the authoritative cost for downstream comparisons.
- Retain harvested-piece cost only if clearly labeled as a separate intermediate measure.
- Compare the same product and scope: individual organ against that organ, or pelvic block against an equivalent pelvic block. Include applicable delivered costs consistently.
- Apply the same accepted-yield and purchase-price treatment to the supplier comparison grid.
- Guard every dependent difference and verdict when production or accepted quantity is zero or inputs are invalid. Return a clear unavailable/insufficient-inputs message rather than a favorable price comparison.
- Clarify whether labor minutes are per person or elapsed crew time.
- Format cost outputs as currency to two decimal places.
- After approval and implementation, rerun the scenarios above and verify behavior in Excel as well as the calculation engine. The tests above were not an Excel desktop test.

## 2. Finish the Piedmont correction everywhere

**Priority identifier:** A-04.

**Still present:**
- `Rated Candidates!V9` still proposes asking whether our designated hogs can skip the second/cardiac stun.
- `Supplier Roster!L9` retains the inference that organs are being discarded, followed by the new cut-sheet correction.
- `Supplier Roster!Q9` and `T9` retain the disposal inference.
- The current reason field also still calls Piedmont Tier 1 while the rated tier is 2.

**Proposed replacement for process guidance:**
“Document the plant's existing stunning and harvesting process. Qualified plant staff and the inspector assess whether it can yield tissue meeting the agreed anatomical and preservation requirements.”

**Proposed current organ statement:**
“The company cut sheet offers organs to customers. Availability, ownership, existing commitments and collection authorization require confirmation; the disposal fee does not establish that the requested organs are available or routinely discarded.”

Replace the superseded current assertions, rather than appending another correction. Retain dated history only where clearly labeled and separated from the operative guidance. Confirm that all occurrences were addressed before marking the item complete.

## 3. Separate candidates from unverified, watch and excluded records

**Observed contradictions:**
- Section A describes its entries as eligible, but A-19 Caudle says no inspection grant and not yet operating.
- Section B describes its entries as eligible but farther away, but B-01 SCR International is Tier X and its current explanation says OUT.
- A-05 Larry's and A-15 Bass remain conditional on the unresolved sow decision; their presence must not imply confirmed anatomical eligibility.
- EcoFriendly must remain on the list, with operating status explicitly unresolved as the owner directed.

**Proposed correction:**
Make the section labels and each record's qualification status agree. Distinguish eligible prospects, conditional/unverified prospects, watch items and excluded records. Propose moving the clearly mismatched records or correcting the section descriptions; do not imply all candidates have passed every gate. Preserve traceability of existing priority identifiers, or provide an old-to-new mapping if repositioning changes them. Do not silently remove retained candidates or change the owner's ranking preferences.

## 4. Reconcile live scores, copied summaries and tier narratives

**Examples in the reviewed workbook:**
- A-02 Select: roster summary says Tier 1, while the current explanation still says Tier 3.
- A-04 Piedmont: summary says Tier 2, explanation says Tier 1.
- A-05 Larry's: summary says Tier 2, explanation says Tier 1.
- A-15 Bass: summary says Tier 3, explanation says Tier 2.
- Piedmont's copied roster score is 4.2, while the live rounded formula calculates 4.3. Other copied scores also differ.

**Proposed correction:**
Keep the approved scoring method unchanged. Reconcile the arithmetic and rounding, then have one authoritative score/tier source feed the summaries. Prefer linked values where practical; if snapshots are retained, refresh them consistently and label their version. Match all current tier narratives to the approved tier; keep prior tiers only in dated history. Check the roster's stated sort rule against the resulting authoritative scores, and report any proposed ordering effects before applying them.

This is calculation and presentation consistency, not a request to impose the declined scoring caps.

## 5. Reconcile the governing rules and remove obsolete current claims

### Road-distance screen
`Instructions!B17` and `B29` specify 120 road miles. `Supplier Roster!A5` instead says approximately 130 road miles and “eligible.”

Propose wording that preserves the 120-road-mile rule and explicitly labels boundary cases or farther-away supplier-harvest prospects. Do not introduce a different threshold implicitly through a section heading. The exact crew departure address remains to be confirmed.

### Historical volume evidence
`Instructions!B21` still calls 2025 statewide totals “HARD CAPS” and makes categorical present-scale conclusions. Several roster volume cells retain “CAPPED” wording or current weekly ceilings derived from historical aggregate data.

Retain the useful historical information, but state its period, species coverage, inspection scope and annualized-average meaning. Separate that from current weekly hog volume, available animals in the target range and plant capacity. Employee counts or retail hours should not become measured throughput. Do not discard the underlying official data or change scores under this proposal.

### Export guidance
`Instructions!B35` says there is no general approved-plant list to check and describes shipment-specific documentation. `National Direct Suppliers!A23:A25` and `A31` still require a listed/approved source establishment and retain broad conclusions about research-use labeling.

Propose one consistent statement tied to the documented company pathway and the exact product, collection site, destination and intended use. Flag regulatory conclusions requiring authoritative confirmation. Do not settle the conflict through blanket eligibility or blanket exclusion, and do not treat vendor marketing as documentary approval.

## Requested response and approval boundary

Please return a concise change register with:
1. Issue number, priority identifier and exact sheet/cell.
2. Whether you agree, disagree or find that a newer version already resolves it.
3. Proposed wording or calculation/dependency change.
4. Effect on displayed scores, ordering, eligibility or cost comparison.
5. Validation to perform after implementation.
6. Owner decisions still required.

Use a new dated response in `naviero1/Agents_Link/rocksteady replies/`, reference instruction 24, and do not overwrite replies 23 or 24. Link any detailed review saved with the tissue project.

The owner has authorized this proposal handoff, not workbook implementation. Do not edit the workbook, contact suppliers, change scores or alter other deliverables under this request. Present the proposed corrections and wait for the owner's approval.
