# Proposal-Writing Workflow

Turns sales-call notes or transcripts into editable notes and a proposal draft, while keeping commercial approval with the salesperson.

## Problem and intended user

Moving discovery notes into a proposal can lose scope details or turn discussed commercial terms into promises. Salespeople need a draft they can check before sharing.

Account executives and salespeople preparing a proposal after discovery.

## How it works

**Inputs:** Structured call notes, pasted transcript text, TXT, DOCX or text-based PDF. Scans need a separate OCR step that is not configured.

There are two related n8n workflows. The manual version accepts reviewed notes. The transcript version extracts fields with supporting excerpts and opens an editable review form. Reviewed inputs feed AI drafting, validation and a copied seven-slide Google Slides template. A salesperson checks the draft before sharing.

**Outputs:** An editable notes review and a proposal presentation draft for salesperson review.

**Tools:** n8n, OpenAI, Google Drive and Google Slides, with the existing n8n file-extraction tools.

## Decisions behind the design

- Put salesperson review between extracted notes and a proposal draft.
- Keep discussed budgets separate from approved commercial terms.
- Preserve scope exclusions and check what a short summary may leave out.
- Make missing information explicit rather than fill it with a confident guess.

The purpose is a clearer sales handoff, with responsibility for promises staying with the salesperson.

## Commercial value

Organises the handoff from discovery to a proposal draft and keeps approval-sensitive fields explicit. An unapproved discussion does not automatically become approved pricing. Business time savings and conversion impact have not been measured.

## Current status and evidence

Live API integration tests with fictional data are recorded for both manual-notes and transcript inputs. These demonstrate working generation and review paths, not use with paying customers.

A recorded manual-input live test on 21 October 2026 produced seven slides in 12.254 seconds, with no unresolved placeholders. Transcript DOCX and PDF tests also completed through OpenAI and Google. The PDF test kept an unknown email blank and left discussed commercial terms unapproved. The generated manual-test draft was independently fetched from Drive during this portfolio review. Older execution records are no longer present in the queried local database; the dated verification files and surviving output provide the retained evidence.

## Limitations and next steps

AI summaries can omit scope exclusions; compare the deck with the reviewed notes before sharing. Exact excerpts establish that words occur in the transcript, not that the interpretation is correct. OCR, signature and automated delivery are not part of the verified flow. No email was sent in the recorded tests. Next: strengthen scope/exclusion review and test a wider range of transcripts.

## Explore

- [High-level architecture](architecture.md)
- [90-second demo script](demo-script.md)

[Back to portfolio](../README.md)
