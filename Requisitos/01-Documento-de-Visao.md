# 📄 Documento de Visão: Sistema de Apoio à Internacionalização (Unifor)

| Versão | Data | Responsável | Alterações |
| :-: | :-: | :--- | :--- |
| 0.1 | — | Grupo 7 | Primeira versão |
| 0.2 | 2026-11-03 | Grupo 7 | Padronização em pt-BR, objetivos e indicadores, escopo (MVP e fora de escopo), premissas e restrições |

> **Status:** rascunho para validação com o NEI. Informações ainda não confirmadas estão marcadas como **hipótese** ou **TBC** (ver [`09-Premissas-Decisoes-e-Fontes.md`](09-Premissas-Decisoes-e-Fontes.md)).

---

## 1. Introdução

### 1.1 Objetivo
Este documento define a visão geral, os objetivos, o público-alvo, os problemas enfrentados e as funcionalidades do **Sistema de Apoio à Internacionalização** da Universidade de Fortaleza (Unifor). O sistema deve centralizar, facilitar e tornar transparente o processo de mobilidade acadêmica internacional de alunos de graduação e a gestão desse processo pelo Núcleo de Estratégias Internacionais (NEI).

### 1.2 Escopo
O sistema abrange a pesquisa de convênios com instituições parceiras, a autoavaliação de elegibilidade, a central de preparação dos candidatos (idiomas, cultura e planejamento financeiro), a gestão de candidaturas e bolsas pelo NEI e, em etapas posteriores, funcionalidades colaborativas e de pós-intercâmbio (relatos, mentoria, Tandem e aproveitamento de créditos). O recorte do que entra no produto mínimo está na seção 6.

### 1.3 Documentos relacionados
[`03-Especificacao-SRS.md`](03-Especificacao-SRS.md) · [`04-Modelagem-UML.md`](04-Modelagem-UML.md) · [`07-Glossario.md`](07-Glossario.md) · [`09-Premissas-Decisoes-e-Fontes.md`](09-Premissas-Decisoes-e-Fontes.md)

---

## 2. Contexto e justificativa da escolha do problema

A internacionalização é uma tendência crescente no meio acadêmico. Segundo a apresentação do projeto, a Unifor oferece acesso a mais de 140 instituições em 30 países (dado a atualizar com o NEI, **TBC-09**).

O material de apoio da disciplina descreve duas necessidades que motivam este projeto: tornar mais acessível e organizado o acompanhamento de editais, bolsas e oportunidades de mobilidade, e melhorar a experiência de estudantes na busca por informações e serviços de internacionalização. Por isso o grupo escolheu as propostas **3 (Gestão de Oportunidades Internacionais)** e **4 (Portal de Internacionalização)**, que tratam da mesma jornada do estudante, e incorporou ao módulo colaborativo elementos da proposta **1 (Conecta Intercâmbio)**, como relatos de experiência e troca entre estudantes.

---

## 3. Posição e oportunidade de negócio

### 3.1 Problema identificado (hipótese a validar nas entrevistas)
As informações sobre editais, requisitos e instituições parceiras estão dispersas. Isso gera incerteza nos estudantes quanto a elegibilidade, prazos e planejamento financeiro e aumenta o volume de atendimento manual da equipe do NEI.

### 3.2 Declaração da posição do produto

| Elemento | Descrição |
| :--- | :--- |
| **Para** | Estudantes de graduação da Unifor e a equipe do NEI |
| **Que** | Precisam de uma solução unificada para gerir a mobilidade acadêmica internacional |
| **O** | Portal de Apoio à Internacionalização |
| **É um** | Sistema web/mobile de gestão de oportunidades, candidaturas e preparação |
| **Que** | Centraliza editais, valida requisitos automaticamente e gerencia candidaturas |
| **Ao contrário de** | Processos manuais descentralizados por e-mail e atendimento presencial |
| **Nosso produto** | Oferece rastreabilidade de candidaturas, preparação integrada e relatórios para o NEI |

