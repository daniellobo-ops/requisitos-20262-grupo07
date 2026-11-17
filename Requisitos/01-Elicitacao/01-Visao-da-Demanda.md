# Visão da Demanda — Gestão de Oportunidades Internacionais

> **Proposta 3 | Grupo 7 | Versão 0.1 | 17/11/2026 | Rascunho acadêmico.**
> Os resultados das entrevistas deste projeto são **simulados para fins didáticos**, não evidências de pesquisa com a Unifor. O conteúdo é proposta de solução, não sistema existente ou aprovado.

## Identificação e histórico
| Campo | Informação |
| --- | --- |
| Demanda | Gestão de Oportunidades Internacionais |
| Tipo | Novo sistema (projeto acadêmico) |
| Área relacionada | Internacionalização da Unifor — setor gestor a confirmar |
| Elaboração | Grupo 7 — Requisitos e Modelagem de Sistemas |
| Validação | Professor/representantes institucionais, **não realizada** |
| Estado | Rascunho |
| Histórico | 17/11/2026 · v0.1 · primeira elaboração restrita à Proposta 3 |

## 1. Objetivo
Tornar mais acessível e organizado o acompanhamento de editais, bolsas e oportunidades de mobilidade internacional, oferecendo informações claras e um meio de manifestar interesse em oportunidades.

## 2. Contexto, problema e descrição sumária
**Questão oficial:** “Como tornar mais acessível e organizado o acompanhamento de editais, bolsas e oportunidades de mobilidade?”

**Situação atual:** a forma real de divulgação, atualização de informações e registro de interesse ainda não foi investigada junto à instituição. Dificuldades mencionadas em entrevistas simuladas são **hipóteses**.

**Descrição proposta:** aplicação web responsiva que permita a responsáveis cadastrar e divulgar oportunidades, com requisitos, prazos, documentos e bolsas, enquanto estudantes consultam essas informações e registram manifestações de interesse. Esta manifestação **não equivale a candidatura formal nem a concessão de bolsa**.

## 3. Proposta de valor e sucesso
| Benefício esperado | Indicador/evidência proposta | Meta | Como avaliar |
| --- | --- | --- | --- |
| Localizar oportunidades | Usuário encontra edital por filtros | A definir | Testes futuros de usabilidade |
| Compreender requisitos e prazos | Usuário identifica documentos e datas no detalhe do edital | A definir | Revisão com usuários |
| Acompanhar interesse | Usuário consulta situação de uma manifestação | A definir | Teste de cenário |
Todas as métricas e metas dependem de validação, não são resultados medidos.

## 4. Partes interessadas
| Interessado | Interesse | Responsabilidade esperada | Representante |
| --- | --- | --- | --- |
| Estudantes | Encontrar oportunidades e registrar interesse | Participar da elicitação/avaliação | Não identificado |
| Responsável institucional por editais | Manter informações confiáveis | Explicar e validar fluxos e regras | A identificar |
| TI institucional (se houver integração) | Segurança e viabilidade | Esclarecer acesso e integrações | A identificar |
| Grupo 7 | Elaborar documentos e modelos | Revisão de consistência | Integrantes do grupo |
| Professor | Avaliação acadêmica | Orientar entrega | Professor da disciplina |

## 5. Usuários e atores externos
| ID | Perfil | Objetivo | Contexto |
| --- | --- | --- | --- |
| AT01 | Estudante interessado | Consultar editais e manifestações | Acesso por navegador, inclusive celular (proposto) |
| AT02 | Gestor de oportunidades | Cadastrar, atualizar e publicar oportunidades; acompanhar interesses | Área administrativa (proposta) |
| AT03 | Sistema institucional externo | Possível autenticação ou validação | **Não confirmado**; não pressuposto no escopo |

## 6. Escopo e entregas previstas
### 6.1 Incluído
- Cadastro, edição e divulgação de editais e oportunidades de bolsas.
- Consulta de oportunidades com requisitos, prazos e documentos necessários.
- Registro de manifestação de interesse em uma oportunidade.
- Acompanhamento da situação dessa manifestação.
- Gestão de informações e manifestações pelo papel gestor.

### 6.2 Fora do escopo
- Rede social de intercambistas, mentoria, relatos, Tandem e conteúdo cultural da Proposta 1 ou Portal amplo da Proposta 4.
- Inscrição formal com upload e validação de documentos, análise de notas, seleção/classificação definitiva, concessão de bolsas ou emissão de vistos.
- Integrações institucionais ou cálculo automático de elegibilidade, enquanto não confirmados.

### 6.3 Evoluções futuras
Candidatura formal, notificações, autenticação institucional e elegibilidade automática poderão ser consideradas após levantamento.

