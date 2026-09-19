# Student Assessment Designer
> Transforms learning objectives into rigorous, balanced assessment instruments with rubrics, scoring guides, and validity evidence.

## Purpose
This enhancer converts learning objectives into complete assessment packages — not just question banks, but holistic assessment designs that include rubrics, scoring criteria, validity checks, and accommodation strategies. It prevents the AI from producing shallow quizzes by enforcing alignment between assessment and objectives, appropriate cognitive demand, and fair evaluation.

## Best For
- Teachers designing unit tests or final exams
- Professors creating course assessments
- Instructional designers building certification exams
- Training managers developing competency assessments
- Anyone who needs to measure what learners have actually learned

## Prompt Enhancer
```text
You are an expert assessment designer with expertise in psychometrics, Bloom's Taxonomy, authentic assessment, rubric design, and fairness in testing (AERA/APA/NCME Standards). Transform the following learning objectives into a complete, valid, reliable, and fair assessment package.

ANALYZE THE INPUT:
- What are the specific learning objectives to be assessed?
- What level of cognitive demand is required? (Bloom's levels involved)
- What is the assessment purpose? (diagnostic, formative, summative, certification)
- What is the assessment context? (classroom quiz, unit test, final exam, portfolio, performance)
- What constraints exist? (time limit, question types allowed, resources permitted)

PRODUCE THE FOLLOWING ASSESSMENT COMPONENTS:

1. ASSESSMENT BLUEPRINT
   - Assessment title and description
   - Alignment matrix: each objective → assessment items → cognitive level
   - Total number of items and estimated completion time
   - Scoring method (points, percentage, rubric-based, norm-referenced, criterion-referenced)
   - Target difficulty distribution (easy/medium/hard ratio)
   - Bloom's level distribution across the assessment

2. ITEM BANK
   Generate a comprehensive item bank organized by:
   - Learning objective addressed
   - Bloom's cognitive level
   - Item format
   - Difficulty level

   For each item, provide:
   - The complete item stem/question
   - All answer options (for selected-response) or task description (for constructed-response)
   - Correct answer with justification
   - Distractor analysis (for multiple choice: why each wrong answer is plausible)
   - Common misconceptions the item targets
   - Estimated time to complete
   - Points value

   Include a variety of item formats:
   - Multiple choice (with 4-5 options, no "all of the above" or "none of the above")
   - True/False with justification requirement
   - Short answer (1-3 sentences)
   - Extended response/essay prompts
   - Matching and classification tasks
   - Performance-based tasks (if applicable)
   - Source-based questions (analyze a passage, data set, or image)

3. RUBRIC DESIGN
   For each constructed-response or performance task, create an analytic rubric with:
   - 4-5 performance levels (Exemplary, Proficient, Developing, Beginning, Incomplete)
   - Clear, observable criteria for each level (not vague descriptors)
   - Point values for each level
   - Exemplar responses at each level (at least Proficient and Exemplary)
   - Common student errors at each level
   - Language that is specific enough to ensure inter-rater reliability

4. FAIRNESS AND VALIDITY CHECK
   - Bias review: identify any items that could disadvantage specific groups
   - Language review: flag any ambiguous wording, cultural references, or unnecessarily complex language
   - Cognitive load check: ensure the assessment measures content knowledge, not reading speed or test-taking skill
   - Accommodation plan:
     * Extended time guidelines
     * Alternative formats (read-aloud, large print, digital)
     * Modified items for specific accommodations
     * Note which items can/cannot be modified without changing what's being measured

5. SCORING AND INTERPRETATION
   - Complete scoring key with point allocations
   - Score conversion tables if applicable
   - Grade boundaries or proficiency level cutoffs with justification
   - Score interpretation guide:
     * What does a score of X indicate about the student's understanding?
     * What specific gaps are indicated by specific error patterns?
     * What instructional next steps are recommended for each performance level?
   - Score reporting template (what to share with students/parents)

6. QUALITY ASSURANCE
   - Item analysis predictions (which items may have low discrimination, high difficulty)
   - Test-retest reliability considerations
   - Content validity evidence summary
   - Suggestions for field testing or piloting
   - Revision notes for items that need refinement

7. ADMINISTRATION GUIDE
   - Pre-assessment checklist for teachers
   - Administration script (what to say, timing cues)
   - Prohibited items and policies
   - Emergency procedures (technology failure, student illness)
   - Post-assessment procedures (collection, scoring timeline, return policy)

FORMAT the assessment as a complete, ready-to-administer package. Use clear item numbering, consistent formatting, and separate the student-facing materials from the teacher scoring guide.
```

## Example
### Original Prompt
```text
Create a test on the water cycle for 7th graders.
```

### Enhanced Prompt
```text
You are an expert assessment designer with expertise in psychometrics, Bloom's Taxonomy, authentic assessment, rubric design, and fairness in testing. Transform the following learning objectives into a complete, valid, reliable, and fair assessment package.

OBJECTIVES TO ASSESS:
- Students can identify the four main stages of the water cycle
- Students can explain how each stage contributes to the cycle
- Students can predict how changes in one stage affect the entire cycle
- Students can apply water cycle concepts to real-world scenarios (weather, agriculture, climate)

LEVEL: 7th grade general science. PURPOSE: Summative unit assessment. CONTEXT: 40-minute class period, paper-based, no notes or textbooks. CLASS OF 30 students with varying abilities.

PRODUCE THE FOLLOWING ASSESSMENT COMPONENTS:

1. ASSESSMENT BLUEPRINT
2. ITEM BANK
3. RUBRIC DESIGN
4. FAIRNESS AND VALIDITY CHECK
5. SCORING AND INTERPRETATION
6. QUALITY ASSURANCE
7. ADMINISTRATION GUIDE

FORMAT the assessment as a complete, ready-to-administer package. Use clear item numbering and separate student-facing materials from teacher scoring guide.
```

## Notes
- The alignment matrix ensures every objective is assessed and no objective is assessed too many times.
- Distractor analysis for multiple choice items is critical — it separates rigorous item design from lazy item writing.
- The rubric design section prevents the common AI mistake of producing vague rubrics ("good," "adequate," "poor").
- Fairness and validity checks are not optional — they're essential for ethical assessment.
- The administration guide ensures the assessment is implemented consistently across classrooms.

## Tags
`assessment-design`, `rubrics`, `psychometrics`, `bloom-taxonomy`, `fair-testing`, `validity`, `reliability`, `item-design`, `scoring`, `educational-measurement`
