# 📋 Especificação de Requisitos de Software (SRS)

---

## 1. Introdução

### 1.1 Objetivo
Este documento apresenta a Especificação de Requisitos de Software (SRS) para o **Sistema de Apoio à Internacionalização** da Universidade de Fortaleza (Unifor). O propósito é detalhar os requisitos funcionais, não funcionais e as regras de negócio que orientarão o desenvolvimento da solução web e mobile.

### 1.2 Escopo do Sistema
O sistema contempla módulos integrados para estudantes, gestores do Núcleo de Estratégias Internacionais (NEI) e coordenadores, cobrindo todo o ciclo de mobilidade acadêmica: desde a busca de instituições parceiras, verificação de elegibilidade, submissão de candidaturas, preparação linguística/financeira até o acompanhamento pós-intercâmbio.

---

## 2. Requisitos Funcionais (RF)

Os requisitos funcionais descrevem as ações e comportamentos que o sistema deve executar para atender aos utilizadores:

* **RF01 - Consulta de Oportunidades:** O sistema deve fornecer um portal unificado de busca com filtros avançados por país, instituição parceira, área de conhecimento e duração do intercâmbio.
* **RF02 - Validação de Elegibilidade:** O sistema deve verificar automaticamente se o estudante atende aos critérios acadêmicos exigidos (matrícula ativa, 30% a 70% do curso concluído, média global superior ou igual a 7,0 e ausência de reprovações).
* **RF03 - Gestão de Candidaturas:** O estudante deve conseguir submeter a sua candidatura a um edital ativo, anexando a documentação exigida (como comprovativo de idioma e carta de motivação).
* **RF04 - Painel de Gestão do NEI:** A equipe do NEI deve dispor de um painel administrativo para cadastrar e atualizar convênios internacionais, publicar editais e gerir o fluxo de análise das candidaturas.
* **RF05 - Central de Preparação:** O sistema deve disponibilizar recursos de apoio para capacitação linguística (materiais e dicas), orientações culturais e ferramentas de planeamento financeiro (estimativa de custos e bolsas).
* **RF06 - Módulo Pós-Intercâmbio:** O sistema deve permitir que os alunos publiquem relatos de experiência, participem de redes de mentoria para futuros candidatos e acompanhem o registo de aproveitamento de créditos.
* **RF07 - Sistema Tandem:** O sistema deve oferecer um espaço colaborativo para a troca de idiomas e integração entre estudantes locais e intercambistas estrangeiros.

---

## 3. Requisitos Não Funcionais (RNF)

Os requisitos não funcionais definem as restrições de qualidade, desempenho e segurança do sistema:

* **RNF01 - Segurança e Privacidade (LGPD):** O sistema deve garantir a proteção de dados pessoais e acadêmicos dos usuários, em total conformidade com a Lei Geral de Proteção de Dados.
* **RNF02 - Usabilidade e Responsabilidade:** A interface deve ser altamente responsiva, adaptando-se perfeitamente a dispositivos móveis (smartphones e tablets) e computadores.
* **RNF03 - Disponibilidade:** O portal deve manter uma disponibilidade contínua de 99% para consulta de editais e envio de documentos durante os períodos de seleção.
* **RNF04 - Desempenho:** As buscas por oportunidades e o carregamento das páginas principais não devem exceder o tempo de resposta de 3 segundos sob condições normais de acesso.

---

## 4. Regras de Negócio (RN)

As regras de negócio estabelecem as políticas institucionais que o sistema deve obrigatoriamente aplicar:

* **RN01 - Critérios de Elegibilidade Acadêmica:** Apenas estudantes de graduação que possuam entre 30% e 70% da carga horária total do curso concluída, média global igual ou superior a 7,0 e histórico acadêmico sem reprovações no semestre anterior podem concluir submissões para editais de mobilidade internacional.
* **RN02 - Vigência de Editais:** Nenhuma candidatura pode ser aceite fora do prazo de encerramento estipulado no cronograma oficial publicado pela equipe do NEI.
* **RN03 - Aprovação de Vagas:** A seleção final dos candidatos para as instituições parceiras no exterior é de competência exclusiva dos gestores do NEI, com base na pontuação obtida e no limite de vagas do convênio vigente.
