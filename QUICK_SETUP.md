# Quick Setup Guide

Get the patient_interview skill working in under 2 minutes!

## For Your Specific Agent: `agent-a77c3048-1987-4713-b8ff-cdf58a86cd5c`

### Step 1: Clone into Your Project Directory (1 minute)

```bash
cd "/Users/bstern03/Library/CloudStorage/Box-Box/Letta/PT Tutor/Clinical_Instructor"

# If you haven't already cloned:
git clone https://github.com/sternb12/patient_interview.git

# The .skills/ directory is now ready!
```

### Step 2: Verify the Skill Files (10 seconds)

```bash
ls -la .skills/patient_interview/SKILL.md
```

You should see:
```
.skills/patient_interview/SKILL.md
```

### Step 3: Test with Your Agent (30 seconds)

```bash
# Open Letta with your agent
letta --agent agent-a77c3048-1987-4713-b8ff-cdf58a86cd5c

# Or just:
letta
```

### Step 4: Ask a Test Question

In the Letta CLI, type:

```
I have a 45-year-old patient with shoulder pain. What should I ask during the interview?
```

**Expected Response:**

The agent should:
1. Load the skill: `Skill(command="load", skills=["patient_interview"])`
2. Ask a Socratic question: "What do you already know about shoulder pain in a patient this age?"
3. Wait for your response and adapt accordingly

---

## Troubleshooting

### Problem: "Skill not found"

**Solution 1: Check the path**
```bash
cd "/Users/bstern03/Library/CloudStorage/Box-Box/Letta/PT Tutor/Clinical_Instructor"
ls .skills/patient_interview/
```

**Solution 2: Copy the .skills directory**
```bash
# If .skills/ doesn't exist in your project
mkdir -p .skills
cp -r patient_interview/.skills/patient_interview .skills/
```

### Problem: Agent doesn't load the skill automatically

**Solution: Explicitly tell it**
```
Please load the patient_interview skill and help me with a patient interview question.
```

### Problem: Agent says "I don't have access to that tool"

**Solution: Check if Skill tool is attached**

Via Letta UI (https://app.letta.com):
1. Find agent: `agent-a77c3048-1987-4713-b8ff-cdf58a86cd5c`
2. Settings → Tools
3. Ensure "Skill" tool is present
4. If not, add it

Or via CLI:
```bash
letta agent info agent-a77c3048-1987-4713-b8ff-cdf58a86cd5c
```

Look for "Skill" in the tools list.

---

## Quick Test Scenarios

Once working, try these:

### Test 1: Basic Interview Question
```
I have a 68-year-old woman with constant low back pain. What should I ask?
```

**Expected**: Agent guides you through red flag screening

### Test 2: ECHOWS Feedback
```
Can you give me feedback on my patient interview using the ECHOWS framework?
```

**Expected**: Agent asks you to self-assess first (Socratic approach)

### Test 3: Communication Skills
```
My patient seemed uncomfortable during the interview. What might I have done wrong?
```

**Expected**: Agent references ECHOWS S section (Summary of Performance)

---

## Success Indicators

✅ Agent loads skill without errors  
✅ Agent asks Socratic questions (Level 1) first  
✅ Agent references ECHOWS components (E, C, H, O, W, S)  
✅ Agent provides progressive support based on your responses  
✅ Agent emphasizes patient safety and red flags  
✅ Agent unloads skill when done  

---

## Next Steps After Setup

1. **Practice**: Try different scenarios from `examples/worked_scenarios.md`
2. **Explore**: Read `SKILL.md` to understand the full capability
3. **Customize**: Modify the skill for your specific needs
4. **Share**: Help colleagues set it up using this guide

---

## Need Help?

- **Issues**: https://github.com/sternb12/patient_interview/issues
- **Documentation**: See main README.md
- **Contact**: Ben Stern, Tufts University DPT Program

---

**Estimated total setup time**: 2 minutes
**Difficulty**: Beginner-friendly
**Prerequisites**: Letta Code 0.7.2+, Git

🎓 **You're ready to use AI-powered Socratic teaching for patient interviewing!**
