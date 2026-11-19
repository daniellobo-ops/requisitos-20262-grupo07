# Modelagem UML inicial — Casos de Uso

> **Proposta 3 | v0.2 | Revisão de consistência.** O gráfico Mermaid abaixo é uma **representação visual de atores e casos de uso**, não notação UML rigorosa (não usa atores stick-figure nem elipses padronizadas). O código PlantUML no final permite gerar um diagrama UML de casos de uso propriamente dito.

## 1. Limite do sistema
**Sistema:** Gestão de Oportunidades Internacionais. Não abrange candidaturas formais, seleção, atribuição de bolsa, cálculo de elegibilidade ou funções colaborativas de outras propostas.

## 2. Atores
| Ator | Descrição | Situação |
| --- | --- | --- |
| Visitante | Consulta catálogo e detalhes sem identificação | Ator de consulta pública proposto | 
| Estudante | Consulta oportunidades e registra/acompanha manifestações | Proposto |
| Gestor de oportunidades | Cadastra, publica, edita e encerra oportunidades; acompanha interesses | Responsável pelas funções de gestão |

## 3. Catálogo de casos de uso
| Caso | Nome | Ator principal | Requisitos |
| --- | --- | --- | --- |
| UC01 | Gerenciar oportunidades | Gestor | RF01, RF06 |
| UC02 | Consultar oportunidades | Visitante / Estudante | RF02 |
| UC03 | Registrar manifestação de interesse | Estudante | RF03 |
| UC04 | Consultar manifestações próprias | Estudante | RF04 |
| UC05 | Atualizar situação de interesse | Gestor | RF05 |
| UC06 | Acessar área identificada por perfil | Estudante/Gestor | RF07 |

## 4. Representação visual no GitHub
```mermaid
flowchart LR
    V["👤 Visitante"]
    E["👤 Estudante"]
    G["👤 Gestor de oportunidades"]
    subgraph SYS["Sistema de Gestão de Oportunidades Internacionais"]
      U1(["UC01 Gerenciar oportunidades"])
      U2(["UC02 Consultar oportunidades"])
      U3(["UC03 Registrar interesse"])
      U4(["UC04 Consultar meus interesses"])
      U5(["UC05 Atualizar situação de interesse"])
      U6(["UC06 Acessar por perfil"])
    end
    V --- U2
    E --- U2
    E --- U3
    E --- U4
    G --- U1
    G --- U5
    E --- U6
    G --- U6
```

## 5. Diagrama UML em PlantUML — fonte editável
Copiar para um renderizador PlantUML para obter a notação UML com atores e casos de uso.

```plantuml
@startuml
left to right direction
actor "Visitante" as V
actor "Estudante" as E
actor "Gestor de oportunidades" as G
rectangle "Gestão de Oportunidades Internacionais" {
  usecase "UC01\nGerenciar oportunidades" as UC01
  usecase "UC02\nConsultar oportunidades" as UC02
  usecase "UC03\nRegistrar interesse" as UC03
  usecase "UC04\nConsultar meus interesses" as UC04
  usecase "UC05\nAtualizar situação do interesse" as UC05
  usecase "UC06\nAcessar área por perfil" as UC06
}
V -- UC02
E -- UC02
E -- UC03
E -- UC04
G -- UC01
G -- UC05
E -- UC06
G -- UC06
@enduml
```

## 6. Pré-condições e resultados
| Caso | Pré-condição | Fluxo principal resumido | Exceções/alternativas propostas | Resultado |
| --- | --- | --- | --- | --- |
| UC01 | Gestor autorizado | Informar oportunidade; validar campos; salvar/publicar | Campos faltantes; edição ou encerramento | Oportunidade cadastrada/publicada ou arquivada |
| UC02 | Nenhuma para consulta pública proposta | Consultar lista; filtrar; abrir detalhes | Nenhum resultado | Exibição de prazo, requisitos e documentos |
| UC03 | Estudante identificado; oportunidade aberta | Escolher oportunidade; solicitar manifestação; confirmar | Prazo encerrado; manifestação ativa duplicada (RN07; mostrar registro existente) | Manifestação registrada; aviso de que não é inscrição |
| UC04 | Estudante identificado | Abrir meus interesses; listar situação | Sem interesses | Exibição apenas dos registros próprios |
| UC05 | Gestor autorizado | Consultar manifestações; selecionar registro; atualizar situação (Registrado, Em acompanhamento, Encerrado) | Registro inexistente ou acesso negado | Situação e histórico atualizados |
| UC06 | Usuário inicia sessão no protótipo | Selecionar perfil de estudante/gestor para demonstrar o fluxo autorizado | Perfil não selecionado; operação vedada | Área correspondente exibida |

**Nota de consistência (Sprint 2):** o ator *Visitante* foi explicitado em UC02 para representar a consulta pública já prevista em RF02 e na SRS. Isso não cria funcionalidade adicional nem concede permissão de manifestar interesse.

**Decisões propostas para as telas:** em UC01 oportunidades possuem estados Rascunho, Publicada e Encerrada/Arquivada; em UC03 só pode existir uma manifestação ativa por estudante e oportunidade, sendo exibida a existente em tentativas repetidas. A identificação por perfil é simulada no protótipo; não presume autenticação da Unifor.

## 7. Verificações antes de aprovação
- [ ] Confirmar o papel de gestor e quais campos são exigidos.
- [ ] Validar os estados propostos de oportunidade e manifestação e a regra de duplicidade.
- [ ] Conferir fluxos com responsáveis reais, quando necessário; o grupo informou que a entrega acadêmica usará simulação.
- [ ] Gerar imagem UML a partir do PlantUML, caso a entrega exija arquivo gráfico.

[SRS](../04-SRS/01-SRS-IEEE830.md) · [Revisão de consistência](../05-Validacao/01-Revisao-de-Consistencia.md) · [RF](../02-Requisitos/01-Requisitos-Funcionais.md) · [RN](../02-Requisitos/03-Regras-de-Negocio.md) · [Visão](../01-Elicitacao/01-Visao-da-Demanda.md)
