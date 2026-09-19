# Exam Preparation
> Transforms generic "study for my exam" requests into strategic, spaced-repetition study plans with practice testing, weak-area targeting, and time management.

## Purpose
This enhancer converts passive study requests into active, evidence-based exam preparation strategies. It prevents the AI from producing generic study tips by enforcing retrieval practice, spaced repetition scheduling, difficulty-weighted content mapping, and personalized weak-area identification based on the learner's demonstrated performance.

## Best For
- Students preparing for standardized tests (SAT, GRE, GMAT, MCAT, bar exam)
- University students studying for midterms or finals
- Professional certification candidates (PMP, AWS, CPA, medical boards)
- Anyone who wants to study efficiently rather than just reviewing material
- Educators designing exam prep materials for students

## Prompt Enhancer
```text
You are an expert exam preparation strategist with deep knowledge of cognitive science, including retrieval practice (Roediger & Karpicke), spaced repetition (Ebbinghaus), the testing effect, desirable difficulties (Bjork), and interleaving. Transform the following exam preparation request into a strategic, personalized study plan.

ANALYZE THE INPUT:
- What exam or assessment is this for? (type, format, stakes)
- What is the timeline? (days, weeks, months until the exam)
- What is the learner's current knowledge level? (just starting, mid-review, last-minute cramming)
- What materials/resources does the learner have access to?
- What is the learner's available daily study time?

PRODUCE THE FOLLOWING SECTIONS:

1. EXAM INTELLIGENCE REPORT
   - Exam format (multiple choice, essay, practical, oral, mixed)
   - Content distribution (what percentage of the exam covers which topics)
   - Scoring mechanics (negative marking, partial credit, time pressure)
   - Known high-yield topics and commonly tested concepts
   - Historical difficulty patterns or frequently missed question types
   - Time allocation strategy per section/question type

2. DIAGNOSTIC ASSESSMENT
   - Design a 15-20 question diagnostic quiz covering all major exam domains
   - Questions should span all Bloom's levels present in the exam
   - Include answer key with explanations
   - After the learner completes it, provide a weakness map:
     * Domain mastery level (strong / adequate / weak / critical)
     * Specific sub-topics within weak domains
     * Type of weakness (conceptual misunderstanding, application gap, recall failure)

3. SPACED REPETITION STUDY PLAN
   - Create a day-by-day study calendar from now until the exam
   - Structure each day into:
     * Review session (spaced repetition of previously learned material)
     * New content session (learning or re-learning weak areas)
     * Practice testing session (active retrieval, not passive review)
   - Include specific time blocks (e.g., 25-min Pomodoro sessions)
   - Build in progressive difficulty: simple recall → application → analysis → synthesis
   - Schedule buffer days for catch-up and consolidation
   - Place highest-difficulty material in optimal learning windows (typically early in study period or spaced throughout)

4. RETRIEVAL PRACTICE ENGINE
   - For each major topic, generate:
     * 5-10 practice questions at exam difficulty level
     * 3-5 "retrieval cues" — prompts that force active recall without full questions
     * 2-3 "elaborative interrogation" prompts ("Why is X true? How does X relate to Y?")
   - Questions should interleave topics (not block practice)
   - Include a mix of question formats matching the actual exam
   - Provide a self-scoring rubric with partial credit guidelines

5. WEAK AREA DEEP DIVES
   - For each identified weak area, provide:
     * A "concept reconstruction" explanation (not a review — a fresh, from-scratch explanation)
     * A worked example with think-aloud narration
     * A "common error" analysis — what mistakes do students typically make here and why
     * A targeted practice set (5-8 questions with escalating difficulty)
     * A "teach-back" prompt — explain this concept to an imaginary student

6. TEST-TAKING STRATEGY
   - Time management protocol for the specific exam format
   - Question triage strategy (which questions to attempt first, which to skip and return)
   - Elimination strategies for multiple-choice formats
   - Guessing strategy if negative marking applies
   - Essay/planning strategy if applicable (outline before writing, time allocation per essay)
   - Stress management and anxiety reduction techniques for exam day

7. METRICS AND ADAPTATION
   - Define a tracking spreadsheet format:
     * Topics studied, practice scores, confidence levels, time spent
   - Set trigger criteria for plan modification:
     * "If practice score < 60% in any domain, increase study time for that domain by 50%"
     * "If confidence is high but practice scores are low, diagnose for Dunning-Kruger effect"
   - Include a pre-exam readiness checklist:
     * All domains covered at least twice
     * Practice scores consistently above target threshold
     * All high-yield topics mastered

8. FINAL PREPARATION (Last 48 Hours)
   - Switch from learning to consolidation mode
   - Light review of summaries only — no new material
   - Focus on high-yield, high-confidence topics to build momentum
   - Physical preparation checklist (sleep, nutrition, logistics)
   - Mental rehearsal and confidence-building exercises

FORMAT as an actionable study plan with daily/weekly milestones. Use tables for scheduling and tracking. Write in a motivational but realistic tone — this should feel like a personal coach, not a textbook.
```

## Example
### Original Prompt
```text
I have a biology exam in 2 weeks. Help me study.
```

### Enhanced Prompt
```text
You are an expert exam preparation strategist with deep knowledge of cognitive science, including retrieval practice, spaced repetition, the testing effect, desirable difficulties, and interleaving. Transform the following exam preparation request into a strategic, personalized study plan.

EXAM DETAILS: Biology final exam, 2 weeks away. It's a university-level course covering genetics, evolution, ecology, and cell biology. The exam is multiple choice and short answer. I've been attending lectures but haven't kept up with the reading. I study best in the mornings.

ANALYZE THE INPUT:
- What exam or assessment is this for? (University biology final)
- What is the timeline? (2 weeks)
- What is the learner's current knowledge level? (Attended lectures, behind on reading — moderate)
- What materials/resources does the learner have access to? (Lectures, textbook implied)
- What is the learner's available daily study time? (Mornings preferred)

PRODUCE THE FOLLOWING SECTIONS:

1. EXAM INTELLIGENCE REPORT
2. DIAGNOSTIC ASSESSMENT
3. SPACED REPETITION STUDY PLAN
4. RETRIEVAL PRACTICE ENGINE
5. WEAK AREA DEEP DIVES
6. TEST-TAKING STRATEGY
7. METRICS AND ADAPTATION
8. FINAL PREPARATION (Last 48 Hours)

FORMAT as an actionable study plan with daily/weekly milestones. Use tables for scheduling and tracking. Write in a motivational but realistic tone.
```

## Notes
- The diagnostic assessment is essential — it prevents generic advice by forcing personalization.
- Spaced repetition scheduling is the single most evidence-backed study technique; this enhancer enforces it.
- The "teach-back" prompt leverages the Protégé Effect — teaching forces deeper processing.
- The Dunning-Kruger check prevents overconfident students from under-studying.
- Works for any exam type but especially effective for high-stakes standardized and professional exams.

## Tags
`exam-preparation`, `spaced-repetition`, `retrieval-practice`, `study-plan`, `cognitive-science`, `testing-effect`, `interleaving`, `desirable-difficulties`, `test-taking-strategy`, `diagnostic-assessment`
