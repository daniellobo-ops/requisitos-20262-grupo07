# Requisitos Não Funcionais — Proposta 3 (LAPIS)

> **v0.1 | Rascunho.** Classificação conforme categorias do [template LAPIS](https://github.com/marcelobezerra-dotcom/Lapis-unifor/blob/main/Requisitos/Artefatos/Templates/template-requisitosNaoFuncionais.md). Metas não foram aprovadas nem testadas.

## Histórico
| Data | Versão | Descrição |
| --- | --- | --- |
| 17/11/2026 | 0.1 | RNF propostos para o escopo reduzido |

## 1. Requisitos de Produto
### 1.1 Eficiência de desempenho
**RNF01 — Tempo de resposta (proposto):** páginas de listagem e detalhes devem responder em até 3 segundos sob condições de teste **a especificar**. **Verificação:** teste de desempenho com cenário e carga definidos. *A confirmar.*

### 1.2 Flexibilidade / portabilidade
**RNF02 — Responsividade:** interface de consulta e gestão deve se ajustar a celular e computador, incluindo largura de tela de 360 px ou superior (valor proposto). **Verificação:** teste de layout e navegação em larguras representativas.

### 1.3 Confiabilidade
**RNF03 — Persistência e recuperação:** registros de interesse e oportunidades não devem se perder após falhas recuperáveis; periodicidade, retenção e restauração de backup **a definir**. **Verificação:** teste de restauração quando política for definida.

### 1.4 Segurança
**RNF04 — Controle de acesso:** apenas gestores autorizados publicam ou alteram oportunidades; estudantes consultam apenas suas próprias manifestações; o transporte de dados pessoais deverá ser protegido. **Verificação:** testes de permissão e transporte protegido.

### 1.5 Privacidade
**RNF05 — Minimização dos dados:** coletar apenas dados necessários para registrar interesse e vincular o estudante; estabelecer finalidade, base legal e retenção antes de produção. **Verificação:** inspeção de campos e política de tratamento; pendência com responsáveis.

### 1.6 Capacidade de interação
**RNF06 — Acessibilidade:** adotar WCAG 2.1 nível AA como meta proposta, com checagem de teclado, contraste, texto e formulários. **Verificação:** inspeção e teste de acessibilidade; meta a confirmar.

**RNF07 — Clareza do fluxo:** a confirmação de manifestação deve esclarecer que não constitui candidatura formal. **Verificação:** teste de cenário de entendimento com usuário.

### 1.7 Manutenibilidade
Não há requisito institucional levantado. A definir na revisão.

### 1.8 Compatibilidade
Integração com serviços acadêmicos não confirmada; fora do escopo inicial.

### 1.9 Segurança operacional
Não se aplica requisito específico identificado nesta fase; reavaliar conforme risco.

### 1.10 Adequação funcional
Os RF01–RF06 definem as capacidades previstas, com critérios de aceitação por cenário.

## 2. Requisitos externos
**Legislativo:** observância da LGPD quando houver tratamento de dados pessoais. Procedimento e base legal dependem de confirmação; não presumir que consentimento é sempre a base aplicável.

## 3. Requisitos organizacionais
- **Operacionais:** responsáveis pela publicação e atualização de editais ainda não identificados.
- **Desenvolvimento/ambiente:** não foram impostas linguagens ou infraestrutura pelo material da Proposta 3.

## 4. Checklist de validação
- [x] Categorias do LAPIS utilizadas onde aplicáveis.
- [x] Itens com identificadores, critérios de verificação e pendências.
- [ ] Metas de desempenho e acessibilidade confirmadas.
- [ ] Segurança, política de dados e recuperação definidas institucionalmente.
- [ ] Revisão por pares e validação documentadas.

## Referências
[Visão](../01-Elicitacao/01-Visao-da-Demanda.md) · [RF](01-Requisitos-Funcionais.md) · [RN](03-Regras-de-Negocio.md).
