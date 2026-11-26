# Relatório de Verificação — Entrega M2

**Projeto:** Gestão de Oportunidades Internacionais • Grupo 7 • Proposta 3  
**Escopo:** conferência de rastreabilidade documental, integridade de links, diagramas UML em SVG e regressão funcional do protótipo navegável.

## 1. Artefatos conferidos

- [SRS IEEE 830](../04-SRS/01-SRS-IEEE830.md) — RF01–RF07, RNF01–RNF07 e RN01–RN09.
- [Revisão de consistência](01-Revisao-de-Consistencia.md).
- UML: [Casos de uso](../03-UML/01-Casos-de-Uso.md), [Componentes](../03-UML/02-Componentes.md), [Implantação](../03-UML/03-Implantacao.md).
- Diagramas visuais: [UC SVG](../03-UML/04-Diagrama-Casos-de-Uso.svg), [Componentes SVG](../03-UML/05-Diagrama-Componentes.svg), [Implantação SVG](../03-UML/06-Diagrama-Implantacao.svg).
- [Wireframes](../06-Prototipos/00-Guia-Wireframes.md), [Design System](../06-Prototipos/04-Design-System.md) e [protótipo navegável](../06-Prototipos/navegavel/index.html).

## 2. Rastreabilidade e conformidade documental

| Verificação | Resultado |
| --- | --- |
| RF01–RF07 identificados na SRS | Conforme |
| UC01–UC06 documentados e associados aos RF | Conforme |
| Componentes conceituais relacionados às funções do sistema | Conforme |
| Implantação descrita como modelo de arquitetura proposta | Conforme |
| RN08: Rascunho → Publicada → Encerrada ⇄ Arquivada | Conforme |
| Diferença entre manifestação de interesse e inscrição formal | Conforme |
| Documentação distingue protótipo local de sistema com backend | Conforme |
| Diagramas UML disponibilizados em arquivos SVG | Conforme |

**Observação:** os SVGs de componentes e implantação representam a arquitetura conceitual. A aplicação demonstrativa HTML executa localmente, sem infraestrutura de servidor, autenticação real ou banco de dados.

## 3. Resultados da regressão programática

Foi executada uma bateria de **27 verificações automatizadas de lógica e geração das telas, todas com resultado positivo (27/27)**.

| Conjunto | Itens verificados | Resultado |
| --- | --- | --- |
| Documentação | RF01–RF07, UC01–UC06, componentes e implantação | 4/4 |
| Controles e escopo | Filtros de tipo/área/destino e aviso de manifestação | 4/4 |
| Navegação | Renderização das oito áreas do protótipo | 8/8 |
| Regras e operações | Filtro combinado, Encerrar, Arquivar, Desarquivar, confirmação e registro de interesse, atualização de situação, privacidade demonstrativa, salvar rascunho, publicar e preservar estado Publicada | 11/11 |
| **Total** | | **27/27** |

**Método:** o JavaScript do arquivo de protótipo foi compilado e exercitado em ambiente simulado, com representação dos eventos e dos elementos essenciais da página. Isso verifica caminhos da lógica, não corresponde à execução completa em um navegador gráfico.

## 4. SVG e navegação documental

- Os três arquivos SVG passaram na conferência da estrutura das tags e entidades XML, sem erros detectados.
- Os artefatos estão referenciados nos arquivos de UML correspondentes.
- Os documentos de especificação, prototipação e README foram associados às respectivas seções do repositório.

## 5. Conferência manual para apresentação

- [ ] Abrir o HTML atualizado no Chrome/Edge e executar o roteiro completo.
- [ ] Conferir aparência, distribuição de conteúdo e legibilidade em desktop e celular.
- [ ] Conferir foco de teclado, contraste e comportamento das mensagens.
- [ ] Revisar os SVGs visualmente e verificar clareza das associações.
- [ ] Registrar revisão final do grupo e eventuais observações do professor.

**Conclusão:** a documentação e os fluxos programáticos centrais da Sprint 2 estão consistentes dentro do escopo de protótipo navegável. Os itens acima são verificação visual e acadêmica complementar e não foram registrados como testes já executados.
