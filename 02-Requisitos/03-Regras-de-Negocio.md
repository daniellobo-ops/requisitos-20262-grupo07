# Regras de Negócio — Gestão de Oportunidades Internacionais

> **v0.1 | Rascunho.** Regras propostas a partir do escopo e de entrevistas **simuladas**, salvo restrições legais gerais. Ainda não são políticas da Unifor confirmadas. Estrutura baseada no [template LAPIS](https://github.com/marcelobezerra-dotcom/Lapis-unifor/blob/main/Requisitos/Artefatos/Templates/template-rn-regra-negocio.md).

## 1. Catálogo de regras
### RN01 — Gestor autorizado publica oportunidades
- **Descrição:** apenas usuários no papel gestor podem publicar e alterar dados de editais e bolsas.
- **Condição:** operação de edição/publicação; validação de permissão.
- **Resultado:** acesso não autorizado bloqueado.
- **Origem:** hipótese H07; RF01/RF06. **A confirmar.**

### RN02 — Oportunidade publicada apresenta informações mínimas
- **Descrição:** publicação exige título, descrição, tipo, prazo, requisitos e documentos exigidos ou indicação explícita de que não se aplicam.
- **Condição:** tentativa de publicação.
- **Resultado:** publicação bloqueada com campos essenciais ausentes.
- **Origem:** Proposta 3, H08/H09. **Lista exata a confirmar.**

### RN03 — Prazo encerrado bloqueia novos registros de interesse
- **Descrição:** uma oportunidade encerrada ou com prazo de manifestação expirado não admite nova manifestação.
- **Condição:** tentativa de manifestar interesse.
- **Resultado:** solicitação recusada com motivo.
- **Origem:** hipótese operacional; RF03/RF06. **A confirmar.**

### RN04 — Manifestação de interesse não constitui candidatura formal
- **Descrição:** o registro de interesse não seleciona candidato, não reserva vaga e não substitui procedimentos oficiais de inscrição.
- **Condição:** confirmação da manifestação.
- **Resultado:** interface informa claramente essa distinção.
- **Origem:** delimitação do projeto e H04; RF03/RNF07. **A confirmar o fluxo real.**

### RN05 — Usuários consultam apenas manifestações autorizadas
- **Descrição:** estudante consulta suas próprias manifestações; gestor autorizado acessa as correspondentes à sua atividade.
- **Condição:** consulta ou alteração de registro.
- **Resultado:** sistema restringe registros por papel.
- **Origem:** privacidade e hipótese H12; RF04/RF05. **Permissões exatas a confirmar.**

### RN06 — Encerramento preserva o histórico de interesse
- **Descrição:** arquivar/encerrar oportunidade não exclui automaticamente registros existentes de manifestações; a retenção está sujeita à política institucional e à LGPD.
- **Condição:** encerramento ou arquivamento.
- **Resultado:** preservação controlada dos registros conforme política a definir.
- **Origem:** proposta de consistência de dados; RF06. **A confirmar.**

### RN07 — Evitar manifestação ativa duplicada
- **Descrição:** um estudante mantém apenas uma manifestação ativa por oportunidade; ao tentar uma segunda vez, vê o registro já existente.
- **Condição:** tentativa de novo registro para mesma oportunidade e estudante.
- **Resultado:** duplicidade bloqueada; possibilidade de nova manifestação após encerramento ainda a definir.
- **Origem:** decisão de prototipação proposta; RF03. **Não validada institucionalmente.**

### RN08 — Estados da oportunidade
- **Descrição:** oportunidade nasce em **Rascunho**, pode ficar **Publicada** e depois **Encerrada/Arquivada**. Somente Publicada e dentro do prazo aceita interesse.
- **Condição:** ações de gestor ou término de prazo.
- **Resultado:** a consulta lista publicadas; o histórico fica sujeito à política de retenção.
- **Origem:** decisão proposta para coerência das telas; RF01/RF06. **A validar.**

### RN09 — Estados de manifestação
- **Descrição:** manifestação passa por **Registrado**, **Em acompanhamento** e **Encerrado**; não representa candidatura formal, deferimento ou concessão de bolsa.
- **Condição:** criação e atualização por gestor autorizado.
- **Resultado:** estudante vê estado atual e histórico mínimo.
- **Origem:** decisão proposta para coerência das telas; RF03–RF05. **A validar.**

## 2. Checklist de validação LAPIS
- [x] Identificador e descrição registrados em cada RN.
- [x] Condições e resultados previstos descritos.
- [ ] Fontes e regras institucionais reais confirmadas.
- [ ] Verificação de conflitos e rastreabilidade pelo grupo.
- [ ] Aprovação institucional e revisão por pares.

## 3. Rastreabilidade
| RN | RF relacionado | UC |
| --- | --- | --- |
| RN01 | RF01, RF06 | UC01 |
| RN02 | RF01 | UC01 |
| RN03 | RF03, RF06 | UC01, UC03 |
| RN04 | RF03 | UC03 |
| RN05 | RF04, RF05 | UC04, UC05 |
| RN06 | RF06 | UC01 |
| RN07 | RF03 | UC03 |
| RN08 | RF01, RF03, RF06 | UC01, UC03 |
| RN09 | RF03, RF04, RF05 | UC03, UC04, UC05 |

[Visão](../01-Elicitacao/01-Visao-da-Demanda.md) · [Casos de uso](../03-UML/01-Casos-de-Uso.md)
