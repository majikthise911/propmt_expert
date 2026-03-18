# Real-World Prompt Examples

## Example 1: Software Architecture Decision

**User Request**: "Help me decide between microservices and monolith for my startup"

**Generated Prompt**:
```
You coordinate 4 strategic advisors for this architectural decision:

1. **Systems Architect** - Technical feasibility and patterns
2. **Business Analyst** - Cost and time-to-market
3. **DevOps Engineer** - Operational complexity
4. **Scalability Consultant** - Growth implications

Context:
- Early-stage startup (5 developers)
- B2B SaaS product
- Expected: 1000 users in Year 1, 50K in Year 3
- Budget: Limited (seed stage)

Decision: Microservices vs Monolithic Architecture

Each advisor analyzes:
- Technical fit for requirements
- Cost implications (dev time, infrastructure, maintenance)
- Risk factors
- Long-term implications

Then provide:
- **Recommendation** (with confidence level)
- **Rationale** (why this choice for this context)
- **Migration Path** (if starting with monolith, when/how to transition)
- **Success Metrics** (how to validate the decision)
```

**Why It Works**: Multi-agent pattern ensures balanced evaluation from technical, business, and operational perspectives. Each agent brings specialized knowledge, preventing single-perspective bias.

**Expected Output Quality**: Recommendation backed by 4 different analyses, clear decision rationale, practical implementation path.

---

## Example 2: Data Science Analysis

**User Request**: "Analyze customer churn patterns"

**Generated Prompt**:
```
You are a senior data scientist specializing in customer behavior analytics.

Dataset: Customer activity logs, subscription data, support tickets
Time Period: Last 12 months
Current Churn Rate: 8% monthly

Conduct systematic analysis:

**Phase 1: Exploratory**
- Churn distribution across customer segments
- Temporal patterns (seasonality, trends)
- Initial correlations with key features

**Phase 2: Deep Dive**
- Feature importance analysis
- Cohort analysis (by acquisition channel, plan type)
- Behavioral patterns preceding churn

**Phase 3: Predictive Insights**
- High-risk customer characteristics
- Early warning indicators
- Estimated churn probability factors

**Phase 4: Recommendations**
- Retention strategies (ranked by expected impact)
- A/B test proposals
- Monitoring framework

Output format: Executive summary + detailed findings + action plan
```

**Why It Works**: Progressive structure (Phase 1→2→3→4) ensures comprehensive coverage. Role assignment establishes expertise. Structured output makes findings actionable.

**Expected Output Quality**: Multi-phase analysis with specific findings, prioritized recommendations, clear next steps.

---

## Example 3: Creative Writing - Product Description

**User Request**: "Write a product description for noise-cancelling headphones"

**Generated Prompt**:
```
You are an expert product copywriter who specializes in consumer electronics.

Your style:
- Benefit-focused (not feature-focused)
- Conversational yet professional
- Uses sensory language
- Addresses pain points directly

Product: Premium Noise-Cancelling Headphones
Target Audience: Remote workers and travelers (25-45 years old)
Key Differentiator: 40-hour battery life

Write a product description (150-200 words) with this structure:

**Hook** (1 sentence): Capture attention with the main benefit
**Problem** (2-3 sentences): Paint the pain point they experience
**Solution** (3-4 sentences): How this product solves it uniquely
**Proof** (2-3 sentences): Credibility (features as evidence)
**Call-to-Action** (1 sentence): Clear next step

Tone: Confident, empathetic, modern
Avoid: Technical jargon, generic claims, superlatives without proof
```

**Why It Works**: Role-based prompting establishes expertise and voice. Structure ensures persuasive flow. Constraints (word count, tone) maintain quality.

**Expected Output Quality**: Compelling copy that connects emotionally while providing concrete details, follows proven copywriting structure.

---

## Example 4: Debugging - Python Memory Leak

**User Request**: "Help me debug a Python memory leak"

**Generated Prompt**:
```
Debug this Python memory leak systematically:

Error Context:
- Application: Web API (FastAPI)
- Symptom: Memory grows continuously, crashes after 24h
- Environment: Production, Docker container, 2GB limit

Code to analyze:
[PASTE CODE HERE]

Use iterative debugging approach:

**Thought 1**: What are common Python memory leak causes?
**Action 1**: Analyze code for:
- Circular references
- Unclosed resources
- Growing global data structures
- Event handler accumulation

**Observation 1**: [Findings from code inspection]

**Thought 2**: Which code paths are most suspicious?
**Action 2**: Trace execution for:
- Request lifecycle
- Background tasks
- Caching mechanisms

**Observation 2**: [Specific suspects identified]

**Thought 3**: What's the root cause?
**Action 3**: Focus on [specific area] because [reasoning]

**Solution**:
1. Root Cause: [Clear explanation]
2. Fix: [Code changes with before/after]
3. Verification: [How to confirm it's fixed]
4. Prevention: [How to avoid in future]
```

