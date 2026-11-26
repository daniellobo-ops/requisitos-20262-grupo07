# Revisão de Consistência — Sprint 2 (M2)

> **Versão 0.1 | Revisão de consistência — Issue #7.**

## 1. Objetivo e documentos revisados

Conferir correspondência, integridade e ausência de contradições conhecidas entre a [SRS](../04-SRS/01-SRS-IEEE830.md), [RF](../02-Requisitos/01-Requisitos-Funcionais.md), [RNF](../02-Requisitos/02-Requisitos-Nao-Funcionais.md), [RN](../02-Requisitos/03-Regras-de-Negocio.md), [backlog](../GestaoConfiguracao/01-Backlog-Priorizado.md) e diagramas UML de [casos de uso](../03-UML/01-Casos-de-Uso.md), [componentes](../03-UML/02-Componentes.md) e [implantação](../03-UML/03-Implantacao.md).

**Escopo fixo:** Proposta 3 — Gestão de Oportunidades Internacionais. Manifestação de interesse **não** corresponde a candidatura formal, seleção ou concessão de bolsa.

## 2. Matriz de rastreabilidade documental

| Necessidade | RF | UC | US | Regras associadas | Evidência na UML |
| --- | --- | --- | --- | --- | --- |
| NEC02 | RF01 | UC01 | US01 | RN01, RN02, RN08 | Gestor gerencia oportunidades |
| NEC01 | RF02 | UC02 | US02 | RN08 | Visitante e estudante consultam oportunidades |
| NEC03 | RF03 | UC03 | US03 | RN03, RN04, RN07, RN08, RN09 | Estudante registra interesse |
| NEC03 | RF04 | UC04 | US04 | RN05, RN09 | Estudante consulta seus interesses |
| NEC03 | RF05 | UC05 | US05 | RN05, RN09 | Gestor atualiza situação |
| NEC02 | RF06 | UC01 | US06 | RN01, RN03, RN06, RN08 | Gestor edita, encerra, arquiva e desarquiva oportunidades |
| NEC02/NEC03 | RF07 | UC06 | US07 | RN01, RN05 | Estudante e gestor entram por perfil |

**Resultado:** 7/7 RF estão associados a casos de uso e histórias; os 6 UC existentes têm RF e as 9 RN aparecem na especificação. Essa contagem demonstra **rastreabilidade documental inicial**, não execução dos testes.

## 3. Comparação entre SRS e UML

### 3.1 Casos de uso
- **Compatível:** UC01 corresponde a RF01 e RF06; UC02 a RF02; UC03–UC05 a RF03–RF05; UC06 a RF07.
- **Correção nesta sprint:** ator **Visitante** acrescentado à representação e ao catálogo de UC02 para explicitar a consulta pública já admitida pela Visão e SRS; o ator Estudante foi mantido.
- **Limite:** visitante não pode registrar interesse ou consultar manifestações privadas.
- **Arquivo visual disponível:** [casos de uso em SVG](../03-UML/04-Diagrama-Casos-de-Uso.svg), com atores, casos de uso e associações. Fonte PlantUML mantida para edição.

### 3.2 Componentes
- **Compatível:** Interface Web, Controle de Acesso, Gestão de Oportunidades, Consulta de Oportunidades, Gestão de Interesse e Persistência correspondem às funções especificadas.
- **Risco de interpretação:** setas conceituais não definem APIs, tecnologias, microsserviços nem integração com sistema institucional.
- **Arquivo visual disponível:** [componentes em SVG](../03-UML/05-Diagrama-Componentes.svg), complementando a representação Mermaid e a fonte PlantUML.

### 3.3 Implantação
- **Compatível:** navegador, aplicação web e persistência representam cenário hipotético para o MVP.
- **Restrições:** não há hospedagem, banco, autenticação institucional ou política de backup confirmados; HTTPS é diretriz proposta.
- **Arquivo visual disponível:** [implantação em SVG](../03-UML/06-Diagrama-Implantacao.svg). Representa a arquitetura conceitual proposta, não a hospedagem do protótipo local.

## 4. Achados e tratamento

