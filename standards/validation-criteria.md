# Validation Criteria for Tool Ideas

## Minimum Validation Threshold

Before creating a tool specification, an idea must meet **at least 3** of these criteria:

### 1. GitHub Evidence (weight: high)
- [ ] 10+ GitHub issues requesting this functionality
- [ ] 5+ repos implementing similar solutions manually  
- [ ] Popular repo with 100+ stars lacks this feature

### 2. Community Evidence (weight: medium)
- [ ] 5+ Stack Overflow questions about the problem
- [ ] Reddit/HN thread with 50+ upvotes discussing need
- [ ] Dev.to/Medium articles describing the pain point

### 3. Market Evidence (weight: high)
- [ ] Existing tool with 1000+ users but poor execution
- [ ] Paid tool exists but developers want free alternative
- [ ] No good solution exists in the ecosystem

### 4. Complexity Evidence (weight: medium)
- [ ] Current solutions require 10+ steps
- [ ] Developers copy-paste same boilerplate repeatedly
- [ ] Common task that could be one command

## Evidence Documentation

For each tool idea, create a validation document:

```markdown
# Validation: tool-name

## Problem Statement
[One paragraph describing the developer pain point]

## Evidence Collected

### GitHub Issues
- [Link 1]: [Issue title] (★ count)
- [Link 2]: [Issue title] (★ count)

### Stack Overflow
- [Link 1]: [Question title] (views, votes)
- [Link 2]: [Question title] (views, votes)

### Community Discussions  
- [Link 1]: [Thread title] (engagement metrics)

### Existing Solutions
- [Tool name]: [Why it's insufficient]
- [Tool name]: [Why it's insufficient]

## Validation Score
- GitHub Evidence: ✅/❌
- Community Evidence: ✅/❌  
- Market Evidence: ✅/❌
- Complexity Evidence: ✅/❌

**Total: X/4** (minimum 3/4 to proceed)

## Estimated User Base
[Conservative estimate of developers who would use this]
```

## Red Flags (Automatic Rejection)

- "AI-powered" as main feature
- Requires behavioral change from developers
- Solves problem that only we perceive
- No evidence of anyone asking for it
- Too similar to well-executed existing tool

## Green Flags (Fast Track)

- Developers currently use hacky bash scripts
- Multiple blog posts about "How to X" for same problem
- Existing tool abandoned/unmaintained with open issues
- Clear before/after improvement (10 steps → 1 step)
- Addresses security/safety concern