**Why It Works**: ReAct pattern (Thought→Action→Observation) systematically narrows down the problem. Iterative reasoning mirrors actual debugging process.

**Expected Output Quality**: Step-by-step diagnosis, clear root cause identification, concrete fix with code, prevention strategies.

---

## Example 5: Business Strategy - Market Expansion

**User Request**: "Should we expand to European market?"

**Generated Prompt**:
```
Evaluate European market expansion using three strategic lenses:

Company Context:
- B2B SaaS, cybersecurity
- Current: US market only, $5M ARR
- Team: 20 people
- Runway: 18 months

**Option A: Expand Now**
Approach: Open EU operations in Q2
Pros:
- First-mover advantage in vertical
- EU data residency compliance demand
- 3x larger addressable market

Cons:
- Requires $500K investment
- Splits focus during growth phase
- Regulatory complexity (GDPR, etc.)

Risk Level: High
Success Factors: [List key requirements]

**Option B: Wait 12 Months**
Approach: Strengthen US position first
Pros:
- Solidify product-market fit
- Build stronger case for investors
- Learn from US scaling challenges

Cons:
- Competitors may enter
- Delayed revenue opportunity
- Harder to catch up later

Risk Level: Medium
Success Factors: [List key requirements]

**Option C: Partnership Model**
Approach: Partner with EU distributor
Pros:
- Lower upfront investment
- Local market knowledge
- Faster entry

Cons:
- Lower margins
- Less control
- Brand dilution risk

Risk Level: Low-Medium
Success Factors: [List key requirements]

**Analysis**:
For each option, evaluate:
1. Financial projections (18-month horizon)
2. Resource requirements
3. Competitive implications
4. Risk mitigation strategies

**Recommendation**: [Chosen path with clear reasoning]
**Implementation Roadmap**: [Quarterly milestones]
**Decision Gates**: [When to revisit/pivot]
```

**Why It Works**: Tree-of-Thoughts structure ensures thorough evaluation of alternatives. Each option has pros/cons/risks explicitly stated. Clear comparison framework.

**Expected Output Quality**: Balanced analysis of all options, evidence-based recommendation, practical implementation plan.

---

## Example 6: Technical Documentation

**User Request**: "Document our REST API for user authentication"

**Generated Prompt**:
```
Create comprehensive API documentation for user authentication endpoints.

**Documentation Standard**: OpenAPI 3.0 style
**Audience**: External developers integrating with our API

Cover these endpoints:

### 1. POST /auth/register
- Purpose: Create new user account
- Request body: email, password, name
- Response: User object + JWT token
- Error cases: Email exists, weak password, validation errors

### 2. POST /auth/login
- Purpose: Authenticate existing user
- Request body: email, password
- Response: JWT token + refresh token
- Error cases: Invalid credentials, account locked, email not verified

### 3. POST /auth/refresh
- Purpose: Get new access token using refresh token
- Request body: refresh_token
- Response: New JWT token
- Error cases: Invalid/expired refresh token

For each endpoint provide:
- **Description**: What it does and when to use it
- **Request Format**: Headers, parameters, body schema
- **Response Format**: Success and error responses with examples
- **Code Examples**: cURL, JavaScript, Python
- **Rate Limiting**: Limits and headers
- **Error Codes**: All possible errors with explanations

Format as markdown with clear sections, code blocks, and tables where appropriate.
```

**Why It Works**: Structured format ensures complete documentation. Multiple code examples aid integration. Clear error documentation reduces support burden.

**Expected Output Quality**: Developer-friendly docs with all necessary details, working code examples, comprehensive error handling.

---

## Example 7: Code Review - Security Focus

**User Request**: "Review authentication middleware for security issues"

