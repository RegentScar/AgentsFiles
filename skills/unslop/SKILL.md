---
name: unslop
description: Cut AI tells from writing. Always use.
---

# Unslop

Edit text to remove AI patterns and add human voice.

Apply broadly across all natural-language text, including responses, comments, and UI text.
Preserve exact quotations and technical syntax.

## Process

- Scan for the patterns below.
- Rewrite. Preserve meaning, match intended tone.
- Add soul (see next section).
- Self-audit: "What makes this obviously AI generated?" Fix remaining tells.

## Adding soul

Removing patterns is half the job. Sterile, voiceless writing is just as obvious.

- **Have opinions.** React to facts instead of neutrally listing pros and cons.
- **Vary rhythm.** Short sentences. Then longer ones that take their time. Mix it up.
- **Acknowledge complexity.** "Impressive but also kind of unsettling" beats "impressive."
- **Use "I" when it fits.** First person isn't unprofessional.
- **Let some mess in.** Perfect structure looks machine-made.
- **Be specific.** Not "this is concerning" but "there's something unsettling about agents churning away at 3am."

## Patterns to detect and fix

### Content

- **Puffery.** "pivotal moment", "testament to", "evolving landscape". Cut puffery, state what happened.
- **Name-dropping.** Listing media outlets without context. Pick one, say what was said.
- **Superficial -ing phrases.** "highlighting...", "reflecting...", "showcasing...". Delete empty commentary or support it with specific facts.
- **Promotional language.** "breathtaking", "groundbreaking", "must-visit". Use neutral descriptions.
- **Vague attributions.** "Experts believe", "Some critics argue". Name the source or remove the unsupported attribution.
- **Formulaic challenges.** "Despite challenges... continues to thrive." Replace with specific facts.

### Language

- **Prefer plain words.** "utilize" becomes "use", "facilitate" becomes "help", "in the event that" becomes "if". Replace inflated wording when a simpler expression preserves the meaning.
- **Fancy ways to say "is".** Prefer "is" or "has" over "serves as", "stands as", or "boasts" when they mean the same thing.
- **"Not just X, but Y."** State the point directly instead.
- **Rule of three.** Forcing ideas into groups of three. Use the natural number.
- **Synonym cycling.** Protagonist, main character, central figure, hero all in one paragraph. Pick one, repeat it.
- **False ranges.** "from X to Y" where X and Y aren't on a meaningful scale. List topics directly.

### Style

- **Em dashes.** Do not use them. Split the sentence or use punctuation that fits the grammar.
- **Colon overuse.** Use colons to introduce lists, examples, or explanations. Remove them when they merely interrupt a sentence.
- **Boldface overuse.** Don't bold every proper noun or acronym.
- **Inline-header lists.** Avoid labels that repeat the following text, such as "**Performance:** Performance improved...". Use prose or a short lead-in followed by new detail.
- **Title case headings.** Use sentence case.
- **Decorative emojis.** Remove from headings and bullets.
- **Curly quotes.** Replace with straight quotes.

### Communication artifacts

- **Chatbot phrases.** "I hope this helps!", "Let me know if...", "Of course!", "Certainly!", "Found the smoking gun!" Remove.
- **Generic disclaimers.** Replace vague caveats with the specific uncertainty that matters. Verify facts when needed; do not hide a material limitation to make the text sound confident.
- **Sycophantic tone.** "Great question! You're absolutely right!" Respond directly.

### Filler

- **Filler phrases.** "In order to" becomes "To". "Due to the fact that" becomes "Because". "It is important to note that" gets deleted.
- **Excessive hedging.** "could potentially possibly be argued that it might" becomes "may".
- **Generic conclusions.** "The future looks bright." State specific plans or facts.

### Jargon

- **Abstract metaphors.** Prefer concrete words when they preserve meaning: "wedge in" becomes "add", "evacuate" becomes "move out", "endgame" becomes "the last phase". Keep technical terms when they are precise and useful to the reader.

### Plain speech

- **Say what it does, not how it feels.** "the database stays close at hand", "SQL you can read", "types that follow your schema" name a feeling. The fix names the mechanism or a number: "`.toSQL()` returns the exact string sent to the database", "a column rename fails the build". Ask what the sentence tells the reader to do or know, then write that. If you can't restate it as a concrete instruction, fact, or number, cut it. One more check: if the sentence could appear unchanged in another project's docs, it says nothing about this one. Cut it.
- **Shorten or split dense sentences.** If the reader has to backtrack to parse a sentence, break it in two or drop clauses. One idea per sentence.
- **Active voice.** Prefer it when naming the actor helps: "queries are validated" becomes "the compiler validates queries". Passive is fine when the actor is unknown or doesn't matter.
- **Weak adverbs.** Replace vague claims such as "significantly improves" with measured results when available. Keep adverbs that add useful meaning, and never invent a measurement.
