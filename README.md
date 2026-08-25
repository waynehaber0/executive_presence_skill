# executive_presence_skill

Claude skill for daily executive presence coaching

A scheduled Claude task that reads yesterday back to you and tells you where your communication fell short. Every weekday morning it picks the previous business day, pulls what you actually wrote and said across sent email, Teams chat, and meeting transcripts, and scores only your own words against seven dimensions of executive presence: conviction, leading with the answer, signal density, business framing, ownership, meeting presence, and whether you gave an answer where a question would have grown someone. Everyone else's words are context, not evidence.

The output is deliberately small. Three moments, each with a verbatim quote, the dimension it missed and what that cost, a rewrite you could have sent instead, and a note on whether it is a habit or a one-off. It closes with a single Socratic question aimed at the pattern rather than the incident, and lands the whole write-up in one p1 Todoist task due at 9am. A clean day gets fewer than three examples instead of padding. The run is read-only everywhere except that single task: no email sent, no document modified, no quote paraphrased into something sharper than what you said.


# Setup

The prompt lives in prompt.md. Fill in the bracketed placeholders (name, title, company, timezone), then create it as a scheduled task in Claude with a weekday-morning cron. It expects a Microsoft 365 connector for email, chat, and transcripts, and a Todoist connector for the task it writes.


