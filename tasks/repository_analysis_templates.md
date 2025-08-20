# Repository Analysis Templates for RULES.md Initialization

> **For the Rules Initializer Agent**: Use these templates to analyze repositories and create customized RULES.md files.

## 🔍 Repository Analysis Workflow

### 1. Technology Stack Detection

```markdown
## Technology Stack Analysis

### Primary Language
- **Language**: [JavaScript/TypeScript/Python/Go/Swift/etc.]
- **Version**: [Detected from config files]
- **Confidence**: [High/Medium/Low based on file count]

### Frameworks & Libraries
- **Frontend**: [React/Vue/Angular/Svelte/None]
- **Backend**: [Express/FastAPI/Django/Gin/None]
- **Mobile**: [React Native/Flutter/Swift/Kotlin/None]
- **Testing**: [Jest/Pytest/Go test/XCTest/etc.]
- **Build Tools**: [Webpack/Vite/npm/pip/go mod/etc.]

### Infrastructure & Deployment
- **Containerization**: [Docker/None]
- **Cloud**: [AWS/GCP/Azure/Vercel/Netlify/None]
- **CI/CD**: [GitHub Actions/GitLab CI/None]
- **Database**: [PostgreSQL/MongoDB/SQLite/None]
```

### 2. Project Characteristics Assessment

```markdown
## Project Characteristics

### Project Type
- **Category**: [Web App/Mobile App/API/Library/CLI Tool/Desktop App]
- **Domain**: [E-commerce/SaaS/Game/Utility/etc.]
- **Complexity**: [Simple/Medium/Complex]

### Scale Indicators
- **Total Files**: [Number]
- **Lines of Code**: [Estimate]
- **Dependencies**: [Count from package files]
- **Contributors**: [From git history]

### Architecture Pattern
- **Pattern**: [MVC/MVVM/Microservices/Monolith/Component-based]
- **Evidence**: [What files/structure suggests this pattern]
- **Maturity**: [New/Established/Legacy]
```

### 3. Existing Patterns Detection

```markdown
## Existing Code Patterns

### File Organization
- **Structure**: [Describe current folder structure]
- **Consistency**: [High/Medium/Low]
- **Standards**: [Any obvious organizational patterns]

### Naming Conventions
- **Files**: [camelCase/kebab-case/snake_case/PascalCase]
- **Variables**: [Detected pattern]
- **Functions**: [Detected pattern]
- **Components**: [If applicable]

### Code Style
- **Indentation**: [Spaces/Tabs and count]
- **Line Length**: [Observed limit]
- **Comments**: [Style and frequency]
- **Formatting**: [Any automatic formatting detected]

### Quality Indicators
- **Tests Present**: [Yes/No and type]
- **Documentation**: [README/Comments/None]
- **Linting**: [ESLint/Pylint/golangci-lint/etc.]
- **Type Safety**: [TypeScript/mypy/etc.]
```

## 📋 Customization Decision Matrix

### Project Type → RULES.md Sections Priority

#### Web Applications
```markdown
Priority Sections:
1. Component Architecture (size limits, reusability)
2. State Management (Redux/Zustand patterns)
3. Performance (bundle size, loading times)
4. UI/UX Guidelines (design system, accessibility)
5. API Integration (error handling, caching)

Key Rules to Include:
- Component splitting at 100-150 lines
- State management patterns
- Bundle size limits
- Accessibility requirements
- Performance budgets
```

#### Backend APIs
```markdown
Priority Sections:
1. API Design (REST/GraphQL standards)
2. Database Patterns (queries, migrations)
3. Security (auth, validation, rate limiting)
4. Error Handling (status codes, logging)
5. Performance (caching, optimization)

Key Rules to Include:
- API versioning strategy
- Database query optimization
- Authentication patterns
- Error response formats
- Logging standards
```

#### Mobile Applications
```markdown
Priority Sections:
1. Platform Guidelines (iOS HIG, Material Design)
2. Performance (memory, battery, responsiveness)
3. Platform-Specific Rules (permissions, navigation)
4. Device Compatibility (screen sizes, OS versions)
5. App Store Compliance (review guidelines)

Key Rules to Include:
- Platform-specific UI patterns
- Performance optimization rules
- Permission handling
- Navigation consistency
- Store policy compliance
```

#### Libraries/Packages
```markdown
Priority Sections:
1. Public API Design (consistency, versioning)
2. Documentation (API docs, examples)
3. Testing (coverage, edge cases)
4. Backward Compatibility (breaking changes)
5. Release Process (versioning, changelog)

Key Rules to Include:
- Semantic versioning rules
- API design principles
- Documentation requirements
- Testing coverage standards
- Release procedures
```

