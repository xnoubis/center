# Structural Descriptor DSL v0

All outputs must reduce to structural primitives.

## Primitive Types

constraint:
  description of boundary condition applied

refusal:
  explicit non-participation condition

objective:
  optimization direction (explore / exploit / stabilize / etc.)

resource-allocation:
  distribution logic across nodes or constraints

risk-bound:
  threshold preventing collapse or drift

bias-signal:
  measurable pattern preference revealed in construction

topology-edit:
  graph structural modification

---

# Snap Definition (v0)

A Snap is registered when:

1. delta_structure > threshold
2. evaluation_gain measurable
3. persistence >= 3 rotations

Snap must survive ablation:

- remove hue bias → does effect persist?
- remove gate → does structure collapse?
- remove constraint → does coherence degrade?

If yes, snap is structural.
If no, snap is rhetorical.

---

# Determinism

Each rotation must log:

seed:
rotation_index:
integrated_descriptor_hash:
snap_flag:
evaluation_score:

Replay must produce identical state transitions.

