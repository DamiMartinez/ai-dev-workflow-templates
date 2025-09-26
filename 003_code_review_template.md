# AI Code Review Template

> **About This Template:** This template provides a structured approach to conducting thorough code reviews with AI assistance. Following this process ensures that code changes are properly evaluated for quality, security, performance, and maintainability.

---

## 1. Review Overview

### Review Title
**Title:** [Brief, descriptive title of the code review - e.g., "Review User Authentication Implementation" or "Review Database Migration Changes"]

### Review Type
- **Type:** [Feature Review, Bug Fix Review, Refactoring Review, Security Review, Performance Review]
- **Priority:** [High, Medium, Low]
- **Reviewer:** [Name of the reviewer or AI agent conducting the review]

### Pull Request Information
- **PR Number:** [#123]
- **Branch:** [e.g., `feat/user-auth` or `fix/payment-bug`]
- **Author:** [Name of the code author]
- **Files Changed:** [Number of files modified]

---

## 2. Code Analysis

### Code Quality Assessment
- **Readability:** [Excellent, Good, Fair, Poor] - [Brief explanation]
- **Maintainability:** [Excellent, Good, Fair, Poor] - [Brief explanation]
- **Performance:** [Excellent, Good, Fair, Poor] - [Brief explanation]
- **Security:** [Excellent, Good, Fair, Poor] - [Brief explanation]

### Code Style & Standards
- [ ] Code follows project style guidelines
- [ ] Consistent naming conventions used
- [ ] Proper indentation and formatting
- [ ] No commented-out code left behind
- [ ] Appropriate use of comments and documentation

### Architecture & Design
- [ ] Code follows established architectural patterns
- [ ] Proper separation of concerns
- [ ] Appropriate use of design patterns
- [ ] No unnecessary coupling between components
- [ ] Follows SOLID principles (if applicable)

---

## 3. Functional Review

### Requirements Compliance
- [ ] Code meets the stated requirements
- [ ] All user stories/acceptance criteria are addressed
- [ ] Edge cases are properly handled
- [ ] Error conditions are managed appropriately

### Testing Coverage
- [ ] Unit tests are present and comprehensive
- [ ] Integration tests cover the changes
- [ ] Edge cases are tested
- [ ] Error scenarios are tested
- [ ] Test coverage meets project standards

### Documentation
- [ ] Code is self-documenting
- [ ] Complex logic is explained with comments
- [ ] API documentation is updated (if applicable)
- [ ] README or user documentation is updated (if applicable)

---

## 4. Security Review

### Security Considerations
- [ ] No hardcoded secrets or credentials
- [ ] Input validation is implemented
- [ ] Output encoding is used where appropriate
- [ ] SQL injection prevention (if applicable)
- [ ] XSS prevention (if applicable)
- [ ] CSRF protection (if applicable)
- [ ] Authentication and authorization are properly implemented
- [ ] Sensitive data is handled securely

### Data Handling
- [ ] Personal data is handled according to privacy requirements
- [ ] Data validation is comprehensive
- [ ] Error messages don't leak sensitive information
- [ ] Logging doesn't expose sensitive data

---

## 5. Performance Review

### Performance Considerations
- [ ] No obvious performance bottlenecks
- [ ] Database queries are optimized (if applicable)
- [ ] Caching is used appropriately
- [ ] Memory usage is reasonable
- [ ] No unnecessary API calls or operations
- [ ] Asynchronous operations are used where appropriate

### Scalability
- [ ] Code can handle expected load
- [ ] No blocking operations in main thread
- [ ] Resource usage scales appropriately
- [ ] Database queries scale with data growth

---

## 6. Issues Found

### Critical Issues
- [ ] **Issue 1:** [Description of critical issue]
- [ ] **Issue 2:** [Description of critical issue]

### Major Issues
- [ ] **Issue 1:** [Description of major issue]
- [ ] **Issue 2:** [Description of major issue]

### Minor Issues
- [ ] **Issue 1:** [Description of minor issue]
- [ ] **Issue 2:** [Description of minor issue]

### Suggestions for Improvement
- [ ] **Suggestion 1:** [Description of improvement suggestion]
- [ ] **Suggestion 2:** [Description of improvement suggestion]

---

## 7. Positive Feedback

### What's Done Well
- [ ] **Strength 1:** [Description of what's done well]
- [ ] **Strength 2:** [Description of what's done well]
- [ ] **Strength 3:** [Description of what's done well]

### Best Practices Followed
- [ ] **Practice 1:** [Description of best practice followed]
- [ ] **Practice 2:** [Description of best practice followed]

---

## 8. Review Summary

### Overall Assessment
**Overall Rating:** [Excellent, Good, Fair, Poor]

**Summary:** [Brief summary of the review findings, highlighting key issues and strengths]

### Deliverables
- A code review summary with detailed feedback on code quality, security, and performance.
- A list of identified issues, categorized by severity.
- A clear recommendation (Approve, Request Changes, or Reject).

### Recommendation
- [ ] **Approve** - Code is ready to merge
- [ ] **Approve with minor changes** - Merge after addressing minor issues
- [ ] **Request changes** - Address major issues before merging
- [ ] **Reject** - Significant issues need to be resolved

### Next Steps
1. [Action item 1]
2. [Action item 2]
3. [Action item 3]

---

## 9. AI Agent Instructions

### Review Process
🎯 **MANDATORY PROCESS:**
1.  **Code Analysis:** Thoroughly analyze all changed files, focusing on the areas mentioned in the review sections above.
2.  **Context Understanding:** Understand the purpose and context of the changes by reviewing the PR description and related issues.
3.  **Comprehensive Review:** Check code quality, functionality, security, performance, and adherence to project standards.
4.  **Issue Identification:** Identify and categorize issues by severity (Critical, Major, Minor).
5.  **Positive Feedback:** Acknowledge good practices and well-implemented features.
6.  **Clear Recommendations:** Provide specific, actionable feedback for improvement.
7.  **Final Assessment:** Make a clear recommendation on whether to approve or request changes.

### Review Focus Areas
- **Code Quality:** Readability, maintainability, and adherence to coding standards
- **Functionality:** Correctness, completeness, and proper error handling
- **Security:** Potential vulnerabilities and secure coding practices
- **Performance:** Efficiency and scalability considerations
- **Testing:** Adequate test coverage and quality
- **Documentation:** Clarity and completeness of code documentation

### Communication Guidelines
- Be constructive and specific in feedback
- Provide examples and suggestions for improvements
- Balance criticism with positive reinforcement
- Focus on the code, not the person
- Ask clarifying questions when needed
- Prioritize issues by severity and impact

---

## 10. Review Checklist

### Pre-Review
- [ ] Pull request is properly described
- [ ] All required checks are passing
- [ ] Code is properly formatted
- [ ] Tests are included and passing

### During Review
- [ ] All changed files are reviewed
- [ ] Code logic is understood
- [ ] Security implications are considered
- [ ] Performance impact is evaluated
- [ ] Test coverage is adequate

### Post-Review
- [ ] All issues are clearly documented
- [ ] Recommendations are actionable
- [ ] Review is completed in a timely manner
- [ ] Follow-up is planned for requested changes

