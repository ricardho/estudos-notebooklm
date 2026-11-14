# 📖 Guia por Capítulo — CTFL v4.0.1

[English](chapter-guide.md) | **Português**

Resumo do syllabus **ISTQB CTFL v4.0.1** organizado por capítulo, com o peso de cada um na prova e os pontos que mais caem.

> **Fontes:** *ISTQB Certified Tester Foundation Level Syllabus v4.0.1* (2024-09-15) e *ISTQB Exam Structures & Rules Tables v1.18* (2026-05-27), ambos em [istqb.org](https://istqb.org/). Este guia é um resumo de estudo e não substitui o syllabus oficial.

---

## 🎯 A prova

| Item | Valor |
|---|---|
| Questões | 40 (múltipla escolha, 1 ponto cada) |
| Aprovação | 26 acertos (65%) |
| Duração | 60 minutos (75 minutos para quem faz em idioma não nativo, +25%) |

### Peso de cada capítulo

| Capítulo | Questões | K1 | K2 | K3 |
|---|:---:|:---:|:---:|:---:|
| 1. Fundamentos de Teste | 8 | 2 | 6 | 0 |
| 2. Teste ao Longo do Ciclo de Vida de Desenvolvimento de Software | 6 | 2 | 4 | 0 |
| 3. Teste Estático | 4 | 2 | 2 | 0 |
| **4. Análise e Modelagem de Teste** | **11** | 0 | 6 | **5** |
| **5. Gerenciamento das Atividades de Teste** | **9** | 1 | 5 | **3** |
| 6. Ferramentas de Teste | 2 | 1 | 1 | 0 |
| **Total** | **40** | **8** | **24** | **8** |

**Níveis K (nível de conhecimento):**
- **K1 — Lembrar:** reconhecer um termo ou conceito.
- **K2 — Entender:** explicar, comparar, classificar, dar exemplos.
- **K3 — Aplicar:** usar uma técnica numa situação concreta (por exemplo, calcular valores limite).

💡 **Estratégia:** os capítulos 4 e 5 valem 20 das 40 questões, e todas as 8 questões K3 estão neles. Pratique as técnicas com os [exercícios K3](k3-exercises.pt-BR.md).

---

## 1. Fundamentos de Teste — 8 questões

**Seções:** 1.1 O que é teste? · 1.2 Por que o teste é necessário? · 1.3 Princípios de teste · 1.4 Atividades de teste, testware e papéis · 1.5 Habilidades essenciais e boas práticas

**Objetivos do teste** (exemplos): avaliar produtos de trabalho, provocar falhas e encontrar defeitos, garantir a cobertura necessária, reduzir o risco de qualidade inadequada, verificar requisitos, fornecer informação para decisões, gerar confiança e validar se o objeto de teste funciona como os stakeholders esperam.

**Teste × depuração:** teste provoca falhas (teste dinâmico) ou encontra defeitos diretamente (teste estático). **Depuração** encontra a causa da falha, analisa e corrige. Depois da correção vêm o **teste de confirmação** e o **teste de regressão**.

**Teste × QA:** teste é **controle de qualidade** — orientado ao produto, corretivo. **QA** (garantia da qualidade) é orientada ao **processo**, preventiva, e é responsabilidade de todos.

**Erro → defeito → falha:**
- **Erro (engano):** ação humana que produz um resultado incorreto.
- **Defeito (falha no artefato, bug):** imperfeição em um produto de trabalho. Pode estar no código, num requisito ou num script de teste.
- **Falha:** o sistema não faz o que deveria (ou faz o que não deveria) quando um defeito é executado. Falhas também podem vir de condições do ambiente, como radiação.
- **Causa raiz:** motivo fundamental do problema, identificado pela análise de causa raiz.

**Os 7 princípios:**
1. O teste mostra a presença, não a ausência de defeitos.
2. O teste exaustivo é impossível.
3. Testar cedo economiza tempo e dinheiro.
4. Defeitos se agrupam (princípio de Pareto).
5. Os testes se desgastam (o antigo "paradoxo do pesticida").
6. O teste depende do contexto.
7. Falácia da ausência de defeitos: software sem defeitos ainda pode não atender às necessidades do usuário.

**Atividades do processo de teste:** planejamento · monitoramento e controle · análise ("**o que** testar") · modelagem ("**como** testar") · implementação · execução · conclusão.

**Papéis:** **papel de gestão de teste** (planejamento, monitoramento, controle e conclusão) e **papel de teste** (análise, modelagem, implementação e execução).

**Abordagem de equipe completa (whole team):** qualquer pessoa da equipe com as habilidades necessárias pode fazer qualquer tarefa, e todos são responsáveis pela qualidade.

**Independência do teste:** ajuda a encontrar defeitos diferentes por causa de vieses diferentes, mas pode isolar o testador da equipe e fazer os desenvolvedores perderem o senso de responsabilidade pela qualidade.

---

## 2. Teste ao Longo do Ciclo de Vida — 6 questões

**Seções:** 2.1 Teste no contexto de um ciclo de vida de desenvolvimento · 2.2 Níveis e tipos de teste · 2.3 Teste de manutenção

**Abordagens test-first:**
- **TDD:** o teste vem antes do código.
- **ATDD:** os testes são derivados dos critérios de aceite.
- **BDD:** o comportamento é descrito em linguagem natural, normalmente no formato Dado/Quando/Então (Given/When/Then).

**DevOps:** CI/CD, feedback rápido, automação e testes de regressão automatizados. **Shift left:** testar mais cedo no ciclo, por exemplo revisando requisitos e escrevendo testes antes do código. **Retrospectivas:** servem para melhorar o processo continuamente.

**Os 5 níveis de teste:**

| Nível | Foco |
|---|---|
| Teste de componente (unidade) | Componente isolado, normalmente feito pelo desenvolvedor |
| Teste de integração de componentes | Interfaces e interações entre componentes |
| Teste de sistema | Comportamento do sistema inteiro, funcional e não funcional |
| Teste de integração de sistemas | Interfaces com outros sistemas e serviços externos |
| Teste de aceite | Validação e prontidão para implantação: UAT, operacional, contratual, regulatório, alfa e beta |

**Os 4 tipos de teste:** funcional ("o quê") · não funcional ("quão bem" — ISO/IEC 25010: eficiência de desempenho, compatibilidade, usabilidade, confiabilidade, segurança, manutenibilidade, portabilidade e *safety*) · caixa-preta (baseado em especificação) · caixa-branca (baseado em estrutura). Todos podem ser aplicados em qualquer nível.

**Confirmação × regressão:**
- **Teste de confirmação:** confirma que o defeito original foi corrigido.
- **Teste de regressão:** confirma que a mudança não causou efeitos colaterais. É um forte candidato à automação.

**Teste de manutenção:** é acionado por modificações, por mudanças no ambiente operacional (migração) e pela aposentadoria do sistema.

---

## 3. Teste Estático — 4 questões

**Seções:** 3.1 Fundamentos do teste estático · 3.2 Feedback e processo de revisão

**Teste estático × dinâmico:** o teste estático **não executa** o software. Ele encontra **defeitos diretamente**, inclusive em documentos, e pode encontrar coisas que o teste dinâmico não encontra, como código inalcançável ou problemas de manutenibilidade. O teste dinâmico provoca **falhas**.

**Processo de revisão:** planejamento → início da revisão → revisão individual → comunicação e análise → correção e relatório.

**Papéis na revisão:**
- **Gerente:** decide o que será revisado e fornece os recursos.
- **Autor:** cria e corrige o produto de trabalho.
- **Moderador (facilitador):** conduz as reuniões de revisão.
- **Redator (*scribe*):** registra as anomalias e as decisões.
- **Revisor:** faz a revisão.
- **Líder da revisão:** é o responsável geral pela revisão; decide quem participa, quando e onde.

**Tipos de revisão** (do menos para o mais formal):

| Tipo | Quem conduz | Ponto-chave |
|---|---|---|
| Revisão informal | — | Sem processo definido nem documentação formal; objetivo: detectar anomalias |
| Walkthrough | **Autor** | Muitos objetivos: educar, chegar a consenso, gerar ideias, detectar anomalias |
| Revisão técnica | **Moderador** | Revisores tecnicamente qualificados; consenso e decisões técnicas |
| Inspeção | — | **A mais formal**: segue o processo completo, coleta métricas, e o autor **não pode** ser líder nem redator |

---

## 4. Análise e Modelagem de Teste — 11 questões (5 K3)

**Seções:** 4.1 Visão geral · 4.2 Técnicas caixa-preta · 4.3 Técnicas caixa-branca · 4.4 Técnicas baseadas na experiência · 4.5 Abordagens baseadas em colaboração

| Categoria | Técnicas | Nível K |
|---|---|---|
| Caixa-preta | Particionamento de equivalência · Análise de valor limite (**2 valores e 3 valores**) · Tabela de decisão · Transição de estados | **K3** |
| Caixa-branca | Teste de instrução · Teste de ramo | K2 |
| Baseadas na experiência | Suposição de erro · Teste exploratório · Teste baseado em checklist | K2 |
| Colaboração | Escrita colaborativa de histórias de usuário · Critérios de aceite · **ATDD** | K2 / **K3** (ATDD) |

**Pontos que mais caem:**
- **Valor limite** só se aplica a partições **ordenadas**.
  - **2 valores:** o limite e o vizinho mais próximo na partição adjacente.
  - **3 valores:** o limite e os dois vizinhos.
- **Cobertura de ramo inclui cobertura de instrução** (*subsumes*): 100% de ramo garante 100% de instrução, mas o contrário não vale.
- **Transição de estados:** a cobertura de todas as transições, que tenta também as inválidas, é mais forte que a de transições válidas (0-switch), que por sua vez é mais forte que a de todos os estados.
- **Histórias de usuário:** os 3 C's (Cartão, Conversa, Confirmação) e o INVEST (Independente, Negociável, Valiosa, Estimável, Pequena, Testável).
- **Critérios de aceite:** podem ser **orientados a cenário** (Dado/Quando/Então) ou **orientados a regra** (lista de verificação ou tabela de entrada e saída).

➡️ Pratique com os [exercícios K3](k3-exercises.pt-BR.md).

---

## 5. Gerenciamento das Atividades de Teste — 9 questões (3 K3)

**Seções:** 5.1 Planejamento · 5.2 Gerenciamento de risco · 5.3 Monitoramento, controle e conclusão · 5.4 Gerenciamento de configuração · 5.5 Gerenciamento de defeitos

**Critérios de entrada × saída:**
- **Critérios de entrada:** pré-condições para começar uma atividade.
- **Critérios de saída:** o que precisa ser alcançado para declarar a atividade concluída.

No ágil, os critérios de saída equivalem à *Definition of Done*, e os de entrada, à *Definition of Ready*.

**Técnicas de estimativa (K3):**
- **Baseada em proporções:** usa dados de projetos anteriores, por exemplo a proporção entre esforço de desenvolvimento e de teste.
- **Extrapolação:** projeta o restante a partir de medições do projeto atual.
- **Wideband Delphi:** especialistas estimam isoladamente e repetem até chegar a consenso. O Planning Poker é uma variante.
- **Estimativa de três pontos:** **E = (a + 4m + b) / 6** e **DP = (b − a) / 6**.

**Priorização de casos de teste (K3):** baseada em **risco**, em **cobertura** (inclusive cobertura adicional) ou em **requisitos**. Sempre respeitando as **dependências**: se um caso de alta prioridade depende de um de baixa, o de baixa roda primeiro.

**Pirâmide de teste:** quanto mais alta a camada, menor a granularidade, menor o isolamento e maior o tempo de execução.

**Quadrantes de teste (Marick):**

| | Apoiam a equipe | Criticam o produto |
|---|---|---|
| **Voltados ao negócio** | **Q2**: testes funcionais, exemplos, testes de história de usuário, protótipos de UX, API, simulações | **Q3**: exploratório, usabilidade, UAT |
| **Voltados à tecnologia** | **Q1**: componente e integração de componentes (automatizados, no CI) | **Q4**: smoke tests e não funcionais (exceto usabilidade) |

**Risco:**
- **Nível de risco** = **probabilidade × impacto** na abordagem quantitativa, ou uma **matriz de risco** na abordagem qualitativa.
- **Risco de projeto** afeta o gerenciamento do projeto, como prazos, pessoas e fornecedores.
- **Risco de produto** afeta a qualidade do produto.

**Relatório de defeito (K3):** identificador, título, data/autor, objeto e ambiente de teste, contexto, descrição da falha com passos para reproduzir, resultado esperado × obtido, severidade, prioridade, status e referências.

---

## 6. Ferramentas de Teste — 2 questões

**Seções:** 6.1 Suporte de ferramentas ao teste · 6.2 Benefícios e riscos da automação de teste

- **Benefícios da automação:** economia de tempo em tarefas repetitivas, mais consistência, medições objetivas, acesso mais fácil à informação, feedback mais rápido e mais tempo para os testadores fazerem testes novos e mais profundos.
- **Riscos da automação:** expectativas irreais, estimativas erradas de tempo e custo, usar a ferramenta onde o teste manual seria mais adequado, depender demais da ferramenta, depender do fornecedor, uso de ferramentas open source abandonadas, incompatibilidade com a plataforma e escolha de uma ferramenta que não atende a requisitos regulatórios ou de *safety*.

---

📚 Veja também: [Exercícios K3](k3-exercises.pt-BR.md) · [Glossário PT ↔ EN](glossary.md) · [README](../README.pt-BR.md)
