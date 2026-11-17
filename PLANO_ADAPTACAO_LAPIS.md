# Plano de adaptação ao modelo LAPIS

Referência: https://github.com/marcelobezerra-dotcom/Lapis-unifor

## Objetivo
Adequar a organização dos artefatos do Sistema de Apoio à Internacionalização — Unifor aos guias de engenharia de requisitos do professor, preservando os documentos originais e seu histórico.

## Correspondência dos artefatos atuais
| Documento existente | Destino proposto no modelo LAPIS | Ação |
|---|---|---|
| 01-Documento-de-Visao.md | Requisitos/Artefatos/Visao/ | Adequar ao template de visão da demanda |
| 02-Stakeholders-e-Entrevistas.md | Requisitos/Elicitacao/ | Separar roteiro de entrevistas e resultados efetivamente coletados |
| 03-Especificacao-SRS.md | Requisitos/Especificacao/ | Preservar SRS e revisar critérios de aceite |
| 04-Modelagem-UML.md | Requisitos/Especificacao-de-Casos-de-Uso/ | Detalhar casos de uso e manter diagramas UML |
| 05-Backlog-Priorizado.md | GestaoConfiguracao/ | Vincular itens às Issues |
| 06-Prototipos-e-Wireframes.md | Requisitos/Prototipos/ | Identificar protótipos pendentes |
| 07-Glossario.md | Requisitos/Artefatos/Glossario/ | Revisar segundo template |
| 08-Rastreabilidade.md | Requisitos/Validacao/ | Ligar requisitos a casos de uso, critérios e evidências |
| 09-Premissas-e-Fontes.md | Requisitos/Artefatos/ | Revisar premissas pendentes |

## Etapas
1. Conferir templates do LAPIS e identificar lacunas sem inventar entrevistas, aprovações ou evidências.
2. Criar pastas e versões adaptadas dos documentos, preservando os originais até revisão do grupo.
3. Criar Issues vinculadas a entregáveis reais e marcos acordados; não inventar Sprints passadas.
4. Configurar GitHub Project/Kanban e Sprints de acordo com o calendário real do grupo.
5. Validar links, conteúdo e rastreabilidade; integrar por Pull Request após revisão.

## Regras de segurança e versionamento
- Não apagar documentos antigos antes da aprovação da migração.
- Não executar scripts externos nem solicitar tokens no chat.
- Não registrar entrevistas, testes ou validações como realizados sem evidências.
- Não renomear o repositório sem confirmar o padrão exato exigido pelo professor.
- Usar commits descritivos, por exemplo: `docs(requisitos): adapta visão ao template LAPIS`.