---

## 4. Objetivos e indicadores de sucesso

| Objetivo | Indicador proposto | Meta |
| :--- | :--- | :--- |
| Reduzir o atendimento manual de dúvidas no NEI | Nº de consultas sobre elegibilidade e prazos atendidas manualmente por edital | A definir com o NEI |
| Dar transparência ao processo | % de candidaturas com status visível ao estudante em tempo real | 100% das candidaturas |
| Agilizar a triagem | Tempo médio entre o envio e a primeira análise da candidatura | A definir com o NEI |
| Ampliar o acesso à informação | Nº de estudantes que usam a consulta de oportunidades por semestre | A definir com o NEI |

---

## 5. Descrição dos stakeholders e usuários

### 5.1 Perfis de usuários do sistema
* **Estudante de graduação:** consulta oportunidades, faz a autoavaliação, candidata-se a editais, envia documentos e acompanha o status.
* **Gestor do NEI:** cadastra convênios, publica editais, analisa candidaturas, gerencia bolsas e vagas e emite relatórios.
* **Coordenador de curso:** acompanha alunos em mobilidade e valida a equivalência de disciplinas e o aproveitamento de créditos.
* **Aluno estrangeiro (incoming):** usuário do módulo colaborativo (Tandem); suas necessidades de integração são investigadas, mas ele não participa do MVP.

O mapa completo de stakeholders está em [`02-Stakeholders-e-Entrevistas.md`](02-Stakeholders-e-Entrevistas.md).

### 5.2 Critérios de elegibilidade do estudante (fonte: apresentação do projeto; confirmar com o NEI)
Matrícula ativa, entre 30% e 70% do curso concluído, média global igual ou superior a 7,0 e ausência de reprovações (**TBC-01**: período considerado).

---

## 6. Escopo do produto

### 6.1 Produto mínimo (MVP)

| Módulo | Funcionalidades |
| :--- | :--- |
| Acesso | Autenticação e perfis de acesso (RF01) |
| Estudante | Portal de oportunidades com filtros por país, instituição, área, idioma e duração (RF02); autoavaliação de elegibilidade (RF03); submissão de candidatura com documentos (RF04); acompanhamento de candidaturas (RF05) |
| Gestão (NEI) | Gestão de convênios (RF06) e de editais (RF07); triagem e decisão sobre candidaturas (RF08) |

### 6.2 Etapa seguinte (Should Have)
Notificações de status (RF09), central de preparação (RF10), gestão de bolsas e vagas (RF11), aproveitamento de créditos pelo coordenador (RF12) e relatórios do NEI (RF13).

### 6.3 Módulo colaborativo e pós-intercâmbio (Could Have)
Relatos de experiência com moderação (RF14) e Tandem (RF15).

### 6.4 Fora do escopo desta especificação
Fórum de dúvidas e agenda de eventos (RF16), integração com agências de viagem e hospedagem (RF17), gestão da produção científica docente e funcionalidades do ENADE.

---

## 7. Restrições, premissas e dependências

### 7.1 Restrições
* **Segurança e LGPD:** tratamento de dados acadêmicos e pessoais em conformidade com a Lei Geral de Proteção de Dados.
* **Plataforma:** acesso responsivo por navegadores e dispositivos móveis.
* **Prazo:** o escopo cabe no cronograma de 15 semanas da disciplina, razão pela qual a especificação prioriza o MVP.

### 7.2 Premissas e dependências
* A origem dos dados acadêmicos usados na elegibilidade (média, percentual concluído, reprovações) ainda não está definida (**TBC-02**). O sistema depende de integração, importação ou comprovação documental.
* As integrações com plataformas institucionais e o uso de dados pessoais dependem de autorização e da observância da LGPD, conforme o material de apoio da disciplina.
* A lista completa de premissas está em [`09-Premissas-Decisoes-e-Fontes.md`](09-Premissas-Decisoes-e-Fontes.md).