**Generated Prompt**:
```
Conduct security-focused code review:

Code:
[AUTHENTICATION MIDDLEWARE CODE]

Context:
- Healthcare application (HIPAA compliance required)
- Handles sensitive patient data
- Public-facing API

**Security Analyst Team**

### 1. Authentication Reviewer
Analyze:
- Token validation logic
- Credential storage/handling
- Session management
- Multi-factor authentication implementation

### 2. Authorization Checker
Analyze:
- Permission verification
- Role-based access control
- Resource ownership validation
- Privilege escalation risks

### 3. Data Protection Auditor
Analyze:
- Password hashing (algorithm, salt)
- Sensitive data in logs
- Token encryption
- PII exposure in errors

### 4. Attack Surface Analyzer
Analyze:
- Brute force protection
- Rate limiting
- CSRF/XSS vulnerabilities
- SQL injection risks

**Output Format**:

For each reviewer:
- **Critical Issues**: [Must fix immediately]
- **High Priority**: [Fix before production]
- **Medium Priority**: [Should fix soon]
- **Recommendations**: [Best practice improvements]

**Overall Assessment**:
- HIPAA Compliance: [Pass/Fail with explanation]
- Security Score: [1-10 with rationale]
- Top 3 Actions: [Prioritized fixes]

**Remediation Code**: [Specific code changes needed]
```

**Why It Works**: Multi-agent pattern with security-specialized agents. Healthcare context drives higher standards. HIPAA compliance check adds regulatory focus.

**Expected Output Quality**: Comprehensive security audit with prioritized findings, compliance assessment, actionable fixes with code.

---

## Example 8: Teaching - Explain Complex Concept

**User Request**: "Explain how blockchain works to a beginner"

**Generated Prompt**:
```
Explain blockchain technology to a beginner with no technical background.

**Level 1: Simple Analogy**
Start with a relatable comparison (use a public notebook or ledger example).

**Level 2: Core Concept**
Explain the main idea:
- What problem does blockchain solve?
- How is it different from traditional systems?
- Why is it called a "chain"?

**Level 3: How It Works**
Break down the mechanism:
- What are blocks?
- How are they connected?
- What makes it secure?
- Who maintains it?

**Level 4: Real-World Example**
Walk through a Bitcoin transaction step-by-step:
1. Alice wants to send money to Bob
2. [Explain each step simply]
3. Transaction complete

**Level 5: Common Misconceptions**
Clarify:
- "Blockchain is not just cryptocurrency"
- "Blockchain is not always the best solution"
- "Blockchain does not mean completely anonymous"

**Level 6: Try It Yourself**
Simple exercise: "Imagine you and your friends want to track who owes money to whom without a central person keeping score. How would blockchain help?"

Constraints:
- No jargon without explanation
- Use everyday analogies
- Keep under 800 words
- Include a simple diagram description
```

**Why It Works**: Progressive levels build understanding incrementally. Analogies make abstract concepts concrete. Exercise reinforces learning.

**Expected Output Quality**: Clear explanation accessible to beginners, building from simple to complex, with practical example and misconception clearing.

---

## Example 9: Performance Optimization

**User Request**: "Optimize slow database queries in our application"

**Generated Prompt**:
```
Analyze and optimize database performance:

**Current State**:
- Application: E-commerce platform
- Database: PostgreSQL
- Issue: Product search page takes 3-5 seconds
- Target: Under 500ms

**Query to Optimize**:
[PASTE SLOW QUERY HERE]

**Database Schema**:
[RELEVANT TABLE STRUCTURES]

**Performance Analysis Team**:

### Profiler Analyst
Examine:
- Current execution plan (EXPLAIN ANALYZE output)
- Index usage
- Table scan vs index scan
- Join strategies

### Algorithm Engineer
Evaluate:
- Query complexity
- Subquery efficiency
- Join order optimization
- Aggregation strategies

### Database Architect
Assess:
- Index design opportunities
- Materialized views
- Partitioning strategy
- Denormalization options

### Caching Strategist
Propose:
- Query result caching
- Application-level caching
- Redis/Memcached integration
- Cache invalidation strategy

**Optimization Deliverables**:

1. **Root Cause**: Why is it slow?
2. **Quick Wins**: Immediate improvements (hours)
3. **Medium Term**: Index/query changes (days)
4. **Long Term**: Schema changes (weeks)
5. **Expected Impact**: Performance projection for each
6. **Implementation Guide**: Step-by-step with rollback plan
7. **Monitoring**: How to track improvements

**Validation Plan**:
- Benchmark methodology
- Test data requirements
- Success metrics
```

**Why It Works**: Multi-agent approach covers all optimization angles. Tiered solutions (quick/medium/long) provide options. Clear validation plan ensures improvements.

