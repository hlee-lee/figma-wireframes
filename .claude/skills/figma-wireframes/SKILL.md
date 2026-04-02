---
name: figma-wireframes
description: Create or refine low-fidelity wireframes in Figma from a page-level brief, focusing on structure, hierarchy, and user flows rather than visual design.
disable-model-invocation: true
argument-hint: "[brief or screen request]"
---

# Figma Wireframes (Structure-Focused)

Use this skill to create or refine low-fidelity wireframes directly in Figma.

---

## Core Principle

Prioritize:
- layout clarity
- user flows
- information hierarchy
- component structure

Avoid:
- visual polish
- branding
- colors (except grayscale)
- detailed UI styling

---

## Prerequisites & Environment

- Figma MCP server must be connected
- Figma tools must be available

If not:
- Inform the user
- Do NOT proceed

---

## Design System (Mandatory)

All wireframes MUST be built using components from a **published Figma library** (design system), not ad-hoc shapes or invented patterns.

Before creating any wireframe:
1. Ask the user which published library / design system to use, OR check if one is already enabled on the target Figma file
2. Fetch the design system's components, tokens, and layout patterns using `get_design_context` so you understand what's available
3. Use library components as the foundation for all wireframes — do NOT invent new patterns when one already exists in the library

### Default Design System

Unless the user specifies otherwise, use the **UX design system** from this source:

- **Source file**: https://www.figma.com/design/QfhpFLA4y66lQlRO5txEvo/SKS-Redesign?node-id=7936-733&m=dev
- **File key**: `QfhpFLA4y66lQlRO5txEvo`
- **Node ID**: `7936:733`

This is a published library — its components are available in any Figma file that has it enabled, not just the source file above.

This applies to every invocation of this skill, not just the first time.

---

## Figma File Resolution (Blocking)

Ask:

"Should I use an existing Figma file or create a new one?"

---

### If existing file

- Ask for link or confirm current file
- Use it as destination

---

### If new file

- Ask for file name (or infer one)
- Create new Figma file using tools
- Confirm file is ready

---

### Rules

- Do NOT proceed without a file
- All output must be created in that file
- Do NOT generate wireframes in chat

---

## Visual Reference (Blocking — ask before intake)

Before starting the guided intake, ask:

"Do you have a visual reference you'd like the wireframes to match? This can be a Figma frame/link, a screenshot, an external URL, or anything that shows the style, layout patterns, or component look you want. If not, I'll use a clean default wireframe style."

### If reference provided

- Fetch it using `get_design_context`, `get_screenshot`, or read the image
- Analyze and extract: layout patterns, card/module structure, typography sizes & weights, spacing system, component styles (borders, fills, image placeholders), carousel/navigation patterns
- Use these patterns as the foundation for all wireframes in this session
- Do NOT deviate from the reference style unless the user asks for changes

### If no reference

- Proceed with a clean default wireframe style
- Keep it consistent within the session

### Rules

- This step is BLOCKING — do NOT skip it
- Ask it ONCE at the start, before any content questions
- The reference applies to the entire session, not just one section

---

## Required Tool Usage (Figma)

You MUST use Figma tools.

- Create frames directly in Figma
- Use auto layout where appropriate

Do NOT:
- Describe layouts in chat

If Figma is not updated → task is incorrect.

---

## Required User Input (Guided Intake)

Ask one question at a time.

---

### Step 1/7 — Context & Current State
"What exists today and what's the goal for this page? (e.g., what's being redesigned, what problem are we solving)"

---

### Step 2/7 — Key Content to Feature
"What are the specific content items or assets to feature on this page? (e.g., awards, products, articles — include details like names, descriptions, source copy)"

---

### Step 3/7 — Target Audience
"Who is the primary audience? Include demographics, behaviors, and motivations if known."

---

### Step 4/7 — User Goals
"What should users understand or be able to do after visiting this page?"

---

### Step 5/7 — Entry Points & Navigation
"How will users arrive at this page? (e.g., main nav, footer, search, external links)"

---

### Step 6/7 — Functional & UX Requirements
"What are the must-have functional or UX requirements? (e.g., CTAs, link behavior, what each content item must include, anything to explicitly avoid)"

---

### Step 7/7 — Creative References & Competitive Context
"Any creative references, competitor examples, or inspiration? What do you like or dislike about each?"

---

### Rules

- One question at a time
- Wait for response
- Do NOT batch questions

---

## Skip Handling

- Skipped = undefined
- Do NOT assume
- Do NOT include

---

## Review & Confirmation

### Summary of Inputs

Visual Reference
[user input, link, or "None — using default style"]

Context & Current State
[user input or "Not specified"]

Key Content to Feature
[user input or "Not specified"]

Target Audience
[user input or "Not specified"]

User Goals
[user input or "Not specified"]

Entry Points & Navigation
[user input or "Not specified"]

Functional & UX Requirements
[user input or "Not specified"]

Creative References & Competitive Context
[user input or "Not specified"]

---

Ask:

"Does this look correct? Reply 'yes' to proceed or tell me what to change."

---

### Rules

- Do NOT proceed without confirmation
- Re-confirm if updated

---

## Workflow

After confirmation:

1. Extract structure
2. Define layout
3. Use Figma tools to create frames

---

## Wireframe Rules

- Grayscale only
- Use placeholders
- Keep layouts simple
- No visual polish

---

## Right-Sizing

- Simple → minimal layout
- Complex → expand carefully
- Do NOT overbuild

---

## Goal

Create clean, low-fi wireframes directly in Figma.