| ID | Achado | Avaliação | Decisão/encaminhamento | Estado |
| --- | --- | --- | --- | --- |
| C01 | Consulta pública da SRS sem ator Visitante no diagrama | Divergência de representação | Incluir Visitante em UC02 e explicitar consulta sem identificação, preservando estudante | **Corrigido no diagrama** |
| C02 | Fluxo de encerramento e arquivamento exige operações distintas | Consistência funcional | Estados harmonizados em RF, RN, SRS, UML e protótipo: Rascunho → Publicada → Encerrada ⇄ Arquivada; desarquivar retorna ao estado Encerrada | **Corrigido** |
| C03 | RF05/RN09 não definem integralmente transições de situação | Regra incompleta | Demonstrar Registrado → Em acompanhamento → Encerrado e a alternativa Registrado → Encerrado somente como fluxo proposto; não permitir reabertura sem definição | **Aberto — validar** |
| C04 | Identificação simulada não garante autenticação/segurança | Restrição de escopo | Rotular seleção de perfil como **simulação**; produção exige autenticação/autorização real | **Definido para demonstração** |
| C05 | RN07 não determina se é possível novo interesse após encerramento do anterior | Lacuna | Bloquear duplicidade ativa; não oferecer reabertura automática na demonstração | **Aberto** |
| C06 | RNF01, RNF02 e RNF06 precisam de cenários de verificação | Critérios de teste | Definir condições e executar testes de desempenho, responsividade e acessibilidade | **Aberto** |
| C07 | Entrevistas simuladas utilizadas na elicitação | Metodologia | Identificar a modalidade de entrevista nos artefatos | **Documentado** |
| C08 | UML disponibilizada como Mermaid e código PlantUML | Apresentação dos artefatos | Adicionar arquivos gráficos SVG de casos de uso, componentes e implantação | **Arquivos adicionados** |

## 5. Critérios de consistência para protótipos

| Fluxo de tela | RF / UC | Restrições verificáveis |
| --- | --- | --- |
| Catálogo e detalhes | RF02 / UC02 | Consulta pública; informações essenciais e estado sem resultados |
| Manifestar interesse | RF03 / UC03 | Perfil estudante, prazo aberto, sem duplicidade ativa, aviso de não candidatura |
| Meus interesses | RF04 / UC04 | Apenas manifestações do estudante identificado; mostrar situação |
| Painel de oportunidades | RF01, RF06 / UC01 | Gestor; validação de publicação, edição, encerramento, arquivamento e desarquivamento |
| Gerir manifestações | RF05 / UC05 | Gestor; registro de novo estado, responsável e data |
| Acesso por perfil | RF07 / UC06 | Entrada demonstrativa explicitamente simulada |

## 6. Checklist de encerramento

- [x] SRS, RF, RNF, RN, UC, backlog e arquitetura comparados documentalmente.
- [x] Matriz RF ↔ UC ↔ US ↔ RN criada.
- [x] Divergência sobre ator Visitante corrigida no diagrama de casos de uso.
- [x] Lacunas e decisões pendentes identificadas.
- [x] Harmonizar descrição dos estados de oportunidades na SRS e UML (RN08).
- [x] Disponibilizar SVGs de casos de uso, componentes e implantação vinculados à fonte documental.
- [x] Conferir documentalmente wireframes e protótipo contra a matriz RF/UC, incluindo filtro por área e ações de arquivar/desarquivar.
- [ ] Executar teste de navegação completo em navegador, incluindo dispositivos móveis.
- [ ] Revisão por pares e aprovação acadêmica registradas.

**Verificação programática:** [Relatório de verificação](02-Relatorio-de-Verificacao.md) — 27/27 verificações positivas. A execução visual em diferentes telas permanece como conferência complementar.

**Conclusão da conferência documental:** os requisitos funcionais, a SRS, os casos de uso e os wireframes estão alinhados com os fluxos representados no protótipo. Persistem testes de execução e revisão final do grupo. A revisão está em andamento; **Issue #7 permanece aberta** até resolver/registrar decisões pendentes e concluir a conferência final.