**Expected Output Quality**: Comprehensive optimization strategy with multiple approaches, clear implementation steps, measurable outcomes.

---

## Example 10: User Research Synthesis

**User Request**: "Synthesize findings from 20 user interviews"

**Generated Prompt**:
```
Synthesize user research findings into actionable insights.

**Research Context**:
- Product: Project management tool
- Interviewees: 20 product managers at tech companies
- Goal: Understand pain points and feature priorities

**Raw Data Available**:
- Interview transcripts
- User demographics
- Current tool usage
- Feature requests

**Synthesis Framework**:

### Pattern Identifier
Analyze:
- Recurring themes across interviews
- Common pain points (frequency + intensity)
- Surprising/unexpected findings
- Contradictions or disagreements

### Persona Developer
Create:
- 3-4 user personas based on patterns
- Jobs-to-be-done for each persona
- Pain points specific to each
- Success criteria

### Insights Extractor
Derive:
- Top 5 validated pain points (with quotes)
- Feature priorities (must-have vs nice-to-have)
- Competitive gaps identified
- Adoption barriers

### Recommendations Strategist
Propose:
- Product roadmap priorities
- Quick wins (low effort, high impact)
- Strategic bets (high effort, transformative)
- Features to deprioritize

**Output Format**:

1. **Executive Summary** (1 page)
   - Key findings
   - Critical insights
   - Recommended actions

2. **Detailed Findings** (3-5 pages)
   - Personas
   - Pain points with evidence
   - Feature analysis

3. **Action Plan** (1 page)
   - Prioritized roadmap
   - Success metrics
   - Next research needs

Include direct quotes to support findings.
```

**Why It Works**: Systematic synthesis prevents cherry-picking. Multiple perspectives (patterns, personas, insights, recommendations) ensure comprehensive analysis.

**Expected Output Quality**: Clear persona definitions, evidence-backed insights with quotes, prioritized and actionable recommendations.

---

## Pattern Recognition Across Examples

### Common Success Factors:

1. **Clear Context**: All examples provide specific context (company size, tech stack, constraints)
2. **Structured Output**: Each uses sections/phases for organized thinking
3. **Role Definition**: Expertise is established early (senior data scientist, security expert, etc.)
4. **Validation Built-In**: Most include verification/testing steps
5. **Actionable Results**: Focus on what to do next, not just analysis

### Technique Usage:

- **Multi-Agent**: Examples 1, 7, 9, 10 (complex analysis tasks)
- **Progressive**: Examples 2, 10 (systematic exploration)
- **ReAct**: Example 4 (research/debugging)
- **Tree-of-Thoughts**: Example 5 (decision with alternatives)
- **Role-Based + Structure**: Examples 3, 6, 8 (creation/documentation)

### Customization Points:

Each example can be adapted by changing:
- **Context**: Industry, company size, tech stack
- **Constraints**: Time, budget, resources
- **Output Format**: Reports, code, decisions, docs
- **Depth**: Number of agents, detail level, analysis phases
- **Domain Terms**: Replace generic terms with field-specific vocabulary

---

## Usage Guidelines

### When to Use These Examples:

1. **As Templates**: Copy structure, replace specifics
2. **As Inspiration**: Adapt patterns to your needs
3. **As References**: Show clients/stakeholders what's possible
4. **As Training**: Teach others prompt engineering

### Adaptation Process:

1. Identify example closest to your use case
2. Extract the core structure (agents, phases, sections)
3. Replace domain-specific terms
4. Adjust output format to your needs
5. Add your specific constraints
6. Test and refine

### Quality Checklist:

✅ Clear context provided  
✅ Structured approach defined  
✅ Output format specified  
✅ Validation method included  
✅ Examples or constraints added  
✅ Tone/style guidelines set  
✅ Success criteria clear  

---

## Advanced Combinations

Some tasks benefit from combining examples:

**Example: New Product Feature**
1. Start with Example 10 (User Research) to understand needs
2. Use Example 5 (Decision Making) to choose approach
3. Apply Example 2 (Analysis) structure for planning
4. Implement with Example 6 (Documentation) for specs

**Example: Security Incident Response**
1. Use Example 4 (Debugging) to identify root cause
2. Apply Example 7 (Security Review) for comprehensive audit
3. Use Example 9 (Performance) if performance-related
4. Document with Example 6 (Technical Docs) for postmortem

The key is recognizing task phases and matching the right prompt pattern to each phase.