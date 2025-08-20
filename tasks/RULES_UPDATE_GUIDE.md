# RULES.md Update Guide for Agents

> **For AI Agents**: This guide helps you understand when and how to suggest updates to RULES.md to keep it current and useful.

## 🎯 When to Suggest RULES.md Updates

### Always Suggest Updates When:
- **New Patterns Emerge**: You discover a code pattern that should be standardized
- **Constraints Are Broken**: You notice violations that indicate missing rules
- **Bugs Could Have Been Prevented**: Issues that a rule could have caught
- **Architecture Decisions**: New architectural choices that should be documented
- **Dependency Changes**: New approved/banned libraries or frameworks
- **Performance Learnings**: New performance constraints or optimizations
- **Security Requirements**: New security patterns or constraints discovered

### Examples of Update Triggers:
```
❌ BAD: "The code works fine" 
✅ GOOD: "This pattern of extracting components after 100 lines should be in RULES.md"

❌ BAD: "I'll just fix this bug"
✅ GOOD: "This bug happened because we lack a rule about null checking - suggest adding to RULES.md"

❌ BAD: "I'll use this library for now"
✅ GOOD: "Suggest adding [library] to approved dependencies in RULES.md"
```

## 📝 How to Suggest RULES.md Updates

### 1. Identify the Category
```markdown
## RULES.md Update Suggestion

**Category**: [Architecture/Dependencies/Code Standards/UI Guidelines/Workflow/etc.]
**Priority**: [High/Medium/Low]
**Trigger**: [What caused this suggestion]
```

### 2. Provide Specific Rule Text
```markdown
**Proposed Rule Addition/Change**:
```
[Exact text to add to RULES.md]
```

**Rationale**: [Why this rule is needed]
**Location in RULES.md**: [Which section should be updated]
```

### 3. Give Context
```markdown
**Current Problem**: [What issue this solves]
**Impact**: [What happens without this rule]
**Examples**: [Code examples or scenarios]
```

## 🔄 Update Process for Agents

### During Research Phase:
1. **Read RULES.md thoroughly**
2. **Note any gaps or conflicts** while researching
3. **Document potential updates** in your research report
4. **Suggest specific rule text** in your recommendations

### When Writing Research Reports:
Include a section like this:
```markdown
## RULES.md Update Suggestions

### Suggested Addition - [Category]
**Rule**: [Exact rule text]
**Reason**: [Why this is needed]
**Section**: [Where in RULES.md this belongs]

### Suggested Change - [Category]  
**Current Rule**: [What currently exists]
**Proposed Change**: [How to modify it]
**Reason**: [Why the change is needed]
```

### In Context File Updates:
Always include:
```markdown
**RULES.md updates needed**: 
- [ ] [Specific rule about X that should be added]
- [ ] [Constraint about Y that needs clarification]
- [ ] [Pattern Z that should be standardized]
```

## 📋 Common Rule Categories to Watch For

### Architecture Rules
- Component structure patterns
- State management approaches
- Module organization principles
- Design pattern decisions

### Code Quality Rules
- File size limits (lines of code)
- Function complexity limits
- Naming conventions
- Comment requirements

### Dependency Rules
- Approved libraries and frameworks
- Banned packages and why
- Version constraints
- Bundle size considerations

### UI/UX Rules
- Design system compliance
- Accessibility requirements
- Platform guideline adherence
- Component reusability standards

### Performance Rules
- Loading time requirements
- Memory usage constraints
- Optimization guidelines
- Caching strategies

### Security Rules
- Authentication patterns
- Data handling requirements
- API security standards
- Input validation rules

### Workflow Rules
- Testing requirements
- Code review standards
- Documentation needs
- Deployment constraints

## ✅ Good Rule Writing Guidelines

### Make Rules Specific and Actionable
```
❌ BAD: "Keep components small"
✅ GOOD: "Split components when they exceed 100 lines (soft ceiling)"

❌ BAD: "Don't use too many dependencies"  
✅ GOOD: "Never add third-party packages without approval - stick to platform-native solutions"

❌ BAD: "Follow best practices"
✅ GOOD: "Always include static previews for SwiftUI views"
```

### Include the "Why"
```
✅ GOOD: 
**Rule**: Files shouldn't exceed 200 lines
**Why**: Keeps code readable and maintainable
```

### Be Clear About Enforcement
```
✅ GOOD:
**NEVER**: Add random customization features
**ALWAYS**: Document complex functions
**PREFER**: Platform-native solutions over third-party libraries
```

## 🚨 Red Flags for RULES.md Updates

Watch for these situations that almost always need rules:

### Code Smells
- Repeated debugging of the same type of issue
- Inconsistent implementations of similar features
- Architecture decisions made differently across files
- Performance issues that could have been prevented

### Process Breakdowns
- Features taking longer than expected due to rework
- Bugs introduced by not following established patterns
- Time wasted on decisions that should be standardized
- Confusion about "how we do things here"

### Knowledge Gaps
- New team members (including AI) making wrong assumptions
- Forgetting lessons learned from previous mistakes
- Losing context about why certain decisions were made
- Repeating discussions that were already settled

## 💡 Remember

**RULES.md is a living document.** Your job as an agent is to help it evolve by:

1. **Spotting patterns** that should become rules
2. **Identifying constraints** that prevent problems
3. **Documenting decisions** so they don't get remade
4. **Capturing wisdom** from your research and analysis

**The goal**: Make RULES.md so comprehensive and current that future agents (and humans) can onboard instantly and make consistent decisions.

---

*Keep RULES.md alive, current, and useful. It's the contract between all team members - human and AI.*