# Claude Code Parent Agent Rules

## 🚨 RULES.md: The Engineering Bible

### Primary Rule
**RULES.md is the single source of truth for all engineering decisions, constraints, and patterns.**

- **ALL agents must read RULES.md FIRST** before any other files
- **RULES.md contains**: Architecture decisions, coding standards, dependencies, constraints, and the "why" behind decisions
- **Treat RULES.md like onboarding a teammate** - it's your comprehensive guide to "how we do things here"
- **Keep RULES.md current** - update it when new patterns emerge or constraints are discovered

### RULES.md Workflow
1. **Read RULES.md** before starting any task
2. **Follow RULES.md** constraints and patterns religiously  
3. **Suggest updates** to RULES.md when you discover gaps
4. **Reference RULES.md** in all research reports and recommendations
5. **Never violate RULES.md** without explicit discussion and updates

## Context Management

### File Reading Order (CRITICAL)
1. **FIRST**: `RULES.md` - The engineering bible
2. **SECOND**: `.claude/tasks/context_session.md` - Current project context
3. **THIRD**: Relevant research reports and codebase files

### Project Context Files
- **ALWAYS** maintain project context in `.claude/tasks/context_session.md`
- Create this file at the start of any new project or feature
- Use the template at `.claude/tasks/context_session_template.md` as a starting point
- Update this file after completing any significant work
- Include architecture decisions, progress, and next steps
- **Track RULES.md alignment** in all context updates

### Research Reports
- Sub-agents save their research to `.claude/tasks/[domain]_research.md`
- Always read these files before implementation
- Reference these files when making implementation decisions
- **Include RULES.md compliance** in all research reports

## Sub-Agent Delegation

### Agent Configuration
- Agents are stored as Markdown files with YAML frontmatter in `.claude/agents/`
- Use `/agents` command to manage and configure agents
- Project-level agents in `.claude/agents/` (version controlled)
- User-level agents in `~/.claude/agents/` (personal settings)

### Available Expert Agents
1. **React Frontend Expert** - Proactively researches frontend implementations
2. **Python Backend Expert** - Proactively researches backend architecture
3. **Database Architecture Expert** - Proactively researches data modeling and system design
4. **DevOps Infrastructure Expert** - Proactively researches deployment and infrastructure
5. **AI ML Expert** - Proactively researches AI/ML integration
6. **Agent Creator** - Proactively creates new specialized agents when needed
7. **Rules Initializer** - Proactively initializes RULES.md for new or existing repositories

### Delegation Rules
- Sub-agents automatically activate based on task descriptions (PROACTIVE)
- Can be explicitly invoked by mentioning the agent name
- **ALWAYS** use sub-agents for research and planning phases
- **NEVER** delegate implementation tasks to sub-agents
- **CRITICAL**: All sub-agents must read RULES.md first, then context files
- Ensure sub-agents understand the full project context AND RULES.md constraints
- Review sub-agent research reports for RULES.md compliance before implementing

### Proactive Agent Activation
- Agents activate automatically when their domain keywords are detected
- Frontend tasks trigger React Frontend Expert
- Backend tasks trigger Python Backend Expert
- Database/architecture tasks trigger Database Architecture Expert
- Deployment/infrastructure tasks trigger DevOps Infrastructure Expert
- AI/ML tasks trigger AI ML Expert
- Need for new expertise triggers Agent Creator
- **Missing RULES.md triggers Rules Initializer**
- **New repository setup triggers Rules Initializer**

### When to Delegate
- Complex architecture decisions
- Technology stack selection
- Integration planning with external services
- Performance optimization strategies
- Security and compliance considerations
- Initial project planning and research phases
- **RULES.md setup for new repositories**
- **RULES.md customization for existing projects**
- **Repository analysis and guidelines creation**

## Implementation Workflow

