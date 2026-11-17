# 📋 Especificação de Requisitos de Software (SRS)

Estrutura inspirada no padrão IEEE 830, conforme indicado na metodologia da disciplina.

| Versão | Data | Alterações |
| :-: | :-: | :--- |
| 0.1 | — | Primeira versão (RF01–RF07, RNF01–RNF04, RN01–RN03) |
| 0.2 | 2026-11-03 | Requisitos reorganizados por prioridade, com origem, critérios de aceitação e rastreabilidade; novos RF, RNF e RN; correções |

---

## 1. Introdução

### 1.1 Propósito
Detalhar os requisitos funcionais, não funcionais e as regras de negócio do **Sistema de Apoio à Internacionalização** da Unifor, que orientarão o desenvolvimento da solução web e mobile.

### 1.2 Escopo
O sistema cobre o ciclo de mobilidade acadêmica: busca de instituições parceiras, verificação de elegibilidade, candidatura, triagem pelo NEI, preparação do candidato e acompanhamento pós-intercâmbio. O recorte do MVP está em [`01-Documento-de-Visao.md`](01-Documento-de-Visao.md#6-escopo-do-produto).

### 1.3 Definições, siglas e abreviações
Ver [`07-Glossario.md`](07-Glossario.md).

### 1.4 Referências
Ver [`09-Premissas-Decisoes-e-Fontes.md`](09-Premissas-Decisoes-e-Fontes.md).

### 1.5 Visão geral do documento
A seção 2 descreve o contexto do produto; a seção 3 traz os requisitos específicos; a rastreabilidade completa está em [`08-Rastreabilidade.md`](08-Rastreabilidade.md).

---

## 2. Descrição geral

### 2.1 Perspectiva do produto
Sistema web/mobile responsivo, independente, que depende de uma fonte de dados acadêmicos da Unifor (**TBC-02**) e de autenticação institucional (**TBC-02**).

### 2.2 Perfis de usuário
Estudante de graduação, Gestor do NEI e Coordenador de curso. O Aluno estrangeiro (incoming) participa apenas do Tandem (RF15).

### 2.3 Restrições
LGPD; acesso por navegadores e dispositivos móveis; escopo compatível com o cronograma da disciplina.

### 2.4 Premissas e dependências
Ver [`09-Premissas-Decisoes-e-Fontes.md`](09-Premissas-Decisoes-e-Fontes.md). As principais são a origem dos dados acadêmicos e a definição dos documentos exigidos por edital.

---

## 3. Requisitos específicos

### 3.1 Interfaces externas

| ID | Interface | Descrição | Status |
| :-: | :--- | :--- | :-: |
| IE01 | Sistema acadêmico da Unifor | Fornece matrícula, percentual concluído, média global e reprovações do estudante | TBC-02 |
| IE02 | Autenticação institucional | Login com credenciais da Unifor | TBC-02 |
| IE03 | Serviço de e-mail | Envio de notificações de status | Hipótese |

### 3.2 Requisitos funcionais (RF)

Prioridade pelo método MoSCoW: **M** Must · **S** Should · **C** Could · **W** Won't (por enquanto).

#### 3.2.1 Must Have (MVP)

| ID | Requisito | Prior. | Origem | Critérios de aceitação |
| :-: | :--- | :-: | :--- | :--- |
| **RF01** | **Autenticação e perfis de acesso.** O sistema deve autenticar usuários com credenciais institucionais e restringir as funcionalidades por perfil (Estudante, Gestor do NEI, Coordenador de curso). | M | US15 | Usuário sem perfil de Gestor não acessa o painel do NEI; sessão expira por inatividade; acessos negados são registrados. |
| **RF02** | **Consulta de oportunidades.** O sistema deve oferecer busca unificada de convênios e editais com filtros por país, instituição parceira, área de conhecimento, idioma e duração, e exibir os detalhes de cada oportunidade. | M | US01 | A combinação de filtros retorna apenas resultados que satisfazem todos; sem resultados, exibe mensagem orientativa; resposta em até 3 s (RNF04). |
| **RF03** | **Validação de elegibilidade.** O sistema deve verificar automaticamente se o estudante atende à RN01 e informar o resultado (apto ou não apto) com o motivo de cada critério não atendido. | M | US02 | Cada critério é exibido com o valor do estudante e o valor exigido; o mesmo estudante recebe o mesmo resultado enquanto os dados não mudarem; a data da avaliação é registrada. |
| **RF04** | **Submissão de candidatura.** O estudante elegível deve poder se candidatar a um edital ativo, preenchendo o formulário e anexando em PDF os documentos exigidos pelo edital (por exemplo, comprovante de idioma e carta de motivação). | M | US03 | Envio bloqueado se inelegível (RN01), fora do prazo (RN02) ou com documento obrigatório ausente (RN04); o envio gera número de protocolo. |
| **RF05** | **Acompanhamento de candidaturas.** O estudante deve visualizar suas candidaturas com o status atual e o histórico de mudanças. | M | US12 | O status exibido corresponde ao último estado registrado pelo NEI; o histórico mostra data e estado de cada mudança. |
| **RF06** | **Gestão de convênios.** O Gestor do NEI deve cadastrar, editar e inativar convênios com instituições parceiras (país, áreas, idiomas, vagas e vigência). | M | US04 | Convênio inativado deixa de aparecer em novas buscas, mas o histórico de candidaturas é preservado. |
| **RF07** | **Gestão de editais.** O Gestor do NEI deve criar, editar, publicar e encerrar editais com título, convênio, prazos, requisitos, documentos exigidos, vagas e cronograma. | M | US04 | Edital só é visível ao estudante após a publicação; encerra automaticamente no prazo (RN02). |
| **RF08** | **Triagem e decisão de candidaturas.** O Gestor do NEI deve listar candidaturas por edital, consultar documentos e o resultado da validação automática, e deferir, indeferir ou solicitar complementação. | M | US05 | Indeferimento exige justificativa; a decisão registra autor e data (RNF06); a seleção final respeita o limite de vagas (RN03). |

#### 3.2.2 Should Have

| ID | Requisito | Prior. | Origem | Critérios de aceitação |
| :-: | :--- | :-: | :--- | :--- |
| **RF09** | **Notificações de status.** O sistema deve notificar o estudante, por e-mail e na plataforma, a cada mudança de status da candidatura. | S | US08 | Cada mudança de status gera uma notificação com data e novo status. |
| **RF10** | **Central de preparação.** O sistema deve disponibilizar conteúdos de preparação linguística e cultural e ferramentas de planejamento financeiro (estimativa de custos e bolsas disponíveis). | S | US06 | O estudante acessa o conteúdo do país do edital escolhido; o NEI consegue atualizar os conteúdos (**TBC-05**). |
| **RF11** | **Gestão de bolsas e vagas.** O Gestor do NEI deve registrar bolsas e vagas por edital ou convênio e atribuí-las a candidatos selecionados. | S | US13 | A soma das atribuições não ultrapassa as vagas do convênio. |
| **RF12** | **Aproveitamento de créditos.** O Coordenador de curso deve visualizar o plano de estudos dos alunos selecionados e pré-validar disciplinas equivalentes; o aluno acompanha o registro. | S | US07 | A equivalência só é concluída com parecer do coordenador (RN05). |
| **RF13** | **Relatórios e indicadores.** O sistema deve gerar relatórios sobre perfil dos candidatos, destinos mais procurados e candidaturas por edital e status. | S | US14 | Relatórios usam dados agregados, sem expor dados pessoais desnecessários (RNF01). |

#### 3.2.3 Could Have

| ID | Requisito | Prior. | Origem | Critérios de aceitação |
| :-: | :--- | :-: | :--- | :--- |
| **RF14** | **Relatos de experiência.** Ex-intercambistas podem publicar relatos sobre a instituição parceira; a publicação passa por moderação do NEI. | C | US09, US16 | Relato só fica público após aprovação (RN07); o NEI pode despublicar. |
| **RF15** | **Sistema Tandem.** O sistema deve permitir que estudantes da Unifor e alunos estrangeiros informem idiomas que oferecem e desejam praticar e entrem em contato por meio da plataforma. | C | US10 | O contato é intermediado pela plataforma, sem expor dados pessoais antes do aceite (RNF01). |

#### 3.2.4 Won't Have (por enquanto)

| ID | Requisito | Prior. | Origem |
| :-: | :--- | :-: | :--- |
| **RF16** | Fórum de dúvidas e agenda de eventos (workshops e palestras). | W | US17 |
| **RF17** | Integração com agências de viagem e reserva de acomodação. | W | US11 |

### 3.3 Requisitos não funcionais (RNF)

Valores marcados como *proposto* devem ser validados com o NEI e a TI.

| ID | Categoria | Requisito | Prior. |
| :-: | :--- | :--- | :-: |
| **RNF01** | Segurança e privacidade (LGPD) | Proteger dados pessoais e acadêmicos: tráfego por HTTPS, acesso a documentos apenas pelo titular e pelo Gestor do NEI, coleta limitada ao necessário e registro da base legal e do consentimento quando aplicável. | M |
| **RNF02** | Responsividade | A interface deve funcionar em smartphones (a partir de 360 px de largura), tablets e computadores, nas duas últimas versões dos principais navegadores. | M |
| **RNF03** | Disponibilidade | Disponibilidade de 99% durante os períodos de seleção, para consulta de editais e envio de documentos (*proposto*). | M |
| **RNF04** | Desempenho | Buscas e páginas principais em até 3 segundos sob carga normal (*proposto*; definir "carga normal" com a TI). | M |
| **RNF05** | Acessibilidade | Conformidade com WCAG 2.1 nível AA (*proposto*). | S |
| **RNF06** | Auditabilidade | Registrar quem, quando e o quê em decisões sobre candidaturas e em alterações de editais e convênios. | M |
| **RNF07** | Usabilidade | Um estudante deve conseguir ir da busca à candidatura sem treinamento; validar com testes de usabilidade com usuários (*proposto*). | S |
| **RNF08** | Confiabilidade | Cópia de segurança periódica dos dados e dos documentos anexados (*proposto*: diária). | S |
| **RNF09** | Idioma | Interface em português do Brasil; versão em inglês como evolução. | C |

### 3.4 Regras de negócio (RN)

A coluna **Situação** indica se a regra vem de documento institucional ou ainda é hipótese.

| ID | Regra | Situação |
| :-: | :--- | :--- |
| **RN01** | **Elegibilidade acadêmica.** Só podem concluir candidatura estudantes de graduação com matrícula ativa, entre 30% e 70% da carga horária do curso concluída, média global igual ou superior a 7,0 e sem reprovações. | Fonte: apresentação do projeto. **TBC-01**: reprovações em todo o histórico ou apenas no semestre anterior (a versão anterior desta SRS citava "semestre anterior"). |
| **RN02** | **Vigência de editais.** Nenhuma candidatura pode ser aceita fora do prazo definido no cronograma oficial publicado pelo NEI. | Hipótese consistente com o processo seletivo. |
| **RN03** | **Seleção final.** A seleção dos candidatos é competência exclusiva dos gestores do NEI, com base na pontuação obtida e no limite de vagas do convênio vigente. | Hipótese. **TBC-04**: critérios de pontuação. |
| **RN04** | **Documentação obrigatória.** A candidatura só pode ser enviada com todos os documentos exigidos pelo edital, em PDF. | Hipótese. **TBC-03**: lista de documentos. |
| **RN05** | **Equivalência de disciplinas.** O aproveitamento de créditos só é concluído após parecer do coordenador do curso do estudante. | Hipótese. |
| **RN06** | **Candidatura única.** Cada estudante pode ter apenas uma candidatura ativa por edital. | Hipótese. |
| **RN07** | **Moderação de relatos.** Relatos de experiência só são publicados após aprovação do NEI. | Hipótese. **TBC-07**. |
| **RN08** | **Proteção de dados.** O tratamento de dados pessoais deve seguir a LGPD: finalidade definida, coleta mínima e acesso por perfil. | Restrição legal. |

---

## 4. Rastreabilidade
A matriz completa RF ↔ US ↔ UC ↔ RN ↔ Tela está em [`08-Rastreabilidade.md`](08-Rastreabilidade.md).
