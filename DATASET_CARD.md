---
license: cc-by-4.0
language:
- en
pretty_name: Contextual Bandit Decision Simulator Synthetic Evaluation Set
size_categories:
- n<1K
task_categories:
- reinforcement-learning
tags:
- synthetic
- reinforcement-learning
- evaluation
- reinforcement-learning
- text-classification
- feature-extraction
- sentence-similarity
configs:
- config_name: default
  data_files:
  - split: train
    path: data/train.jsonl
  - split: test
    path: data/test.jsonl
---

# Contextual Bandit Decision Simulator Synthetic Dataset

## Summary

This dataset contains 14 training examples and 4
held-out examples for **Teams need to validate decision policies offline before exposing users or systems to online reinforcement learning.**

Every record is synthetic and includes:

- `input`: query, event, or feature description
- `label`: expected class, route, relation, or evidence category
- `context`: synthetic supporting context
- `source`: fictional source identifier
- `variant`: generation pattern
- `synthetic`: always `true`

## Uses

- Reproducible unit and integration tests
- Baseline model training
- Evaluation harness development
- Schema and architecture demonstrations

## Limitations

Offline simulated rewards cannot prove online safety or business impact. Real experiments require review and guardrails.

This dataset does not represent real users, patients, customers, production
traffic, or licensed media. It must not be presented as real-world evidence.

## Related Model

[{{HF_NAMESPACE}}/contextual-bandit-simulator-20260923-model](https://huggingface.co/{{HF_NAMESPACE}}/contextual-bandit-simulator-20260923-model)
