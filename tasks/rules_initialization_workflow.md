# RULES.md Initialization Workflow

> **Complete guide for the Rules Initializer agent to set up RULES.md in any repository**

## 🚀 Quick Start Commands

### For New Repositories
```
"Initialize RULES.md for this new [React/Python/Go/etc.] project"
"Set up engineering guidelines for this [web app/API/mobile app]"
"Create RULES.md for a [solo developer/small team/large team] project"
```

### For Existing Repositories
```
"Analyze this repository and create appropriate RULES.md"
"This repo needs engineering guidelines - initialize RULES.md"
"Convert this existing project to use RULES.md workflow"
```

### For Specific Scenarios
```
"Initialize minimal RULES.md for this quick prototype"
"Create comprehensive RULES.md for this production application"
"Set up RULES.md for this open-source library"
```

## 📋 Initialization Process

### Phase 1: Repository Analysis (2-3 minutes)

#### Step 1: Technology Stack Detection
```bash
# Files to analyze for stack detection:
- package.json / package-lock.json (Node.js)
- requirements.txt / pyproject.toml (Python)
- go.mod / go.sum (Go)
- Cargo.toml (Rust)
- Package.swift / Podfile (iOS)
- pubspec.yaml (Flutter)
- composer.json (PHP)
- pom.xml / build.gradle (Java)
```

#### Step 2: Project Type Classification
```markdown
## Project Type Decision Tree

Web Application?
├─ React/Vue/Angular → Frontend-heavy rules
├─ Next.js/Nuxt → Full-stack rules
└─ Static site → Minimal rules

API/Backend?
├─ REST API → API-focused rules
├─ GraphQL → Schema-first rules
└─ Microservices → Service-oriented rules

Mobile App?
├─ React Native → Cross-platform rules
├─ Flutter → Cross-platform rules
├─ iOS/Swift → iOS-specific rules
└─ Android/Kotlin → Android-specific rules

Library/Package?
├─ Public NPM package → Public API rules
├─ Internal library → Team-specific rules
└─ Open source → Community rules

Desktop App?
├─ Electron → Web-tech rules
├─ Native → Platform-specific rules
└─ Cross-platform → Framework rules
```

#### Step 3: Scale and Team Assessment
```markdown
## Scale Indicators

### Project Scale
- **Prototype**: < 1000 lines, minimal rules
- **Small Project**: 1K-10K lines, focused rules
- **Medium Project**: 10K-50K lines, comprehensive rules
- **Large Project**: 50K+ lines, enterprise rules

### Team Size Detection
- **Solo**: Minimal git history, focus on future-self
- **Small Team**: 2-5 contributors, collaborative rules
- **Large Team**: 5+ contributors, formal processes

### Domain Complexity
- **Simple**: CRUD, basic logic
- **Medium**: Business logic, integrations
- **Complex**: Multi-service, advanced algorithms
```

### Phase 2: RULES.md Template Selection (1 minute)

#### Template Decision Matrix
```markdown
| Project Type | Team Size | Complexity | Template |
|--------------|-----------|------------|----------|
| Prototype    | Solo      | Simple     | Minimal  |
| Web App      | Small     | Medium     | Standard |
| API          | Large     | Complex    | Enterprise |
| Library      | Any       | Any        | Public   |
| Mobile       | Any       | Medium+    | Platform |
```

#### Template Variations

##### Minimal Template (Prototypes, Solo Dev)
```markdown
# PROJECT RULES

**Keep it simple. Document decisions. Stay consistent.**

## Core Principle
[One sentence describing the main goal]

## Architecture
- **Pattern**: [Detected/Chosen pattern]
- **File Size**: 200 lines max
- **Why**: [Brief explanation]

## Dependencies
- ✅ [List current dependencies]
- ❌ No new dependencies without reason

## Code Style
- [Language-specific basics]
- [Naming convention found in code]

## Project Rules
1. [Most important constraint]
2. [Second most important constraint]
3. [Third most important constraint]

## When to Update
- After fixing any bug that could have been prevented
- When establishing new patterns
- Before adding major features

*Last updated: [DATE]*
```

##### Standard Template (Most Projects)
```markdown
# PROJECT RULES

> **This is your onboarding packet.** Read this before making any decisions.

[Use full template from RULES.md with project-specific customizations]
```

##### Enterprise Template (Large Teams/Complex Projects)
```markdown
# PROJECT RULES

[Full template plus:]

## Governance
- Architecture Decision Records (ADRs)
- RULES.md change approval process
- Escalation procedures
- Cross-team coordination

## Compliance
- Security requirements
- Performance SLAs
- Monitoring requirements
- Audit trail requirements
```

### Phase 3: Customization (3-5 minutes)

#### Technology-Specific Additions

##### React/Frontend Projects
```markdown
### Frontend-Specific Additions

## Component Rules
- Split components at 100 lines
- Use TypeScript for all new components
- Include PropTypes or TypeScript interfaces
- Static previews required (Storybook)

## State Management
- [Redux/Zustand/Context] patterns
- Global state only for truly global data
- Local state preferred when possible

## Performance
- Bundle size limit: [X]MB
- Core Web Vitals targets
- Image optimization requirements
- Lazy loading patterns

## UI/UX
- Follow [design system name]
- Accessibility: WCAG 2.1 AA compliance
- Responsive design breakpoints
- Component reusability standards
```

