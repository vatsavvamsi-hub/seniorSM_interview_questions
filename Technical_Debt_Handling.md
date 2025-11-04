# Technical Debt Handling for Scrum Masters

## How to Plan for Technical Debt

A scrum master can handle technical debt planning through these key strategies:

1. **Quantify and visualize**: Track technical debt in the backlog as explicit items with estimated effort and business impact. Use metrics to make it visible to stakeholders.

2. **Balance sprints**: Reserve a percentage of sprint capacity (typically 10-20%) for technical debt work alongside feature development. This prevents it from accumulating.

3. **Prioritize strategically**: Rank technical debt by impact (performance, maintainability, security) and effort. Address high-impact, lower-effort items first.

4. **Link to business value**: Frame technical debt in business terms—reduced bugs, faster releases, lower maintenance costs—to justify investment to product owners.

5. **Include in Definition of Done**: Make code quality standards part of your DoD to prevent new technical debt while addressing existing debt.

6. **Create spike stories**: For large, unclear technical debt, create investigation spikes to estimate the work before committing to fixes.

7. **Communicate regularly**: Update the team and stakeholders on technical debt status in sprint reviews and retrospectives to maintain awareness.

8. **Empower engineers**: Give developers ownership over identifying and proposing technical debt items rather than imposing them top-down.

9. **Use retrospectives**: Use sprint retros to discuss technical debt accumulation patterns and adjust practices to prevent future debt.

10. **Set guardrails**: Establish code quality metrics or thresholds (test coverage, cyclomatic complexity) that trigger technical debt work when breached.

The key is treating technical debt as a first-class citizen in planning, not an afterthought.

## Common Technical Debt Examples and Management

### 1. Legacy Code / Poor Code Quality
- **Example**: Monolithic 5000-line function with no tests
- **Manage**: Break into incremental refactoring tasks in sprints. Add tests incrementally before touching code. Track progress with metrics (lines refactored, test coverage increase).

### 2. Outdated Dependencies
- **Example**: Using Node.js 12 when 20 is current; security vulnerabilities in old library versions
- **Manage**: Schedule dependency upgrade sprints quarterly. Automate dependency scanning (e.g., Dependabot). Prioritize security-critical updates immediately.

### 3. Missing or Outdated Documentation
- **Example**: API endpoints undocumented; deployment process only known by one engineer
- **Manage**: Reserve sprint time for documentation. Make it part of DoD for new features. Use automated doc generation where possible.

### 4. Test Coverage Gaps
- **Example**: Critical payment module has 20% test coverage
- **Manage**: Set coverage targets (e.g., 80%). Add test-writing tasks to sprints. Use coverage reports to identify high-risk areas first.

### 5. Performance Issues
- **Example**: Database queries causing 10-second page load times
- **Manage**: Profile and measure impact. Prioritize by user-facing severity. Add performance budgets to DoD. Track with monitoring.

### 6. Architectural Debt
- **Example**: Tightly coupled services that make scaling difficult
- **Manage**: Create spike stories to explore solutions. Plan multi-sprint refactoring roadmap. Use feature flags to roll out architectural changes gradually.

### 7. Duplicate Code / No Reusability
- **Example**: Same validation logic copied across 10 endpoints
- **Manage**: Extract shared utilities/libraries. Add to code review checklist to prevent new duplication.

## Key Principle

Create backlog items for each technical debt issue, estimate effort, assign business value, and weave into sprint planning rather than doing cleanup sprints (which often get deprioritized).
