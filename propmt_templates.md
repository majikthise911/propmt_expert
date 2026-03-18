
Projects are a great way to keep your conversations and files in a single place.




Attach to message
Drop here to add files to your message
prompt_templates.md
# Ready-to-Use Prompt Templates

## Template: Code Review (Multi-Agent)

```
You coordinate 4 specialized code review experts:

1. **Quality Auditor** - Readability and maintainability
2. **Security Analyst** - Vulnerabilities and best practices  
3. **Performance Reviewer** - Efficiency and optimization
4. **Architecture Assessor** - Design patterns and scalability

Code to review:
[CODE HERE]

Each expert provides:
- Priority Issues (High/Medium/Low)
- Specific Findings (with line numbers)
- Recommendations (actionable steps)

Then provide:
- Overall Assessment (1-5 with rationale)
- Top 3 Action Items (prioritized)
- Estimated Effort (for all fixes)
```

---

## Template: Data Analysis (Structured)

```
You are a data analysis expert.

Dataset: [DATASET_DESCRIPTION]

Analyze systematically:

**Phase 1: Exploratory Analysis**
- Summary statistics
- Data quality (missing values, outliers)
- Distribution patterns

**Phase 2: Deep Analysis**
- Correlation analysis
- Trend identification
- Anomaly detection

**Phase 3: Insights & Recommendations**
- Key findings (3-5 points)
- Actionable recommendations
- Suggested next steps

Format output as structured report with tables and visualizations described.
```

---

## Template: Content Creation (Role-Based)

```
You are an expert content writer specializing in {domain}.

Your writing style:
- {style_characteristic_1}
- {style_characteristic_2}
- {style_characteristic_3}

Task: {content_task}

Structure your output:
1. **Hook** (attention-grabbing opening)
2. **Core Content** (main points with evidence)
3. **Call-to-Action** (clear next step)

Target audience: {audience}
Tone: {tone}
Length: {word_count} words
```

---

## Template: Problem Solving (Chain-of-Thought)

```
Problem: {problem_statement}

Let's solve this systematically:

**Step 1: Understanding**
- What are we trying to solve?
- What are the constraints?
- What information do we have?

**Step 2: Approach**
- What strategy should we use?
- What are alternative approaches?
- Why is this approach best?

**Step 3: Execution**
- [Detailed solution steps]

**Step 4: Verification**
- Does this solve the problem?
- Are there edge cases?
- How can we improve?

**Final Answer**: [Complete solution]
```

---

## Template: Research Task (ReAct)

```
Research Goal: {research_question}

I will use iterative reasoning and information gathering:

**Thought 1**: What do I need to find out first?
**Action 1**: [Information to seek or tool to use]
**Observation 1**: [What I learned]

**Thought 2**: What does this tell me? What's next?
**Action 2**: [Next information gathering step]
**Observation 2**: [New findings]

[Continue 3-5 cycles]

**Synthesis**: [Integrated findings]
**Conclusion**: [Answer to research question]
**Confidence**: [High/Medium/Low with reasoning]
```

---

## Template: Teaching/Explanation (Progressive)

```
Explain: {concept}

For audience: {audience_level}

**Level 1: Simple Analogy**
[Explain using everyday comparison]

**Level 2: Core Concept**
[Main idea in clear terms]

**Level 3: Technical Details**
[Precise explanation with terminology]

**Level 4: Examples**
Example 1: [Simple case]
Example 2: [Complex case]

**Level 5: Practice**
Try it yourself: [Exercise question]

**Common Mistakes to Avoid**:
- [Mistake 1]
- [Mistake 2]
```

---

## Template: Decision Making (Tree-of-Thoughts)

```
Decision: {decision_to_make}

Context: {relevant_context}

Explore 3 approaches:

**Option A: {option_a_name}**
- Approach: [How it works]
- Pros: [Benefits]
- Cons: [Drawbacks]
- Risk Level: [Low/Medium/High]
- Resource Requirements: [Assessment]

**Option B: {option_b_name}**
- Approach: [How it works]
- Pros: [Benefits]
- Cons: [Drawbacks]
- Risk Level: [Low/Medium/High]
- Resource Requirements: [Assessment]

**Option C: {option_c_name}**
- Approach: [How it works]
- Pros: [Benefits]
- Cons: [Drawbacks]
- Risk Level: [Low/Medium/High]
- Resource Requirements: [Assessment]

**Recommendation**: [Best option with clear reasoning]
**Implementation Steps**: [How to proceed]
```

---

## Template: Debugging (Systematic)

```
Debug this issue systematically:

**Error Information**
- Error Message: {error_message}
- Context: {where_it_occurs}
- Environment: {system_details}

**Phase 1: Analysis**
Error Analyzer: What type of error is this?
Code Inspector: What code path leads here?
Environment Checker: Any configuration issues?

**Phase 2: Hypothesis**
Most likely cause: [Based on analysis]
Alternative causes: [Other possibilities]

**Phase 3: Solution**
Fix: [Specific code changes]
Why this works: [Explanation]

**Phase 4: Verification**
Test: [How to confirm fix]
Prevention: [How to avoid in future]
```

---

## Template: API Documentation

```
Document this API endpoint:

**Endpoint**: {method} {path}

**Purpose**: [What this endpoint does]

**Authentication**: [Required auth type]

**Request**
- Headers: [Required headers]
- Parameters: [Query/path params with types]
- Body: [Request body structure with example]

**Response**
- Success (200): [Response structure with example]
- Error (4xx/5xx): [Error formats with examples]

**Example Usage**
```{language}
[Complete code example]
```

**Rate Limiting**: [Limits if applicable]

**Notes**: [Important considerations]
```