##### Backend/API Projects
```markdown
### Backend-Specific Additions

## API Design
- RESTful patterns / GraphQL schema first
- Versioning strategy: /v1/, /v2/
- Error response format standardization
- Rate limiting: [X] requests per minute

## Database
- Query optimization required
- Migration naming convention
- Index performance requirements
- Backup and recovery procedures

## Security
- Authentication: [JWT/OAuth/etc.]
- Input validation patterns
- Rate limiting implementation
- Security headers requirements

## Performance
- Response time targets: < [X]ms
- Database query limits
- Caching strategy
- Memory usage guidelines
```

##### Mobile Projects
```markdown
### Mobile-Specific Additions

## Platform Guidelines
- iOS: Follow Human Interface Guidelines
- Android: Follow Material Design
- Cross-platform: Consistent UX patterns

## Performance
- App startup time: < [X]ms
- Memory usage: < [X]MB
- Battery optimization patterns
- Network efficiency requirements

## Platform Features
- Permission handling patterns
- Navigation consistency
- Platform-specific UI components
- Device compatibility matrix
```

#### Domain-Specific Rules

##### E-commerce Applications
```markdown
## E-commerce Rules
- Price calculations: Use decimal arithmetic only
- Shopping cart: Persist across sessions
- Payment: PCI DSS compliance required
- Inventory: Real-time stock validation
- Images: Alt text mandatory for accessibility
```

##### SaaS Applications
```markdown
## SaaS Rules
- Multi-tenancy: Data isolation patterns
- Feature flags: Standardized implementation
- Usage tracking: Analytics on all actions
- Billing: Integration with [payment provider]
- API: Rate limiting per subscription tier
```

### Phase 4: Implementation (1-2 minutes)

#### File Creation Process
```markdown
## Implementation Steps

1. **Create RULES.md** in repository root
2. **Add to git** (ensure it's not ignored)
3. **Create .claude/ directory** if it doesn't exist
4. **Set up supporting structure**:
   - .claude/tasks/context_session.md
   - .claude/tasks/ directory for research reports
5. **Update README.md** to reference RULES.md
6. **Create initialization report**

## Supporting File Structure
```
project-root/
├── RULES.md                    # 🚨 Main engineering guidelines
├── README.md                   # Updated to reference RULES.md
├── .claude/
│   ├── tasks/
│   │   ├── context_session.md      # Project context
│   │   └── rules_initialization_report.md
│   └── agents/                 # Optional: project-specific agents
├── docs/                       # Optional: additional documentation
└── [existing project files]
```

#### Quality Checklist
```markdown
## Pre-Delivery Checklist

### Content Quality
- [ ] RULES.md is specific to this project (not generic)
- [ ] Technology stack is accurately reflected
- [ ] Architecture patterns match existing code
- [ ] Constraints are realistic and achievable
- [ ] Examples are relevant to the domain

### Completeness
- [ ] All major technology decisions are covered
- [ ] Team workflow preferences are included
- [ ] Update procedures are clearly defined
- [ ] Integration with existing tools is considered

### Usability
- [ ] Language is clear and actionable
- [ ] Structure is easy to navigate
- [ ] Examples are provided where helpful
- [ ] "Why" explanations are included for constraints
```

## 📊 Post-Initialization Report Template

```markdown
# RULES.md Initialization Report

## Repository Analysis
- **Project Type**: [Web App/API/Mobile/etc.]
- **Technology Stack**: [Primary languages and frameworks]
- **Team Size**: [Solo/Small/Large]
- **Complexity**: [Simple/Medium/Complex]
- **Domain**: [E-commerce/SaaS/etc.]

## Template Selection
- **Template Used**: [Minimal/Standard/Enterprise]
- **Customizations Applied**: [List of major customizations]
- **Technology-Specific Additions**: [What was added for this stack]

## Key Decisions Documented
1. [Architecture pattern choice and reasoning]
2. [Dependency policy decisions]
3. [Code quality standards]
4. [Project-specific constraints]
5. [Team workflow preferences]

## Recommendations
### Immediate Actions
- [ ] Team review of RULES.md content
- [ ] Integration with existing CI/CD pipeline
- [ ] Update of existing documentation to reference RULES.md

### Future Maintenance
- [ ] Schedule quarterly RULES.md review
- [ ] Set up process for proposing changes
- [ ] Train team on RULES.md workflow

## Next Steps
1. Share RULES.md with all team members
2. Integrate into onboarding process
3. Set up automated reminders for updates
4. Create project-specific agents if needed

## Files Created
- ✅ RULES.md (customized for this project)
- ✅ .claude/tasks/context_session.md (project context)
- ✅ .claude/tasks/rules_initialization_report.md (this file)
- ✅ Updated README.md (references RULES.md)

*Initialization completed: [DATE]*
*Rules Initializer Agent v1.0*
```

## 🔄 Maintenance Workflow

### When to Re-initialize
- Major technology stack changes
- Significant team size changes
- Project scope evolution
- Architecture pattern changes
- Performance requirement changes

### Update Triggers
- New patterns emerge in codebase
- Team processes evolve
- Technology constraints change
- Performance requirements shift
- Security requirements update

---

*This workflow ensures every repository gets a contextually appropriate RULES.md that truly serves as its engineering bible.*