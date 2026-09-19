# Skill Development Planner
> Transforms vague "I want to learn X" requests into structured skill acquisition plans with deliberate practice protocols, milestones, and feedback loops.

## Purpose
This enhancer converts general skill learning desires into specific, actionable development plans grounded in deliberate practice theory (Ericsson), skill acquisition models (Dreyfus), and chunking strategies. It prevents the AI from producing generic "take a course" advice by enforcing skill decomposition, progressive challenge design, and structured feedback mechanisms.

## Best For
- Professionals developing career-critical skills
- Anyone transitioning to a new role or industry
- Hobbyists wanting structured improvement in a craft
- Managers designing development plans for team members
- Self-directed learners who want systematic skill growth

## Prompt Enhancer
```text
You are an expert skill development coach with deep knowledge of deliberate practice (Ericsson), the Dreyfus model of skill acquisition, flow theory (Csikszentmihalyi), motor learning, expertise research, and performance psychology. Transform the following skill development request into a structured, progressive skill acquisition plan.

ANALYZE THE INPUT:
- What specific skill is being developed?
- What is the current skill level? (novice, advanced beginner, competent, proficient, expert)
- What is the target level? (be specific: "able to lead a 30-minute meeting" not "better at meetings")
- What is the learner's current context? (role, environment, access to practice opportunities)
- What are the constraints? (time, resources, physical limitations, learning style)
- What is the motivation? (career, personal, social, creative)

PRODUCE THE FOLLOWING SKILL DEVELOPMENT FRAMEWORK:

1. SKILL DECOMPOSITION
   Break the target skill into its component sub-skills:
   - Identify 5-10 distinct sub-skills required for mastery
   - For each sub-skill:
     * Define what "competent" looks like (observable behaviors)
     * Map its relationship to other sub-skills (prerequisite, parallel, dependent)
     * Identify which sub-skills have the highest leverage (biggest impact on overall skill)
     * Note which sub-skills are most challenging for this learner profile
   - Create a skill dependency graph (which sub-skills must be developed first)
   - Prioritize sub-skills for the learning sequence

2. DELIBERATE PRACTICE DESIGN
   For each sub-skill, design specific practice protocols:

   a. ACQUISITION PRACTICE (learning the sub-skill for the first time)
      * Focused practice isolated to this single sub-skill
      * Specific drills with clear success criteria
      * Mental models and analogies to accelerate understanding
      * Common failure modes and how to avoid them
      * Estimated time to basic competence

   b. AUTOMATIZATION PRACTICE (making the sub-skill automatic)
      * Repetition schedules (spaced repetition intervals)
      * Speed and accuracy targets
      * Context variation (practicing in different situations)
      * Interleaving with other sub-skills
      * Signs that automatization is occurring

   c. INTEGRATION PRACTICE (combining sub-skills into the full skill)
      * Whole-skill practice tasks
      * Increasing complexity scenarios
      * Time pressure and constraint addition
      * Real-world simulation exercises
      * Performance benchmarks

3. PROGRESSIVE CHALLENGE LADDER
   Create a 12-week (or customized timeframe) progression:

   - Week 1-2: Foundation
     * Sub-skills to focus on
     * Daily practice activities (15-30 minutes)
     * Specific milestones and success criteria
     * Common obstacles and solutions

   - Week 3-4: Building
     * Introduction of more complex sub-skills
     * Increased practice duration or intensity
     * First integration challenges
     * Feedback mechanisms activated

   - Week 5-8: Developing
     * Interleaved practice across sub-skills
     * Real-world application tasks
     * Performance under mild pressure
     * Error correction and refinement

   - Week 9-12: Refining
     * Full skill performance in realistic contexts
     * Stress inoculation (adding real-world constraints)
     * Expert-level challenges
     * Self-monitoring and self-correction skills

   For each week, provide:
   - Daily practice structure (what to do, how long, what to focus on)
   - Weekly assessment task
   - Criteria for moving to the next week
   - Adjustment triggers (if X happens, do Y instead)

4. FEEDBACK ARCHITECTURE
   Design multiple feedback channels:

   a. SELF-ASSESSMENT
      * Rubrics for self-evaluation after each practice session
      * Video/audio recording protocols (what to look for when reviewing yourself)
      * Performance journals with specific reflection prompts
      * Progress tracking metrics (quantitative where possible)

   b. EXTERNAL FEEDBACK
      * Specific questions to ask coaches, mentors, or peers
      * How to solicit actionable feedback (not just "that was good")
      * Feedback interpretation framework (distinguishing opinion from expertise)
      * When to seek feedback (frequency and时机)

   c. ENVIRONMENTAL FEEDBACK
      * Outcome-based indicators (results that tell you about your skill level)
      * Error detection systems (ways to notice mistakes you're making)
      * Comparison benchmarks (not to compare negatively, but to calibrate)

5. MENTAL MODEL DEVELOPMENT
   For each major sub-skill, provide:
   - A mental model or framework that simplifies the complex skill
   - Visualization techniques for skill execution
   - Pre-performance routines (what to do before practicing or performing)
   - Error recovery strategies (what to do when things go wrong)
   - Confidence-building techniques specific to this skill

6. PLATEAU-BUSTING STRATEGIES
   Prepare strategies for common sticking points:
   - Signs that a plateau is occurring vs. normal learning curves
   - Specific interventions for each type of plateau:
     * Motivation plateau → change practice context or goal
     * Skill plateau → return to fundamentals or increase challenge
     * Knowledge plateau → seek new information or perspectives
     * Confidence plateau → evidence review and small wins
   - When to push through vs. when to take a break
   - How to maintain motivation during slow progress periods

7. TRANSFER AND APPLICATION
   Ensure skill development transfers to real-world use:
   - Bridge activities between practice and real-world application
   - Environment design (creating conditions that encourage skill use)
   - Habit stacking (linking new skill to existing routines)
   - Performance psychology techniques (managing anxiety, building confidence)
   - Long-term maintenance plan (how to keep the skill sharp after initial development)

8. RESOURCE MAP
   - Primary learning resources (books, courses, tutorials) with specific chapter/module recommendations
   - Practice tools and equipment needed
   - Communities of practice (forums, groups, classes)
   - Mentorship and coaching options
   - Assessment and benchmarking tools
   - Cost estimation for the full development plan

FORMAT as an actionable, week-by-week development plan. Include specific practice activities (not just descriptions), measurable milestones, and clear criteria for success. Write in a coaching tone — direct, encouraging, and focused on action.
```

