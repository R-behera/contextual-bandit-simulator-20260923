# Contextual Bandit Decision Simulator

A safe offline contextual-bandit simulator for comparing exploration policies before production experimentation.

Generated on 2026-09-23 as an independent production-AI architecture project.

## Real-World Problem

Teams need to validate decision policies offline before exposing users or systems to online reinforcement learning.

## Hugging Face Tasks

- `reinforcement-learning`
- `text-classification`
- `feature-extraction`
- `sentence-similarity`

## Recommended Production Stack

- FastAPI for policy and feedback endpoints
- Vowpal Wabbit or River for online-learning baselines
- PostgreSQL for contexts, actions, propensities, and rewards
- Redis for low-latency policy serving
- MLflow for policy versioning
- OpenTelemetry for decisions and delayed rewards

## Included

- Runnable Python pipeline with no runtime dependencies
- Local JSON HTTP inference service
- Public-data API connector with explicit provenance
- Reproducible training script
- Held-out evaluation command
- Synthetic dataset with explicit provenance
- Trained transparent baseline model
- Architecture and production-boundary documentation
- Unit tests, CI workflow, and Dockerfile
- Hugging Face-ready model and dataset cards

## Architecture

1. Context and action schema
1. Offline reward simulator
1. Epsilon-greedy baseline
1. Policy regret report
1. Safety action constraints

See [ARCHITECTURE.md](ARCHITECTURE.md) for the full flow and production
boundaries.

## Quick Start

```bash
python3 -m unittest discover -s tests
PYTHONPATH=src python3 -m contextual_bandit.cli "experienced user asks for API parameter details"
PYTHONPATH=src python3 evaluate.py
PYTHONPATH=src python3 -m contextual_bandit.service
```

The service exposes `GET /health` and `POST /predict`.

Rebuild the model:

```bash
python3 train.py
```

## Baseline Evaluation

- Held-out synthetic examples: 4
- Accuracy: 1
- Target metrics: average_reward, policy_regret, unsafe_action_block_rate

This score verifies that the code and evaluation contract work. It does not
claim production performance.

## Hugging Face Artifacts

When the controller has a Hugging Face token and namespace configured, it
publishes:

- Dataset: `contextual-bandit-simulator-20260923-dataset`
- Model: `contextual-bandit-simulator-20260923-model`

## Portfolio Value

This repository maps to production AI engineering work in:

- Contextual bandits and offline policy evaluation
- Propensity logging and counterfactual metrics
- Low-latency decision services
- Safe exploration and constrained actions
- Delayed-feedback pipelines and policy monitoring

See [PORTFOLIO.md](PORTFOLIO.md) for resume-ready impact targets and interview
discussion areas.

## 1-3 Month Expansion

Follow [ROADMAP.md](ROADMAP.md) to add real-world APIs, a stronger open model,
durable orchestration, evaluation, observability, scalability testing, and a
public deployment.

## Safety

Offline simulated rewards cannot prove online safety or business impact. Real experiments require review and guardrails.

Review [ARCHITECTURE.md](ARCHITECTURE.md),
[PRODUCTION.md](PRODUCTION.md), [SECURITY.md](SECURITY.md),
[MODEL_CARD.md](MODEL_CARD.md), and [DATASET_CARD.md](DATASET_CARD.md) before
adapting this project.
