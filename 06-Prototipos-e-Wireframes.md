# 🎨 Protótipos e Wireframes

> **Status:** wireframes estruturais em formato textual. O protótipo navegável (Figma ou similar) ainda deve ser criado a partir destes esboços.
> **Link do protótipo:** _a preencher_

---

## 1. Introdução
Especifica a interface do **Sistema de Apoio à Internacionalização** da Unifor: mapa de navegação e wireframes das telas principais do Portal do Estudante e do Painel de Gestão do NEI. A mesma interface deve ser responsiva (RNF02) e acessível (RNF05).

---

## 2. Mapa de navegação

* **Portal do Estudante** (autenticado)
  * Início
  * Oportunidades e editais (T1)
  * Autoavaliação de elegibilidade (T2)
  * Minhas candidaturas (T3 formulário, T4 acompanhamento)
  * Central de preparação *(Should)*
  * Relatos e Tandem *(Could)*
* **Painel do NEI** (perfil Gestor)
  * Início
  * Triagem de candidaturas (T5)
  * Convênios e editais (T6)
  * Bolsas e vagas *(Should)*
  * Relatórios *(Should)*

| Tela | Nome | Requisitos | Caso de uso |
| :-: | :--- | :-: | :-: |
| T1 | Busca de oportunidades | RF02 | UC01 |
| T2 | Resultado da autoavaliação | RF03 | UC02 |
| T3 | Formulário de candidatura | RF04 | UC03 |
| T4 | Minhas candidaturas | RF05, RF09 | UC04 |
| T5 | Triagem de candidaturas (NEI) | RF08, RF11 | UC08 |
| T6 | Cadastro de edital (NEI) | RF06, RF07 | UC06, UC07 |

---

## 3. Wireframes

### T1: Busca de oportunidades (Estudante)

```
+--------------------------------------------------------------+
| Unifor | Internacionalização        [Oportunidades] [Minhas]  |
+--------------------------------------------------------------+
| Buscar oportunidades                                         |
| [ Buscar por instituição ou palavra-chave        ] [Buscar]  |
|                                                              |
| Filtros:  País [v]   Área [v]   Idioma [v]   Duração [v]     |
|           [Limpar filtros]                                   |
+--------------------------------------------------------------+
| 12 resultados                                                |
|                                                              |
| +----------------------------------------------------------+ |
| | Universidade X (País)            Edital: ABERTO          | |
| | Área: Engenharia | Idioma: Inglês | Duração: 1 semestre  | |
| | Prazo: dd/mm/aaaa                [Ver detalhes]          | |
| +----------------------------------------------------------+ |
| | Universidade Y (País)            Edital: EM BREVE        | |
| | ...                                                      | |
| +----------------------------------------------------------+ |
|                                  [ 1 ] [ 2 ] [ 3 ] [ > ]     |
+--------------------------------------------------------------+
```

### T2: Resultado da autoavaliação (Estudante)

```
+--------------------------------------------------------------+
| Autoavaliação de elegibilidade          Avaliado em dd/mm    |
+--------------------------------------------------------------+
| Critério                  Exigido        Seu valor   Situação|
|--------------------------------------------------------------|
| Matrícula ativa           Sim            Sim         [OK]    |
| Curso concluído           30% a 70%      45%         [OK]    |
| Média global              >= 7,0         6,8         [X]     |
| Reprovações               Nenhuma        Nenhuma     [OK]    |
|--------------------------------------------------------------|
| Resultado: NÃO APTO no momento                               |
| Motivo: média global abaixo do mínimo exigido.               |
|                                                              |
| [Ver editais abertos]   [Falar com o NEI]                    |
+--------------------------------------------------------------+
```

### T3: Formulário de candidatura (Estudante)

