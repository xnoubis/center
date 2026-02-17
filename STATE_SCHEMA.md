# STATE_SCHEMA v0

The Center state is structural-only and content-free.

It must contain the minimum data required to:

- Maintain rotation continuity
- Record structural evolution
- Evaluate snap conditions
- Support deterministic replay

---

## Core Fields

seed:
  deterministic replay seed (integer or hex)

rotation_index:
  integer incremented each activation

active_constraints:
  list of constraint descriptors

descriptor_history:
  list of structural descriptor hashes (ordered)

snap_history:
  list of:
    rotation_index
    snap_flag (true/false)
    snap_type
    delta_structure
    evaluation_gain
    persistence_count

evaluation_history:
  list of:
    rotation_index
    evaluation_score

current_objective:
  active optimization direction

current_spine:
  identifier of active expert / spine

---

## Invariants

1. No conversational text stored.
2. No agent identity privilege.
3. All fields deterministic and replayable.
4. State must be serializable as JSON.
5. Any modification produces a new descriptor hash.

The Center is not interpretation.
It is state.