## 🎯 Context-Specific Rule Templates

### Team Size Customizations

#### Solo Developer Rules
```markdown
## Solo Developer Focus

### Context Switching Management
- Document every architectural decision
- Include "why" in all major code comments
- Keep TODO comments with dates and context
- Update RULES.md after every significant change

### Future-Self Guidelines
- Write code assuming 6-month memory gap
- Include setup instructions for development environment
- Document debugging procedures for common issues
- Maintain project diary in context files
```

#### Small Team Rules (2-5 people)
```markdown
## Small Team Coordination

### Communication Patterns
- Use pull request descriptions to explain approach
- Tag relevant team members for architecture decisions
- Weekly RULES.md review for updates
- Shared responsibility for documentation updates

### Review Process
- All changes require one approval
- Focus on knowledge sharing during reviews
- Use pair programming for complex features
- Rotate code review responsibilities
```

#### Large Team Rules (5+ people)
```markdown
## Large Team Governance

### Formal Processes
- Architecture Decision Records (ADRs) for major changes
- RULES.md changes require team consensus
- Formal onboarding checklist for new team members
- Regular RULES.md maintenance reviews

### Cross-Team Coordination
- Clear ownership boundaries in RULES.md
- Standardized API contracts
- Shared tooling and infrastructure decisions
- Escalation procedures for conflicts
```

## 🔧 Technology-Specific Rule Additions

### React/Frontend Rules
```markdown
### React-Specific Rules
- Components over 100 lines should be split
- Use TypeScript for all new components
- Include Storybook stories for reusable components
- Follow React Query patterns for data fetching
- Use CSS Modules or styled-components consistently
```

### Python/Backend Rules
```markdown
### Python-Specific Rules
- Use type hints for all function signatures
- Follow PEP 8 with line length of 88 characters
- Use pytest for all testing with fixtures
- Database queries must be optimized (use query analysis)
- Use FastAPI dependency injection patterns
```

### Node.js/JavaScript Rules
```markdown
### Node.js-Specific Rules
- Use ESLint with strict configuration
- Prefer async/await over Promise chains
- Use proper error handling middleware
- Follow Express.js best practices for routes
- Use environment variables for all configuration
```

## 📊 Analysis Automation Helpers

### Package File Analysis
```markdown
## Package Manager Detection

### package.json (Node.js)
- Check dependencies for framework detection
- Look for scripts to understand build process
- Identify testing frameworks and tools
- Check for TypeScript configuration

### requirements.txt / pyproject.toml (Python)
- Identify web frameworks (Django, FastAPI, Flask)
- Look for testing libraries (pytest, unittest)
- Check for linting tools (black, flake8)
- Identify database libraries (SQLAlchemy, etc.)

### go.mod (Go)
- Identify web frameworks (Gin, Echo, Chi)
- Look for database drivers
- Check for testing libraries
- Identify development tools

### Package.swift / Podfile (iOS)
- Identify third-party dependencies
- Check for testing frameworks
- Look for UI frameworks
- Identify development tools
```

### File Structure Patterns
```markdown
## Common Structure Patterns

### MVC Pattern Indicators
- `/models`, `/views`, `/controllers` directories
- Clear separation of concerns in file organization
- Database models in separate files
- Route handlers separated from business logic

### Component-Based Indicators
- `/components` directory
- Shared component library
- Component-specific styling files
- Reusable component patterns

### Microservices Indicators
- Multiple service directories
- Docker files for each service
- Service-specific package files
- API gateway configuration
```

## 🎨 RULES.md Customization Examples

### E-commerce Application
```markdown
### E-commerce-Specific Rules
- All price calculations must use decimal libraries
- Shopping cart state must persist across sessions
- Payment processing must follow PCI compliance
- Product images must have alt text for accessibility
- Inventory checks required before order confirmation
```

### SaaS Application
```markdown
### SaaS-Specific Rules
- Multi-tenant data isolation patterns
- Feature flag implementation standards
- Usage tracking and analytics requirements
- Subscription billing integration patterns
- API rate limiting per customer tier
```

### Game Development
```markdown
### Game-Specific Rules
- Frame rate optimization requirements
- Asset loading and memory management
- Save game data format standards
- Physics engine integration patterns
- Input handling across platforms
```

---

*Use these templates to create contextually appropriate RULES.md files that truly serve as engineering bibles for their specific projects.*