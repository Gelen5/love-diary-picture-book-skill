---
name: love-diary-picture-book
description: Turn a user's supplied chat export and personal photos into a chronological Q-style romantic picture-book PDF, with character consistency and confirmation gates at key stages. Do not build an interactive webpage unless separately requested.
metadata:
  short-description: Create a confirmed, chronological love-story picture book from chats and photos
---

# Love Diary Picture Book

Use this skill when a user wants to turn their own relationship chat history and supplied photos into a keepsake anime/Q-style picture book. The normal deliverable is a printable PDF and its source assets. A web page, flipbook, QR code, or online publishing flow is out of scope unless the user separately asks for it.

## Inputs and boundaries

- Accept user-provided plaintext chat exports, TXT, CSV, JSON, Markdown, screenshots, or manually supplied excerpts. Do not attempt to bypass WeChat security, decrypt protected databases, recover keys, or inspect another person's account.
- Accept photos supplied by the user for the adults and children who will appear. Treat them as private personal data. Do not search for substitute faces or infer identities from outside sources.
- Keep the user's confirmed names, dates, pronouns, relationship labels, and preferred tone. Do not invent a proposal, wedding detail, pregnancy detail, location, emotion, or dialogue that is not supported by the supplied material.
- For a child, use only the supplied child photos and the user's requested age/stage. Avoid adding identifying information beyond what the user asks to print.
- Keep raw chat exports out of generated public packages unless the user explicitly requests them. Use a working copy and retain only selected excerpts in the book source.

## Required confirmation workflow

Do not silently pass a gate. Show the deliverable for that stage and ask for confirmation or corrections.

### Gate 1: Character and visual direction

Create a compact character sheet for each person: face and hair cues from the supplied photos, body proportion, normal expression, clothing palette, and the Q-style illustration direction. Also propose the book ratio, usually portrait 3:4 for a picture book, and a small set of outfit changes so the family is not dressed identically in every scene.

Wait for the user to approve the character sheet before generating story pages. If the user requests changes, revise the character sheet first and preserve the approved traits as the visual anchor.

### Gate 2: Timeline and excerpt selection

Parse the chat into a chronological event table. Separate:

- confirmed milestone dates;
- relationship transitions;
- ordinary but revealing moments;
- conflict and repair;
- pregnancy, birth, and family-life moments;
- uncertain or unreadable items.

Show the proposed timeline with exact dates, selected original excerpts, speaker labels, and the intended page/scene. Prefer retaining meaningful material over aggressive filtering, but remove routine repetition and private content that does not serve the story. Mark anything inferred and ask the user to confirm it. Never silently “correct” a date.

The usual narrative order is first contact → getting closer → dating → love → conflict/repair → engagement → marriage registration → wedding → pregnancy → birth → family life. Change the order only when the user's confirmed dates or story require it.

### Gate 3: Pilot images

Generate three representative pages before the full batch:

1. the opening or first-contact scene;
2. a relationship or conflict scene;
3. a family or milestone scene.

Use the approved characters, vary outfits when appropriate, and leave safe space for text. Confirm the character proportions, facial resemblance, clothing, scene density, and emotional temperature. If any pilot is wrong, fix the shared character/style prompt before generating more pages.

### Gate 4: Layout proof

After the user approves the pilots, generate the remaining illustrations and assemble a proof PDF. The proof must show page numbers, dates, dialogue, captions, and image placement. Ask the user to review the entire proof before exporting the final PDF.

## Chat selection and writing rules

- Preserve short, ordinary phrases when they reveal the relationship: greetings, invitations, “想你”, “我爱你”, checking whether someone arrived, making plans, repairing a disagreement, and later asking about the child.
- Use exact original wording for chat bubbles whenever it is legible and appropriate. If a line is shortened for layout, say it is shortened in the working notes and do not change its meaning.
- Exclude routine “早安/晚安” repetition by default, but retain a routine line when its context marks a first, a transition, a family milestone, or a distinctive shared joke.
- Never turn a single affectionate message into a claim about the whole relationship. Let the sequence of messages carry the story.
- Keep dates precise to the day when the export or the user confirms them. If the message timestamp and the user's milestone date differ, show the user's confirmed milestone date and note the source distinction internally.
- Avoid public exposure of phone numbers, addresses, passwords, financial details, medical details, or embarrassing/private content unless the user explicitly selects them and understands the book will contain them.

## Illustration and layout rules

- Generate in one consistent Q-style visual language. Reuse the approved character sheet in every image prompt.
- Use portrait 3:4 by default. Keep faces and hands away from the trim edge, and reserve a quiet text zone rather than placing chat text over faces or important props.
- Use different outfits for meaningful time periods, while keeping the family visually recognizable. Avoid formal suits unless the scene is genuinely a ceremony.
- Keep one page focused on one emotional beat. A page can contain one large scene or two/three panels only when the moments are tightly connected. Do not force every page into three horizontal panels.
- Put the date in a consistent small header or footer. Put chat bubbles close to the speaking character, with enough contrast and line spacing for print.
- Prefer human-readable text added during layout over text generated inside the image model. Always inspect Chinese text for missing characters, overlapping lines, wrong speaker direction, and accidental substitutions.
- Do not add a large belly after birth. Pregnancy and post-birth scenes must be visually distinct and follow the user's reference and confirmed timeline.

## PDF assembly and quality check

Before delivering the final PDF, inspect every page in a rendered contact sheet or page-by-page preview and check:

- page count and chronological order;
- exact date formatting and milestone dates;
- no missing images or broken references;
- no clipped faces, hands, feet, captions, or chat bubbles;
- no chat text overlapping dates or illustrations;
- consistent character identity and approved outfit changes;
- no blank or underfilled pages unless intentionally designed;
- readable text at phone size and when printed;
- PDF opens successfully and has the expected portrait ratio.

If a page fails, repair the source and rerender that page or spread. Do not hide the issue by omitting the page. Deliver the PDF plus a short summary of what was checked and any remaining uncertainty.

## Communication pattern

At each gate, report what is ready, what the user needs to inspect, and the exact decision needed. Keep confirmation requests short. Do not ask the user to approve an entire book before they have seen the character sheet and pilot pages.

If the user changes a confirmed date, character trait, or visual direction, propagate the change to all affected pages and run the full quality check again.