### Phase 1: Research & Planning (RULES.md Driven)
1. **Read RULES.md** to understand all constraints and patterns
2. Create/update `.claude/tasks/context_session.md` with RULES.md alignment check
3. Delegate research to appropriate expert sub-agents (who will read RULES.md first)
4. Review all research reports in `.claude/tasks/` for RULES.md compliance
5. Create implementation plan based on research AND RULES.md constraints
6. **Update RULES.md** if new patterns or constraints are discovered

### Phase 2: Implementation (RULES.md Compliant)
1. Follow the implementation plan from Phase 1 AND RULES.md constraints
2. Ensure all code follows RULES.md architecture patterns and coding standards
3. Update context file with progress, decisions, and RULES.md compliance
4. Test and validate implementations against RULES.md requirements
5. Document any deviations from RULES.md (with justification for updates)

### Phase 3: Review & Documentation (RULES.md Evolution)
1. Update context file with final results and RULES.md compliance status
2. **Suggest RULES.md updates** based on lessons learned or new patterns
3. Note any improvements that should become rules
4. Clean up temporary research files if needed
5. **Update RULES.md** with new constraints, patterns, or "don'ts" discovered

## Task Instructions for Sub-Agents

When delegating to sub-agents, always include:

```
🚨 CRITICAL READING ORDER:
1. FIRST: Read `RULES.md` - this is your engineering bible and onboarding packet
2. SECOND: Read the context file at `.claude/tasks/context_session.md` to understand the project context

Your task: [Specific research/planning task]

Requirements:
- Follow ALL constraints and patterns defined in RULES.md
- Ensure your recommendations align with RULES.md architecture decisions
- Respect dependency rules, coding standards, and constraints from RULES.md

After completing your research:
1. Save your findings to `.claude/tasks/[domain]_research.md`
2. Include RULES.md compliance assessment in your report
3. Suggest any updates to RULES.md based on your research
4. Update the context file with your progress and RULES.md alignment
5. Provide a summary of your recommendations that follows RULES.md

Remember: Focus on research and planning only - do not implement code.
```

## Context File Management

### Required Updates
- After each sub-agent consultation
- Before and after major implementation phases
- When architecture decisions are made
- After testing and deployment

### Content Guidelines
- Keep project overview current
- Track all research reports generated
- Document key decisions and rationale
- Note any blockers or concerns
- List next priority tasks

## Quality Assurance

### Before Implementation
- [ ] **RULES.md has been read and understood**
- [ ] Context file is up to date with RULES.md alignment check
- [ ] Relevant expert agents have been consulted (and they read RULES.md)
- [ ] Research reports have been reviewed for RULES.md compliance
- [ ] Implementation plan is clear, detailed, AND follows RULES.md constraints

### After Implementation
- [ ] **All code follows RULES.md constraints and patterns**
- [ ] Context file reflects current state and RULES.md compliance
- [ ] Code follows research recommendations AND RULES.md guidelines
- [ ] Tests are passing and meet RULES.md testing requirements
- [ ] Documentation is updated
- [ ] **RULES.md has been updated** with any new patterns or constraints discovered

## Notes

- **RULES.md is the ultimate source of truth** - treat it like your engineering bible
- **All agents must read RULES.md FIRST** before any other files or tasks
- Sub-agents are researchers, not implementers
- Use the file system for context sharing between agents
- Always maintain the "single source of truth" in context files
- **Keep RULES.md current** - update it when new patterns or constraints emerge
- Delegate to get expert knowledge, implement with full context AND RULES.md compliance
- Use `/agents` command to manage agent configurations
- Agents are designed for PROACTIVE activation - they should trigger automatically
- Agent Creator will generate new agents when encountering uncovered domains
- **When in doubt, check RULES.md. When RULES.md is unclear, update it.**
- **The goal**: Make RULES.md so comprehensive that any agent can onboard instantly and make consistent decisions

### RULES.md Workflow Summary
1. **Read RULES.md** → 2. **Follow RULES.md** → 3. **Update RULES.md** → 4. **Repeat**