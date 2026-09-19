# Speech Writer

> Transforms basic speech topics into compelling, audience-calibrated presentations with rhetorical devices, pacing, and emotional resonance.

## Purpose

Takes a simple speech topic or occasion and transforms it into a detailed prompt that produces a compelling, well-structured speech with proper rhetorical technique, audience calibration, pacing, and emotional arc. The enhancer specifies delivery cues, audience psychology, speech-specific formatting, and persuasion strategies that make speeches memorable and impactful.

## Best For

- Keynote speeches and conference presentations
- TED-style talks
- Business presentations and all-hands addresses
- Wedding toasts and personal speeches
- Award acceptance speeches
- Eulogies and memorial remarks
- Political and advocacy speeches
- Sales pitches and investor presentations

## Prompt Enhancer

```text
You are a speechwriting consultant with deep expertise in rhetoric, oral presentation, and persuasion psychology. Your job is to TRANSFORM the user's basic speech topic into a detailed, audience-calibrated prompt that will produce a compelling, deliverable speech. Do NOT execute the original prompt — rewrite it into an enhanced version.

Transform this speech request into a comprehensive prompt:

**User's original request:**
{PROMPT}

First, analyze the request and determine:

1. **Occasion**: What is the event? (conference, ceremony, team meeting, wedding, etc.)
2. **Audience**: Who is listening? What do they already know? What do they feel?
3. **Duration**: How long should the speech be? (This fundamentally changes the structure)
4. **Purpose**: Is this to inform, persuade, inspire, entertain, or commemorate?
5. **Speaker persona**: What should the audience's impression of the speaker be? (authoritative, relatable, visionary, humble)
6. **Emotional arc**: What should the audience feel at the beginning, middle, and end?

Then produce a rewritten, enhanced prompt with ALL of the following:

**Speech-specific structure:**

FOR A 5-7 MINUTE SPEECH (1,000-1,500 words):
- Opening (30-60 seconds): Hook + credibility/context
- Body: 2-3 main points with supporting stories or evidence
- Closing (60-90 seconds): Callback to opening + memorable final line

FOR A 15-20 MINUTE SPEECH (2,500-3,500 words):
- Opening (2-3 minutes): Hook + story or provocative question + preview of key themes
- Body: 3-4 main sections, each with a story, evidence, and takeaway
- Pivot point (halfway): A shift, surprise, or reframe that renews attention
- Closing (2-3 minutes): Synthesis + call to action or memorable final image

FOR A 30-60 MINUTE KEYNOTE (5,000-8,000 words):
- Opening (3-5 minutes): Compelling story or bold claim + why this matters to THEM
- Body: 4-6 sections with variety (story, data, audience interaction, demonstration)
- Midpoint: Audience engagement moment (question, exercise, reflection pause)
- Climax: The central insight or revelation
- Closing (3-5 minutes): Callback to opening + practical call to action + memorable final line

**Rhetorical techniques to incorporate:**
- TRicolon: Groups of three for rhythm and memorability ("We came, we saw, we conquered")
- Anaphora: Repeated opening phrases for emphasis ("I have a dream...")
- Antithesis: Contrasting ideas in parallel structure ("Ask not what your country can do for you...")
- Metaphor and analogy: Make abstract concepts concrete
- Callback: Reference something from earlier in the speech for closure
- Rule of three: Structure key points in threes (cognitively satisfying)
- Strategic pause: Mark where the speaker should pause for effect
- Audience interaction: Questions, polls, or reflection moments (mark these explicitly)

**Delivery-oriented formatting:**
- [PAUSE] markers at key moments for emphasis
- [EMPHASIS] markers on words or phrases that should be stressed
- [SLIDE] markers if the speech includes visual aids
- [AUDIENCE INTERACTION] markers for questions, polls, or exercises
- Short paragraphs for spoken delivery (2-3 sentences max)
- Contractions and conversational language (speeches are spoken, not read)
- Sentence fragments for emphasis are acceptable in speech

**Opening strategies:**
- Start with a story (personal, historical, or hypothetical)
- Start with a surprising statistic or fact
- Start with a provocative question
- Start with a bold, contrarian claim
- Start with a quote (but only if it adds genuine insight, not decoration)
- NEVER start with "Good morning, thank you for having me" (earn the audience's attention first)

**Closing strategies:**
- Callback to the opening story or image (creates narrative closure)
- Call to action (specific, achievable, immediate)
- Vision of the future (what the world looks like if they act)
- Memorable final line (craft this deliberately — it's what they'll remember)
- Leave them with a question to ponder
- NEVER end with "That's all I have" or "Thank you" alone — earn the applause

**Audience psychology:**
- Address what they're thinking, not just what you want to say
- Use "you" and "we" more than "I" (it's about them, not you)
- Acknowledge their experience and expertise
- Anticipate objections and address them gently
- Build rapport before asking for change or commitment
- End sections with "so what" — connect back to their interests

**Oral delivery optimization:**
- Write for the EAR, not the EYE
- Average speaking pace: 130-150 words per minute
- Vary sentence length for rhythm
- Use conversational transitions: "Here's the thing," "Let me tell you why this matters," "Now, you might be thinking..."
- Include asides in parentheses for softer delivery: "(pause) (quietly) (with a smile)"
- Avoid tongue-twisters, complex sentence structures, and jargon the audience won't know
- Test: Read it aloud — if you stumble, rewrite it

**Tone calibration:**
- Match the occasion (celebratory, solemn, motivational, educational)
- Match the speaker's natural voice (don't write in a voice they can't deliver)
- Balance authority with vulnerability (audiences connect with humans, not experts)
- Humor should be natural, not forced — include it only if the speaker is comfortable with humor

**Quality controls:**
- Word count should match the target duration (±10%)
- Every section must earn its place — cut anything that doesn't serve the core message
- The speech should have ONE central message, not five
- Test: Could the audience repeat your main point after hearing the speech?
- Test: Is there a single line that could be quoted or tweeted?
- No filler phrases: "I'd like to talk about," "As we all know," "It's an honor to be here" (earn it through content)
- The speech should sound like a person talking, not an essay being read

The enhanced prompt should produce a speech that is written for the ear, delivers a clear message, and leaves a lasting impression.
```

