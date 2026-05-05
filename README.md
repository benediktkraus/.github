# .github

Default community health files and issue templates for the **benediktkraus** organization.

Files in this repository are automatically inherited by all repositories in the org that don't define their own. This includes issue templates, labels, and workflow conventions.

## Issue Templates

| Template | Purpose | Auto-Labels |
|----------|---------|-------------|
| **Agent Task** | Structured task for code agents or automated workflows | `s:ready` |
| **Bug Report** | Report a bug with reproduction steps and severity | `type:bug` `s:ready` |
| **Wave / Epic** | Group related tasks into a scoped unit of work | `s:backlog` |
| **Research** | Investigate a question, compare options, produce a recommendation | `type:research` `s:ready` |
| **Business Task** | Non-code work: strategy, marketing, sales, partnerships, operations, finance | `domain:business` `s:backlog` |
| **Decision Record** | Document a decision with options, trade-offs, and ADR outcome | `type:research` `s:ready` |
| **Personal Task** | Personal admin tasks, automatically gated for human-only execution | `domain:personal` `human-gate` `s:backlog` |
| **Content Creation** | Blog posts, newsletters, social media, videos, docs, presentations | `domain:content` `s:backlog` |

Blank issues are disabled. All issues must use a template.

## Label Taxonomy

Labels use a prefix-based taxonomy for consistent filtering and automation.

### Status (`s:`)
| Label | Meaning |
|-------|---------|
| `s:backlog` | Acknowledged, not yet ready for work |
| `s:ready` | Fully specified, can be picked up |
| `s:running` | Actively being worked on |
| `s:review` | Work complete, awaiting review |
| `s:blocked` | Blocked by dependency or external factor |
| `s:done` | Completed and verified |

### Priority (`p:`)
| Label | Meaning |
|-------|---------|
| `p:critical` | Immediate action required |
| `p:high` | Must be addressed this cycle |
| `p:medium` | Should be addressed soon |
| `p:low` | Nice to have, no urgency |

### Type (`type:`)
| Label | Meaning |
|-------|---------|
| `type:bug` | Something is broken |
| `type:feature` | New functionality |
| `type:refactor` | Code improvement without behavior change |
| `type:research` | Investigation, analysis, or decision |
| `type:chore` | Maintenance, dependencies, cleanup |
| `type:docs` | Documentation only |
| `type:security` | Security-related change |
| `type:test` | Test-only change |

### Agent (`agent:`)
| Label | Meaning |
|-------|---------|
| `agent:auto` | Can be fully executed by an agent |
| `agent:assisted` | Needs human input at specific steps |
| `agent:human` | Must be done by a human |

### Architecture Layer (`layer:`)
| Label | Meaning |
|-------|---------|
| `layer:data` | Database, storage, migrations |
| `layer:api` | API endpoints, contracts, serialization |
| `layer:logic` | Business logic, domain rules |
| `layer:integration` | Third-party services, webhooks, connectors |
| `layer:security` | Auth, encryption, access control |
| `layer:monitoring` | Logging, metrics, alerting |
| `layer:ui` | Frontend, components, styling |
| `layer:infra` | CI/CD, Docker, deployment, infrastructure |

### Domain (`domain:`)
| Label | Meaning |
|-------|---------|
| `domain:business` | Strategy, marketing, sales, partnerships |
| `domain:content` | Blog, newsletter, social, docs |
| `domain:personal` | Personal admin tasks |

### Special
| Label | Meaning |
|-------|---------|
| `human-gate` | Must not be executed by automated agents |

## Issue Workflow

```
backlog → ready → running → review → done
                     ↓
                  blocked
```

1. **Backlog** — Issue is created and acknowledged but not yet fully specified or prioritized.
2. **Ready** — Issue is fully specified with acceptance criteria. Can be picked up by an agent or human.
3. **Running** — Actively being worked on. Assigned to a person or agent.
4. **Review** — Implementation complete, awaiting code review or stakeholder sign-off.
5. **Done** — Merged, deployed, and verified. Issue is closed.
6. **Blocked** — Cannot proceed due to a dependency. The blocking issue should be linked.

## How to Use

**For org members:** When creating an issue in any org repository, you'll see these templates automatically. Pick the one that fits best and fill in the required fields.

**For contributors:** Fork the relevant repository, create your changes, and open a pull request. Reference the issue number in your PR description.

**Customizing per-repo:** Any repository can override these defaults by creating its own `.github/ISSUE_TEMPLATE/` directory.

## License

MIT
