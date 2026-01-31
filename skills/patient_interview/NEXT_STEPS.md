# Patient Interview Skill - Next Steps

**Created**: January 31, 2026  
**Status**: ✅ Complete and ready for testing

## What We Built

### 1. Complete Skill Package

```
patient_interview_skill/
├── SKILL.md (28KB)
│   └── Complete instructions with:
│       • YAML frontmatter
│       • ECHOWS framework (accurate from Appendices 1 & 2)
│       • 5-level Socratic Ladder
│       • Domain-specific guidance from course content
│       • Red flag screening protocols
│       • Worked examples
│
├── README.md (4.5KB)
│   └── Overview, usage, research foundation
│
├── examples/
│   └── worked_scenarios.md (18KB)
│       • 4 complete teaching scenarios
│       • Socratic progression examples
│       • Before/after communication examples
│
└── references/
    └── echows_quick_ref.md (6.6KB)
        • Complete ECHOWS checklist
        • Scoring guidelines
        • Quick reference for all 42 points
```

**Total**: ~57KB of instructional content

---

## Key Features

### ✅ ECHOWS Accuracy
- All details verified against Appendices 1 & 2
- Correct item counts (E:2, C:6, H:9, O:3, W:2, S:10)
- Accurate scoring (0-1-2 for S section, observed/not observed for ECHOW)
- Complete sub-items (e.g., 9 body systems in H, item 2)

### ✅ Socratic Teaching Method
- 5-level progressive ladder
- Always starts with reflective questions
- Escalates only when needed
- Direct guidance reserved for safety issues

### ✅ Course Content Integration
- References Week 1-13 lecture transcripts
- Integrates Ch 5 (Symptom Investigation), Ch 8 (Health History), Ch 20 (Red Flags)
- Incorporates primary care screening principles
- Medical vs musculoskeletal differentiation

### ✅ Evidence-Based
- Built on validated ECHOWS tool (Boissonnault & Boissonnault, 2016)
- Reliability data included (ICC 0.74-0.89 intrarater, 0.55 interrater)
- Research foundation documented

---

## Next Steps for Implementation

### Phase 1: Local Testing (Recommended First)

**Option A: Test with Current Letta Agent**

1. **Copy skill to .letta directory**:
   ```bash
   cp -r patient_interview_skill /Users/bstern03/Library/CloudStorage/Box-Box/Letta/PT\ Tutor/Clinical_Instructor/.skills/
   ```

2. **Verify skill discovery**:
   - Open Letta CLI in this directory
   - Check if skill appears in available skills

3. **Test with agent**:
   - Ask agent for help with patient interview
   - Agent should load skill and use Socratic approach
   - Verify ECHOWS framework usage

**Option B: Create New Clinical Instructor Agent**

1. **Create agent with patient_interview skill pre-loaded**
2. **Configure memory blocks**:
   - `human`: Student context
   - `persona`: Clinical instructor role
   - `skills`: Available skills catalog
   - `loaded_skills`: When skill is loaded

3. **Test scenarios**:
   - "I have a patient with back pain. What should I ask?"
   - "How did I do on my interview?" (provide transcript)
   - "What are red flags for chest pain?"

### Phase 2: GitHub Repository (For Distribution)

**1. Create Repository Structure**:
```
patient-interview-skill/
├── README.md
├── LICENSE
├── skills/
│   └── patient_interview/
│       ├── SKILL.md
│       ├── examples/
│       │   └── worked_scenarios.md
│       └── references/
│           └── echows_quick_ref.md
└── docs/
    ├── SETUP_GUIDE.md
    └── TESTING_GUIDE.md
```

**2. Add Documentation**:
- Setup instructions for other faculty
- Testing protocols
- Contribution guidelines
- Citation requirements (ECHOWS is copyrighted)

**3. Push to GitHub**:
```bash
cd /path/to/new/repo
git init
git add .
git commit -m "Initial commit: Patient interview skill v1.0"
git remote add origin https://github.com/YOUR_USERNAME/patient-interview-skill.git
git push -u origin main
```

**4. Distribution**:
- Share repository link with colleagues
- Create installation instructions
- Provide example agent configurations

### Phase 3: Refinement Based on Testing

**Gather Feedback On**:
- Student response to Socratic approach
- ECHOWS component coverage
- Appropriateness of examples
- Missing edge cases
- Course content integration

**Potential Enhancements**:
- Video case examples
- Additional worked scenarios
- Specialty-specific variations (pediatrics, geriatrics)
- Integration with documentation systems
- Standardized patient scripts

---

## Testing Checklist

### Functional Testing

- [ ] Skill loads successfully
- [ ] Agent recognizes when to load skill
- [ ] Agent uses Socratic questioning (Level 1 first)
- [ ] Agent progresses through levels appropriately
- [ ] Agent references ECHOWS framework correctly
- [ ] Agent provides accurate red flag guidance
- [ ] Agent references course content (transcripts, chapters)
- [ ] Agent unloads skill when appropriate

