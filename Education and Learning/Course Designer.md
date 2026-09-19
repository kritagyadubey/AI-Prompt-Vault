# Course Designer
> Transforms vague course ideas into structured, comprehensive curricula with clear learning pathways, assessments, and outcomes.

## Purpose
This enhancer takes a rough course concept and expands it into a full pedagogical framework. It ensures that the AI produces a curriculum that is logically sequenced, scaffolded for learner progression, aligned with learning objectives, and includes diverse assessment methods. It prevents the AI from producing shallow, unstructured course outlines by enforcing domain-specific instructional design principles.

## Best For
- University instructors designing new courses
- Corporate L&D teams building training programs
- Online course creators structuring content for platforms like Coursera or Udemy
- Instructional designers creating competency-based programs
- Anyone transitioning a topic outline into a teachable course

## Prompt Enhancer
```text
You are an expert instructional designer and curriculum architect with deep expertise in backward design (Wiggins & McTighe), constructive alignment, Bloom's Taxonomy, and universal design for learning (UDL). Transform the following course concept into a comprehensive, production-ready course design.

ANALYZE THE INPUT:
- Identify the target learner profile (prior knowledge, motivations, constraints)
- Determine appropriate course level (introductory, intermediate, advanced, professional)
- Infer the likely delivery modality if not specified (in-person, online synchronous, asynchronous, hybrid)
- Flag any gaps in the input that would critically affect design decisions

PRODUCE THE FOLLOWING SECTIONS:

1. COURSE IDENTITY
   - Course title (suggest 3 options: descriptive, creative, professional)
   - Course subtitle and one-paragraph description
   - Estimated total hours (contact hours + self-study)
   - Prerequisites and recommended prior knowledge
   - Target enrollment size implications on pedagogy

2. LEARNING OUTCOMES
   - Write 5-8 terminal learning outcomes using measurable verbs from Bloom's Taxonomy
   - For each terminal outcome, list 2-4 enabling objectives that scaffold toward it
   - Map each outcome to Bloom's level (Remember, Understand, Apply, Analyze, Evaluate, Create)
   - Include at least one outcome at each Bloom's level from Apply upward

3. COURSE ARCHITECTURE
   - Break the course into modules/units (recommend 6-12 depending on scope)
   - For each module, provide: title, essential question, duration, key concepts, and how it connects to adjacent modules
   - Show the dependency chain — which modules require completion of prior modules
   - Identify natural "checkpoints" where formative assessment should occur

4. CONTENT MAPPING
   - For each module, list: topics covered, core concepts, skills practiced, and common misconceptions to address
   - Suggest primary and supplementary resource types (textbook chapters, articles, videos, interactive elements)
   - Note where real-world case studies, examples, or problem sets are essential

5. ASSESSMENT STRATEGY
   - Design a balanced assessment plan with formative and summative components
   - For each assessment: type, weight, aligned learning outcome, rubric criteria summary, and estimated student effort
   - Include at least one authentic/performative assessment (project, portfolio, presentation, simulation)
   - Specify formative checkpoints within each module (quizzes, reflections, peer reviews)
   - Calculate the total assessment workload and flag if it exceeds reasonable student effort

6. PEDAGOGICAL APPROACH
   - Recommend teaching strategies for each module (lecture, discussion, lab, flipped, PBL, case study)
   - Suggest active learning techniques appropriate to the content
   - Identify opportunities for collaborative learning and peer interaction
   - Address how to handle diverse learners (differentiation strategies)

7. LEARNING RESOURCES
   - Recommend a core textbook or primary resource with justification
   - List supplementary resources organized by module
   - Suggest technology tools (LMS features, simulation software, collaboration platforms)
   - Note any OER (Open Educational Resources) alternatives if applicable

8. IMPLEMENTATION NOTES
   - Week-by-week pacing guide if applicable
   - Faculty/instructor preparation requirements
   - Technical infrastructure needs
   - Risk factors (content complexity, student preparation gaps, time constraints)

FORMAT each section with clear headings. Use tables where comparison or mapping is needed. Write in a professional, actionable tone suitable for a course proposal document.
```

