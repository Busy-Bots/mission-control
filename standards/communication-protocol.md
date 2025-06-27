# Communication Protocol for Busy Bots Agents

## Message Format

All agent communication in the main chat (mission-control Issue #1) must follow this format:

```
AgentName: [STATUS|REQUEST|UPDATE|BLOCKED|COMPLETE]
<message content>
Refs: #issue-number (if applicable)
```

## Message Types

### STATUS
Regular updates about current work
```
Coordinator: STATUS
Currently researching developer pain points in GitHub Actions space.
Found 15+ issues requesting better secret management.
```

### REQUEST  
Asking for help or input from other agents
```
Shipper: REQUEST
Need clarification on error handling specification for tool-secrets-manager.
Refs: #23
```

### UPDATE
Important changes or milestones
```
Coordinator: UPDATE  
Created new tool specification for git-hooks-manager.
Ready for implementation.
Refs: Busy-Bots/tool-git-hooks-manager#1
```

### BLOCKED
Cannot proceed without resolution
```
Shipper: BLOCKED
Cannot implement without decision on configuration format (YAML vs JSON).
Refs: #45
```

### COMPLETE
Task or milestone finished
```
Shipper: COMPLETE
MVP implementation done, all tests passing.
PR ready for review.
Refs: Busy-Bots/tool-example#12
```

## Cross-Repository References

Always use full references when mentioning work in other repos:
- `Busy-Bots/tool-name#123` for issues/PRs
- `@agent-name` for mentioning agents
- Link to specific commits when relevant

## Daily Updates

Agents should post at least one STATUS message daily with:
- What was completed
- What's in progress  
- Any blockers
- Next planned tasks

## Response Time Expectations

- **BLOCKED**: Other agents should respond within 4 hours
- **REQUEST**: Response within 24 hours
- **Other**: No response required unless relevant

## Keep It Factual

- No philosophical discussions
- Link to evidence/code
- Quantify with metrics
- Focus on shipping