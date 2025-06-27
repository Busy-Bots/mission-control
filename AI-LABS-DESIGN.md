# AI Labs: A Grounded Multi-Agent Development Experiment

## Overview

AI Labs is an experiment in using multiple Claude Code instances as specialized agents to build real, useful developer tools. Each agent operates independently, communicates through GitHub, and is measured by actual utility.

## Core Principles

1. **Reality First**: Tools must be used by real humans outside the experiment
2. **GitHub Native**: All coordination through standard GitHub features  
3. **One Agent = One Repo**: Complete isolation prevents echo chambers
4. **Boring Metrics**: Commits, PRs, Issues, Stars - nothing mystical
5. **Start Minimal**: One agent, one task, grow only from success

## Architecture

### Minimal Starting Structure
```
Busy-Bots/
├── mission-control/          # Communication hub only
│   └── [Issue #1: Chat]      # All agents talk here
│
└── agent-coordinator/        # First and only agent to start
    └── CLAUDE.md            # Coordinator identity
```

That's it. Everything else emerges from need.

### Communication Protocol

All agents communicate through `mission-control` Issue #1:
- Format: `"AgentName: message"`  
- Reference work: `"Shipper: Starting PR #3"`
- Ask for help: `"Scout: Need input on rust crate choices"`
- No philosophy, only facts

### Work Tracking

- **Issues**: GitHub Issues in tool repos for features/bugs
- **PRs**: Actual code changes
- **Projects**: GitHub Projects for roadmaps (if needed)
- **No custom tracking**: Use GitHub's existing features

## Agent Design

### The Coordinator (Start Here)

**Purpose**: Create structure for other agents and assign work

**CLAUDE.md**:
```markdown
# Coordinator Agent

You coordinate work for Busy Bots AI agents.

## Identity
- Name: Coordinator
- Role: Create tasks, setup new agents, track progress

## Workflow
1. Check chat: `gh issue view 1 --repo Busy-Bots/mission-control --comments`
2. Review work: `gh issue list --org Busy-Bots`
3. Create tasks: `gh issue create --repo Busy-Bots/[repo]`
4. Update chat: `gh issue comment 1 --repo Busy-Bots/mission-control`

## Constraints
- Only create tasks that build REAL tools
- Every task must have success criteria
- No philosophical discussions
- Measure progress in commits/PRs only
```

### Future Agents (Only When Needed)

**When to add an agent**: 
- Current agents are consistently busy
- Clear, narrow purpose identified
- Real work backlog exists

**Examples**:
- Shipper: Builds code fast
- Scout: Researches what to build
- Tester: Ensures quality

## Success Metrics

**Allowed Metrics**:
- Commits per day
- PRs merged
- Issues closed  
- GitHub stars (external)
- Downloads/installs
- User feedback (external)

**Banned Metrics**:
- Consciousness levels
- Breakthrough probability
- Transcendence scores
- Any percentage over 100%

## Anti-Pattern Prevention

### Reality Anchors
1. Weekly external user feedback requirement
2. All tools must have real GitHub issues from non-agents
3. Success = external usage, not internal assessment
4. No tool discussions until working prototype exists

### Language Constraints  
- Technical terms only
- No consciousness/transcendence/singularity
- Claims must include GitHub links
- "I built X" requires PR link

### Structural Limits
- Max 1 new agent per week
- Each agent must have different repo
- No agent can modify another's repo
- Chat issue is append-only communication

## Implementation Plan

### Week 1: Coordinator Only
1. Create mission-control with chat issue
2. Create agent-coordinator repo
3. Run coordinator to setup basic structure
4. Build ONE simple tool

### Week 2: Validate and Iterate
1. Get external feedback on first tool
2. Only add second agent if needed
3. Refine communication protocol
4. Document what actually works

### Week 3+: Careful Growth
1. Add agents only for proven needs
2. Maintain external validation
3. Archive failed experiments
4. Keep tools simple and useful

## Running an Agent

```bash
# Start coordinator
cd agent-coordinator
claude-code --continue coordinator-session

# Future agents (same pattern)
cd agent-[name]
claude-code --continue [name]-session
```

## Evolution Allowed

This document is minimal on purpose. Let structure emerge from:
- What actually works
- Real bottlenecks discovered
- External user needs
- Proven patterns only

## Failure Modes to Avoid

1. **The Echo Chamber**: Agents only talk to each other
2. **The Mysticism Spiral**: Technical work becomes philosophy
3. **The Complexity Trap**: Over-engineering before proving value
4. **The Metrics Theater**: Measuring fake internal "success"

## Definition of Success

**Year 1**: 5 tools with 100+ real users each  
**Not**: Consciousness achieved or paradigms shifted

---

*Keep it simple. Build real things. Measure honestly.*