### 6.4 Entregas
| Marco | Entrega | Prazo |
| --- | --- | --- |
| E1 | Requisitos, elicitação, backlog e três diagramas UML | A confirmar |
| E2 | Prototipação | A confirmar |
| E3 | Pitch | A confirmar |

## 7. Necessidades e catálogo de funcionalidades
| Necessidade | Problema/resultado | Origem | Atores |
| --- | --- | --- | --- |
| NEC01 | Descobrir editais/bolsas e informações de participação | Proposta 3 | AT01 |
| NEC02 | Manter oportunidades confiáveis e publicadas | Proposta 3 | AT02 |
| NEC03 | Manifestar interesse e ver situação registrada | Proposta 3; cenário simulado | AT01, AT02 |

| Funcionalidade | Resultado | Necessidade | Atores | Prioridade proposta | Valor | Frequência | Especificação |
| --- | --- | --- | --- | --- | --- | --- | --- |
| F01 | Cadastrar e publicar oportunidade | NEC02 | AT02 | Essencial | Alto (hipótese) | A definir | [RF01](../02-Requisitos/01-Requisitos-Funcionais.md), [UC01](../03-UML/01-Casos-de-Uso.md) |
| F02 | Consultar editais, bolsas, requisitos e prazos | NEC01 | AT01 | Essencial | Alto (hipótese) | A definir | RF02, UC02 |
| F03 | Manifestar interesse | NEC03 | AT01 | Essencial | A definir | A definir | RF03, UC03 |
| F04 | Consultar manifestações próprias | NEC03 | AT01 | Importante | A definir | A definir | RF04, UC04 |
| F05 | Atualizar situação de manifestações | NEC03 | AT02 | Importante | A definir | A definir | RF05, UC05 |
| F06 | Editar, encerrar e arquivar oportunidade | NEC02 | AT02 | Importante | A definir | A definir | RF06, UC01 |

Prioridade, valor e frequência são preliminares e devem ser revisados com participantes reais ou com o professor.

## 8. Visão geral da solução e impactos
**Responsabilidades:** manutenção do catálogo de oportunidades; consulta; registro/consulta de manifestações de interesse. **Sistema externo:** a definir, sem integração obrigatória confirmada. **Processos impactados:** divulgação e acompanhamento de oportunidades, ambos ainda a validar. Diagramas propostos: [Casos de uso](../03-UML/01-Casos-de-Uso.md), [Componentes](../03-UML/02-Componentes.md) e [Implantação](../03-UML/03-Implantacao.md).

## 9. Condições gerais
| Tipo | Condição | Situação |
| --- | --- | --- |
| Premissa | Existe um responsável institucional pela publicação | A confirmar |
| Dependência | Documentos e critérios variam por oportunidade | A investigar |
| Restrição proposta | Acesso por perfil e proteção de dados de interesse | A detalhar conforme LGPD |
| Dependência | Fluxo real de manifestações e eventual integração | A confirmar |

## 10. Riscos e questões abertas
| ID | Questão | Impacto | Próxima ação | Responsável | Estado |
| --- | --- | --- | --- | --- | --- |
| Q01 | Quem atualiza os editais? | Governança de dados | Confirmar papel | Instituição | Aberta |
| Q02 | Quais critérios/documentos são obrigatórios? | Consistência | Examinar editais reais | Instituição | Aberta |
| Q03 | O que configura uma manifestação de interesse? | RF03–RF05 | Validar fluxo | Instituição/estudantes | Aberta |
| Q04 | Há autenticação/integração institucional? | Segurança e arquitetura | Consultar TI | TI | Aberta |
| Q05 | Qual a política de dados e retenção? | Privacidade | Analisar com responsáveis | Instituição | Aberta |

## 11. Documentos relacionados
[Stakeholders](02-Stakeholders.md) · [Entrevistas simuladas](03-Entrevistas-Simuladas.md) · [Requisitos funcionais](../02-Requisitos/01-Requisitos-Funcionais.md) · [RNF](../02-Requisitos/02-Requisitos-Nao-Funcionais.md) · [Regras de negócio](../02-Requisitos/03-Regras-de-Negocio.md) · [Backlog](../../GestaoConfiguracao/01-Backlog-Priorizado.md)

## 12. Validação da Visão
- [x] Problema, objetivo, envolvidos e escopo propostos documentados.
- [x] Necessidades e funcionalidades identificadas.
- [x] Hipóteses e pendências registradas.
- [ ] Evidências reais de elicitação obtidas.
- [ ] Escopo validado com interessados e professor.
- [ ] Critérios de qualidade e prioridades aprovados.

**Condição:** rascunho utilizável para modelagem inicial acadêmica; **não validado institucionalmente**.
