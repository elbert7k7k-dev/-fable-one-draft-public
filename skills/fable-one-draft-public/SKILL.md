---
name: fable-one-draft-public
description: Use when creating a public one-draft fable workflow that turns Chinese short concepts into Xiaohongshu comic scripts and Zhihu fable stories, with automatic topic choice and safe image QA rules.
---

# Fable One-Draft Public

## When To Use

Use this skill when the user wants to generate a complete Chinese self-media fable package:

- Automatic topic selection from public trends.
- Xiaohongshu 9-page comic script.
- Realistic scene image prompts.
- Xiaohongshu publishing copy in Markdown and standalone HTML.
- Zhihu fable article in Markdown and HTML image-insertion edition.
- Zhihu publishing recommendation pack with search keywords, 3 topic keywords, and 1 submission direction.
- QA checklist.

## Core Rule

If the user asks for automation, end-to-end execution, no manual confirmation, or blank topic auto-selection, do not stop at candidate topics. Candidate topics and story directions are records, not pause points.

## Workflow

1. Pick or validate a short topic.
2. Check risk boundaries.
3. Explain the mechanism.
4. Choose the best comic story direction.
5. Write a 9-page Xiaohongshu comic script.
6. Provide realistic scene image prompts and negative prompts.
7. If an Image2 / image generation tool is available, call it directly to generate 9 no-text base comic pages. Do not only write prompts.
8. After base pages are generated, complete Chinese text overlay and produce 9 final upload pages. Do not stop at no-text base pages.
9. Provide text overlay instructions.
10. Write Xiaohongshu copy in Markdown and standalone HTML.
11. Reverse-build the Zhihu fable from the comic story and produce a Zhihu HTML image-insertion edition.
12. Produce Zhihu publishing recommendation: search keywords, 3 topic keywords, 1 submission question/direction, and reasons.
13. Run QA and verify required image files, HTML files, and Zhihu recommendation file actually exist.

## Image Guardrail

Final images must not be local script placeholders. Use realistic scene generation or equivalent high-fidelity visual generation for the base image. Local scripts can only add text, watermark, crop, check size, and make contact sheets.

When Image2 or equivalent image generation is available, do not stop at prompts. Generate one page at a time, 9 pages total, 1024x1536 portrait, 2 columns x 3 rows. First generate no-text, no-watermark, no-caption-box base pages, then add Chinese subtitles/dialogue as no-background outlined text to create final upload pages.

Each comic page must contain clear story action, not mood-only scenery or knowledge-card layout. The 9-page script must include 6 panel actions, per-panel overlay text, a page-level summary subtitle, character actions, expressions, key objects, and scene changes. Page 9 is an author-note page but must still be a six-panel life-scene comic page.

Final delivery is incomplete until both 9 no-text base pages and 9 final text-overlaid upload pages exist. If no image tool is available, explicitly say images were not generated and output complete worker prompts, negative prompts, overlay text list, and QA criteria instead.

Full delivery is also incomplete if it only contains images or Markdown. A complete pass requires:

- Xiaohongshu publishing-copy HTML.
- Zhihu fable article HTML image-insertion edition.
- QA proof that both HTML files actually exist.

If final upload images exist, the Zhihu HTML must insert the 9 comic images in the story body before "作者的话" using `<figure><img></figure>` or equivalent image blocks. Markdown copies are useful backups, but Markdown alone is not a complete delivery.

Zhihu publishing recommendation is required. It must include:

- Search keywords for the Zhihu publishing UI.
- Exactly 3 recommended topic keywords.
- Exactly 1 recommended submission question/direction.
- Reasons based on article mechanism, relevance, risk boundary, and reader intent.

If live Zhihu browsing is unavailable, mark the recommendation as "待发布时复核" and do not invent heat numbers. Do not log in, do not click publish, and do not read credentials.

Text overlay defaults to no-background outlined text: no white caption boxes, no black bars, no large translucent backing, 8-14 Chinese characters per panel when possible, 1-2 lines, placed in empty scene areas without covering faces, hand actions, or key objects.

If generated images are not six-panel comic pages, not realistic life scenes, severely broken, or contain garbled text, regenerate the affected page. If repeated attempts fail, record the failure in QA and do not pass low-quality images as final output.

## Safety

Do not publish to platforms. Do not read credentials, tokens, cookies, QR codes, passwords, App Secrets, private keys, browser profiles, or account state.