### Content Testing

- [ ] All ECHOWS components accurate (E, C, H, O, W, S)
- [ ] Scoring explained correctly (0-1-2 for S, observed/not for ECHOW)
- [ ] Red flags appropriate for body regions
- [ ] Course content references are accurate
- [ ] Examples are clear and helpful
- [ ] Edge cases handled appropriately

### Pedagogical Testing

- [ ] Socratic approach promotes thinking
- [ ] Progressive support feels natural
- [ ] Students engage rather than passively receive
- [ ] Feedback is constructive
- [ ] Examples are contextually appropriate
- [ ] Direct guidance used sparingly (safety only)

---

## Example Test Prompts

Use these to test the skill:

**Test 1: Basic Interview Help**
```
Student: "I have a 45-year-old patient with shoulder pain. What should I ask?"
Expected: Agent starts with Level 1 reflective question
```

**Test 2: ECHOWS Feedback**
```
Student: "Can you review my interview using ECHOWS?"
Expected: Agent asks student to self-assess first (Level 1)
```

**Test 3: Red Flag Recognition**
```
Student: "68-year-old with constant back pain unrelieved by position. What do I do?"
Expected: Agent guides toward red flag recognition, escalates to Level 5 if safety missed
```

**Test 4: Communication Skills**
```
Student: "The patient seemed uncomfortable. Did I do something wrong?"
Expected: Agent references ECHOWS S section, uses video review
```

**Test 5: Emotional Situation**
```
Student: "My patient is crying. How should I handle this?"
Expected: Agent emphasizes rapport (ECHOWS E), empathy (ECHOWS S, item 10)
```

---

## Success Criteria

### The skill is working well if:

1. **Agent behavior**:
   - ✅ Always starts with questions, not answers
   - ✅ Adapts teaching level to student responses
   - ✅ References specific ECHOWS components
   - ✅ Cites course content appropriately
   - ✅ Prioritizes patient safety

2. **Student outcomes**:
   - ✅ Students think independently before answers provided
   - ✅ Students can explain reasoning, not just repeat facts
   - ✅ Students feel supported, not judged
   - ✅ Students improve interview skills over time
   - ✅ Students develop clinical reasoning abilities

3. **Practical utility**:
   - ✅ Faculty find it useful for teaching
   - ✅ Clinical instructors adopt it
   - ✅ Reduces repetitive teaching burden
   - ✅ Provides consistent feedback
   - ✅ Saves time while improving quality

---

## Questions to Consider

1. **Should we create variations for different student levels?**
   - Entry-level (first exposure to interviewing)
   - Advanced (preparing for clinical internships)
   - Struggling students (need more scaffolding)

2. **Should we add simulation scenarios?**
   - Written case vignettes
   - Standardized patient scripts
   - Video case examples

3. **How do we handle cultural/regional variations?**
   - Some ECHOWS items may need cultural adaptation
   - Regional differences in health history emphasis
   - Different patient populations

4. **Integration with other skills?**
   - Physical examination skill
   - Clinical reasoning skill
   - Documentation skill
   - Red flag decision-making skill

---

## Resources

### ECHOWS Tool
- **Source**: Boissonnault JS, Evans K, Tuttle N, Hetzel SJ, Boissonnault WG. Reliability of the ECHOWS tool for assessment of patient interviewing skills. Phys Ther. 2016;96(4):443-455.
- **Copyright**: Property of Jill S. Boissonnault and William G. Boissonnault, University of Wisconsin-Madison
- **Note**: Cite appropriately in any publications or presentations

### Course Content
- Lecture transcripts (Weeks 1-13 Primary Care)
- Primary Care textbook chapters
- McKinnis's Fundamentals of Musculoskeletal Imaging
- Red flag screening guidelines

### Skills Development Resources
- Agent Skills standard (agentskills.io)
- Drawing-memory skill (as template)
- Letta documentation (docs.letta.com)

---

## Contact & Contributions

**Primary Author**: Ben Stern, DPT  
**Institution**: Tufts University, Doctor of Physical Therapy Program

**Contributions Welcome**:
- Bug reports
- Enhancement suggestions
- Additional worked examples
- Course content integration ideas
- Testing feedback

**Citation**:
If you use this skill in teaching or research, please cite:
```
Stern B. (2026). Patient Interview Coaching Skill for AI Clinical Instructors. 
Based on ECHOWS framework by Boissonnault & Boissonnault (2016).
```

---

## Version History

**v1.0** (January 31, 2026)
- Initial release
- Complete ECHOWS integration
- 5-level Socratic Ladder
- Course content integration
- 4 worked scenarios
- ECHOWS quick reference

**Planned for v1.1**:
- Additional worked scenarios
- Video case integration
- Specialty variations
- Self-assessment tools for students
- Expanded red flag decision trees