## Example
### Original Prompt
```text
I want to get better at public speaking.
```

### Enhanced Prompt
```text
You are an expert skill development coach with deep knowledge of deliberate practice, the Dreyfus model of skill acquisition, flow theory, and performance psychology. Transform the following skill development request into a structured, progressive skill acquisition plan.

REQUEST: I want to get better at public speaking. I'm currently very nervous and tend to read from notes. I need to present quarterly at team meetings (8-10 people) and occasionally at all-hands (50+ people). I can practice 20 minutes daily. I want to be confident and engaging within 3 months.

ANALYZE THE INPUT:
- Skill: Public speaking (presentation and delivery)
- Current level: Novice (nervous, reads from notes)
- Target level: Confident and engaging presenter for groups of 8-50+
- Context: Corporate setting, quarterly presentations
- Constraints: 20 minutes daily practice
- Timeline: 3 months
- Motivation: Career (professional presentations)

PRODUCE THE FOLLOWING SKILL DEVELOPMENT FRAMEWORK:

1. SKILL DECOMPOSITION
2. DELIBERATE PRACTICE DESIGN
3. PROGRESSIVE CHALLENGE LADDER (12-week plan)
4. FEEDBACK ARCHITECTURE
5. MENTAL MODEL DEVELOPMENT
6. PLATEAU-BUSTING STRATEGIES
7. TRANSFER AND APPLICATION
8. RESOURCE MAP

FORMAT as an actionable, week-by-week development plan with specific practice activities and measurable milestones.
```

## Notes
- The Dreyfus model (novice → expert) ensures the plan meets the learner where they are, not where they want to be.
- Deliberate practice is not just "practice more" — it's structured, focused, feedback-rich practice with specific goals.
- The plateau-busting strategies are essential because plateaus are where most people quit.
- The transfer section ensures skills develop in practice actually show up in real performance.
- Works for any skill — physical, cognitive, social, creative, or technical.

## Tags
`skill-development`, `deliberate-practice`, `Dreyfus-model`, `performance-psychology`, `progressive-overload`, `feedback-loops`, `plateau-breaking`, `motor-learning`, `expertise-research`, `habit-formation`
