# 📐 Modelagem UML: Sistema de Apoio à Internacionalização

Os diagramas usam [Mermaid](https://mermaid.js.org/) e são renderizados diretamente no GitHub. O Mermaid não possui diagrama de atividades nativo; por isso o diagrama de atividades da seção 6 é representado como fluxograma com decisões.

| # | Diagrama | Seção |
| :-: | :--- | :-: |
| 1 | Casos de uso | 2 |
| 2 | Especificação de casos de uso | 3 |
| 3 | Classes | 4 |
| 4 | Sequência: submissão de candidatura | 5 |
| 5 | Atividades: processo de seleção | 6 |
| 6 | Estados: candidatura e edital | 7 |
| 7 | Componentes | 8 |
| 8 | Implantação | 9 |

---

## 1. Introdução
Os modelos representam os atores, os fluxos de casos de uso, a estrutura de dados, o comportamento do processo seletivo e a arquitetura sugerida da solução. Eles derivam dos requisitos da [SRS](03-Especificacao-SRS.md) e podem ser rastreados na [matriz de rastreabilidade](08-Rastreabilidade.md).

---

## 2. Diagrama de casos de uso

### 2.1 Atores

| Ator | Descrição |
| :--- | :--- |
| **Estudante** | Estudante de graduação que busca oportunidades, candidata-se e acompanha o processo. Quando ex-intercambista, publica relatos. |
| **Aluno estrangeiro (incoming)** | Estudante de instituição parceira; participa do Tandem. |
| **Gestor do NEI** | Cadastra convênios e editais, analisa candidaturas, gerencia bolsas, modera relatos e emite relatórios. |
| **Coordenador de curso** | Valida a equivalência de disciplinas e o aproveitamento de créditos. |
| **Sistema acadêmico** (ator secundário) | Fonte dos dados acadêmicos usados na elegibilidade (**TBC-02**). |

### 2.2 Diagrama

```mermaid
flowchart LR
    est["👤 Estudante"]
    inc["👤 Aluno estrangeiro"]
    nei["👤 Gestor do NEI"]
    coord["👤 Coordenador de curso"]
    acad["🖥️ Sistema acadêmico"]

    subgraph sistema["Sistema de Apoio à Internacionalização"]
        UC01(["UC01 Consultar oportunidades e convênios"])
        UC02(["UC02 Realizar autoavaliação de elegibilidade"])
        UC03(["UC03 Submeter candidatura a edital"])
        UC04(["UC04 Acompanhar candidaturas"])
        UC05(["UC05 Acessar central de preparação"])
        UC06(["UC06 Gerir convênios"])
        UC07(["UC07 Gerir editais"])
        UC08(["UC08 Analisar candidaturas"])
        UC09(["UC09 Gerir bolsas e vagas"])
        UC10(["UC10 Emitir relatórios"])
        UC11(["UC11 Validar aproveitamento de créditos"])
        UC12(["UC12 Notificar mudança de status"])
        UC13(["UC13 Publicar relato de experiência"])
        UC14(["UC14 Moderar relatos"])
        UC15(["UC15 Participar do Tandem"])
    end

    est --- UC01
    est --- UC02
    est --- UC03
    est --- UC04
    est --- UC05
    est --- UC13
    est --- UC15
    inc --- UC15

    nei --- UC06
    nei --- UC07
    nei --- UC08
    nei --- UC09
    nei --- UC10
    nei --- UC14

    coord --- UC11

    UC02 --- acad
    UC03 -. include .-> UC02
    UC08 -. include .-> UC12
```

---

## 3. Especificação dos principais casos de uso

### UC02: Realizar autoavaliação de elegibilidade
| Campo | Descrição |
| :--- | :--- |
| **Ator principal** | Estudante |
| **Ator secundário** | Sistema acadêmico |
| **Requisitos** | RF03 · RN01 · US02 |
| **Pré-condição** | Estudante autenticado. |
| **Fluxo principal** | 1. O estudante solicita a autoavaliação. 2. O sistema obtém matrícula, percentual concluído, média e reprovações. 3. O sistema compara cada dado com os critérios da RN01. 4. O sistema exibe o resultado "Apto" com o valor de cada critério. |
| **Fluxo alternativo A** | No passo 4, algum critério não é atendido: o sistema exibe "Não apto" e os critérios não atendidos com o valor do estudante e o exigido. |
| **Fluxo de exceção** | No passo 2, a fonte de dados está indisponível: o sistema informa a falha e orienta a tentar novamente ou procurar o NEI. |
| **Pós-condição** | A data e o resultado da avaliação ficam registrados. |

### UC03: Submeter candidatura a edital
| Campo | Descrição |
| :--- | :--- |
| **Ator principal** | Estudante |
| **Requisitos** | RF04 · RN01 · RN02 · RN04 · RN06 · US03 |
| **Pré-condição** | Estudante autenticado; edital publicado e dentro do prazo. |
| **Fluxo principal** | 1. O estudante escolhe o edital e seleciona "Candidatar-se". 2. O sistema executa UC02 e confirma que o estudante é apto. 3. O sistema exibe o formulário e a lista de documentos exigidos. 4. O estudante preenche os campos e anexa os PDFs. 5. O estudante confirma o envio. 6. O sistema valida prazo e documentos, registra a candidatura com status "Enviada" e gera o protocolo. 7. O sistema notifica o estudante (UC12). |
| **Fluxo alternativo A** | No passo 2, o estudante é inapto: o sistema exibe os motivos e encerra o caso de uso. |
| **Fluxo alternativo B** | No passo 4, o estudante salva o formulário sem enviar: a candidatura fica como "Rascunho". |
| **Fluxo de exceção** | No passo 6, falta documento obrigatório ou o prazo expirou: o sistema bloqueia o envio e informa a pendência. |
| **Pós-condição** | Candidatura registrada com protocolo e status "Enviada". |

### UC08: Analisar candidaturas
| Campo | Descrição |
| :--- | :--- |
| **Ator principal** | Gestor do NEI |
| **Requisitos** | RF08 · RN03 · RNF06 · US05 |
| **Pré-condição** | Gestor autenticado; edital com candidaturas enviadas. |
| **Fluxo principal** | 1. O gestor seleciona um edital. 2. O sistema lista as candidaturas com o resultado da validação automática. 3. O gestor abre uma candidatura e confere os documentos. 4. O gestor registra a decisão: deferir, indeferir ou solicitar complementação. 5. O sistema registra autor, data e decisão e notifica o estudante (UC12). |
| **Fluxo alternativo A** | No passo 4, indeferimento sem justificativa: o sistema exige a justificativa antes de salvar. |
| **Fluxo alternativo B** | Ao deferir além do limite de vagas: o sistema bloqueia a atribuição (RN03). |
| **Pós-condição** | Candidatura com novo status e decisão registrada. |

---

## 4. Diagrama de classes

```mermaid
classDiagram
    class Usuario {
        <<abstract>>
        +UUID id
        +String nome
        +String emailInstitucional
        +autenticar()
    }
    class Estudante {
        +String matricula
        +String curso
        +Boolean incoming
    }
    class PerfilAcademico {
        +Boolean matriculaAtiva
        +Decimal percentualConcluido
        +Decimal mediaGlobal
        +Boolean possuiReprovacoes
        +Date dataAtualizacao
    }
    class GestorNEI {
        +String cargo
    }
    class CoordenadorCurso {
        +String curso
    }
    class InstituicaoParceira {
        +String nome
        +String pais
        +String idiomas
    }
    class Convenio {
        +Date vigenciaInicio
        +Date vigenciaFim
        +String areas
        +Integer vagasTotais
        +Boolean ativo
    }
    class Edital {
        +String titulo
        +Date prazoInscricao
        +String requisitos
        +String documentosExigidos
        +StatusEdital status
    }
    class Bolsa {
        +String nome
        +Decimal valor
        +Integer quantidade
    }
    class Candidatura {
        +String protocolo
        +Date dataEnvio
        +Decimal pontuacao
        +StatusCandidatura status
        +enviar()
        +cancelar()
    }
    class Documento {
        +String tipo
        +String nomeArquivo
        +String url
        +Date dataUpload
    }
    class AvaliacaoElegibilidade {
        +Date dataAvaliacao
        +Boolean apto
        +String motivos
    }
    class DecisaoCandidatura {
        +String tipo
        +String justificativa
        +Date data
    }
    class AproveitamentoCredito {
        +String disciplinaOrigem
        +String disciplinaEquivalente
        +String status
        +String parecer
    }
    class Notificacao {
        +String canal
        +String mensagem
        +Date dataEnvio
        +Boolean lida
    }
    class RelatoExperiencia {
        +String titulo
        +String texto
        +String statusModeracao
        +Date dataPublicacao
    }
    class PerfilTandem {
        +String idiomasOferecidos
        +String idiomasDesejados
    }
    class StatusCandidatura {
        <<enumeration>>
        RASCUNHO
        ENVIADA
        EM_ANALISE
        PENDENTE_DOCUMENTOS
        DEFERIDA
        INDEFERIDA
        SELECIONADA
        NAO_SELECIONADA
        CANCELADA
    }
    class StatusEdital {
        <<enumeration>>
        RASCUNHO
        PUBLICADO
        ENCERRADO
        CANCELADO
    }

    Usuario <|-- Estudante
    Usuario <|-- GestorNEI
    Usuario <|-- CoordenadorCurso
    Estudante "1" --> "1" PerfilAcademico : possui
    Estudante "1" --> "0..*" Candidatura : realiza
    Estudante "1" --> "0..*" RelatoExperiencia : escreve
    Estudante "1" --> "0..1" PerfilTandem : mantém
    InstituicaoParceira "1" --> "0..*" Convenio : firma
    Convenio "1" --> "0..*" Edital : origina
    Edital "1" --> "0..*" Bolsa : oferece
    Edital "1" --> "0..*" Candidatura : recebe
    Candidatura "1" *-- "1..*" Documento : contém
    Candidatura "1" --> "1" AvaliacaoElegibilidade : tem
    Candidatura "1" --> "0..*" DecisaoCandidatura : recebe
    Candidatura "1" --> "0..*" AproveitamentoCredito : gera
    GestorNEI "1" --> "0..*" DecisaoCandidatura : registra
    CoordenadorCurso "1" --> "0..*" AproveitamentoCredito : valida
    Usuario "1" --> "0..*" Notificacao : recebe
    RelatoExperiencia "0..*" --> "1" InstituicaoParceira : sobre
    Candidatura --> StatusCandidatura
    Edital --> StatusEdital
```

---

## 5. Diagrama de sequência: submissão de candidatura (UC03)

```mermaid
sequenceDiagram
    autonumber
    actor E as Estudante
    participant P as Portal Web/Mobile
    participant G as API Gateway e Autenticação
    participant EL as Serviço de Elegibilidade
    participant CA as Serviço de Candidaturas
    participant ST as Armazenamento de arquivos
    participant NT as Serviço de Notificações

    E->>P: Seleciona o edital e clica em Candidatar-se
    P->>G: Solicita verificação de elegibilidade
    G->>EL: verificarElegibilidade(estudante, edital)
    EL-->>P: Resultado (apto ou não apto, com motivos)
    alt Não apto (RN01)
        P-->>E: Exibe os critérios não atendidos
    else Apto
        P-->>E: Exibe formulário e documentos exigidos
        E->>P: Preenche, anexa os PDFs e confirma
        P->>G: enviarCandidatura(dados, arquivos)
        G->>CA: registrarCandidatura(dados, arquivos)
        CA->>CA: Valida prazo (RN02) e documentos (RN04)
        alt Validação falhou
            CA-->>P: Erro com as pendências
            P-->>E: Informa pendências
        else Validação ok
            CA->>ST: Armazena os documentos
            ST-->>CA: Referências dos arquivos
            CA-->>P: Protocolo e status Enviada
            CA->>NT: notificar(estudante, Enviada)
            P-->>E: Exibe o protocolo
        end
    end
```

---

## 6. Diagrama de atividades: processo de seleção

```mermaid
flowchart TD
    A([Início]) --> B["NEI publica o edital"]
    B --> C["Estudante consulta oportunidades e faz a autoavaliação"]
    C --> D{"Atende à RN01?"}
    D -- Não --> E["Sistema exibe os critérios não atendidos"]
    E --> Z([Fim])
    D -- Sim --> F["Estudante anexa documentos e envia a candidatura"]
    F --> G{"Dentro do prazo e com documentos completos?"}
    G -- Não --> H["Sistema bloqueia o envio e informa as pendências"]
    H --> F
    G -- Sim --> I["Candidatura registrada com status Enviada"]
    I --> J["NEI analisa a candidatura"]
    J --> K{"Decisão do NEI"}
    K -- Complementação --> L["Sistema solicita documentos e notifica o estudante"]
    L --> F
    K -- Indeferir --> M["Sistema registra a justificativa e notifica o estudante"]
    M --> Z
    K -- Deferir --> N{"Há vaga disponível no convênio?"}
    N -- Não --> O["Candidatura marcada como não selecionada"]
    O --> Z
    N -- Sim --> P["NEI atribui vaga ou bolsa e notifica o estudante"]
    P --> Q["Coordenador pré-valida disciplinas equivalentes"]
    Q --> Z
```

---

## 7. Diagramas de estados

### 7.1 Candidatura

```mermaid
stateDiagram-v2
    state "Em análise" as EmAnalise
    state "Pendente de documentos" as PendenteDocumentos
    state "Não selecionada" as NaoSelecionada

    [*] --> Rascunho
    Rascunho --> Enviada : enviar
    Rascunho --> Cancelada : cancelar
    Enviada --> EmAnalise : NEI inicia a análise
    Enviada --> Cancelada : estudante cancela
    EmAnalise --> PendenteDocumentos : solicitar complementação
    PendenteDocumentos --> EmAnalise : estudante reenvia documentos
    PendenteDocumentos --> Cancelada : prazo expirado ou cancelamento
    EmAnalise --> Deferida : deferir
    EmAnalise --> Indeferida : indeferir com justificativa
    Deferida --> Selecionada : vaga atribuída
    Deferida --> NaoSelecionada : sem vaga disponível
    Indeferida --> [*]
    Selecionada --> [*]
    NaoSelecionada --> [*]
    Cancelada --> [*]
```

### 7.2 Edital

```mermaid
stateDiagram-v2
    [*] --> Rascunho
    Rascunho --> Publicado : publicar
    Publicado --> Encerrado : prazo final atingido
    Publicado --> Cancelado : cancelar edital
    Rascunho --> Cancelado : descartar
    Encerrado --> [*]
    Cancelado --> [*]
```

---

## 8. Diagrama de componentes

Arquitetura **sugerida** em camadas. A escolha final de tecnologias não faz parte da especificação de requisitos.

```mermaid
graph LR
    subgraph apresentacao["Camada de apresentação"]
        WebClient["Portal Web / Mobile"]
    end

    subgraph servicos["Camada de serviços"]
        Gateway["API Gateway e Autenticação"]
    end

    subgraph negocio["Camada de negócio"]
        ModElegibilidade["Serviço de Elegibilidade"]
        ModCandidatura["Serviço de Candidaturas"]
        ModConvenio["Serviço de Convênios e Editais"]
        ModNotificacao["Serviço de Notificações"]
        ModColaborativo["Serviço Colaborativo e Tandem"]
        ModRelatorios["Serviço de Relatórios"]
    end

    subgraph dados["Camada de dados"]
        DB[("Banco de dados relacional")]
        Storage[("Armazenamento de arquivos")]
    end

    subgraph externos["Sistemas externos"]
        Acad["Sistema acadêmico da Unifor"]
        Email["Serviço de e-mail"]
    end

    WebClient --> Gateway
    Gateway --> ModElegibilidade
    Gateway --> ModCandidatura
    Gateway --> ModConvenio
    Gateway --> ModColaborativo
    Gateway --> ModRelatorios

    ModElegibilidade --> DB
    ModElegibilidade --> Acad
    ModCandidatura --> DB
    ModCandidatura --> Storage
    ModCandidatura --> ModNotificacao
    ModConvenio --> DB
    ModColaborativo --> DB
    ModRelatorios --> DB
    ModNotificacao --> Email
```

---

## 9. Diagrama de implantação

```mermaid
graph TD
    subgraph cliente["Dispositivo do cliente"]
        ClientDevice["Navegador ou app mobile"]
    end

    subgraph nuvem["Infraestrutura em nuvem"]
        LoadBalancer["Servidor web e balanceador HTTPS"]

        subgraph appsrv["Servidor de aplicação"]
            AppServer["Contêiner de serviços backend"]
        end

        subgraph persistencia["Camada de persistência"]
            DatabaseNode[("Servidor de banco de dados relacional")]
            StorageNode[("Armazenamento de arquivos na nuvem")]
        end
    end

    Acad["Sistema acadêmico da Unifor"]

    ClientDevice -->|HTTPS| LoadBalancer
    LoadBalancer --> AppServer
    AppServer -->|SQL| DatabaseNode
    AppServer -->|API de objetos| StorageNode
    AppServer -->|Integração - TBC-02| Acad
```