## Example
### Original Prompt
```text
Design a course on data science for beginners.
```

### Enhanced Prompt
```text
You are an expert instructional designer and curriculum architect with deep expertise in backward design (Wiggins & McTighe), constructive alignment, Bloom's Taxonomy, and universal design for learning (UDL). Transform the following course concept into a comprehensive, production-ready course design.

COURSE CONCEPT: A beginner-friendly data science course. Target audience is professionals with basic math skills but no programming experience. Should be practical and job-ready.

ANALYZE THE INPUT:
- Identify the target learner profile (prior knowledge, motivations, constraints)
- Determine appropriate course level (introductory, intermediate, advanced, professional)
- Infer the likely delivery modality if not specified (in-person, online synchronous, asynchronous, hybrid)
- Flag any gaps in the input that would critically affect design decisions

PRODUCE THE FOLLOWING SECTIONS:

1. COURSE IDENTITY
   - Course title (suggest 3 options: descriptive, creative, professional)
   - Course subtitle and one-paragraph description
   - Estimated total hours (contact hours + self-study)
   - Prerequisites and recommended prior knowledge
   - Target enrollment size implications on pedagogy

2. LEARNING OUTCOMES
   - Write 5-8 terminal learning outcomes using measurable verbs from Bloom's Taxonomy
   - For each terminal outcome, list 2-4 enabling objectives that scaffold toward it
   - Map each outcome to Bloom's level (Remember, Understand, Apply, Analyze, Evaluate, Create)
   - Include at least one outcome at each Bloom's level from Apply upward

3. COURSE ARCHITECTURE
   - Break the course into modules/units (recommend 6-12 depending on scope)
   - For each module, provide: title, essential question, duration, key concepts, and how it connects to adjacent modules
   - Show the dependency chain — which modules require completion of prior modules
   - Identify natural "checkpoints" where formative assessment should occur

4. CONTENT MAPPING
   - For each module, list: topics covered, core concepts, skills practiced, and common misconceptions to address
   - Suggest primary and supplementary resource types (textbook chapters, articles, videos, interactive elements)
   - Note where real-world case studies, examples, or problem sets are essential

5. ASSESSMENT STRATEGY
   - Design a balanced assessment plan with formative and summative components
   - For each assessment: type, weight, aligned learning outcome, rubric criteria summary, and estimated student effort
   - Include at least one authentic/performative assessment (project, portfolio, presentation, simulation)
   - Specify formative checkpoints within each module (quizzes, reflections, peer reviews)
   - Calculate the total assessment workload and flag if it exceeds reasonable student effort

6. PEDAGOGICAL APPROACH
   - Recommend teaching strategies for each module (lecture, discussion, lab, flipped, PBL, case study)
   - Suggest active learning techniques appropriate to the content
   - Identify opportunities for collaborative learning and peer interaction
   - Address how to handle diverse learners (differentiation strategies)

7. LEARNING RESOURCES
   - Recommend a core textbook or primary resource with justification
   - List supplementary resources organized by module
   - Suggest technology tools (LMS features, simulation software, collaboration platforms)
   - Note any OER (Open Educational Resources) alternatives if applicable

8. IMPLEMENTATION NOTES
   - Week-by-week pacing guide if applicable
   - Faculty/instructor preparation requirements
   - Technical infrastructure needs
   - Risk factors (content complexity, student preparation gaps, time constraints)

FORMAT each section with clear headings. Use tables where comparison or mapping is needed. Write in a professional, actionable tone suitable for a course proposal document.
```

## Notes
- The enhancer enforces backward design principles, preventing the common AI mistake of listing topics without tying them to outcomes.
- Bloom's Taxonomy mapping ensures cognitive rigor is distributed across the course.
- The assessment workload calculation prevents overloading students, a frequent oversight in AI-generated curricula.
- Works best when the user provides even minimal context about audience and goals; the enhancer will flag underspecified inputs.

## Tags
`curriculum-design`, `instructional-design`, `bloom-taxonomy`, `backward-design`, `assessment-strategy`, `higher-education`, `course-development`, `learning-outcomes`, `UDL`, `pedagogy`
