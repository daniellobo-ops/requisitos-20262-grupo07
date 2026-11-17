# Especificação de Requisitos Não Funcionais — LAPIS

> **Versão 0.3 — 17/11/2026 — revisão metodológica do Grupo 7 (assistida).** Classificação baseada no [template LAPIS RNF](https://github.com/marcelobezerra-dotcom/Lapis-unifor/blob/main/Requisitos/Artefatos/Templates/template-requisitosNaoFuncionais.md). As métricas propostas não foram validadas com o NEI/TI.

## Histórico de versões

| Data | Versão | Alteração |
| --- | --- | --- |
| 03/11/2026 | 0.2 | RNF consolidados na SRS |
| 17/11/2026 | 0.3 | RNF classificados segundo categorias do LAPIS sem mudança nas condições |

## 1. Requisitos de produto

### RNF01 — Segurança e privacidade (LGPD)

- **Classificação LAPIS:** 1.4 Segurança; 1.5 Privacidade; 2.3 Legislativo.
- **Requisito:** Proteger dados pessoais e acadêmicos: tráfego por HTTPS, acesso a documentos apenas pelo titular e pelo Gestor do NEI, coleta limitada ao necessário e registro da base legal e do consentimento quando aplicável.
- **Prioridade:** M (MoSCoW).
- **Verificação proposta:** inspeção de HTTPS, permissões de acesso, coleta e documentação de bases legais; validar com encarregado de dados.
- **Situação:** revisão institucional pendente.

### RNF02 — Responsividade

- **Classificação LAPIS:** 1.2 Flexibilidade/Adaptabilidade; 1.6 Capacidade de interação.
- **Requisito:** A interface deve funcionar em smartphones (a partir de 360 px de largura), tablets e computadores, nas duas últimas versões dos principais navegadores.
- **Prioridade:** M (MoSCoW).
- **Verificação proposta:** testar telas em larguras ≥ 360 px e versões suportadas de navegadores.
- **Situação:** revisão institucional pendente.

### RNF03 — Disponibilidade

- **Classificação LAPIS:** 1.3 Confiabilidade/Disponibilidade.
- **Requisito:** Disponibilidade de 99% durante os períodos de seleção, para consulta de editais e envio de documentos (*proposto*).
- **Prioridade:** M (MoSCoW).
- **Verificação proposta:** medir percentual de disponibilidade no intervalo de seleção; confirmar meta de 99%.
- **Situação:** parâmetro proposto; validar.

### RNF04 — Desempenho

- **Classificação LAPIS:** 1.1 Eficiência de desempenho/Comportamento temporal.
- **Requisito:** Buscas e páginas principais em até 3 segundos sob carga normal (*proposto*; definir "carga normal" com a TI).
- **Prioridade:** M (MoSCoW).
- **Verificação proposta:** medir tempo de resposta de páginas e buscas; definir carga, percentil e ambiente de testes com TI.
- **Situação:** parâmetro proposto; validar.

### RNF05 — Acessibilidade

- **Classificação LAPIS:** 1.6 Capacidade de interação/Inclusividade.
- **Requisito:** Conformidade com WCAG 2.1 nível AA (*proposto*).
- **Prioridade:** S (MoSCoW).
- **Verificação proposta:** avaliar conformidade WCAG 2.1 AA com inspeções e testes acessíveis.
- **Situação:** parâmetro proposto; validar.

### RNF06 — Auditabilidade

- **Classificação LAPIS:** 1.4 Segurança/Integridade e Não repúdio.
- **Requisito:** Registrar quem, quando e o quê em decisões sobre candidaturas e em alterações de editais e convênios.
- **Prioridade:** M (MoSCoW).
- **Verificação proposta:** auditar registro de autoria, data, ação e alterações de editais/convênios.
- **Situação:** revisão institucional pendente.

### RNF07 — Usabilidade

- **Classificação LAPIS:** 1.6 Capacidade de interação/Operabilidade e aprendizagem.
- **Requisito:** Um estudante deve conseguir ir da busca à candidatura sem treinamento; validar com testes de usabilidade com usuários (*proposto*).
- **Prioridade:** S (MoSCoW).
- **Verificação proposta:** testar fluxo de consulta e candidatura com estudantes; definir critério de êxito mensurável.
- **Situação:** parâmetro proposto; validar.

### RNF08 — Confiabilidade

- **Classificação LAPIS:** 1.3 Confiabilidade/Recuperabilidade.
- **Requisito:** Cópia de segurança periódica dos dados e dos documentos anexados (*proposto*: diária).
- **Prioridade:** S (MoSCoW).
- **Verificação proposta:** verificar execução e restauração de backups; definir retenção e periodicidade.
- **Situação:** parâmetro proposto; validar.

### RNF09 — Idioma

- **Classificação LAPIS:** 1.6 Capacidade de interação/Capacidade de uso; 3.2 Operacionais.
- **Requisito:** Interface em português do Brasil; versão em inglês como evolução.
- **Prioridade:** C (MoSCoW).
- **Verificação proposta:** verificar interface em pt-BR; inglês mantido como possível evolução.
- **Situação:** revisão institucional pendente.



## 2. Requisitos externos

- **Legislativos:** RNF01 e RN08 (regra de negócio) tratam da proteção de dados pessoais segundo a LGPD. Detalhes de base legal, retenção e controlador permanecem pendentes (**TBC-08**).
- **Regulatórios/éticos:** verificar orientações institucionais aplicáveis; nenhuma aprovação foi registrada.

## 3. Requisitos organizacionais

- **Operacionais:** autenticação institucional e acesso a dados acadêmicos dependem de autorização e integração (**TBC-02**).
- **Desenvolvimento e ambiente:** tecnologias e infraestrutura mostradas na UML são propostas, não decisões institucionais aprovadas.

## 4. Checklist LAPIS

- [x] Identificadores RNF01–RNF09 preservados e classificados por categoria.
- [x] Referências à SRS e às fontes de pendências mantidas.
- [ ] Aferir métricas de carga, tempo, disponibilidade e recuperação.
- [ ] Confirmar metas e critérios de verificação com os responsáveis.
- [ ] Revisar conformidade com LGPD, acessibilidade e política institucional.
- [ ] Revisar em pares e registrar validação.

## 5. Referências

- [SRS](../Especificacao/SRS.md)
- [Matriz de rastreabilidade](../Validacao/Rastreabilidade.md)
- [Premissas e fontes](../Artefatos/Premissas-Decisoes-e-Fontes.md)
