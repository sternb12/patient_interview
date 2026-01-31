# Patient Interview Coaching Skill

**A Letta AI skill for teaching DPT students patient interviewing using the validated ECHOWS framework and Socratic methodology**

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Version](https://img.shields.io/badge/version-1.0.0-green.svg)](https://github.com/sternb12/patient_interview/releases)

## Overview

This skill enables AI clinical instructor agents to guide Doctor of Physical Therapy (DPT) students through patient-centered interviewing using evidence-based teaching methods. Built on the validated ECHOWS framework (Boissonnault & Boissonnault, 2016), it employs a 5-level Socratic teaching approach that promotes independent clinical reasoning.

### What is ECHOWS?

**ECHOWS** is a validated 42-point assessment tool for evaluating physical therapy student patient interviewing skills:
- **E**: Establish Rapport
- **C**: Chief Complaint
- **H**: Health History
- **O**: Obtain Psychosocial Perspective
- **W**: Wrap-up
- **S**: Summary of Performance

**Research validation**: Excellent intrarater reliability (ICC 0.74-0.89), moderate interrater reliability (ICC 0.55)

## Features

✅ **Evidence-Based**: Built on validated ECHOWS tool with published reliability data  
✅ **Socratic Teaching**: 5-level progressive support (question → hint → example → direct guidance)  
✅ **Comprehensive**: 67KB of instructional content covering all interview scenarios  
✅ **Practical**: Ready to use with Letta AI agents today  
✅ **Educational**: Integrates course content (lectures, textbooks, red flag protocols)  
✅ **Safe**: Emphasizes patient safety and red flag screening

## Quick Start

### Prerequisites

- [Letta Code](https://docs.letta.com/letta-code/index.md) v0.7.2 or higher
- Python 3.8+
- Git

### Installation

**Option 1: Clone to Letta Skills Directory**
```bash
# Clone this repository
git clone https://github.com/sternb12/patient_interview.git

# Copy to your Letta skills directory
cp -r patient_interview/skills/patient_interview ~/.letta/skills/

# Verify installation
letta
# The skill should appear in your available skills
```

**Option 2: Clone to Project-Specific Directory**
```bash
# In your Letta project directory
mkdir -p .skills
cd .skills
git clone https://github.com/sternb12/patient_interview.git
cp -r patient_interview/skills/patient_interview ./
```

### Usage

**Load the skill in your agent:**
```
Skill(command="load", skills=["patient_interview"])
```

**Example interaction:**
```
Student: "I have a 45-year-old patient with shoulder pain. What should I ask?"

Agent: [Loads patient_interview skill]
       "Let's start with what you already know. What do you think is 
        important to understand about shoulder pain in a patient this age?"

[Progresses through Socratic ladder based on student responses]
```

**Unload when done:**
```
Skill(command="unload", skills=["patient_interview"])
```

## Skill Contents

```
skills/patient_interview/
├── SKILL.md (28KB)              # Main skill instructions
│   ├── YAML frontmatter
│   ├── Research foundation
│   ├── 5-Level Socratic Ladder
│   ├── Complete ECHOWS framework (42 points)
│   ├── Course content integration
│   └── Progressive teaching examples
│
├── README.md (4.5KB)            # Skill overview
├── NEXT_STEPS.md (9.5KB)        # Implementation & testing guide
│
├── examples/
│   └── worked_scenarios.md (18KB)  # 4 detailed teaching scenarios
│
└── references/
    └── echows_quick_ref.md (6.5KB) # Quick reference checklist
```

## Teaching Approach: 5-Level Socratic Ladder

The skill uses progressive support that adapts to student needs:

| Level | When to Use | Example |
|-------|-------------|---------|
| **Level 1: Reflective Question** | Always start here | "What stands out to you about this presentation?" |
| **Level 2: Focused Question** | Student tries but is partially correct | "Which ECHOWS section addresses rapport?" |
| **Level 3: Hint** | Student needs direction | "Patient-centered means acknowledging emotions first..." |
| **Level 4: Example** | Student needs concrete illustration | "You might say: 'I can see you're upset...'" |
| **Level 5: Direct Guidance** | Safety issue or critical learning | "STOP: These are red flags requiring physician contact..." |

**Key Principle**: Start with questions to promote thinking. Provide answers only when necessary for learning or safety.

## ECHOWS Framework (42 Points)

### ECHOW Sections (22 points, observed/not observed)
- **E**: Establish Rapport (2 items)
- **C**: Chief Complaint (6 items)
- **H**: Health History (9 items)
- **O**: Obtain Psychosocial Perspective (3 items)
- **W**: Wrap-up (2 items)

### S Section (20 points, scored 0-2 each)
10 skill items including:
- Questioning strategies
- Verbal communication
- Attentive listening
- Nonverbal behavior
- Time management

## Example Scenarios

### Scenario 1: Student Asks About Interview Approach
```
Student: "I have a 55-year-old patient who is coughing and very angry. What should I ask?"

Agent (Level 1): "What stands out about this presentation—both the cough and the anger?"

[If student identifies both elements correctly]
Agent: "Good! Now, thinking about ECHOWS, how would you address her emotional state?"

[If student is stuck]
Agent (Level 3): "Remember: patient-centered interviewing means acknowledging 
                  emotions before clinical details..."

[If still needs help]
Agent (Level 4): "You might start with: 'I can see you're upset. Before we talk 
                  about your cough, can you tell me what's most frustrating?'"
```

### Scenario 2: Red Flag Identification
```
Student: "68-year-old with constant back pain unrelieved by position. What should I do?"

Agent (Level 1): "What concerns you about this presentation?"

Student: "The age and that it doesn't change with position?"

Agent (Level 2): "Excellent observations! What does constant pain unrelieved by 
                  position suggest about mechanical vs non-mechanical causes?"

[Guides through red flag screening using ECHOWS H, item 1: constitutional symptoms]

Agent (Level 5 - if safety missed): "This requires physician referral BEFORE physical 
                                     therapy because multiple red flags are present..."
```

## Research Foundation

### Primary Source
Boissonnault JS, Evans K, Tuttle N, Hetzel SJ, Boissonnault WG. **Reliability of the ECHOWS tool for assessment of patient interviewing skills.** *Phys Ther.* 2016;96(4):443-455. [doi:10.2522/ptj.20150172](https://doi.org/10.2522/ptj.20150172)

### Key Findings
- **Intrarater reliability**: ICC 0.74-0.89 (excellent)
- **Interrater reliability**: ICC 0.55 (moderate overall), 0.82 (excellent for ECHOW sections)
- **Validity**: Content validity established, construct validity assessed
- **International**: Tested with US and Australian students and faculty

### Course Content Integration
- Primary Care lecture transcripts (Weeks 1-13)
- Boissonnault WG, ed. *Primary Care for the Physical Therapist: Examination and Triage.* 2nd ed.
- McKinnis LN. *Fundamentals of Musculoskeletal Imaging.*
- Red flag screening protocols from Ch 20: "Nine Do Not Want to Miss Conditions"

## Use Cases

### For Faculty
- Consistent feedback on student interviews
- Automated initial assessment with ECHOWS framework
- Socratic questioning reduces repetitive teaching
- Frees time for higher-level clinical reasoning discussions

### For Clinical Instructors
- Standardized teaching approach across sites
- Evidence-based framework familiar to students
- Reduces subjectivity in feedback
- Provides structure for formative assessment

### For Students
- Self-assessment using familiar ECHOWS framework
- Immediate feedback on interview technique
- Socratic approach promotes independent thinking
- Accessible 24/7 for practice and review

## Testing

See [`skills/patient_interview/NEXT_STEPS.md`](skills/patient_interview/NEXT_STEPS.md) for complete testing guide.

**Quick Test**:
```bash
# In Letta CLI
letta

# Test basic functionality
> "I have a patient with knee pain. What should I ask?"

# Expected: Agent loads skill and starts with Level 1 reflective question
```

## Configuration

### Memory Blocks Needed

The clinical instructor agent should have these memory blocks:
- `human`: Student context and progress
- `persona`: Clinical instructor role and teaching philosophy
- `skills`: Available skills catalog (auto-populated)
- `loaded_skills`: Active skill content (managed by Skill tool)

### Example Agent Configuration

```yaml
agent_name: clinical_instructor
system_prompt: |
  You are a clinical instructor teaching DPT students patient interviewing.
  Use Socratic questioning to promote independent thinking.
  Reference ECHOWS framework for structured feedback.
  Prioritize patient safety in all teaching.
  
tools:
  - memory
  - conversation_search
  - Skill (for loading/unloading skills)
  
skills_directory: .skills/
```

## Contributing

Contributions welcome! Areas for enhancement:
- Additional worked scenarios
- Video case examples
- Specialty-specific variations (pediatrics, geriatrics, sports)
- Integration with documentation systems
- Expanded red flag decision trees
- Multilingual support

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

## Citation

If you use this skill in teaching or research, please cite:

```bibtex
@software{stern2026patient_interview_skill,
  author = {Stern, Benjamin},
  title = {Patient Interview Coaching Skill for AI Clinical Instructors},
  year = {2026},
  publisher = {GitHub},
  url = {https://github.com/sternb12/patient_interview},
  note = {Based on ECHOWS framework by Boissonnault \& Boissonnault (2016)}
}
```

**ECHOWS Tool Citation**:
```bibtex
@article{boissonnault2016echows,
  title={Reliability of the ECHOWS tool for assessment of patient interviewing skills},
  author={Boissonnault, Jill S and Evans, Kerrie and Tuttle, Neil and Hetzel, Scott J and Boissonnault, William G},
  journal={Physical Therapy},
  volume={96},
  number={4},
  pages={443--455},
  year={2016},
  publisher={Oxford University Press}
}
```

## License

This project is licensed under the Apache License 2.0 - see the [LICENSE](LICENSE) file for details.

**IMPORTANT**: The ECHOWS tool itself is property of Jill S. Boissonnault and William G. Boissonnault, University of Wisconsin-Madison. This skill provides teaching guidance based on the published framework and does not redistribute the copyrighted assessment tool.

## Acknowledgments

- **ECHOWS Framework**: Jill S. Boissonnault, PT, PhD, WCS and William G. Boissonnault, PT, DPT, DHSc, FAAOMPT, FAPTA, University of Wisconsin-Madison
- **Research Foundation**: Physical Therapy journal article (2016;96(4):443-455)
- **Course Content**: Primary Care textbook (Boissonnault WG, ed.) and lecture materials
- **Technical Platform**: [Letta AI](https://letta.com) and [Agent Skills](https://agentskills.io) framework
- **AI Assistance**: Skill development supported by Trace (Letta Code agent)

## Contact

**Primary Author**: Benjamin Stern, DPT  
**Institution**: Tufts University, Doctor of Physical Therapy Program  
**Email**: [Your contact email]  
**Repository**: https://github.com/sternb12/patient_interview

## Version History

- **v1.0.0** (January 31, 2026): Initial release
  - Complete ECHOWS integration (42 points)
  - 5-level Socratic Ladder implementation
  - 4 worked teaching scenarios
  - Course content integration
  - Quick reference guide

## Roadmap

**Planned for v1.1**:
- [ ] Additional worked scenarios (n=10 total)
- [ ] Video case integration
- [ ] Specialty variations (peds, geriatrics, sports)
- [ ] Self-assessment tools for students
- [ ] Expanded red flag decision trees
- [ ] Spanish language support

**Planned for v2.0**:
- [ ] Integration with clinical documentation systems
- [ ] Automated ECHOWS scoring from transcripts
- [ ] Multi-agent teaching scenarios
- [ ] Peer assessment capabilities
- [ ] Analytics dashboard for student progress

---

## Quick Links

- [Main Skill File](skills/patient_interview/SKILL.md)
- [Worked Examples](skills/patient_interview/examples/worked_scenarios.md)
- [ECHOWS Quick Reference](skills/patient_interview/references/echows_quick_ref.md)
- [Implementation Guide](skills/patient_interview/NEXT_STEPS.md)
- [Issues](https://github.com/sternb12/patient_interview/issues)
- [Discussions](https://github.com/sternb12/patient_interview/discussions)

---

**Made with ❤️ for DPT education** | Powered by [Letta AI](https://letta.com)
