# 🌍 Sistema de Apoio à Internacionalização — Unifor

Repositório do **Grupo 7** da disciplina **Requisitos e Modelagem de Sistemas** (Semestre 2026.2), Universidade de Fortaleza (Unifor). Projeto de Extensão em Internacionalização, desenvolvido em parceria com o Núcleo de Estratégias Internacionais (NEI).

## 👥 Integrantes

| Nome | Matrícula |
| :--- | :--- |
| Daniel Willian Moura Lobo | 2612716 |
| Arthur Cavalcante Melo Teixeira | 2612652 |
| Andre Eisler Comar | 2612709 |

---

## 🎯 Sobre o projeto

Especificação de um sistema web/mobile para a **gestão da mobilidade acadêmica internacional**, alinhado às diretrizes do NEI da Unifor. A solução busca centralizar o acesso às instituições parceiras (mais de 140 instituições em 30 países, segundo a apresentação do projeto), dar transparência ao processo seletivo e reduzir o atendimento manual da equipe do NEI.

**Problema investigado:** como tornar mais acessível e organizado o acompanhamento de editais, bolsas e oportunidades de mobilidade, e como melhorar a experiência de estudantes na busca por informações de internacionalização.

**Proposta de origem:** este projeto parte das propostas *3 (Gestão de Oportunidades Internacionais)* e *4 (Portal de Internacionalização)* do material de apoio da disciplina, com elementos da proposta *1 (Conecta Intercâmbio)* no módulo colaborativo. A justificativa está em [`09-Premissas-Decisoes-e-Fontes.md`](Requisitos/09-Premissas-Decisoes-e-Fontes.md).

### Produto mínimo (MVP)

Autenticação por perfil, consulta de oportunidades, autoavaliação de elegibilidade, submissão e acompanhamento de candidaturas, gestão de convênios e editais e triagem de candidaturas pelo NEI (RF01 a RF08).

### Fora do escopo desta especificação

Integração com agências de viagem e hospedagem, gestão da produção científica docente e funcionalidades do ENADE (propostas 2, 5 e 6 do material de apoio).

---

## 📦 Entregáveis (`/Requisitos`)

| # | Documento | Conteúdo | Status |
| :-: | :--- | :--- | :--- |
| 01 | [Documento de Visão](Requisitos/01-Documento-de-Visao.md) | Problema, objetivos, escopo (MVP e fora de escopo), usuários e restrições | ✅ Rascunho completo |
| 02 | [Stakeholders e Entrevistas](Requisitos/02-Stakeholders-e-Entrevistas.md) | Mapa de stakeholders, roteiros, hipóteses e registro de entrevistas | 🟡 Falta registrar entrevistas reais |
| 03 | [Especificação SRS](Requisitos/03-Especificacao-SRS.md) | RF, RNF e RN com prioridade, origem e critérios de aceitação | ✅ Rascunho completo |
| 04 | [Modelagem UML](Requisitos/04-Modelagem-UML.md) | Casos de uso, classes, sequência, atividades, estados, componentes e implantação | ✅ Rascunho completo |
| 05 | [Backlog Priorizado](Requisitos/05-Backlog-Priorizado.md) | Histórias de usuário (MoSCoW) com critérios de aceitação | ✅ Rascunho completo |
| 06 | [Protótipos e Wireframes](Requisitos/06-Prototipos-e-Wireframes.md) | Mapa de navegação e wireframes das telas principais | 🟡 Falta protótipo navegável (Figma) |
| 07 | [Glossário](Requisitos/07-Glossario.md) | Termos e siglas do domínio | ✅ |
| 08 | [Matriz de Rastreabilidade](Requisitos/08-Rastreabilidade.md) | RF ↔ US ↔ UC ↔ RN ↔ Tela | ✅ |
| 09 | [Premissas, Decisões e Fontes](Requisitos/09-Premissas-Decisoes-e-Fontes.md) | Premissas, restrições, decisões de escopo, fontes e pendências a confirmar | 🟡 Pendências abertas |

---

## ✅ Cobertura dos critérios de avaliação

| Critério | Peso | Onde está | Situação |
| :--- | :-: | :--- | :--- |
| Especificação (completude e clareza) | 30% | 03, 05, 07, 08 | ✅ Coberto; revisar após validação com o NEI |
| Modelagem UML (adequação à realidade da Unifor) | 25% | 04 | ✅ Coberto; validar regras com o NEI |
| Elicitação (entrevistas e questionários) | 20% | 02 | 🟡 Roteiros prontos; registrar as entrevistas e respostas reais |
| Protótipos (qualidade e usabilidade) | 15% | 06 | 🟡 Wireframes textuais; falta versão no Figma |
| Apresentação (defesa e comunicação) | 10% | — | ⬜ A preparar (pitch para a banca com o NEI) |

---

## 🧩 Convenções do repositório

* **Idioma:** português do Brasil em todos os documentos.
* **Identificadores:** `RF` requisito funcional, `RNF` não funcional, `RN` regra de negócio, `US` história de usuário, `UC` caso de uso, `TBC` pendência a confirmar. Os identificadores não mudam de número depois de criados.
* **Hipótese x confirmado:** toda informação ainda não validada com o NEI ou com os alunos é marcada como **hipótese** ou **TBC**.
* **Diagramas:** escritos em [Mermaid](https://mermaid.js.org/) e renderizados diretamente no GitHub.
* **Numeração dos arquivos:** `NN-Nome-do-Documento.md`.

## 📚 Fontes

* Apresentação *Projeto de Extensão: Internacionalização* (Requisitos e Modelagem de Sistemas, Unifor).
* *Propostas de Projetos de Sistemas: Internacionalização e ENADE*, material didático Unifor 2026.2.

A lista completa, com as fontes ainda a consultar, está em [`09-Premissas-Decisoes-e-Fontes.md`](Requisitos/09-Premissas-Decisoes-e-Fontes.md).
