# Requisitos Funcionais — Gestão de Oportunidades Internacionais

> **Proposta 3 | v0.1 | 17/11/2026 | Rascunho não validado.** RF derivam do enunciado oficial e de cenários de entrevistas **simuladas**. Não representam necessidades comprovadas de usuários reais.

## 1. Escopo
Cadastro e divulgação de editais/oportunidades de mobilidade e bolsas, consulta de requisitos, prazos e documentação, registro e acompanhamento de **manifestações de interesse**. Não se realiza inscrição formal, seleção, avaliação acadêmica ou concessão de bolsas.

## 2. Catálogo de requisitos
| ID | Requisito | Prioridade (proposta) | Origem | Critério de aceitação proposto |
| --- | --- | --- | --- | --- |
| RF01 | O gestor autorizado deve criar e publicar oportunidades informando título, descrição, tipo (edital/bolsa), destino quando aplicável, prazo, requisitos e documentos exigidos. | Must | Proposta 3 / H07–H09 (simulação) | Oportunidade incompleta não é publicada; oportunidade publicada aparece na consulta. |
| RF02 | O estudante deve pesquisar oportunidades publicadas e consultar seus detalhes, com filtros por país/destino, área e tipo quando esses dados existirem. | Must | Proposta 3 / H01–H03 (simulação) | Filtros retornam oportunidades compatíveis; detalhe exibe prazo, requisitos e documentos; lista vazia mostra aviso. |
| RF03 | O estudante autenticado deve registrar uma manifestação de interesse em oportunidade publicada e com prazo aberto. | Must | Proposta 3 / H04 (simulação) | Registro vincula estudante e oportunidade e apresenta confirmação explicitando que não é inscrição formal. |
| RF04 | O estudante autenticado deve consultar suas próprias manifestações e a situação de cada uma. | Should | Proposta 3 / H05 (simulação) | Usuário vê apenas seus registros e respectivos estados. |
| RF05 | O gestor autorizado deve consultar manifestações de interesse e atualizar sua situação com registro de responsável e data. | Should | Proposta 3 / H10 (simulação) | Atualização altera o estado e preserva histórico mínimo, sem decidir seleção ou concessão de bolsa. |
| RF06 | O gestor autorizado deve editar, encerrar ou arquivar oportunidades, mantendo o registro de manifestações existentes. | Should | Proposta 3 / H07–H09 (simulação) | Oportunidade encerrada não recebe novo interesse; registros anteriores permanecem disponíveis a usuários autorizados. |

**Nota de escopo:** autenticação é pré-condição dos fluxos com dados pessoais. Forma de login institucional/conta local **a definir**, sem presumir integração institucional.

## 3. Regras de qualidade e negócio
[RNF](02-Requisitos-Nao-Funcionais.md) · [RN](03-Regras-de-Negocio.md) · [Visão](../01-Elicitacao/01-Visao-da-Demanda.md).

## 4. Rastreabilidade
| RF | Necessidade | Caso de uso | Hipótese |
| --- | --- | --- | --- |
| RF01 | NEC02 | UC01 | H07–H09 |
| RF02 | NEC01 | UC02 | H01–H03 |
| RF03 | NEC03 | UC03 | H04 |
| RF04 | NEC03 | UC04 | H05 |
| RF05 | NEC03 | UC05 | H10 |
| RF06 | NEC02 | UC01 | H07–H09 |

## 5. Pendências
- [ ] Confirmar se manifestação de interesse é registrada pelo sistema e sua relação com inscrições formais.
- [ ] Confirmar os papéis e permissões institucionais.
- [ ] Confirmar campos obrigatórios, categorias e regras de prazo.
- [ ] Revisar requisitos com professor e/ou responsáveis reais.
