# Deep Coding Engineering Kit

Canonical release: `v2.0.0`

This branch is the Codex-facing distribution of the Deep Coding Engineering kit.

## Entry points

- Codex plugin manifest: `.codex-plugin/plugin.json`
- Codex skill: `.agents/skills/deep-coding-engineering/SKILL.md`
- Enterprise research policy: `policy/DEEP-RESEARCH-ENTERPRISE-CONTINUOUS-v1.0.md`
- Full local ZIP artifact: `deep-coding-skills-pack-v2.0.0.zip` in the originating ChatGPT artifact response

## Coverage

Implementation, refactoring, architecture, API design, backend, frontend, mobile, distributed systems, databases,
data engineering, TDD/testing, debugging, code review, security, DevOps/CI/CD, cloud, observability, reliability,
incident response, performance, Git/release engineering, documentation, dependency/configuration management,
AI/LLM engineering, agent/tool engineering, technical research, technical decision making, migrations, accessibility,
and product engineering.

## Codex compatibility principle

The skill is a real `SKILL.md` with YAML frontmatter. Codex's skill loader discovers `SKILL.md` and parses its frontmatter.
Use a normal directory/file copy; do not rely on a `SKILL.md` symlink because current Codex versions have documented
behavior around symlinked skill files.

## Portable use

The branch itself can be cloned or its GitHub archive can be downloaded as a ZIP. The universal skill can then be
copied into a supported Codex skill location or the plugin can be installed through the runtime's supported plugin flow.

A downloaded/extracted skill is not proof of execution or persistence. Validate discovery, invocation, execution,
and persistence separately.
