# 🧾 Premissas, Decisões de Escopo, Fontes e Pendências

Registro exigido pelo material de apoio da disciplina: premissas, restrições, fontes consultadas, decisões de escopo e distinção entre hipóteses e informações confirmadas.

---

## 1. Fontes

| ID | Fonte | Uso no projeto |
| :-: | :--- | :--- |
| F1 | Apresentação *Projeto de Extensão: Internacionalização* (Requisitos e Modelagem de Sistemas, Unifor) | Objetivos, módulos, entregáveis, metodologia, critérios de elegibilidade, cronograma e avaliação |
| F2 | *Propostas de Projetos de Sistemas: Internacionalização e ENADE* (material didático Unifor 2026.2) | Propostas de origem, questões para levantamento, orientações às equipes |
| F3 | Site da Unifor e documentos públicos do NEI | **A consultar**: editais anteriores, lista de convênios, regulamentos |
| F4 | Entrevistas com o NEI, coordenadores, TI e questionário com estudantes | **A realizar**: ver [`02-Stakeholders-e-Entrevistas.md`](02-Stakeholders-e-Entrevistas.md) |

---

## 2. Decisões de escopo

| ID | Decisão | Justificativa |
| :-: | :--- | :--- |
| D01 | Adotar como base as propostas 3 e 4 do material de apoio, com elementos da proposta 1 no módulo colaborativo | Tratam da mesma jornada do estudante: encontrar oportunidade, candidatar-se e preparar-se |
| D02 | MVP = RF01 a RF08 | Cobre o ciclo mínimo de valor (buscar, verificar elegibilidade, candidatar-se e ser analisado) dentro das 15 semanas |
| D03 | Fora do escopo: produção científica docente e ENADE (propostas 2, 5 e 6) | Outros eixos e públicos |
| D04 | RF16 e RF17 ficam como Won't Have | Dependem de integrações externas e de definição institucional |
| D05 | A arquitetura e as tecnologias dos diagramas de componentes e implantação são sugestões | A SRS especifica o quê, não o como |

> **Confirmar D01 com o professor da disciplina**, já que o material pede que cada equipe selecione uma das propostas e justifique.

---

## 3. Premissas

| ID | Premissa |
| :-: | :--- |
| P01 | O NEI aceita receber candidaturas e documentos de forma digital (PDF). |
| P02 | Existe forma de obter os dados acadêmicos do estudante (integração, importação ou comprovação). |
| P03 | Os critérios de elegibilidade informados na apresentação do projeto refletem o documento institucional vigente. |
| P04 | Os números "mais de 140 instituições em 30 países" estão atualizados. |

## 4. Restrições

| ID | Restrição |
| :-: | :--- |
| R01 | Conformidade com a LGPD no tratamento de dados acadêmicos e pessoais. |
| R02 | Integrações com plataformas institucionais dependem de autorização e acesso. |
| R03 | Cronograma de 15 semanas, com entrega final e apresentação à banca com o NEI. |
| R04 | Grupos de 3 a 5 alunos; ferramentas gratuitas de modelagem e prototipação. |

---

## 5. Pendências a confirmar (TBC)

| ID | Pendência | Impacta | Com quem confirmar | Status |
| :-: | :--- | :-: | :--- | :-: |
| TBC-01 | A regra "sem reprovações" vale para todo o histórico ou só para o semestre anterior? | RN01, RF03 | NEI | Aberta |
| TBC-02 | De onde vêm os dados acadêmicos e como o sistema os acessa (integração, importação ou autodeclaração com comprovação)? Existe login institucional? | RF01, RF03, IE01, IE02 | TI, Secretaria | Aberta |
| TBC-03 | Quais documentos são exigidos em cada edital? | RN04, RF04 | NEI | Aberta |
| TBC-04 | Quais são os critérios de pontuação do processo seletivo? | RN03, RF08 | NEI | Aberta |
| TBC-05 | Quem atualiza convênios, editais e conteúdos de orientação? | RF06, RF07, RF10 | NEI | Aberta |
| TBC-06 | Qual a relação entre NEI e DRI nos serviços de internacionalização? (o material de apoio cita a DRI) | Escopo, stakeholders | NEI, professor | Aberta |
| TBC-07 | Quem modera os relatos e as informações de hospedagem, e qual a responsabilidade institucional? | RF14, RN07 | NEI | Aberta |
| TBC-08 | Qual a base legal, o tempo de retenção e quem é o controlador dos dados? | RNF01, RN08 | NEI, encarregado de dados | Aberta |
| TBC-09 | Os números de convênios e países estão atualizados? | Visão | NEI | Aberta |
| TBC-10 | Os valores de disponibilidade (99%) e desempenho (3 s) são adequados? | RNF03, RNF04 | TI | Aberta |

---

## 6. Hipóteses x confirmado

Hipóteses do grupo: [`02-Stakeholders-e-Entrevistas.md`](02-Stakeholders-e-Entrevistas.md#5-hipóteses-iniciais-a-validar). Regras de negócio com situação individual: [`03-Especificacao-SRS.md`](03-Especificacao-SRS.md#34-regras-de-negócio-rn).
