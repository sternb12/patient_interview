# Patient Interview Coaching Skill

**Version**: 1.0  
**Created**: January 31, 2026  
**Author**: Ben Stern, DPT (with Trace AI assistance)

## Overview

This skill enables clinical instructor agents to guide DPT students through patient-centered interviewing using the validated ECHOWS framework and Socratic teaching methodology.

## What This Skill Does

- **Socratic questioning**: Promotes independent thinking before providing answers
- **ECHOWS framework integration**: Uses validated 42-point assessment tool
- **Progressive support**: Escalates from questions → hints → examples → direct guidance only when needed
- **Evidence-based feedback**: References course transcripts, textbook chapters, and ECHOWS criteria
- **Red flag awareness**: Emphasizes patient safety and medical screening

## When to Use

Load this skill when students need help with:
- Patient interview techniques
- History taking and documentation
- Establishing rapport with patients
- Clinical reasoning and red flag identification
- ECHOWS component completion

## Research Foundation

Based on:
- **ECHOWS tool** (Boissonnault & Boissonnault, 2016): Excellent intrarater reliability (ICC 0.74-0.89)
- **Patient-centered interviewing**: Open-ended questions, active listening, cultural sensitivity
- **Medical screening principles**: Differentiating musculoskeletal from systemic causes
- **Socratic teaching**: Develops clinical reasoning, not just knowledge transfer

## Skill Components

### ECHOWS Framework (42 points total)
- **E**: Establish Rapport (2 items)
- **C**: Chief Complaint (6 items)
- **H**: Health History (9 items)
- **O**: Obtain Psychosocial Perspective (3 items)
- **W**: Wrap-up (2 items)
- **S**: Summary of Performance (10 skills, scored 0-2 each = 20 points)

### Teaching Approach: 5-Level Socratic Ladder
1. **Reflective Question**: Student thinks first
2. **Focused Question**: Guide thinking without answers
3. **Hint**: Provide direction, point to frameworks
4. **Example**: Show concrete samples
5. **Direct Guidance**: Only for safety or critical issues

## Course Content Integration

This skill references:
- **Lecture transcripts** (Weeks 1-13 Primary Care)
- **Textbook chapters** (Ch 5: Symptom Investigation, Ch 6: Chief Complaint by Symptom, Ch 8: Patient Health History, Ch 12-13: Screening Exams, Ch 20: Nine Do Not Miss Conditions)
- **McKinnis chapters** (Imaging principles and interpretation)
- **ECHOWS tool and Guide** (Appendices 1 & 2 from research article)

## Files in This Skill

```
patient_interview_skill/
├── SKILL.md                    # Main skill instructions (28KB)
├── README.md                   # This file
├── examples/
│   └── worked_scenarios.md     # Detailed teaching examples
└── references/
    ├── echows_quick_ref.md     # Quick reference for ECHOWS items
    └── red_flags_by_region.md  # Red flag screening guide
```

## Usage Example

```
User: "I have a 45-year-old patient with abdominal pain. What should I ask?"

Agent: [Loads patient_interview skill]

Agent (Level 1—Socratic): "Before jumping to questions, what's the first thing you want to establish when meeting this patient?"

[Progresses through Socratic ladder based on student responses]
```

## Loading & Unloading

**Load:**
```
Skill(command="load", skills=["patient_interview"])
```

**Unload:**
```
Skill(command="unload", skills=["patient_interview"])
```

## Design Philosophy

**Key Principle**: Clinical instructors should develop clinical reasoners, not just provide answers.

- Start with **questions** to promote thinking
- Provide **hints and examples** to guide learning
- Give **direct answers** only when necessary for safety or time constraints
- Always reference **evidence-based content** (ECHOWS, textbooks, lectures)

## Validation

This skill has been designed based on:
- Validated ECHOWS tool with published reliability data
- Course content from UW-Madison DPT program
- Primary Care textbook (Boissonnault WG, ed.)
- McKinnis's Fundamentals of Musculoskeletal Imaging
- Clinical teaching best practices for health professions education

## Future Enhancements

Potential additions:
- Video case examples
- Standardized patient scenarios
- Self-assessment rubrics for students
- Integration with clinical documentation systems
- Expanded red flag decision trees

## License

Educational use only. ECHOWS tool is property of Jill S. Boissonnault and William G. Boissonnault, University of Wisconsin-Madison.

## Contact

For questions or suggestions about this skill, contact Ben Stern (DPT faculty, Tufts University).
