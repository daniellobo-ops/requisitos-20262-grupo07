# 🌍 Gestão de Oportunidades Internacionais — Unifor

Repositório do **Grupo 7** da disciplina **Requisitos e Modelagem de Sistemas** (Semestre 2026.2), Universidade de Fortaleza (Unifor). Projeto acadêmico voltado à internacionalização e à organização de oportunidades de mobilidade estudantil.

## 👥 Integrantes

| Nome | Matrícula |
| :--- | :--- |
| Daniel Willian Moura Lobo | 2612716 |
| Arthur Cavalcante Melo Teixeira | 2612652 |
| Andre Eisler Comar | 2612709 |

---

## 🎯 Sobre o projeto

Especificação de um sistema web responsivo para a **gestão de oportunidades internacionais**, desenvolvido com base na **Proposta 3 — Gestão de Oportunidades Internacionais** do material da disciplina. A solução proposta busca tornar mais acessível e organizado o acompanhamento de **editais, bolsas e oportunidades de mobilidade**, incluindo informações sobre requisitos, prazos e documentação necessária.

**Problema investigado:** como tornar mais acessível e organizado o acompanhamento de editais, bolsas e oportunidades de mobilidade?

**Proposta de origem:** O projeto tem como base a **Proposta 3 — Gestão de Oportunidades Internacionais**, apresentada no material da disciplina de Requisitos e Modelagem de Sistemas da Unifor. A solução busca facilitar a divulgação, a consulta e o acompanhamento de editais, bolsas e oportunidades de mobilidade acadêmica internacional.

### Produto mínimo (MVP)

Cadastro, edição e divulgação de oportunidades por um responsável autorizado; consulta e filtragem de editais e bolsas; visualização de requisitos, prazos e documentos; registro de **manifestação de interesse** pelo estudante e acompanhamento da situação desse registro (RF01 a RF07).

A manifestação de interesse **não substitui inscrição formal**, seleção ou concessão de bolsa. O protótipo adotará fluxos propostos de identificação por perfil, cadastro de oportunidades e acompanhamento de interesse; seus detalhes permanecem decisões acadêmicas, não regras institucionais confirmadas.

### Fora do escopo desta especificação

Processos de inscrição e avaliação formal de candidaturas, classificação e seleção de estudantes, concessão de bolsas, verificação automática de elegibilidade e integrações com sistemas institucionais que ainda não tenham sido confirmadas. A prototipação e o pitch são entregas posteriores à documentação da primeira etapa.

---

## 📦 Entregáveis

### 1ª entrega — Elicitação, definição de requisitos e modelagem UML inicial

| # | Documento | Conteúdo | Status |
| :-: | :--- | :--- | :--- |
| 01 | [Documento de Visão](01-Elicitacao/01-Visao-da-Demanda.md) | Problema, objetivos, escopo, usuários, necessidades e pendências | ✅ Rascunho elaborado |
| 02 | [Identificação de Stakeholders](01-Elicitacao/02-Stakeholders.md) | Interessados, papéis, influência e plano de levantamento | ✅ Rascunho elaborado |
| 03 | [Roteiro e resultados de entrevistas](01-Elicitacao/03-Entrevistas-Simuladas.md) | Perguntas e respostas **simuladas**, sem entrevistas reais | ✅ Entrevistas simuladas realizadas no exercício acadêmico |
| 04 | [Requisitos Funcionais](02-Requisitos/01-Requisitos-Funcionais.md) | RF01–RF07, prioridades e critérios de aceitação | ✅ Rascunho elaborado |
| 05 | [Requisitos Não Funcionais](02-Requisitos/02-Requisitos-Nao-Funcionais.md) | Qualidade, segurança, desempenho, acessibilidade e verificações propostas | ✅ Rascunho elaborado |
| 06 | [Regras de Negócio](02-Requisitos/03-Regras-de-Negocio.md) | RN01–RN09 e vínculos com os requisitos | ✅ Rascunho elaborado |
| 07 | [Backlog Priorizado](GestaoConfiguracao/01-Backlog-Priorizado.md) | Histórias de usuário e priorização MoSCoW proposta | ✅ Rascunho elaborado |
| 08 | [UML — Casos de Uso](03-UML/01-Casos-de-Uso.md) | Atores, funcionalidades e fluxos iniciais | 🟡 Fonte PlantUML pronta; revisar/exportar |
| 09 | [UML — Componentes](03-UML/02-Componentes.md) | Componentes lógicos e dependências propostas | 🟡 Fonte PlantUML pronta; revisar/exportar |
| 10 | [UML — Implantação](03-UML/03-Implantacao.md) | Nós e ambiente de implantação hipotético | 🟡 Fonte PlantUML pronta; revisar/exportar |

### Entregas seguintes

- **2ª entrega — Prototipação:** elaboração das telas e do fluxo de navegação com base nos requisitos revisados.
- **3ª entrega — Pitch:** apresentação do problema, da proposta de solução e dos benefícios esperados.

---

## ✅ Cobertura dos critérios de avaliação

Os **pesos abaixo foram mantidos como referência do README antigo**; precisam ser conferidos com as orientações atuais do professor. A primeira entrega foi definida pelos dez artefatos obrigatórios listados acima.

| Critério | Peso (referência anterior) | Onde está | Situação |
| :--- | :-: | :--- | :--- |
| Especificação (completude e clareza) | 30% | 01, 04–07 | 🟡 Rascunhos prontos; revisão e validação pendentes |
| Modelagem UML | 25% | 08–10 | 🟡 Diagramas descritos em Mermaid/PlantUML; revisão e exportação pendentes |
| Elicitação (entrevistas e questionários) | 20% | 02–03 | ✅ Entrevistas simuladas realizadas, não pesquisa de campo |
| Protótipos (qualidade e usabilidade) | 15% | 2ª entrega | ⬜ Ainda não iniciada |
| Apresentação (defesa e comunicação) | 10% | 3ª entrega | ⬜ Ainda não iniciada |

---

## 🧩 Convenções do repositório

* **Idioma:** português do Brasil em todos os documentos.
* **Identificadores:** `RF` requisito funcional, `RNF` requisito não funcional, `RN` regra de negócio, `US` história de usuário, `UC` caso de uso, `NEC` necessidade e `AT` ator.
* **Hipótese x confirmado:** informações não verificadas são identificadas como **hipóteses**, **propostas** ou **pendências**. As entrevistas são **inteiramente simuladas** e não representam validação pela Unifor.
* **Diagramas:** prévias em [Mermaid](https://mermaid.js.org/) para visualização no GitHub e fontes em PlantUML para exportação em notação UML.
* **Numeração dos arquivos:** `NN-Nome-do-Documento.md`, organizados por área na raiz do repositório.
* **Organização do trabalho:** [Issues da primeira entrega](https://github.com/daniellobo-ops/requisitos-20262-grupo07/issues) registram a revisão dos artefatos.

## 📚 Fontes

* Material didático da disciplina *Requisitos e Modelagem de Sistemas*, Unifor 2026.2: **Proposta 3 — Gestão de Oportunidades Internacionais**.
* [LAPIS — Engenharia de Requisitos (repositório de referência do professor)](https://github.com/marcelobezerra-dotcom/Lapis-unifor).
* [Templates de requisitos do LAPIS](https://github.com/marcelobezerra-dotcom/Lapis-unifor/tree/main/Requisitos/Artefatos/Templates).

**Nota:** os roteiros e resultados de entrevistas deste repositório são construções fictícias para o exercício acadêmico. A modalidade simulada foi informada pelo grupo como definida para esta entrega; isso não transforma as respostas em dados obtidos de participantes reais.
