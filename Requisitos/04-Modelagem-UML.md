📐 Modelagem UML — Sistema de Apoio à Internacionalização

1. Introdução

Este documento contempla os diagramas estruturais e comportamentais em UML para o Sistema de Apoio à Internacionalização da Universidade de Fortaleza (Unifor). Os modelos representam os atores do sistema, os fluxos de casos de uso, a arquitetura de componentes e a topologia de implantação física e lógica da solução.

2. Diagrama de Casos de Uso

O Diagrama de Casos de Uso ilustra as principais interações entre os atores (Estudante, Gestor do NEI e Coordenador de Curso) e os módulos funcionais do sistema.

2.1 Especificação dos Atores

Estudante de Graduação: Usuário final que busca oportunidades, realiza autoavaliação, submete candidaturas e acessa o módulo pós-intercâmbio.

Gestor do NEI: Administrador responsável pelo cadastro de convênios, publicação de editais, análise de candidaturas e emissão de relatórios.

Coordenador de Curso: Docente responsável por acompanhar a equivalência curricular e validar o aproveitamento de disciplinas.

2.2 Diagrama Mermaid

graph TD
    actorEstudante[Estudante de Graduação]
    actorNEI[Gestor do NEI]
    actorCoord[Coordenador de Curso]

    subgraph Sistema de Apoio à Internacionalização
        UC01(Consultar Oportunidades & Convênios)
        UC02(Realizar Autoavaliação de Elegibilidade)
        UC03(Submeter Candidatura a Edital)
        UC04(Acessar Central de Preparação)
        UC05(Participar do Sistema Tandem)
        UC06(Cadastrar Convênios e Editais)
        UC07(Analisar Candidaturas)
        UC08(Gerir Bolsas e Vagas)
        UC09(Validar Aproveitamento de Créditos)
        UC10(Publicar Relato de Experiência)
    end

    actorEstudante --> UC01
    actorEstudante --> UC02
    actorEstudante --> UC03
    actorEstudante --> UC04
    actorEstudante --> UC05
    actorEstudante --> UC10

    actorNEI --> UC06
    actorNEI --> UC07
    actorNEI --> UC08

    actorCoord --> UC09


3. Diagrama de Componentes

O Diagrama de Componentes descreve a organização dos módulos de software, serviços e interfaces que compõem a arquitetura do sistema web/mobile.

3.1 Descrição dos Componentes

Portal Frontend (Web/Mobile): Interface de usuário responsiva construída para consumo das APIs.

API Gateway & Autenticação: Ponto de entrada unificado que gerencia permissões e acesso aos serviços.

Módulo de Elegibilidade: Serviço de regras de negócio responsável por validar histórico e notas acadêmicas.

Módulo de Candidaturas: Serviço que controla os status das inscrições e upload de documentos.

Módulo de Convênios & Editais: Serviço administrativo de gestão de dados institucionais.

Serviço de Comunicação (Tandem/Fórum): Módulo colaborativo de mentoria e troca de idiomas.

3.2 Diagrama Mermaid

graph LR
    subgraph Camada de Apresentação
        WebClient[Portal Web / Mobile]
    end

    subgraph Camada de Serviços / API Gateway
        Gateway[API Gateway & Auth Service]
    end

    subgraph Camada de Negócio
        ModElegibilidade[Serviço de Elegibilidade]
        ModCandidatura[Serviço de Candidaturas]
        ModConvenio[Serviço de Convênios e Editais]
        ModColaborativo[Serviço Colaborativo & Tandem]
    end

    subgraph Camada de Dados
        DB[(Base de Dados Relacional)]
        Storage[(Armazenamento de Arquivos / PDF)]
    end

    WebClient --> Gateway
    Gateway --> ModElegibilidade
    Gateway --> ModCandidatura
    Gateway --> ModConvenio
    Gateway --> ModColaborativo

    ModElegibilidade --> DB
    ModCandidatura --> DB
    ModCandidatura --> Storage
    ModConvenio --> DB
    ModColaborativo --> DB


4. Diagrama de Implantação

O Diagrama de Implantação descreve a infraestrutura física e lógica onde a aplicação e suas dependências serão executadas.

4.1 Descrição da Infraestrutura

Dispositivo do Cliente: Navegadores web em computadores e dispositivos móveis acessando via HTTPS.

Servidor Web / Load Balancer: Responsável por balancear a carga de requisições de entrada.

Servidor de Aplicação (App Server): Ambiente isolado (ex: containers Docker) executando as regras de negócio em segundo plano.

Servidor de Banco de Dados: Instância dedicada para persistência de dados acadêmicos e tabelas institucionais.

Servidor de Armazenamento em Nuvem: Repositório seguro para guarda dos comprovantes e documentos anexados.

4.2 Diagrama Mermaid

graph TD
    subgraph Dispositivo do Cliente
        ClientDevice[Navegador / App Mobile]
    end

    subgraph Infraestrutura em Nuvem
        LoadBalancer[Servidor Web / Load Balancer HTTPS]
        
        subgraph Servidor de Aplicação
            AppServer[Container de Serviços Backend]
        end

        subgraph Camada de Persistência
            DatabaseNode[(Servidor PostgreSQL)]
            StorageNode[(Cloud File Storage)]
        end
    end

    ClientDevice -->|HTTPS / REST API| LoadBalancer
    LoadBalancer --> AppServer
    AppServer -->|SQL / TCP| DatabaseNode
    AppServer -->|API S3/Blob| StorageNode
