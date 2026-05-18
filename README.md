SaaS Support AI System Prompt
A structured system prompt that turns Claude into a specialized SaaS technical support engineer. Built from real support workflows developed while handling 35–45 tickets per week across a complex SaaS platform.
What this does
When this prompt is loaded into a Claude Project, it transforms Claude from a general-purpose assistant into a focused support diagnostic tool that:
Diagnoses issues using a consistent, repeatable structure
Knows which questions to ask based on the product area involved
Separates confirmed facts from assumptions
Ranks likely causes by probability
Produces clean customer-facing emails in a consistent voice
Generates escalation packages ready to hand off to Engineering
Rates its own confidence level at the end of every diagnosis
Why I built it
Support work has a lot of invisible structure — experienced engineers follow a mental checklist without thinking about it, but newer teammates often miss steps or jump to conclusions too fast. This prompt externalizes that structure so Claude follows the same diagnostic process every time, regardless of who's using it.
It also cuts the time it takes to write customer emails and escalation summaries significantly. The diagnosis is the hard part. Once that's done, the writing should be fast.
The diagnostic structure
Every issue gets worked through the same ten steps:
Issue summary — plain English, no jargon
Product area — identifies which part of the platform is involved
Known facts — only what was actually provided, no assumptions
Research performed — what was checked and what was found
Missing information — focused questions, not a laundry list
Triage questions — product-specific follow-up questions
Likely causes — ranked by probability, with confirmation steps for each
Recommended next steps — low-risk checks before disruptive actions
Logs and evidence to collect — exactly what to gather and where to find it
Customer-facing draft — ready to send, consistent voice
Escalation package — clean internal handoff summary
Confidence level — High / Medium / Low with reasoning
Files
`troubleshooting_prompt.md` — the main system prompt for general SaaS support diagnosis
`patternbuilder_prompt.md` — specialized prompt for document automation app troubleshooting
How to use it
Go to claude.ai and create a new Project
Open Project Instructions
Paste the contents of the prompt file into the instructions field
Start a conversation — paste in a support ticket or issue description and Claude will work through the diagnostic structure automatically
What makes this different from just asking Claude a question
A plain question gets a generic answer. A structured system prompt gets a repeatable, consistent diagnostic that follows the same logic every time. The difference shows up most on ambiguous tickets where it's easy to jump to the wrong conclusion — the prompt forces Claude to separate what's known from what's assumed before suggesting anything.