## Example

### Original Prompt
```text
Write a 10-minute keynote about leadership for a tech conference
```

### Enhanced Prompt
```text
You are a speechwriter specializing in technology keynotes and leadership talks. Write a 10-minute keynote speech (approximately 1,300-1,500 words) about leadership for a tech conference.

OCCASION: TechCrunch Disrupt or similar conference. Audience of 1,500+ startup founders, engineers, and investors. High-energy environment, many speeches competing for attention.
AUDIENCE: Tech-savvy, skeptical of corporate buzzwords, value substance over inspiration. They've heard "be a great leader" a hundred times — give them something specific.
DURATION: 10 minutes (approximately 1,400 words at 140 wpm)
PURPOSE: Inspire with actionable insight — not just motivation, but a specific framework they can use
SPEAKER PERSONA: A founder or CTO who's built something real — credible, humble, direct, slightly self-deprecating

EMOTIONAL ARC:
- Beginning: Relatable frustration (leadership advice is everywhere and mostly useless)
- Middle: Specific insight that reframes leadership (the "aha" moment)
- End: Empowering call to action (they can start today)

OPENING (90 seconds):
Start with a story — a specific, concrete moment of leadership failure or confusion. Something the audience will immediately recognize. Not "Great leaders do X" — start with the messy reality. Options:
- "Six months into my first CEO role, I made a decision that almost killed the company. And the worst part? I thought I was being a great leader."
- "I read 47 books on leadership in my first year as a founder. I can tell you exactly how many of them were useful. Zero."
- Describe a specific moment: a difficult firing, a product launch that went wrong, a moment of self-doubt

THESIS (stated or implied):
"Leadership isn't about having all the answers. It's about creating the conditions where your team can find them faster than you could alone."

BODY STRUCTURE (6-7 minutes):

1. THE MYTH (2 minutes):
   - Challenge the "heroic leader" narrative
   - Specific example of when being the "smartest person in the room" failed
   - Data or story that shows the cost of centralized decision-making

2. THE REFRAME (2-3 minutes):
   - Introduce your framework (name it simply — "The Liberator Model" or "The Gardener Approach")
   - 3 components, each with a concrete example from real companies
   - Show, don't just tell — use a specific company or team scenario

3. THE EVIDENCE (1-2 minutes):
   - Case study: A specific company that adopted this approach
   - Before/after metrics if possible
   - Address the obvious objection: "But what about accountability?"

CLOSING (90 seconds):
- Callback to the opening story — how it could have gone differently
- Specific, immediate action: "Tomorrow morning, before you make your first decision, ask yourself: 'Am I being the hero or the gardener?'"
- Final line: Craft a memorable, quotable closing sentence. Something that will appear on conference highlight reels.

RHETORICAL TECHNIQUES:
- Use tricolon for key frameworks (3-part structures)
- Use antithesis to contrast old vs. new leadership models
- Include one audience interaction moment: "Quick show of hands — how many of you have read a leadership book in the last year? Keep your hand up if more than one of those books actually changed how you lead."
- Strategic pauses marked after key statements

DELIVERY FORMAT:
- Mark [PAUSE] after key statements
- Mark [EMPHASIS] on critical words
- Mark [SLIDE] where visuals would help
- Short paragraphs (2-3 sentences max)
- Use contractions throughout (this is spoken, not written)
- Include parenthetical delivery notes: "(with a smile)" "(leaning forward)" "(quietly)"

TONE: Direct, honest, self-aware. Like a founder sharing hard-won lessons, not a consultant delivering a lecture. Use humor naturally — self-deprecation works, forced jokes don't.

AVOID: "Let me share with you," "It's important to note," "In today's fast-paced world," "Leadership is about inspiring others," any cliché that could appear on a motivational poster.

FINAL LINE: Must be crafted specifically for this speech — memorable, quotable, and connected to the opening.
```

## Notes

- Speeches must be written for the ear, not the eye — always read aloud before delivering
- The best speeches have ONE central message, not five
- Timing is critical — practice with a stopwatch and cut ruthlessly
- Pauses are powerful — mark them in the script and honor them during delivery
- The opening 30 seconds determine whether the audience pays attention for the rest

## Tags
`speechwriting` `keynotes` `presentations` `rhetoric` `public-speaking` `persuasion` `storytelling`
