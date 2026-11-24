# Protótipo Navegável — Gestão de Oportunidades Internacionais

**Sprint 2 • Issue #9 • Proposta 3**

Protótipo interativo responsivo com oito telas/áreas e fluxos de **Visitante**, **Estudante** e **Gestor**. Implementado em HTML, CSS e JavaScript, sem dependências externas.

**Identidade visual:** interface moderna de plataforma digital profissional, com marca OI, design tokens, componentes padronizados, estados de foco e layout responsivo, seguindo o [Design System](04-Design-System.md).

## Como executar

1. Acesse [index.html](navegavel/index.html) e use **Download raw file** no GitHub para salvar o arquivo.
2. Abra o arquivo baixado em um navegador moderno, como Chrome ou Edge.
3. O protótipo funciona localmente, sem servidor, instalação ou conta.
4. **Importante:** a visualização de código do GitHub não executa a interface HTML. Para navegar, abra o arquivo no navegador. Um link público hospedado pode ser acrescentado posteriormente, caso o grupo habilite uma hospedagem estática.

**Arquivo:** [Protótipo HTML navegável](navegavel/index.html)

## Identidade visual e experiência

- Paleta azul-marinho, azul principal e teal; superfícies claras e hierarquia tipográfica uniforme.
- Navegação e botões com estados visuais consistentes; cards de oportunidades, dashboard e formulários padronizados.
- Layout responsivo em desktop e celular, sem dependência de fontes ou bibliotecas online.
- Foco de teclado visível e redução de movimento conforme preferência do dispositivo.
- A identidade visual não altera os requisitos RF01–RF07 nem as regras RN01–RN09.

## Telas e navegação

| Tela | Função | RF / UC |
| --- | --- | --- |
| Início | Destaques e acesso ao catálogo | RF02 / UC02 |
| Catálogo | Pesquisa, filtros por tipo/destino/área, lista vazia | RF02 / UC02 |
| Detalhe | Requisitos, documentos, prazo, manifestação | RF02, RF03 / UC02, UC03 |
| Entrada por perfil | Alternância demonstrativa Estudante/Gestor/Visitante | RF07 / UC06 |
| Meus interesses | Registros e histórico do estudante | RF04 / UC04 |
| Painel do gestor | Oportunidades e resumo de interesses | RF01, RF06 / UC01 |
| Cadastro/edição | Rascunho, publicação e validação de obrigatórios | RF01, RF06 / UC01 |
| Gestão de manifestações | Atualização de estado e histórico | RF05 / UC05 |

## Roteiro sugerido para a apresentação

### Fluxo 1 — Estudante
1. Abra **Catálogo** e filtre oportunidades por tipo, destino ou área.
2. Escolha uma oportunidade **Publicada**, com prazo aberto, e acesse os detalhes.
3. Clique em **Manifestar interesse**; selecione **Estudante** se necessário.
4. Confira o aviso de que interesse **não constitui candidatura formal** e confirme.
5. Consulte o registro em **Meus interesses**.
6. Tente registrar interesse novamente: a aplicação oferece o registro já existente, impedindo duplicidade ativa.

### Fluxo 2 — Gestor
1. Em **Perfil**, selecione **Gestor de oportunidades**.
2. No painel, clique **Nova oportunidade**.
3. Tente publicar com campos vazios para visualizar a validação.
4. Preencha o formulário e escolha **Salvar rascunho** ou **Publicar**.
5. Abra **Manifestações** e altere um registro de **Registrado** para **Em acompanhamento**.
6. Volte ao perfil Estudante para observar o estado alterado.
7. Encerre uma oportunidade publicada no painel e confira que ela deixa de aceitar novos interesses.
8. Clique em **Arquivar** na oportunidade encerrada e confira sua transferência para **Arquivo de oportunidades**, mantendo os registros de interesse no histórico.
9. No arquivo, clique em **Desarquivar** e confira que ela volta à lista de gestão como **Encerrada**, sem aceitar novos interesses.

## Regras demonstradas

- **RN01–RN02:** operações de edição/publicação restritas à área do gestor; publicação exige dados mínimos.
- **RN03 e RN08:** oportunidade encerrada ou com prazo vencido não aceita novo interesse.
- **RN04:** manifestação de interesse não é inscrição formal.
- **RN05:** estudante visualiza somente os próprios registros demonstrativos.
- **RN06:** encerrar e arquivar não eliminam manifestações existentes.
- **RN07:** bloqueio de interesse ativo duplicado.
- **RN08:** oportunidades seguem Rascunho → Publicada → Encerrada ⇄ Arquivada, com retorno por Desarquivar para Encerrada e arquivo administrativo separado.
- **RN09:** estados Registrado, Em acompanhamento e Encerrado com histórico de alterações.

## Limites do protótipo

Os dados são **fictícios**, mantidos em memória durante a sessão da página; ao recarregar, o cenário inicial é restaurado. A seleção de perfil é **simulada** e não implementa login real. O protótipo não realiza candidaturas, seleção de bolsistas, integrações acadêmicas ou gravação em banco de dados.

## Artefatos relacionados

- [Wireframes](00-Guia-Wireframes.md)
- [Design System](04-Design-System.md)
- [SRS — IEEE 830](../../04-SRS/01-SRS-IEEE830.md)
- [Revisão de consistência](../../05-Validacao/01-Revisao-de-Consistencia.md)

## Checklist da Issue #9

- [x] Telas navegáveis para estudante e gestor implementadas.
- [x] Fluxos principais da SRS representados.
- [x] Interface responsiva em HTML/CSS.
- [x] Formulário, filtros, manifestações e estados demonstrativos implementados.
- [x] Código versionado no repositório.
- [x] Design system definido e identidade visual moderna aplicada no HTML.
- [ ] Revisar visualmente a execução em navegadores e telas diferentes.
- [ ] Verificar roteiro de apresentação com o grupo.
- [ ] Acrescentar URL hospedada, caso exigida para acesso remoto.

**Situação:** protótipo implementado e disponível para revisão; não equivale a sistema em produção.
