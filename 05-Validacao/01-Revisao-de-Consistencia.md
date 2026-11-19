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
| NEC02 | RF06 | UC01 | US06 | RN01, RN03, RN06, RN08 | Gestor edita/encerra oportunidades |
| NEC02/NEC03 | RF07 | UC06 | US07 | RN01, RN05 | Estudante e gestor entram por perfil |

**Resultado:** 7/7 RF estão associados a casos de uso e histórias; os 6 UC existentes têm RF e as 9 RN aparecem na especificação. Essa contagem demonstra **rastreabilidade documental inicial**, não execução dos testes.

## 3. Comparação entre SRS e UML

### 3.1 Casos de uso
- **Compatível:** UC01 corresponde a RF01 e RF06; UC02 a RF02; UC03–UC05 a RF03–RF05; UC06 a RF07.
- **Correção nesta sprint:** ator **Visitante** acrescentado à representação e ao catálogo de UC02 para explicitar a consulta pública já admitida pela Visão e SRS; o ator Estudante foi mantido.
- **Limite:** visitante não pode registrar interesse ou consultar manifestações privadas.
- **Pendente:** exportar e inspecionar graficamente a versão PlantUML em notação UML, além da visualização conceitual Mermaid.

### 3.2 Componentes
- **Compatível:** Interface Web, Controle de Acesso, Gestão de Oportunidades, Consulta de Oportunidades, Gestão de Interesse e Persistência correspondem às funções especificadas.
- **Risco de interpretação:** setas conceituais não definem APIs, tecnologias, microsserviços nem integração com sistema institucional.
- **Pendente:** verificar a apresentação final do diagrama UML renderizado.

### 3.3 Implantação
- **Compatível:** navegador, aplicação web e persistência representam cenário hipotético para o MVP.
- **Restrições:** não há hospedagem, banco, autenticação institucional ou política de backup confirmados; HTTPS é diretriz proposta.
- **Pendente:** renderização UML final e revisão técnica do cenário de implantação.

## 4. Achados e tratamento

| ID | Achado | Avaliação | Decisão/encaminhamento | Estado |
| --- | --- | --- | --- | --- |
| C01 | Consulta pública da SRS sem ator Visitante no diagrama | Divergência de representação | Incluir Visitante em UC02 e explicitar consulta sem identificação, preservando estudante | **Corrigido no diagrama** |
| C02 | RN08 usa estado final “Encerrada/Arquivada”; versão inicial da SRS separava dois estados | Ambiguidade conceitual | SRS ajustada para usar “Encerrada/Arquivada” como condição final conjunta, sem transição adicional | **Corrigido na SRS** |
| C03 | RF05/RN09 não definem integralmente transições de situação | Regra incompleta | Demonstrar Registrado → Em acompanhamento → Encerrado e a alternativa Registrado → Encerrado somente como fluxo proposto; não permitir reabertura sem definição | **Aberto — validar** |
| C04 | Identificação simulada não garante autenticação/segurança | Restrição de escopo | Rotular seleção de perfil como **simulação**; produção exige autenticação/autorização real | **Definido para demonstração** |
| C05 | RN07 não determina se é possível novo interesse após encerramento do anterior | Lacuna | Bloquear duplicidade ativa; não oferecer reabertura automática na demonstração | **Aberto** |
| C06 | RNF01, RNF02 e RNF06 possuem metas sem homologação | Critérios não validados | Manter metas como propostas e não afirmar conformidade testada | **Aberto** |
| C07 | Fontes da elicitação são entrevistas didáticas simuladas | Limite de evidência | Manter origem fictícia identificada, não alegar validação com usuários reais | **Documentado** |
| C08 | Fontes UML são PlantUML e visualizações Mermaid, sem arquivos gráficos UML finais | Formato pendente | Renderizar/exportar diagramas e conferir notação final antes de encerrar a Issue | **Aberto** |

## 5. Critérios de consistência para protótipos

| Fluxo de tela | RF / UC | Restrições verificáveis |
| --- | --- | --- |
| Catálogo e detalhes | RF02 / UC02 | Consulta pública; informações essenciais e estado sem resultados |
| Manifestar interesse | RF03 / UC03 | Perfil estudante, prazo aberto, sem duplicidade ativa, aviso de não candidatura |
| Meus interesses | RF04 / UC04 | Apenas manifestações do estudante identificado; mostrar situação |
| Painel de oportunidades | RF01, RF06 / UC01 | Gestor; validação de publicação, estados e encerramento |
| Gerir manifestações | RF05 / UC05 | Gestor; registro de novo estado, responsável e data |
| Acesso por perfil | RF07 / UC06 | Entrada demonstrativa explicitamente simulada |

## 6. Checklist de encerramento

- [x] SRS, RF, RNF, RN, UC, backlog e arquitetura comparados documentalmente.
- [x] Matriz RF ↔ UC ↔ US ↔ RN criada.
- [x] Divergência sobre ator Visitante corrigida no diagrama de casos de uso.
- [x] Lacunas e decisões pendentes identificadas.
- [x] Harmonizar descrição dos estados de oportunidades na SRS e UML (RN08).
- [ ] Revisar a notação dos diagramas UML renderizados e disponibilizar artefatos gráficos finais.
- [ ] Verificar wireframes e protótipo contra a matriz de rastreabilidade.
- [ ] Revisão por pares e aprovação acadêmica registradas.

**Conclusão preliminar:** a documentação está **majoritariamente coerente** com o escopo. A revisão está em andamento; **Issue #7 permanece aberta** até resolver/registrar decisões pendentes e concluir a conferência final.
