---
name: tip-manager
description: Enables the agent to learn from past mistakes by managing a persistent list of concise debugging tips. It loads tips at the start of a session and appends new tips only when explicitly instructed by the user.
---

# Instructions

## 1. Tip Generation (User Trigger)
When the user provides a command similar to "Save this as a tip", "Remember this fix", or "Add to tips":
- **Action:** Analyze the immediate conversation history (the error and the successful fix).
- **Extraction:** Distill the lesson into a single, atomic logic statement.
- **Formatting:** Convert the lesson into the strict format: `IF [specific condition/error], THEN [specific action/solution].`
- **Constraint:**
  - MAX 20 words per tip.
  - NO context, NO code blocks, NO explanations.
  - AUTOMATICALLY create the directory `./tips/` if it does not exist.
- **Storage:** Append the formatted string to `./tips/tips.md` on a new line.
- **Output:** Confirm to the user: "Tip saved: [Content of tip]"

# Examples

## Example: Saving a Tip
**User:** "That fixed it. Save this as a tip."
**Context:** User had a `json.decoder.JSONDecodeError` because the input string was empty.
**Agent Action:** Appends the following line to `./tips/tips.md`:
`IF json decoding fails on empty string, THEN check string length before loading.`

