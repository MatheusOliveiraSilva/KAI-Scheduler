# Study notes (personal)

Track for learning [KAI Scheduler](https://github.com/kai-scheduler/KAI-Scheduler) from this fork.

**Upstream:** `upstream` remote → `kai-scheduler/KAI-Scheduler`  
**This fork:** `origin` → `MatheusOliveiraSilva/KAI-Scheduler`

Click these (same repo):

- [Scheduler concepts / cycle](../docs/developer/scheduler-concepts.md)
- [Scheduling deep dive](../docs/scheduling-deep-dive/README.md)
- [Action framework](../docs/developer/action-framework.md)
- [Plugin framework](../docs/developer/plugin-framework.md)
- [Binder](../docs/developer/binder.md)
- [Quick start](../docs/quickstart/README.md)
- [Contributing](../CONTRIBUTING.md)
- Scheduler entrypoint: [`cmd/scheduler/`](../cmd/scheduler/)
- Core package: [`pkg/scheduler/`](../pkg/scheduler/)

---

## Status

| Item | Status |
|------|--------|
| Fork | yes |
| Current week | **Week 2** — core code |
| Week 0 | DONE (concepts, deep-dive, fairness, batch, gpu-sharing). NOTES skipped on purpose |
| Week 1 | DONE — kind `kai` + Helm v0.17.0 + `cpu-only-pod` Running + events |
| Next action | Ler [action-framework.md](../docs/developer/action-framework.md) — Action vs Plugin. Depois: `cmd/scheduler` + trace Allocate |
| Tools | go ✅ kubectl ✅ kind ✅ helm ✅ · cluster `kai` up |
| Resume | Open [PROGRESS.md](./PROGRESS.md) then [CHECKLIST.md](./CHECKLIST.md) |

---

## MapReduce → KAI bridge

| MIT 6.5840 Lab 1 | KAI Scheduler |
|------------------|---------------|
| Coordinator | Scheduler cycle (periodic loop) |
| Worker | Node + GPU |
| Map/Reduce task | Pod / PodGroup |
| Intermediate files | Cache + Snapshot (cluster state) |
| "wait for all maps" | Batch / gang scheduling (all or nothing) |

Related: HCP `ai-scheduler` runs agents; KAI **places** workloads on the cluster.

---

## 4-week plan (~5–8h/week)

### Week 0 — Mental map (~1h)

1. Read [scheduler-concepts.md](../docs/developer/scheduler-concepts.md) (~25 min)
2. Read deep-dive through Queues (~20 min)
3. Fill [NOTES.md](./NOTES.md)

### Week 1 — Run (~3–4h)

1. `brew install kind helm`
2. `kind create cluster --name kai`
3. Helm install KAI (upstream README)
4. [Quick start](../docs/quickstart/) — CPU pod
5. `kubectl get events`

### Week 2 — Core code (~4–6h)

1. [`cmd/scheduler/`](../cmd/scheduler/)
2. [action-framework.md](../docs/developer/action-framework.md)
3. Trace Allocate in [`pkg/scheduler/`](../pkg/scheduler/)
4. Run one test package

### Week 3 — Surrounding (~4h, pick 2)

1. Binder
2. Queues + fairness
3. PodGrouper

### Week 4 — Contribute (~3–5h)

1. Sign [CLA](../CLA.md)
2. `good first issue` / `help wanted`
3. Prefer docs → test → small bug
4. Branch from `upstream/main` (do **not** include `study/` in contribution PRs)

---

## Gaps strategy

| Gap | Approach |
|-----|----------|
| Networks / low-level | Only when it appears (informers, watch). No abstract TCP. |
| Advanced Go | Learn via plugin interfaces |
| Distributed systems | Snapshot consistency + reclaim/preempt |

---

## Cursor Cloud

Open **this fork**. You get docs + `.go` + `study/`. Update NOTES/PROGRESS/CHECKLIST as you go.
