# Prompt Engineering Framework Overview

## Core Paradigms (Liu et al. 2021)

### Pre-train, Prompt, and Predict
The modern NLP paradigm where:
1. Models are pre-trained on large text corpora
2. Tasks are reformulated as text-to-text prompts
3. Model generates predictions based on prompt structure

### Key Insight
"The way we phrase the prompt fundamentally shapes the model's behavior and output quality."

## Technique Taxonomy (Schulhoff et al. 2024)

### Category 1: Basic Instruction
- Zero-Shot: Direct task instruction
- Few-Shot: Task + examples
- Role-Based: Assign expertise/persona

### Category 2: Reasoning Enhancement
- Chain-of-Thought: Explicit reasoning steps
- Self-Consistency: Multiple paths + voting
- Tree-of-Thoughts: Branch exploration
- Least-to-Most: Progressive complexity

### Category 3: Agentic Patterns
- ReAct: Reasoning + Acting cycles
- Reflexion: Self-reflection + improvement
- Multi-Agent: Coordinated specialists

### Category 4: Output Control
- Structured Output: Format specification
- Template-Based: Fill-in patterns
- Constrained Generation: Rule-based limits

### Category 5: Context Enhancement
- Retrieval-Augmented: External knowledge
- Example Selection: Optimal few-shot examples
- Context Distillation: Key information extraction

## Performance Characteristics

### Task Type Performance Matrix

| Technique | Math/Logic | Creative | Analysis | Code | General Q&A |
|-----------|------------|----------|----------|------|-------------|
| Zero-Shot | ⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐⭐⭐⭐ |
| Few-Shot | ⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ |
| Chain-of-Thought | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐ |
| ReAct | ⭐⭐⭐ | ⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐⭐ |
| Multi-Agent | ⭐⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ |

## Evidence Base

### Most Cited Techniques (Schulhoff et al. 2024)
1. Chain-of-Thought: 1,800+ citations
2. ReAct: 850+ citations
3. Self-Consistency: 900+ citations
4. Tree-of-Thoughts: 600+ citations

### Performance Improvements
- CoT on math: +40% accuracy (GSM8K benchmark)
- Self-Consistency: +15-20% over single-path CoT
- Few-Shot: +10-30% over zero-shot (task-dependent)
- Multi-Agent: +30-40% in complex analysis tasks