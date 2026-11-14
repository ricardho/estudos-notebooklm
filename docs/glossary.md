# 🔤 Glossário PT ↔ EN · Glossary EN ↔ PT — CTFL v4.0.1

🇧🇷 A prova pode ser feita em português, mas o syllabus, os simulados oficiais e a maior parte do material estão em inglês. Esta tabela reúne os termos mais cobrados nas duas línguas.

🇺🇸 The exam is available in Portuguese, but the syllabus, the official sample exams and most study material are in English. This table brings together the most frequently tested terms in both languages.

> 🇧🇷 Termos de acordo com a terminologia usual da tradução brasileira (BSTQB). Em caso de dúvida, consulte o glossário oficial em [glossary.istqb.org](https://glossary.istqb.org/) (permite escolher o idioma Português).
>
> 🇺🇸 Portuguese terms follow the usual Brazilian (BSTQB) terminology. When in doubt, check the official glossary at [glossary.istqb.org](https://glossary.istqb.org/), where you can choose Portuguese as the language.

---

## Fundamentos · Fundamentals

| English | Português | Nota · Note |
|---|---|---|
| error (mistake) | erro (engano) | ação humana · human action |
| defect (fault, bug) | defeito | imperfeição no produto de trabalho · imperfection in a work product |
| failure | falha | comportamento incorreto observado · observed incorrect behavior |
| root cause | causa raiz | |
| debugging | depuração | não é uma atividade de teste · not a testing activity |
| quality assurance (QA) | garantia da qualidade | processo, preventiva · process, preventive |
| quality control (QC) | controle de qualidade | produto, corretivo · product, corrective |
| test object | objeto de teste | |
| test item | item de teste | |
| test basis | base de teste | |
| test condition | condição de teste | "o que" testar · "what" to test |
| test case | caso de teste | |
| test oracle | oráculo de teste | fonte do resultado esperado · source of the expected result |
| testware | testware | |
| traceability | rastreabilidade | |
| whole team approach | abordagem de equipe completa | |
| independence of testing | independência do teste | |

## Processo de teste · Test process

| English | Português |
|---|---|
| test planning | planejamento do teste |
| test monitoring and control | monitoramento e controle do teste |
| test analysis | análise do teste |
| test design | modelagem do teste |
| test implementation | implementação do teste |
| test execution | execução do teste |
| test completion | conclusão do teste |
| entry criteria / exit criteria | critérios de entrada / critérios de saída |
| test plan | plano de teste |
| test progress report / test completion report | relatório de progresso do teste / relatório de conclusão do teste |

## Ciclo de vida · Lifecycle

| English | Português |
|---|---|
| software development lifecycle (SDLC) | ciclo de vida de desenvolvimento de software |
| test level | nível de teste |
| test type | tipo de teste |
| component testing (unit testing) | teste de componente (teste de unidade) |
| component integration testing | teste de integração de componentes |
| system testing | teste de sistema |
| system integration testing | teste de integração de sistemas |
| acceptance testing | teste de aceite |
| functional / non-functional testing | teste funcional / não funcional |
| confirmation testing | teste de confirmação |
| regression testing | teste de regressão |
| maintenance testing | teste de manutenção |
| shift left | shift left |

## Teste estático · Static testing

| English | Português |
|---|---|
| static testing / dynamic testing | teste estático / teste dinâmico |
| static analysis | análise estática |
| review | revisão |
| informal review | revisão informal |
| walkthrough | walkthrough (acompanhamento) |
| technical review | revisão técnica |
| inspection | inspeção |
| anomaly | anomalia |
| moderator (facilitator) | moderador (facilitador) |
| scribe (recorder) | redator (registrador) |
| review leader | líder da revisão |

## Técnicas de teste · Test techniques

| English | Português |
|---|---|
| black-box / white-box / experience-based test technique | técnica de teste caixa-preta / caixa-branca / baseada na experiência |
| equivalence partitioning (EP) | particionamento de equivalência |
| valid / invalid partition | partição válida / inválida |
| boundary value analysis (BVA) | análise de valor limite |
| decision table testing | teste de tabela de decisão |
| state transition testing | teste de transição de estados |
| statement testing / statement coverage | teste de instrução / cobertura de instrução |
| branch testing / branch coverage | teste de ramo / cobertura de ramo |
| coverage item | item de cobertura |
| defect masking | mascaramento de defeitos |
| error guessing | suposição de erro |
| exploratory testing | teste exploratório |
| checklist-based testing | teste baseado em lista de verificação (checklist) |
| acceptance criteria | critérios de aceite |
| acceptance test-driven development (ATDD) | desenvolvimento orientado por teste de aceite (ATDD) |

## Gerenciamento · Management

| English | Português |
|---|---|
| risk / risk level | risco / nível de risco |
| risk likelihood / risk impact | probabilidade do risco / impacto do risco |
| product risk / project risk | risco de produto / risco de projeto |
| risk-based testing | teste baseado em risco |
| test pyramid | pirâmide de teste |
| testing quadrants | quadrantes de teste |
| configuration management | gerenciamento de configuração |
| defect report | relatório de defeito |
| severity / priority | severidade / prioridade |

---

## ⚠️ Pares que mais confundem · Most confused pairs

| | 🇧🇷 | 🇺🇸 |
|---|---|---|
| **erro × defeito × falha** | O erro é humano, o defeito está no artefato, a falha é o que se observa ao executar. | The error is human, the defect is in the artifact, the failure is what you observe when it runs. |
| **verificação × validação** | Verificação: construímos o produto corretamente? Validação: construímos o produto certo? | Verification: are we building the product right? Validation: are we building the right product? |
| **teste × depuração** | O teste encontra a falha ou o defeito; a depuração encontra a causa e corrige. | Testing finds the failure or defect; debugging finds the cause and fixes it. |
| **confirmação × regressão** | Confirmação: o defeito foi corrigido? Regressão: a mudança quebrou outra coisa? | Confirmation: was the defect fixed? Regression: did the change break something else? |
| **nível × tipo de teste** | Nível: *onde* testar (componente, sistema…). Tipo: *o quê* avaliar (funcional, não funcional…). | Level: *where* to test (component, system…). Type: *what* to evaluate (functional, non-functional…). |
| **severidade × prioridade** | Severidade: o tamanho do impacto. Prioridade: a urgência da correção. | Severity: how big the impact is. Priority: how urgent the fix is. |
| **walkthrough × revisão técnica × inspeção** | Walkthrough é conduzido pelo autor; revisão técnica, pelo moderador; inspeção é a mais formal. | A walkthrough is led by the author; a technical review by a moderator; an inspection is the most formal. |

---

📚 [Guia por capítulo](chapter-guide.pt-BR.md) · [Chapter guide](chapter-guide.md) · [Exercícios K3](k3-exercises.pt-BR.md) · [K3 exercises](k3-exercises.md)
