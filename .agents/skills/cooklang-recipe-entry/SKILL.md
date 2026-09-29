---
name: cooklang-recipe-entry
description: Add or revise Cooklang .cook recipes from user-provided sources, preserving quantities and cooking method while validating the finished file.
---

# Cooklang recipe entry

Create or update a `.cook` recipe using Cooklang markup: `@` for ingredients and quantities, `#` for cookware, and `~` for cooking timers. Include useful metadata such as title and servings when known.

Before editing, identify the source's servings, ingredient quantities, cooking sequence, temperatures, durations, and finish/serving instructions. Use the intended serving column consistently. Reconcile the ingredient list with the directions, distinguishing quantities supplied from quantities actually used. Ask only when missing or ambiguous information prevents faithful entry; do not invent quantities or alter the method.

Preserve meaningful qualifiers such as "to taste," optional ingredients, divided quantities, and instructions to remove food from the heat. Record known counts as quantities (for example, `@lime{1}`), and ensure divided uses do not double-count ingredients.

Before delivery, perform a source-to-recipe verification pass against both the original ingredient list and directions. Compare every ingredient and amount, step order, temperature, duration, and finishing instruction. Correct any mismatch. Then run `cook recipe <file>` when CookCLI is available and inspect the rendered ingredient list and steps for missing quantities, duplicate totals, or unintended markup. Successful parsing does not establish source fidelity; report any validation limitation clearly.
