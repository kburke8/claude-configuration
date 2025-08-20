# Claude Code Sub-Agent System

This repository contains a sophisticated sub-agent system for Claude Code based on best practices for context management and specialized research agents.

## Overview

The system follows the principle that **sub-agents are researchers, not implementers**. This approach optimizes token usage and improves code quality by separating planning from execution.

## Architecture

### Expert Research Agents (Proactive)
- **React Frontend Expert** - Proactively researches UI/UX, React, Next.js implementations
- **Python Backend Expert** - Proactively researches API, backend architecture
- **Database Architecture Expert** - Proactively researches data modeling, system design
- **DevOps Infrastructure Expert** - Proactively researches deployment, CI/CD
- **AI ML Expert** - Proactively researches AI/ML integration
- **Agent Creator** - Proactively creates new specialized agents when needed

### Context Management
- **`.claude/tasks/context_session.md`** - Main project context file
- **`.claude/tasks/[domain]_research.md`** - Research reports from expert agents
- **`.claude/tasks/context_session_template.md`** - Template for new projects

## How It Works

1. **Research Phase**: Expert agents analyze requirements and create detailed plans
2. **Implementation Phase**: Parent agent implements based on research
3. **Context Sharing**: File system maintains state between agents

## Usage

### Starting a New Project
1. Copy `context_session_template.md` to `context_session.md`
2. Fill in project details and requirements
3. Expert agents activate automatically based on task descriptions
4. Review research reports before implementing

### Example Workflow
```
# 1. Agents activate automatically
"Help me create a Next.js app with authentication"
# → React Frontend Expert and Database Architecture Expert activate

# 2. Review research
"Show me the research reports from the experts"

# 3. Implement
"Based on the research, implement the authentication system"
```

### Proactive Agent Activation

Agents automatically activate when their domains are detected:

**Frontend Tasks**:
- "Build a React dashboard" → React Frontend Expert activates
- "Style with Tailwind CSS" → React Frontend Expert activates

**Backend Tasks**:
- "Create FastAPI endpoints" → Python Backend Expert activates
- "Implement authentication" → Python Backend Expert activates

**Database Tasks**:
- "Design user schema" → Database Architecture Expert activates
- "Optimize database performance" → Database Architecture Expert activates

**DevOps Tasks**:
- "Set up CI/CD pipeline" → DevOps Infrastructure Expert activates
- "Deploy to AWS" → DevOps Infrastructure Expert activates

**AI/ML Tasks**:
- "Integrate OpenAI API" → AI ML Expert activates
- "Build RAG system" → AI ML Expert activates

**New Domains**:
- "Build mobile app with React Native" → Agent Creator creates Mobile Expert

## Benefits

- **Token Optimization**: Research happens in isolated contexts
- **Expert Knowledge**: Specialized agents provide domain expertise
- **Context Preservation**: File system maintains project state
- **Better Planning**: Separate research from implementation
- **Consistency**: Standardized workflow across projects
- **Proactive Assistance**: Agents activate automatically when needed

## File Structure

```
.claude/                               # Main Claude directory
├── agents/                            # Sub-agent configurations (Markdown)
│   ├── react-frontend-expert.md      # Frontend research specialist
│   ├── python-backend-expert.md      # Backend research specialist  
│   ├── database-architecture-expert.md # Architecture research specialist
│   ├── devops-infrastructure-expert.md # DevOps research specialist
│   ├── ai-ml-expert.md               # AI/ML research specialist
│   ├── agent-creator.md              # Creates new specialized agents
│   └── rules-initializer.md          # Initializes RULES.md for repos
├── tasks/                             # Task templates and guides
│   ├── context_session_template.md   # Project context template
│   ├── RULES_UPDATE_GUIDE.md         # Guide for updating RULES.md
│   ├── repository_analysis_templates.md # Repo analysis templates
│   ├── rules_initialization_workflow.md # RULES.md setup workflow
│   ├── context_session.md            # Current project context (created per project)
│   ├── frontend_research.md          # Frontend research reports (created as needed)
│   ├── backend_research.md           # Backend research reports (created as needed)
│   ├── architecture_research.md      # Architecture research reports (created as needed)
│   ├── devops_research.md            # DevOps research reports (created as needed)
│   └── ai_ml_research.md             # AI/ML research reports (created as needed)
├── settings.local.json               # Claude built-in settings (ignored by git)
├── CLAUDE.md                         # Parent agent rules and workflows
├── README.md                         # This documentation file
├── RULES.md                          # Engineering guidelines template
└── .gitignore                        # Git ignore rules for Claude files
```

## Best Practices

1. **Agents activate automatically** - no need to explicitly invoke them
2. **Keep context files updated** throughout the project
3. **Review research reports** before implementing recommendations
4. **Let agents create new specialists** when encountering new domains
5. **Maintain the separation** between research and implementation

## Customization

You can create additional expert agents by:
1. Using the Agent Creator agent (automatically detects needs)
2. Adding new Markdown files to `.claude/agents/`
3. Following the existing agent structure with YAML frontmatter
4. Updating CLAUDE.md to reference new agents
5. Creating corresponding research file patterns

## Proactive Agent System

Agents are designed to activate automatically when:
- Frontend tasks are mentioned → React Frontend Expert activates
- Backend tasks are mentioned → Python Backend Expert activates
- Database/architecture tasks → Database Architecture Expert activates
- DevOps/deployment tasks → DevOps Infrastructure Expert activates
- AI/ML tasks → AI ML Expert activates
- New domains encountered → Agent Creator creates specialized agents

This system scales with your needs while maintaining optimal performance and context management through proactive, intelligent agent activation.