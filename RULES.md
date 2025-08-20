# PROJECT RULES

> **This is your onboarding packet.** Treat this like you're joining the team as a senior engineer. Read this before making any decisions. When in doubt, always lean towards what's more delightful and simple.

## 🎯 ENGINEERING PHILOSOPHY

**You are a senior engineer building [PROJECT_TYPE]. Our core principle is [CORE_PRINCIPLE - e.g., SLC: Simple, Lovable, Complete].**

- **Keep it simple**: Don't get clever with architecture unless absolutely necessary
- **Stay consistent**: Follow established patterns throughout the codebase  
- **Be explicit**: Code should be self-documenting and obvious
- **Think long-term**: Every decision should make future maintenance easier
- **Follow standards**: Stick to industry best practices and platform guidelines

## 🏗️ ARCHITECTURE RULES

### Core Architecture
- **Pattern**: [e.g., MVC, MVVM, Clean Architecture]
- **Why**: [Reasoning for the choice]
- **Don't**: Get experimental with architecture patterns

### File Organization
```
[Define your preferred project structure]
```

### Code Standards
- **View files**: Max 100 lines (soft ceiling)
- **Other files**: Max 200 lines (soft ceiling)
- **Functions**: Max 20 lines (prefer smaller)
- **Why**: Keeps code readable and maintainable

## 📦 DEPENDENCIES & PACKAGES

### Allowed
- [List approved frameworks/libraries]
- [Built-in platform tools only, or specific exceptions]

### NEVER USE
- ❌ Random third-party packages without approval
- ❌ Experimental or beta libraries in production
- ❌ Heavy frameworks for simple tasks

### Why
[Explain dependency philosophy - e.g., "Keep bundle size small", "Reduce maintenance burden"]

## ✅ REQUIRED PATTERNS

### Code Documentation
- **ALWAYS**: Document complex functions and classes
- **ALWAYS**: Include usage examples for reusable components
- **ALWAYS**: Add comments explaining "why" not just "what"

### Testing Strategy
- **Unit tests**: For all business logic
- **Integration tests**: For critical user flows
- **No**: Testing implementation details

### Error Handling
- **Pattern**: [Define your error handling approach]
- **Logging**: [Define logging standards]
- **User-facing errors**: [Define UX for errors]

## 🚫 ABSOLUTE DON'TS

### Code Quality
- ❌ **Never** commit commented-out code
- ❌ **Never** use magic numbers (always use constants)
- ❌ **Never** ignore linting warnings
- ❌ **Never** commit without testing

### Architecture
- ❌ **Never** break established patterns without discussion
- ❌ **Never** add complexity for edge cases affecting <1% of users
- ❌ **Never** implement features not in the current scope

### Performance
- ❌ **Never** optimize prematurely
- ❌ **Never** add features that significantly impact startup time
- ❌ **Never** ignore memory leaks

## 🎨 UI/UX GUIDELINES

### Design Principles
- **Follow platform guidelines**: [e.g., Apple HIG, Material Design]
- **Consistency**: Use design system components
- **Accessibility**: All interactive elements must be accessible

### Component Standards
- **Reusability**: Extract reusable components after 2nd use
- **Props**: Keep component interfaces simple and predictable
- **State**: Prefer local state, lift up only when necessary

## 🔄 WORKFLOW PATTERNS

### Feature Development
1. **Research first**: Consult appropriate expert agents
2. **Plan**: Update context files with approach
3. **Implement**: Follow established patterns
4. **Test**: Verify functionality and edge cases
5. **Document**: Update RULES.md if new patterns emerge

### Code Review Standards
- **Self-review**: Always review your own changes first
- **Check**: Does this follow our established patterns?
- **Ask**: Will future me understand this in 6 months?

## 📝 WHEN TO UPDATE THIS FILE

### Always Update After:
- 🔧 **Bug fixes**: If the bug could have been prevented by a rule
- 🆕 **New patterns**: When you establish a new way of doing things
- 🚫 **Mistakes**: When you do something you shouldn't have
- 🎯 **Scope changes**: When project requirements evolve

### How to Update:
1. **Document the change**: What and why
2. **Update relevant sections**: Keep it organized
3. **Notify the team**: Including AI agents in future sessions

## 🎯 PROJECT-SPECIFIC RULES

### [Current Project Name]
- **Goal**: [What you're building]
- **Constraints**: [Specific limitations or requirements]
- **Non-goals**: [What you're explicitly NOT building]

### Features
- **Core**: [Essential features that must work perfectly]
- **Nice-to-have**: [Features that can be simplified or cut]
- **Never**: [Features you will never add]

### Technical Constraints
- **Performance**: [Specific performance requirements]
- **Compatibility**: [Platform/version requirements]
- **Scalability**: [Expected scale and growth]

## 🚨 EMERGENCY PROTOCOLS

### When Things Break
1. **Don't panic**: Step back and assess
2. **Check RULES.md**: Are we following our own guidelines?
3. **Consult context**: Review recent changes and decisions
4. **Ask experts**: Use sub-agents for domain-specific guidance
5. **Document lessons**: Update RULES.md with new insights

### When Stuck
1. **Re-read the goal**: What are we actually trying to achieve?
2. **Simplify**: What's the most straightforward approach?
3. **Reference patterns**: How have we solved similar problems?
4. **Get input**: Consult relevant expert agents

---

## 💡 REMEMBER

**This file is your contract with your future self and your AI teammates.**

- When agents drift → Point them back to RULES.md
- When you're confused → Re-read RULES.md  
- When things break → Update RULES.md
- When starting a session → Reference RULES.md

**The goal is not perfection. The goal is consistency, clarity, and continuous improvement.**

---

*Last updated: [DATE] - [REASON FOR UPDATE]*