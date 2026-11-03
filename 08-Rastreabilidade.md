# 🔗 Matriz de Rastreabilidade

Relaciona cada requisito funcional à história de usuário, ao caso de uso, às regras de negócio e à tela do protótipo.

| RF | Requisito | Prior. | US | UC | RN | Tela (doc. 06) |
| :-: | :--- | :-: | :-: | :-: | :-: | :-: |
| RF01 | Autenticação e perfis de acesso | M | US15 | todos | RN08 | — |
| RF02 | Consulta de oportunidades | M | US01 | UC01 | — | T1 |
| RF03 | Validação de elegibilidade | M | US02 | UC02 | RN01 | T2 |
| RF04 | Submissão de candidatura | M | US03 | UC03 | RN01, RN02, RN04, RN06 | T3 |
| RF05 | Acompanhamento de candidaturas | M | US12 | UC04 | — | T4 |
| RF06 | Gestão de convênios | M | US04 | UC06 | — | T6 |
| RF07 | Gestão de editais | M | US04 | UC07 | RN02 | T6 |
| RF08 | Triagem e decisão de candidaturas | M | US05 | UC08 | RN03 | T5 |
| RF09 | Notificações de status | S | US08 | UC12 | — | T4 |
| RF10 | Central de preparação | S | US06 | UC05 | — | — |
| RF11 | Gestão de bolsas e vagas | S | US13 | UC09 | RN03 | T5 |
| RF12 | Aproveitamento de créditos | S | US07 | UC11 | RN05 | — |
| RF13 | Relatórios e indicadores | S | US14 | UC10 | RN08 | — |
| RF14 | Relatos de experiência | C | US09, US16 | UC13, UC14 | RN07 | — |
| RF15 | Sistema Tandem | C | US10 | UC15 | RN08 | — |
| RF16 | Fórum e agenda de eventos | W | US17 | — | — | — |
| RF17 | Integração com agências e hospedagem | W | US11 | — | — | — |

## Requisitos não funcionais por área

| RNF | Impacta principalmente |
| :-: | :--- |
| RNF01 (LGPD), RNF06 (auditoria) | RF01, RF03, RF04, RF08, RF13 |
| RNF02 (responsividade), RNF05 (acessibilidade), RNF07 (usabilidade) | Todas as telas |
| RNF03 (disponibilidade), RNF04 (desempenho) | RF02, RF04 |
| RNF08 (backup) | RF04 e demais dados persistidos |
| RNF09 (idioma) | Todas as telas (evolução) |
