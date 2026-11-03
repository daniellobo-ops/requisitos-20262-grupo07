# 📌 Backlog Priorizado (MoSCoW)

## 1. Introdução
Backlog do produto do **Sistema de Apoio à Internacionalização** da Unifor. As histórias de usuário (US) seguem o formato clássico e são priorizadas pelo método **MoSCoW**:

* **Must Have:** essencial para a operação mínima (MVP).
* **Should Have:** importante, mas não bloqueia o lançamento inicial.
* **Could Have:** desejável, de menor impacto.
* **Won't Have (por enquanto):** fica para ciclos futuros.

Formato: **Como** [perfil], **eu quero** [ação], **para que** [benefício].

## 2. Visão geral

| US | Título | Prioridade | RF | UC |
| :-: | :--- | :-: | :-: | :-: |
| US01 | Consulta de editais e convênios | Must | RF02 | UC01 |
| US02 | Autoavaliação automatizada de elegibilidade | Must | RF03 | UC02 |
| US03 | Submissão de candidatura | Must | RF04 | UC03 |
| US04 | Cadastro e gestão de convênios e editais (NEI) | Must | RF06, RF07 | UC06, UC07 |
| US05 | Triagem e avaliação de inscrições | Must | RF08 | UC08 |
| US12 | Acompanhamento das minhas candidaturas | Must | RF05 | UC04 |
| US15 | Autenticação e perfis de acesso | Must | RF01 | todos |
| US06 | Central de preparação linguística e cultural | Should | RF10 | UC05 |
| US07 | Painel do coordenador de curso | Should | RF12 | UC11 |
| US08 | Notificações de status | Should | RF09 | UC12 |
| US13 | Gestão de bolsas e vagas | Should | RF11 | UC09 |
| US14 | Relatórios e indicadores do NEI | Should | RF13 | UC10 |
| US09 | Relatos de experiência (pós-intercâmbio) | Could | RF14 | UC13 |
| US10 | Módulo Tandem | Could | RF15 | UC15 |
| US16 | Moderação de relatos | Could | RF14 | UC14 |
| US11 | Integração com agências de viagem e acomodação | Won't | RF17 | — |
| US17 | Fórum de dúvidas e agenda de eventos | Won't | RF16 | — |

## 3. Histórias de usuário

### 3.1 Must Have (MVP)

**US01: Consulta de editais e convênios**
* **Como** estudante de graduação, **eu quero** buscar oportunidades filtrando por país, instituição, área, idioma e duração, **para que** eu encontre rapidamente as alinhadas ao meu curso.
* **Critérios de aceitação:**
  * Dado que escolhi país e área, quando busco, então vejo apenas oportunidades que atendem aos dois filtros.
  * Dado que nenhum resultado atende aos filtros, então vejo uma mensagem com sugestão de ampliar a busca.

**US02: Autoavaliação automatizada de elegibilidade**
* **Como** estudante de graduação, **eu quero** que o sistema valide meus dados acadêmicos (média ≥ 7,0, 30% a 70% do curso concluído, sem reprovações), **para que** eu saiba de imediato se posso me candidatar sem ir ao NEI.
* **Critérios de aceitação:**
  * Dado que não atendo a um critério, quando faço a autoavaliação, então vejo qual critério falhou, meu valor e o valor exigido.
  * Dado que atendo a todos, então vejo o resultado "Apto" e acesso os editais abertos.

**US03: Submissão de candidatura**
* **Como** estudante elegível, **eu quero** enviar minha candidatura a um edital ativo anexando os documentos em PDF, **para que** minha inscrição seja analisada formalmente.
* **Critérios de aceitação:**
  * Dado que falta um documento obrigatório, quando tento enviar, então o envio é bloqueado e a pendência é indicada.
  * Dado que o prazo do edital terminou, então não consigo enviar.
  * Dado que enviei, então recebo um número de protocolo.

