# Progress log

Newest on top.

## 2026-08-09 — Week 1 DONE (PC local)

- kind + helm instalados (`brew`)
- `kind create cluster --name kai` (Colima como Docker runtime)
- Helm: `kai-scheduler` v0.17.0 → namespace `kai-scheduler` deployed
- Quickstart: `cpu-only-pod` → `Running` no nó `kai-control-plane`
- Events: Scheduled → Bound → Started (KAI agendou)
- Conceitos ops fixados: kubectl vs API, namespace, CRD, queues KAI (`scheduling.run.ai`)
- Control plane local: `https://127.0.0.1:58534`
- **Próximo:** Week 2 — ler [action-framework.md](../docs/developer/action-framework.md) (celular) → Action vs Plugin
- Tools: go ✅ kubectl ✅ kind ✅ helm ✅ · cluster `kai` ainda up

## 2026-08-09 — resume no PC local

- **Week 0 mental map DONE** (sem preencher NOTES — escolha explícita)
- Lido + discutido:
  - `docs/developer/scheduler-concepts.md`
  - `docs/scheduling-deep-dive/README.md` (inteiro; FAQs de preemption/reclaim)
  - `docs/fairness/README.md` (reclaim)
  - `docs/batch/README.md` (núcleo: separado / gang / min-member; JobSet externo = depois)
  - `docs/gpu-sharing/README.md`
- Conceitos que clicaram: preempt = intra-queue · reclaim = inter-queue · non-preemptible só in-quota · gang vs min-member
- **Próximo:** Week 1 no laptop — kind + helm + pod CPU do quickstart
- Tools: go ✅ kubectl ✅ kind ❌ helm ❌
- Sessão Cloud encerrada; retomar no PC local a partir deste arquivo + [README.md](./README.md) Status

## 2026-08-07

- Forked `kai-scheduler/KAI-Scheduler` → `MatheusOliveiraSilva/KAI-Scheduler`
- Local remotes: `origin` = fork, `upstream` = official
- Moved study notes into `study/` so Cloud AI sees docs + Go together
- **Week 0 in progress:** read scheduling cycle, fill NOTES.md
- Tools: go ✅ kubectl ✅ kind ❌ helm ❌
