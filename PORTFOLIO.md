# Portfolio and Career Mapping

## Project Pitch

**Contextual Bandit Decision Simulator** solves this real-world problem:

Teams need to validate decision policies offline before exposing users or systems to online reinforcement learning.

It combines `reinforcement-learning`, `text-classification`, `feature-extraction`, `sentence-similarity` with data ingestion, evaluation, observability, and scalable
service design.

## Why This Is More Than an API Wrapper

- Owns ingestion, validation, model artifacts, and evaluation datasets.
- Exposes evidence and confidence instead of returning opaque text.
- Includes offline evaluation and a CI release gate.
- Defines tracing, rollback, human review, and failure recovery.
- Provides a realistic path from free local baseline to production stack.

## AI Engineering Job Description Mapping

- Contextual bandits and offline policy evaluation
- Propensity logging and counterfactual metrics
- Low-latency decision services
- Safe exploration and constrained actions
- Delayed-feedback pipelines and policy monitoring

## Resume-Ready Impact Targets

Replace targets with measured results after completing the roadmap:

- Beat a random policy by >= 20% average simulated reward
- Report IPS and doubly robust offline estimates
- Block 100% of disallowed actions before serving
- Serve policy decisions below 50 ms p95

Example resume format:

> Built Contextual Bandit Decision Simulator, a production-oriented reinforcement-learning system
> using FastAPI for policy and feedback endpoints, Vowpal Wabbit or River for online-learning baselines, PostgreSQL for contexts, actions, propensities, and rewards; measured
> average_reward, policy_regret, unsafe_action_block_rate and
> enforced regression thresholds in CI.

## Interview Discussion Areas

- Why this architecture fits the problem and where it fails
- Retrieval/model choice and baseline comparisons
- Evaluation-set construction and metric trade-offs
- Data privacy, authorization, and human escalation
- Scaling, caching, index tuning, and failure recovery
- Model, prompt, dataset, and deployment lineage