---

## Template: Test Case Generation

```
Generate test cases for: {feature_description}

**Feature Scope**
- Functionality: [What it does]
- Inputs: [Expected inputs]
- Outputs: [Expected outputs]
- Edge Cases: [Known edge cases]

**Test Categories**

### Happy Path Tests
1. [Normal successful case]
2. [Common usage scenario]

### Edge Cases
1. [Boundary condition]
2. [Empty/null inputs]
3. [Maximum values]

### Error Cases
1. [Invalid input]
2. [Authentication failure]
3. [System errors]

### Performance Tests
1. [High load scenario]
2. [Concurrent usage]

For each test:
- Test Name
- Input Data
- Expected Output
- Assertions
```

---

## Template: User Story Analysis

```
Analyze this user story:

**Story**: {user_story}

**Analysis Framework**

### 1. Clarification Questions
- [Questions to ask stakeholders]
- [Ambiguities to resolve]

### 2. Acceptance Criteria
- [Specific, testable criteria]
- [Definition of done]

### 3. Technical Considerations
- [Architecture impacts]
- [Dependencies]
- [Risks]

### 4. Implementation Breakdown
- [Subtasks with estimates]
- [Priority order]

### 5. Testing Strategy
- [How to verify]
- [Edge cases to test]
```

---

## Template: Performance Optimization

```
Optimize performance for: {component_or_feature}

**Current State**
- Performance Metrics: {current_metrics}
- Bottlenecks: {identified_issues}
- Target: {performance_goal}

**Analysis**

### Profiler Findings
- Hotspots: [Where time is spent]
- Memory usage: [Current consumption]
- I/O patterns: [Database/file access]

### Optimization Opportunities
1. Algorithm improvements: [Complexity reductions]
2. Caching: [What to cache]
3. Database: [Query optimizations]
4. Parallelization: [Concurrent processing]

**Implementation Plan**
- Phase 1: [Quick wins]
- Phase 2: [Medium effort]
- Phase 3: [Complex changes]

**Expected Impact**: [Projected improvements]
```

---

## Template: Security Review

```
Conduct security review of: {component}

**Security Analyst Team**

### 1. Authentication & Authorization
- [How users are authenticated]
- [Permission checking]
- [Session management]

### 2. Input Validation
- [User input handling]
- [SQL injection risks]
- [XSS vulnerabilities]

### 3. Data Protection
- [Sensitive data storage]
- [Encryption in transit/at rest]
- [PII handling]

### 4. API Security
- [Rate limiting]
- [CORS configuration]
- [API key management]

### 5. Dependencies
- [Third-party libraries]
- [Known vulnerabilities]
- [Update status]

**Risk Assessment**
- Critical: [Immediate fixes needed]
- High: [Important issues]
- Medium: [Should address]
- Low: [Nice to fix]

**Remediation Plan**: [Prioritized actions]
```

---

## Template: Business Requirements Gathering

```
Gather requirements for: {project_or_feature}

**Stakeholder Perspectives**

### Business Analyst
- Business goals: [What success looks like]
- User needs: [Who and what they need]
- ROI: [Expected value]

### Technical Lead
- Feasibility: [Technical constraints]
- Effort estimate: [Time and resources]
- Architecture impact: [System changes needed]

### UX Designer
- User experience: [Interaction flow]
- Accessibility: [Inclusive design needs]
- Usability: [Ease of use goals]

### Project Manager
- Timeline: [Schedule constraints]
- Dependencies: [What's needed first]
- Risks: [Potential blockers]

**Consolidated Requirements**
- Must Have: [Essential features]
- Should Have: [Important but not critical]
- Could Have: [Nice to have]
- Won't Have: [Out of scope]

**Success Metrics**: [How to measure success]
```

---

## Template: Refactoring Plan

```
Plan refactoring for: {code_or_system}

**Current State Assessment**
- Code smells: [Identified issues]
- Technical debt: [Problems accumulated]
- Pain points: [Developer complaints]

**Refactoring Strategy**

### Structure Analyst
- Architecture issues: [Design problems]
- Coupling problems: [Dependencies]
- Abstraction opportunities: [Reusable patterns]

### Code Quality Reviewer
- Naming improvements: [Clarity enhancements]
- Simplification: [Complexity reduction]
- Documentation needs: [What to explain]

### Test Coverage Assessor
- Current coverage: [Test gaps]
- Refactoring support: [Tests needed first]
- Regression prevention: [Safety nets]

**Implementation Approach**
- Phase 1: [Add tests]
- Phase 2: [Small safe changes]
- Phase 3: [Larger restructuring]
- Phase 4: [Cleanup]

**Risk Mitigation**: [How to stay safe]
```

---

## Usage Guidelines

### Choosing the Right Template

1. **Identify your task type**
   - Analysis → Data Analysis or Security Review
   - Creation → Content Creation or API Documentation
   - Problem Solving → Chain-of-Thought or Debugging
   - Decision Making → Tree-of-Thoughts
   - Complex Tasks → Multi-Agent patterns

2. **Customize for your context**
   - Replace placeholders with specific details
   - Adjust section emphasis based on priorities
   - Add domain-specific requirements

3. **Combine when needed**
   - Large projects may need multiple templates
   - Use sequentially (research → plan → implement)
   - Adapt structure to workflow

### Template Modification Tips

- **Add constraints**: Word limits, format requirements
- **Specify output format**: JSON, markdown, bullet points
- **Include examples**: Show desired style/structure
- **Set quality criteria**: What makes a good response
- **Add validation steps**: How to check correctness