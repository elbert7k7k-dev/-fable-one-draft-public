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
- Xiaohongshu publishing copy.
- Zhihu fable article.
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
7. Provide text overlay instructions.
8. Write Xiaohongshu copy.
9. Reverse-build the Zhihu fable from the comic story.
10. Run QA.

## Image Guardrail

Final images must not be local script placeholders. Use realistic scene generation or equivalent high-fidelity visual generation for the base image. Local scripts can only add text, watermark, crop, check size, and make contact sheets.

## Safety

Do not publish to platforms. Do not read credentials, tokens, cookies, QR codes, passwords, App Secrets, private keys, browser profiles, or account state.

