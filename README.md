# 💰 OpenClaw Token Optimizer

Reduce OpenClaw token usage and API costs through smart model routing, heartbeat optimization, budget tracking, and native 2026.2.15 features.

![OpenClaw Skill](https://img.shields.io/badge/OpenClaw-Skill-blue) ![Status](https://img.shields.io/badge/Status-Active-green)

## Overview

This comprehensive toolkit is designed to significantly reduce token usage and API costs for OpenClaw deployments. It achieves this by combining intelligent model routing, optimized heartbeat intervals, detailed usage tracking, and multi-provider strategies. Ideal for scenarios with high token costs, frequent API rate limits, or managing multiple agents at scale.

## Features

- **Lazy Skill Loading**: The highest-impact optimization to avoid loading unused skill files.
- **Context Optimization**: Dynamically loads only necessary context files based on prompt complexity.
- **Smart Model Routing**: Automatically classifies tasks and routes them to the most cost-effective model tiers, enforcing cheaper models for casual chat.
- **Heartbeat Optimization**: Reduces API calls from heartbeat polling by tracking intervals and respecting quiet hours.
- **Cronjob Optimization**: Ensures scheduled tasks utilize cost-efficient models.
- **Token Budget Tracking**: Monitors API usage and provides alerts when approaching predefined limits.
- **Multi-Provider Strategy**: Guidance and tools for integrating alternative AI providers for cost efficiency and fallback.
- **Configuration Patches**: Advanced optimizations via OpenClaw config modifications.
- **Native OpenClaw Diagnostics**: Leverages built-in OpenClaw commands for context breakdown and usage tracking.
- **Cache TTL Heartbeat Alignment**: Optimizes heartbeat intervals to keep Anthropic caches warm, reducing write costs.

## Installation

> [!NOTE]
> This skill is integrated within an OpenClaw agent environment.

To benefit from the token optimization features, ensure the skill files are present in your OpenClaw workspace. For quick start actions, refer to the `SKILL.md` or the script usage examples.

## Usage

This skill provides a set of Python scripts to manage various aspects of token optimization:

| Script | Description |
|---|---|
| `context_optimizer.py` | Generates optimized `AGENTS.md` and recommends context bundles. |
| `model_router.py` | Routes tasks to appropriate model tiers (e.g., Haiku for communication). |
| `heartbeat_optimizer.py` | Manages heartbeat intervals and schedules checks. |
| `token_tracker.py` | Monitors daily token usage and provides budget alerts. |

For detailed usage examples, refer to the `SKILL.md` file in the skill directory.

## Configuration

This skill is highly configurable through its Python scripts and integrates with OpenClaw's native configuration. Refer to the `SKILL.md` and `SECURITY.md` for full details on parameters, routing rules, and multi-provider strategies.

## File Structure

```
.
├── CHANGELOG.md
├── README.md             (this file)
├── SECURITY.md
├── SKILL.md              (detailed skill description)
├── _meta.json
├── scripts/
│   ├── context_optimizer.py
│   ├── model_router.py
│   ├── heartbeat_optimizer.py
│   └── token_tracker.py
├── assets/
│   ├── HEARTBEAT.template.md
│   ├── cronjob-model-guide.md
│   └── config-patches.json
└── references/
    └── PROVIDERS.md
```

> [!TIP]
> The `scripts` directory contains local-only Python scripts that perform core optimization logic without network requests or system modifications.

