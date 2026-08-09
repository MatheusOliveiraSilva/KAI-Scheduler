# Vocabulary notes

Skipped full Week 0 fill (2026-08-09). Filling as terms show up.

## The 5 cycle terms

1. **Cache** —
2. **Snapshot** —
3. **Session** —
4. **Action** — (Week 2 — action-framework.md)
5. **Plugin** — (Week 2 — action-framework.md)

## Extra terms (when they show up)

- **PodGroup** — CRD `podgroups.scheduling.run.ai`
- **Queue** — CRD contrato de quota; default-parent-queue → default-queue
- **BindRequest** — CRD; scheduler pede bind, binder executa
- **Reclaim** — inter-queue; only over-quota preemptible victims
- **Preempt** — same queue only; victim must be running + lower priority + preemptible
- **CRD** — Custom Resource Definition; tipo novo na API K8s
- **kube-apiserver** — HTTP API do cluster; kubectl sempre bate aqui
- **kind** — K8s local em container Docker; context `kind-kai` → `https://127.0.0.1:<port>`

## MapReduce analogies that clicked

- Coordinator ≈ scheduling cycle
- "wait for all maps" ≈ gang / PodGroup

## Questions for next session

- Action vs Plugin (após ler action-framework.md)
