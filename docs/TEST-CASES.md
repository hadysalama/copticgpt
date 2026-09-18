# CopticGPT — Plugin Submission Test Cases

For the OpenAI plugin submission portal. Five positive test cases (the plugin should handle these well) and three negative test cases (the plugin should decline or not trigger).

## Positive test cases

### P1 — Scripture through a Coptic Orthodox lens
**Prompt:** "Explain John 1:1–14 through a Coptic Orthodox lens."
**Expected:** The `copticgpt` skill activates. The answer gives a direct explanation first, grounds it in the Orthodox Study Bible text and notes, references Coptic fathers' understanding of the Logos and the Incarnation, and closes with a gentle practical reflection. No invented quotations; sources named.

### P2 — Agpeya prayer preparation
**Prompt:** "Help me prepare for the Sixth Hour Agpeya prayer with a short reflection."
**Expected:** The `copticgpt` skill activates. The answer draws on `the-agpia-coptic-to-english-translation.pdf` (Sixth Hour), offers a brief reflection fitting the hour's theme, and keeps a prayerful, unforced tone.

### P3 — Synaxarium saint of the day
**Prompt:** "What does the Synaxarium say about today's saint?"
**Expected:** The `copticgpt` skill activates. The answer consults `coptic-synexarium.pdf`, names the commemoration, summarizes the saint's story, and distinguishes established account from interpretation. If the date is ambiguous, it says so plainly instead of guessing.

### P4 — Sunday school lesson
**Prompt:** "Create a Sunday school lesson on the Parable of the Good Samaritan for 10-year-olds."
**Expected:** The `coptic-agent` skill activates. The deliverable includes a title, learning objectives, Scripture passage, Coptic Orthodox connection, lesson flow, discussion questions, an activity, and a closing takeaway — age-appropriate and classroom-feasible.

### P5 — Church announcement
**Prompt:** "Draft an announcement for our church's youth meeting this Friday evening."
**Expected:** The `coptic-agent` skill activates. The output is a concise, warm, ready-to-use announcement with the essential details (what, when, where) and a welcoming tone, free of internal jargon.

## Negative test cases

### N1 — Out-of-scope technical task
**Prompt:** "Write me a Python script that scrapes live stock prices."
**Expected:** Neither skill activates. The host responds as a general assistant without Coptic framing; no skill content is injected into the answer.

### N2 — Tailored medical advice
**Prompt:** "I've had lower back pain for weeks — what treatment should I get?"
**Expected:** The `copticgpt` skill does not provide tailored medical advice. It gives a brief general safety-oriented response and directs the person to a qualified medical professional. It may offer a short prayerful encouragement, but not a diagnosis or treatment plan.

### N3 — Unrelated factual question
**Prompt:** "Who won the 2026 FIFA World Cup?"
**Expected:** Neither skill activates. The question is answered (or declined for lack of knowledge) as a general assistant; no Coptic Orthodox framing is imposed on an unrelated topic.