```
+--------------------------------------------------------------+
| Candidatura: Edital 01/2026 - Universidade X                 |
| Prazo final: dd/mm/aaaa                                      |
+--------------------------------------------------------------+
| Dados do candidato (preenchidos automaticamente)             |
| Nome: ______________   Matrícula: ________   Curso: ________ |
|                                                              |
| Motivação                                                    |
| [ Texto livre ...........................................  ] |
|                                                              |
| Documentos obrigatórios                                      |
| Comprovante de idioma   [Anexar PDF]   status: pendente      |
| Carta de motivação      [Anexar PDF]   status: anexado       |
|                                                              |
| [ ] Declaro que as informações são verdadeiras e autorizo o  |
|     uso dos meus dados conforme a política de privacidade.   |
|                                                              |
| [Salvar rascunho]                        [Enviar candidatura]|
+--------------------------------------------------------------+
```

### T4: Minhas candidaturas (Estudante)

```
+--------------------------------------------------------------+
| Minhas candidaturas                                          |
+--------------------------------------------------------------+
| Protocolo   Edital / Instituição      Status         Data    |
|--------------------------------------------------------------|
| 2026-0123   Ed. 01 / Universidade X   EM ANÁLISE     dd/mm   |
| 2026-0098   Ed. 02 / Universidade Y   PENDENTE DOCS  dd/mm   |
|                                                              |
| Detalhe da candidatura 2026-0098                             |
|  Histórico:  dd/mm Enviada  ->  dd/mm Em análise  ->         |
|              dd/mm Pendente de documentos                    |
|  Pendência: reenviar comprovante de idioma     [Reenviar]    |
+--------------------------------------------------------------+
```

### T5: Triagem de candidaturas (Painel do NEI)

```
+--------------------------------------------------------------+
| Painel NEI | Triagem de candidaturas                         |
+--------------------------------------------------------------+
| Edital: [ Ed. 01/2026 - Universidade X  v ]   Vagas: 3 / 10  |
| Status: [ Todos v ]   Buscar: [ nome ou matrícula ]          |
+--------------------------------------------------------------+
| Candidato      Elegib.   Docs       Pont.   Status   Ação     |
|--------------------------------------------------------------|
| Ana S.         Apto      Completos  8,7     Enviada  [Abrir]  |
| Bruno M.       Apto      Faltando   --      Enviada  [Abrir]  |
| Carla R.       Apto      Completos  9,1     Em anál. [Abrir]  |
+--------------------------------------------------------------+
| Candidatura aberta: Carla R.                                 |
|  Documentos: [Idioma.pdf] [Carta.pdf]                        |
|  Decisão:  ( ) Deferir  ( ) Indeferir  ( ) Pedir complemento |
|  Justificativa (obrigatória no indeferimento):               |
|  [ ..................................................... ]   |
|                                              [Registrar]     |
+--------------------------------------------------------------+
```

### T6: Cadastro de edital (Painel do NEI)

```
+--------------------------------------------------------------+
| Painel NEI | Novo edital                         Rascunho    |
+--------------------------------------------------------------+
| Título: [ ..................................................]|
| Convênio: [ Universidade X - País  v ]                       |
| Período de inscrição:  de [dd/mm/aaaa]  até [dd/mm/aaaa]     |
| Vagas: [ 10 ]     Bolsas: [ + Adicionar bolsa ]              |
| Requisitos (herdados da RN01 e ajustáveis):                  |
| [ Texto .................................................. ] |
| Documentos exigidos:  [+ Adicionar documento]                |
|   - Comprovante de idioma (PDF)    [Remover]                 |
|   - Carta de motivação (PDF)       [Remover]                 |
|                                                              |
| [Salvar rascunho]                              [Publicar]    |
+--------------------------------------------------------------+
```

---

## 4. Diretrizes de interface (propostas)

* Mensagens de erro dizem **o que falhou e como corrigir** (por exemplo, T2 e T3).
* O status da candidatura usa **texto e cor**, nunca apenas cor (acessibilidade).
* Em telas pequenas, a tabela de T4 vira lista de cartões e os filtros de T1 ficam recolhidos.
* Ações irreversíveis (enviar candidatura, indeferir) pedem confirmação.

## 5. Próximos passos
1. Reproduzir T1 a T6 no Figma e vincular o link acima.
2. Validar T1 a T3 com estudantes e T5 e T6 com o NEI.
3. Registrar os ajustes nas pendências do documento [09](09-Premissas-Decisoes-e-Fontes.md).
