## Snap Definition (v0)

---

## Snap Threshold Parameters (v0)

epsilon_delta_structure = 0.05
eta_evaluation_gain = 0.05
persistence_required = 3
persistence_tolerance = 0.01

Definitions:

delta_structure:
  Numeric structural delta supplied by evaluator.
  Must be >= epsilon_delta_structure.

evaluation_gain:
  Current evaluation_score minus max(previous 3 evaluation_scores).
  Must be >= eta_evaluation_gain.

persistence:
  Evaluation score must remain within persistence_tolerance
  of the snap-triggering score for persistence_required rotations.