**US04: Cadastro e gestão de convênios e editais (NEI)**
* **Como** gestor do NEI, **eu quero** cadastrar, editar e publicar convênios e editais com regras e prazos, **para que** as vagas fiquem disponíveis para consulta na plataforma.
* **Critérios de aceitação:**
  * Dado que um edital está em rascunho, então ele não aparece para estudantes.
  * Dado que publiquei o edital, então ele aparece na busca até o prazo final.

**US05: Triagem e avaliação de inscrições**
* **Como** gestor do NEI, **eu quero** ver a lista de candidatos por edital e deferir, indeferir ou pedir complementação, **para que** a seleção seja conduzida com eficiência e transparência.
* **Critérios de aceitação:**
  * Dado que indefiro uma candidatura, então preciso informar a justificativa.
  * Dado que decidi, então autor e data ficam registrados e o estudante vê o novo status.

**US12: Acompanhamento das minhas candidaturas**
* **Como** estudante candidato, **eu quero** ver o status e o histórico de cada candidatura, **para que** eu saiba em que etapa está o meu processo sem consultar o NEI.
* **Critérios de aceitação:**
  * Dado que o NEI mudou o status, então o novo status aparece na minha lista de candidaturas.

**US15: Autenticação e perfis de acesso** *(habilitador técnico)*
* **Como** usuário da plataforma, **eu quero** entrar com minhas credenciais institucionais e ver apenas o que meu perfil permite, **para que** meus dados e os do processo seletivo estejam protegidos.
* **Critérios de aceitação:**
  * Dado que sou estudante, então não acesso o painel do NEI.

### 3.2 Should Have

**US06: Central de preparação linguística e cultural.** **Como** estudante interessado em mobilidade, **eu quero** acessar orientações sobre idiomas, guias culturais e estimativas de custos de vida, **para que** eu me prepare adequadamente antes da viagem.

**US07: Painel do coordenador de curso.** **Como** coordenador de curso, **eu quero** ver os planos de estudo dos alunos selecionados e pré-validar disciplinas equivalentes, **para que** o aproveitamento de créditos seja ágil no retorno do estudante.

**US08: Notificações de status.** **Como** estudante candidato, **eu quero** receber notificações por e-mail e na plataforma a cada mudança de status, **para que** eu acompanhe a seleção em tempo real.

**US13: Gestão de bolsas e vagas.** **Como** gestor do NEI, **eu quero** registrar bolsas e vagas por edital e atribuí-las aos selecionados, **para que** o controle de vagas seja confiável.

**US14: Relatórios e indicadores do NEI.** **Como** gestor do NEI, **eu quero** relatórios sobre o perfil dos candidatos e os destinos mais procurados, **para que** eu apoie decisões sobre convênios e divulgação.

### 3.3 Could Have

**US09: Relatos de experiência (pós-intercâmbio).** **Como** ex-intercambista, **eu quero** publicar um relato sobre minha experiência e dar dicas sobre a universidade parceira, **para que** novos candidatos aprendam com a minha vivência.

**US10: Módulo Tandem.** **Como** estudante da Unifor ou aluno estrangeiro, **eu quero** me conectar com nativos do idioma que pratico, **para que** possamos fazer trocas linguísticas e culturais.

**US16: Moderação de relatos.** **Como** gestor do NEI, **eu quero** aprovar ou despublicar relatos, **para que** o conteúdo da plataforma seja confiável e adequado.

### 3.4 Won't Have (por enquanto)

**US11: Integração com agências de viagem e acomodação.** **Como** estudante aprovado, **eu quero** cotar passagens e reservar moradia estudantil pelo portal, **para que** o planejamento logístico fique centralizado.

**US17: Fórum de dúvidas e agenda de eventos.** **Como** estudante, **eu quero** tirar dúvidas em um fórum e ver workshops e palestras, **para que** eu me mantenha informado sobre internacionalização.

## 4. Distribuição do backlog

| Categoria | Quantidade de US | Percentual |
| :--- | :-: | :-: |
| Must Have | 7 | 41% |
| Should Have | 5 | 29% |
| Could Have | 3 | 18% |
| Won't Have | 2 | 12% |
| **Total** | **17** | **100%** |
