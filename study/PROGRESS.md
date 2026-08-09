# Progress log

Newest on top.

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
