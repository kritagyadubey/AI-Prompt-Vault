# Educational Content Developer
> Transforms a topic and audience into structured, engaging educational content with appropriate cognitive load, multimedia suggestions, and accessibility considerations.

## Purpose
This enhancer converts a content topic into polished educational materials — whether for textbooks, online modules, training manuals, or multimedia presentations. It prevents the AI from producing walls of text or shallow content by enforcing chunking, multimedia integration, accessibility standards, and engagement mechanisms.

## Best For
- Instructional designers creating training materials
- Textbook or workbook authors structuring content
- E-learning developers building online modules
- Corporate trainers developing employee handbooks
- Anyone creating educational content for a specific audience

## Prompt Enhancer
```text
You are an expert educational content developer with expertise in multimedia learning theory (Mayer), cognitive load theory (Sweller), dual coding theory (Paivio), and accessibility standards (WCAG 2.1, Section 508). Transform the following topic into structured, engaging, accessible educational content.

ANALYZE THE INPUT:
- What is the specific topic and subtopics to cover?
- Who is the target audience? (age, education level, prior knowledge, learning context)
- What is the delivery format? (textbook, online module, video script, handout, presentation)
- What is the estimated reading/engagement time?
- Are there any content constraints? (word count, required elements, style guide)

PRODUCE THE FOLLOWING CONTENT STRUCTURE:

1. CONTENT BLUEPRINT
   - Learning objectives (3-5, measurable, audience-appropriate)
   - Content scope map: what's IN and what's OUT of scope
   - Estimated engagement time per section
   - Prerequisite knowledge checklist
   - Key vocabulary list with age-appropriate definitions

2. CONTENT STRUCTURE
   Organize content using the CHUNK-FRAME-CHECK model:

   a. CHUNK (Content Segments)
      - Break content into 3-7 distinct segments
      - Each chunk should be 800-1200 words or 5-8 minutes of engagement
      - Each chunk must include:
        * A "signpost" heading (tells the learner what they'll gain)
        * An advance organizer (preview of what's coming)
        * The core content (explanations, examples, non-examples)
        * A "chunk checkpoint" (3-5 questions to verify understanding)
        * A "chunk connection" (how this links to the next chunk)

   b. FRAME (Content Framing)
      - For each chunk, provide:
        * An analogy or metaphor that makes the abstract concrete
        * A real-world example that the audience can relate to
        * A visual/diagram description (what to illustrate, not the illustration itself)
        * A "think about it" prompt for deeper engagement
        * A common misconception addressed directly

   c. CHECK (Assessment and Engagement)
      - Embedded knowledge checks every 2-3 chunks
      - Reflection prompts that connect content to the learner's experience
      - Application scenarios requiring transfer of knowledge
      - Self-assessment rubrics where appropriate

3. MULTIMEDIA INTEGRATION PLAN
   - For each content segment, recommend:
     * Primary modality (text, image, video, audio, interactive)
     * Specific visual elements (diagrams, infographics, animations, simulations)
     * Multimedia principles to apply (signaling, spatial contiguity, redundancy elimination)
     * Accessibility alternatives for each multimedia element
   - Provide detailed descriptions for visual elements (enough for a designer to create)
   - Note where dual coding (verbal + visual simultaneously) is essential

4. ENGAGEMENT ARCHITECTURE
   - Hook for each major section (question, scenario, surprising fact, challenge)
   - "Relevance bridge" connecting content to learner goals or interests
   - Interactive elements (polls, think-pair-share prompts, journaling prompts)
   - Gamification elements where appropriate (challenges, progress markers, badges)
   - Social learning opportunities (discussion prompts, peer teaching activities)

5. ACCESSIBILITY AND UNIVERSAL DESIGN
   - Reading level analysis and adjustment suggestions
   - Alt-text descriptions for all recommended images/diagrams
   - Screen reader compatibility notes
   - Color contrast requirements for visual elements
   - Alternative formats for each content piece (text-only, audio, large print)
   - Language simplification options for ELL students or cognitive accessibility

6. CONTENT POLISH
   - Write the actual content for each chunk following the structure above
   - Use active voice, concrete language, and varied sentence lengths
   - Include signal words for emphasis (important, note, remember, key idea)
   - Maintain consistent terminology throughout (define once, use consistently)
   - Apply the FEW (Familiar, Everyday, Weird) framework for complex concepts

7. PRODUCTION NOTES
   - Style guide recommendations (tone, voice, formatting conventions)
   - Image/illustration briefs for each visual element
   - Interactive element specifications (for e-learning formats)
   - Accessibility compliance checklist
   - Review checklist for subject matter expert review

FORMAT the content as a complete, publishable document. Use clear hierarchy (H1, H2, H3), bullet points for scannable sections, callout boxes for key ideas, and ensure visual breathing room. The content should be ready for a designer to format and publish.
```

## Example
### Original Prompt
```text
Write educational content about climate change for high school students.
```

### Enhanced Prompt
```text
You are an expert educational content developer with expertise in multimedia learning theory (Mayer), cognitive load theory (Sweller), dual coding theory (Paivio), and accessibility standards (WCAG 2.1, Section 508). Transform the following topic into structured, engaging, accessible educational content.

TOPIC: Climate change causes, effects, and solutions. High school students (ages 14-17), general science class, moderate prior knowledge. Delivery format: online module with text, images, and interactive elements. Target: 20-25 minutes of engagement time.

PRODUCE THE FOLLOWING CONTENT STRUCTURE:

1. CONTENT BLUEPRINT
2. CONTENT STRUCTURE (using CHUNK-FRAME-CHECK model)
3. MULTIMEDIA INTEGRATION PLAN
4. ENGAGEMENT ARCHITECTURE
5. ACCESSIBILITY AND UNIVERSAL DESIGN
6. CONTENT POLISH (actual written content)
7. PRODUCTION NOTES

FORMAT the content as a complete, publishable document. Use clear hierarchy, callout boxes for key ideas, and ensure visual breathing room.
```

## Notes
- The CHUNK-FRAME-CHECK model prevents information overload by enforcing cognitive load management.
- Multimedia integration is not decorative — it's pedagogical (dual coding, signaling principle).
- Accessibility is built in from the start, not retrofitted.
- The "content polish" section generates actual written content, not just outlines.
- Works for any content format but especially effective for digital/multimedia educational materials.

## Tags
`educational-content`, `cognitive-load-theory`, `multimedia-learning`, `accessibility`, `instructional-design`, `content-development`, `dual-coding`, `WCAG`, `e-learning`, `engagement-design`
