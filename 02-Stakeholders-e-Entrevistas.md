# 👥 Stakeholders e Elicitação de Requisitos

> **Atenção:** este documento separa o que é **hipótese** do que é **confirmado**. Um achado só passa a "confirmado" depois de registrado na seção 6 (data, entrevistado e evidência).

---

## 1. Introdução
Mapeia as partes interessadas do Sistema de Apoio à Internacionalização da Unifor e organiza o planejamento e o registro das técnicas de elicitação: análise documental, entrevistas com o NEI e questionários com estudantes.

---

## 2. Mapa de stakeholders

| ID | Stakeholder | Tipo | Interesse e necessidades | Como será envolvido | Contato |
| :-: | :--- | :--- | :--- | :--- | :-: |
| S01 | Estudantes de graduação (candidatos) | Direto | Transparência nos editais, facilidade para achar destinos, acompanhamento da candidatura | Questionário e entrevistas | ⬜ |
| S02 | Equipe do NEI (gestores) | Direto | Automatizar a análise de elegibilidade, gerir convênios e editais, emitir relatórios | Entrevista semiestruturada e validação | ⬜ |
| S03 | Alunos estrangeiros (incoming) | Direto | Apoio de integração e ambientação | Questionário curto (opcional) | ⬜ |
| S04 | Ex-intercambistas | Direto | Compartilhar experiências, mentoria | Entrevista ou questionário | ⬜ |
| S05 | Coordenadores de curso | Indireto | Acompanhar alunos em mobilidade, validar equivalência e aproveitamento de créditos | Entrevista | ⬜ |
| S06 | Professores e pesquisadores | Indireto | Cooperações e coorientações internacionais | Análise documental | ⬜ |
| S07 | Administração superior | Indireto | Indicadores de internacionalização | Relatórios (RF13) | ⬜ |
| S08 | TI / Secretaria acadêmica | Indireto | Fonte dos dados acadêmicos e autorização de integração (TBC-02) | Entrevista técnica | ⬜ |
| S09 | Professor da disciplina | Validador | Valida o escopo e a qualidade da especificação | Reuniões de acompanhamento | ⬜ |

Legenda de contato: ⬜ não realizado · 🟡 agendado · ✅ realizado.

---

## 3. Técnicas de elicitação

1. **Análise documental:** editais anteriores do NEI, páginas institucionais, regulamentos de mobilidade e portais de outras universidades.
2. **Entrevistas semiestruturadas:** gestores do NEI, coordenadores de curso e TI.
3. **Questionário eletrônico:** amostra de estudantes de graduação.

---

## 4. Roteiro de entrevistas

### 4.1 Equipe do NEI (S02)
* **Q1.** Como é feita hoje a divulgação de editais e a gestão dos convênios?
* **Q2.** Quais são os maiores gargalos na validação manual dos pré-requisitos (média, percentual concluído, reprovações)?
* **Q3.** A restrição de reprovações vale para todo o histórico ou só para o semestre anterior? (TBC-01)
* **Q4.** Quais documentos são exigidos em cada edital e quem define os critérios de pontuação? (TBC-03, TBC-04)
* **Q5.** Quem é responsável por atualizar convênios, editais e conteúdos de orientação? (TBC-05)
* **Q6.** Como é feito o acompanhamento de quem está no exterior e o registro do pós-intercâmbio?
* **Q7.** Qual a relação entre o NEI e a DRI nos serviços de internacionalização? (TBC-06)
* **Q8.** Há restrições sobre quais dados dos alunos podem ser exibidos ou compartilhados? (TBC-08)

### 4.2 Coordenadores de curso (S05)
* **Q1.** Como é feita hoje a análise de equivalência de disciplinas após o intercâmbio?
* **Q2.** Que informações o coordenador precisa ver para pré-validar o plano de estudos?

### 4.3 TI / Secretaria acadêmica (S08)
* **Q1.** De onde vêm média global, percentual concluído e situação de reprovações, e como o sistema pode acessá-los? (TBC-02)
* **Q2.** Existe login institucional (SSO) que o portal possa usar?

### 4.4 Estudantes (S01)
* **Q1.** Onde você encontra dificuldade para localizar um destino compatível com seu curso?
* **Q2.** O processo de preparação documental (idioma, visto, planejamento financeiro) é claro?
* **Q3.** Que informação você sentiu falta ao pensar em fazer intercâmbio?
* **Q4.** Qual a importância de ter um canal com ex-intercambistas?
* **Q5.** Você usaria o portal pelo celular? Para quais tarefas?

### 4.5 Ex-intercambistas (S04)
* **Q1.** Que informação teria facilitado a sua preparação?
* **Q2.** Você compartilharia seu relato? Que cuidados de privacidade esperaria? (TBC-07)

---

## 5. Hipóteses iniciais (a validar)

Resultado da síntese preliminar do grupo. **Ainda não há registro de evidência no repositório**; por isso são tratadas como hipóteses.

| ID | Hipótese | Requisitos relacionados | Status |
| :-: | :--- | :--- | :-: |
| H01 | A informação sobre editais e convênios é fragmentada e gera desinformação e sobrecarga de atendimento no NEI | RF02, RF06, RF07 | A validar |
| H02 | A verificação de elegibilidade feita à mão causa erros e retrabalho; deve ser automatizada | RF03, RN01 | A validar |
| H03 | Há demanda por preparação linguística e cultural e por mentoria com ex-alunos | RF10, RF14 | A validar |

---

## 6. Registro de entrevistas e questionários

> Preencher **uma linha por atividade realizada**. Anexar notas, áudio autorizado ou formulário em `Requisitos/evidencias/` (criar a pasta) e informar o caminho.

| ID | Data | Técnica | Stakeholder (perfil) | Responsável do grupo | Principais achados | Requisitos derivados | Evidência |
| :-: | :-: | :--- | :--- | :--- | :--- | :--- | :--- |
| E01 | _a preencher_ | Entrevista | NEI | | | | |
| E02 | _a preencher_ | Entrevista | Coordenador de curso | | | | |
| Q01 | _a preencher_ | Questionário | Estudantes (n = ?) | | | | |

---

## 7. Resultados confirmados

_Nenhum resultado confirmado até o momento._ Mover para cá as hipóteses da seção 5 que forem validadas, citando o ID do registro da seção 6 (por exemplo: "H02 confirmada em E01").
