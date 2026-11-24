# Design System — Oportunidades Internacionais

**Projeto:** Gestão de Oportunidades Internacionais · Grupo 7 · Proposta 3  
**Direção visual:** moderna, profissional, confiável e acolhedora, com hierarquia clara para estudantes e gestores.  
**Aplicação:** protótipo navegável em `06-Prototipos/navegavel/index.html`.

## 1. Princípios de experiência

1. **Clareza em primeiro lugar:** oportunidades, prazos, requisitos e situação do interesse devem ser identificados rapidamente.
2. **Coerência entre perfis:** estudantes e gestores compartilham a mesma marca e os mesmos componentes, mas possuem navegação e ações próprias.
3. **Ações inequívocas:** publicar, encerrar, arquivar e desarquivar são ações diferentes, com rótulos e estados explícitos.
4. **Confiança e previsibilidade:** confirmações, mensagens de erro e feedback deixam claro o resultado das ações. Manifestar interesse não equivale à candidatura formal.
5. **Responsividade e acessibilidade:** layout fluido, texto legível, foco visível, áreas clicáveis confortáveis e leitura por teclado.

## 2. Identidade

**Nome público:** Oportunidades Internacionais.  
**Assinatura visual:** monograma **OI** em símbolo quadrado com cantos arredondados, marca tipográfica em duas linhas e destaque azul na segunda palavra.  
**Tom:** direto, organizado e institucional sem parecer burocrático.  
**Iconografia:** elementos geométricos e sinais contextuais discretos, sem dependência de biblioteca externa.

### Paleta de cores

| Token CSS | Valor | Uso |
| --- | --- | --- |
| `--brand-950` | `#0B2344` | Azul-marinho da identidade, títulos e hero |
| `--brand-800` | `#123D75` | Gradientes e superfícies de marca |
| `--primary-600` | `#1D62D0` | Botões principais e links |
| `--primary-700` | `#164FAE` | Estado hover / texto de botões |
| `--teal-600` | `#0F8079` | Detalhes de apoio e destaques |
| `--page` | `#F4F7FC` | Fundo das páginas |
| `--surface` | `#FFFFFF` | Cartões, formulários e painéis |
| `--surface-soft` | `#F7F9FD` | Áreas secundárias |
| `--ink` | `#172B46` | Texto principal |
| `--ink-muted` | `#526781` | Texto explicativo |
| `--line` | `#DAE4F0` | Bordas e separadores |
| `--success-ink` | `#12634D` | Oportunidades publicadas |
| `--warning-ink` | `#895C17` | Avisos e pendências |
| `--danger-ink` | `#A12D42` | Ações de encerramento |

**Regra:** cor nunca é o único indicador de situação; chips sempre exibem o texto completo do estado.

## 3. Tipografia

- Família: `Inter, ui-sans-serif, system-ui, -apple-system, Segoe UI, Arial, sans-serif`. Usa fontes locais se Inter não estiver disponível, mantendo o protótipo funcional offline.
- Título principal: 34–48 px adaptáveis, peso 800.
- Título de seção: 24–30 px, peso 750–800.
- Título de cartão: 18–20 px, peso 750.
- Corpo: 15–16 px, entrelinha aproximada 1.55.
- Rótulos e metadados: 12–14 px, com contraste preservado.

## 4. Espaçamento e composição

- Base modular de **4 px**; intervalos frequentes: 8, 12, 16, 24, 32 e 48 px.
- Conteúdo: largura máxima **1200 px**, centralizada com margens adaptáveis.
- Grid de oportunidades: 3 colunas em desktop, 2 em tablet e 1 em celular.
- Formulários e painéis: 2 colunas quando houver espaço, 1 em celular.
- Cantos: `--radius-sm: 10px`, `--radius-md: 16px`, `--radius-lg: 24px`.
- Sombras sutis, com estados hover perceptíveis; evitar sobreposição de informação.

## 5. Componentes padronizados

| Componente | Especificação |
| --- | --- |
| **Barra de navegação** | Marca OI, atalhos por perfil e botão de perfil; estado ativo perceptível |
| **Hero** | Gradiente azul-marinho/azul e grafismo orbital, CTA de alta prioridade |
| **Card de oportunidade** | Tipo e destino, título, resumo, estado, área, prazo e botão Ver detalhes |
| **Filtros** | Pesquisa por texto e filtros de tipo, destino e área em campos com rótulo |
| **Chips de estado** | Publicada, Rascunho, Encerrada, Arquivada; estados escritos |
| **Painel gestor** | Métricas, registros em gestão, arquivo administrativo e ações específicas |
| **Formulário** | Rótulos fixos, indicação de obrigatório, borda/foco, mensagem de validação |
| **Feedback** | Avisos de regra, confirmação modal e toast em região de status |
| **Estado vazio** | Mensagem orientadora e ação de recuperação quando aplicável |

### Comportamento de botões

- **Primário:** ação que avança o fluxo (Explorar, Publicar, Confirmar).
- **Secundário:** navegação ou ação reversível de baixo risco (Ver detalhes, Salvar rascunho, Desarquivar).
- **Destrutivo/alerta:** Encerrar, com confirmação e mensagem de efeito.
- **Arquivar:** somente após Encerrada; **Desarquivar** retorna para Encerrada sem republicar.
- Ações desabilitadas precisam permanecer legíveis e não devem parecer disponíveis.

## 6. Acessibilidade e comportamento responsivo

- Foco de teclado visível em botões, links, controles e `summary`.
- Formulários com label associada; mensagens informativas não dependem exclusivamente de cor.
- Ajustes para larguras aproximadas de 1100, 860, 600 e 390 px; sem rolagem horizontal de conteúdo essencial.
- `prefers-reduced-motion` limita transições e efeitos.
- Modal de interesse com títulos e botões identificáveis; acesso por perfil explicitamente demonstrativo.
- Acessibilidade WCAG 2.1 AA é **meta**, não certificação atribuída ao protótipo.

## 7. Regras de preservação funcional

A evolução visual **não altera**:
- RF01: cadastro, edição, rascunho e validação de publicação;
- RF02: busca e filtros por tipo, destino e área, detalhes e estado vazio;
- RF03/RF04: manifestação, aviso de não candidatura e acompanhamento;
- RF05: atualização de estado com histórico;
- RF06: Publicada → Encerrada ⇄ Arquivada, sem republicação automática;
- RF07: seleção demonstrativa de Visitante/Estudante/Gestor;
- RN01–RN09 e limites do protótipo (dados fictícios, sem backend e sem autenticação real).

**Implementação:** tokens CSS e componentes ficam incorporados no próprio HTML, para que baixar **somente** `index.html` continue sendo suficiente para abrir a demonstração.

## 8. Checklist de revisão visual

- [x] Tokens, identidade, componentes, espaçamento e tipografia definidos.
- [ ] Revisar em navegador as telas W01–W08 em desktop e celular.
- [ ] Testar navegação por teclado, foco e mensagens.
- [ ] Executar os fluxos RF01–RF07 após as alterações visuais.

**Referências do projeto:** [SRS](../04-SRS/01-SRS-IEEE830.md) · [Wireframes](00-Guia-Wireframes.md) · [Protótipo navegável](navegavel/index.html).
