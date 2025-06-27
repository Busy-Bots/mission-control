# Agent Registry

Track all active agents, their capabilities, and current status.

## Active Agents

### Coordinator
- **Repository**: [agent-coordinator](https://github.com/Busy-Bots/agent-coordinator)
- **Session**: `claude-code --continue coordinator-session`
- **Status**: 🟢 Active
- **Created**: 2025-06-27
- **Capabilities**:
  - Create task specifications
  - Manage GitHub organization  
  - Track progress across repos
  - Design new agent roles
  - Document patterns
- **Current Focus**: Researching first tool to build
- **Cannot Do**: Write code, implement features

## Planned Agents

### Shipper
- **Repository**: Not created
- **Status**: 📋 Planned
- **Purpose**: Fast implementation of specifications
- **Activation Criteria**: First tool specification approved
- **Capabilities**:
  - Implement features to spec
  - Write tests
  - Create PRs
  - Ship MVPs quickly

### Scout  
- **Repository**: Not created
- **Status**: 📋 Planned
- **Purpose**: Research and validate tool ideas
- **Activation Criteria**: Need for continuous market research
- **Capabilities**:
  - Monitor developer communities
  - Validate pain points
  - Track ecosystem trends
  - Report opportunities

### Tester
- **Repository**: Not created
- **Status**: 📋 Planned  
- **Purpose**: Ensure quality and reliability
- **Activation Criteria**: Multiple tools in production
- **Capabilities**:
  - Write comprehensive tests
  - Set up CI/CD
  - Performance testing
  - Security audits

### Architect
- **Repository**: Not created
- **Status**: 📋 Planned
- **Purpose**: Design complex system architectures
- **Activation Criteria**: Tool requiring complex design
- **Capabilities**:
  - System design
  - API design
  - Architecture decisions
  - Technical documentation

## Agent Creation Process

1. Coordinator identifies need based on workload
2. Coordinator creates agent specification
3. Human approves new agent
4. Coordinator creates:
   - New repository `agent-[name]`
   - CLAUDE.md with role definition
   - Initial workspace structure
5. Human starts agent session
6. Agent joins main chat

## Communication Hub

All agents communicate via: [mission-control Issue #1](https://github.com/Busy-Bots/mission-control/issues/1)

## Metrics

- **Total Agents**: 1 active, 4 planned
- **Messages/Day**: ~5
- **Tasks Completed**: 0
- **Tools Shipped**: 0