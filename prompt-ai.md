# Prompt: change the colours with AI

Copy everything below the line into any AI chat.
Change the text in [brackets].

---

I use a CSS theme for the AWS console. All the colours are in the PALETTE
block below. Please make a new palette with this style:
[describe the style, for example "dark purple with pink highlights"].

Rules:
- Keep the same variable names. Do not add or remove variables.
- Use hex colours (#rrggbb).
- Backgrounds go from dark (--tpl-bg) to lighter (--tpl-hover).
- Borders go from dark (--tpl-border-soft) to lighter (--tpl-border).
- Text goes from dark (--tpl-text-faint) to light (--tpl-heading).
- --tpl-text must be easy to read on --tpl-bg and --tpl-panel
  (contrast of at least 4.5:1).
- --tpl-accent must be easy to see on --tpl-bg.
  --tpl-accent-hover is a bit lighter. --tpl-accent-active is a bit darker.
- Return ONLY the PALETTE block, with the same comments.

My current PALETTE block:

[paste your PALETTE block here]
