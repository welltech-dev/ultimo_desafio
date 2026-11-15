# 🚀 Executando Tarefas Automatizadas com AWS Lambda e Amazon S3

## 📌 Sobre o Projeto

Este repositório foi desenvolvido como parte do desafio prático da formação **AWS Cloud Foundations**, oferecida pela [DIO](https://www.dio.me/).

O objetivo deste laboratório é consolidar os conhecimentos sobre automação de tarefas utilizando serviços da AWS, com foco na integração entre **AWS Lambda** e **Amazon S3**.

Durante o desenvolvimento, a proposta é compreender como eventos relacionados ao armazenamento de objetos no S3 podem acionar funções Lambda automaticamente, permitindo executar processos sem a necessidade de gerenciamento de servidores.

Este repositório reúne anotações técnicas, procedimentos, configurações, testes e aprendizados adquiridos durante a realização do laboratório.

---

## 🎯 Objetivos de Aprendizagem

- Compreender o funcionamento do AWS Lambda.
- Conhecer os recursos e funcionalidades do Amazon S3.
- Entender a integração entre eventos do S3 e funções Lambda.
- Automatizar tarefas a partir de eventos de armazenamento.
- Compreender permissões e políticas necessárias para a comunicação entre serviços AWS.
- Explorar a infraestrutura como código utilizando AWS CloudFormation.
- Documentar procedimentos técnicos e compartilhar conhecimentos utilizando GitHub.

---

## ☁️ Serviços AWS Utilizados

### 1. Amazon S3 (Simple Storage Service)

Serviço de armazenamento de objetos da AWS, utilizado para armazenar arquivos de forma escalável, segura e durável.

Principais conceitos estudados:

- Criação e configuração de buckets.
- Armazenamento de objetos.
- Organização de arquivos.
- Eventos de notificação do S3.
- Permissões de acesso aos recursos.

### 2. AWS Lambda

Serviço de computação serverless que permite executar códigos em resposta a eventos, sem a necessidade de provisionar ou administrar servidores.

Principais conceitos estudados:

- Criação de funções Lambda.
- Configuração do ambiente de execução.
- Manipulação de eventos.
- Integração com serviços AWS.
- Execução automatizada de tarefas.
- Monitoramento e análise de logs.

### 3. AWS CloudFormation

Serviço de infraestrutura como código (IaC), utilizado para provisionar e gerenciar recursos AWS por meio de templates declarativos.

Conceitos relacionados:

- Templates YAML e JSON.
- Criação de stacks.
- Definição de recursos.
- Configuração de propriedades.
- Automatização da infraestrutura.

---

## 🏗️ Arquitetura e Funcionamento

A proposta do laboratório é trabalhar com uma arquitetura orientada a eventos (*Event-Driven Architecture*).

Fluxo conceitual da automação:

1. Um arquivo é enviado para um bucket do Amazon S3.
2. O S3 identifica o evento configurado, como o envio de um novo objeto.
3. O evento aciona a função AWS Lambda.
4. A função Lambda recebe os dados do evento.
5. O código executa a tarefa automatizada definida no laboratório.
6. A execução pode ser acompanhada por meio dos logs do Amazon CloudWatch.

### Fluxo da automação

```text
       USUÁRIO / APLICAÇÃO
                |
                v
        AMAZON S3 BUCKET
                |
                v
       EVENT NOTIFICATION
                |
                v
          AWS LAMBDA
                |
                v
       EXECUÇÃO DA FUNÇÃO
                |
                v
       AMAZON CLOUDWATCH
          (LOGS)
```

*Observação: o fluxo acima representa a arquitetura conceitual de uma automação baseada em eventos S3 e Lambda. A implementação efetiva deve refletir os recursos e configurações utilizados durante o laboratório.*

---

## 🧪 Desenvolvimento do Laboratório

Nesta seção serão documentadas as etapas realizadas durante a prática.

### Etapa 1 — Preparação do ambiente

- Acompanhamento das vídeo-aulas da formação.
- Revisão dos conceitos de armazenamento e computação serverless.
- Preparação do ambiente de desenvolvimento.
- Organização dos arquivos e documentação do projeto.

### Etapa 2 — Configuração do Amazon S3

Registrar nesta etapa:

- Criação do bucket.
- Configurações realizadas.
- Propriedades de armazenamento.
- Permissões e políticas aplicadas.
- Configuração dos eventos de notificação, quando aplicável.

### Etapa 3 — Configuração do AWS Lambda

Registrar nesta etapa:

- Criação da função Lambda.
- Linguagem de programação utilizada.
- Configuração do runtime.
- Código implementado.
- Permissões IAM necessárias.
- Configuração do acionamento pela integração com S3.

### Etapa 4 — Integração entre S3 e Lambda

Documentar:

- Como foi estabelecida a comunicação entre os serviços.
- Qual evento foi configurado.
- Como os dados do evento são recebidos pela função.
- Qual tarefa automatizada foi executada.
- Quais testes foram realizados.

### Etapa 5 — Testes e validação

Registrar os resultados obtidos:

- Testes de envio de objetos ao S3.
- Verificação do acionamento da função Lambda.
- Análise dos resultados da execução.
- Consulta aos logs no CloudWatch.
- Identificação e correção de possíveis erros.

---

## 🔐 Segurança e Permissões

Durante a implementação de arquiteturas AWS, é importante observar o princípio do menor privilégio (*Principle of Least Privilege*).

Alguns pontos importantes:

- Utilizar políticas IAM específicas para cada função.
- Evitar permissões administrativas desnecessárias.
- Restringir o acesso aos buckets.
- Configurar corretamente as permissões de execução da Lambda.
- Não armazenar credenciais ou chaves de acesso diretamente no código.
- Não publicar arquivos contendo informações sensíveis no GitHub.

---

## 📂 Estrutura do Repositório

```text
ultimo_desafio/
│
├── README.md
│
├── docs/
│   ├── conceitos-aws.md
│   ├── amazon-s3.md
│   ├── aws-lambda.md
│   ├── integracao-s3-lambda.md
│   └── cloudformation.md
│
├── templates/
│   └── cloudformation/
│       └── template.yaml
│
├── lambda/
│   └── function.py
│
└── images/
    ├── arquitetura.png
    ├── s3-bucket.png
    ├── lambda-function.png
    └── testes.png
```

*Estrutura sugerida. Os diretórios e arquivos podem ser adaptados conforme os materiais efetivamente produzidos no laboratório.*

---

## 📚 Principais Aprendizados

Este laboratório permite aprofundar conhecimentos importantes para o desenvolvimento de soluções em nuvem:

- Arquitetura serverless e seus benefícios.
- Integração entre serviços gerenciados da AWS.
- Processamento orientado a eventos.
- Automação de tarefas utilizando funções Lambda.
- Armazenamento de objetos com Amazon S3.
- Gerenciamento de permissões e segurança com IAM.
- Infraestrutura como código com CloudFormation.
- Monitoramento de aplicações e análise de logs.
- Versionamento e documentação técnica utilizando Git e GitHub.

---

## 🛠️ Tecnologias e Ferramentas

| Tecnologia | Finalidade |
|---|---|
| AWS Lambda | Execução de funções serverless |
| Amazon S3 | Armazenamento de objetos |
| AWS CloudFormation | Infraestrutura como código |
| AWS IAM | Gerenciamento de identidades e permissões |
| Amazon CloudWatch | Monitoramento e logs |
| Python | Desenvolvimento de funções, quando utilizado |
| Git | Controle de versão |
| GitHub | Hospedagem e documentação do projeto |
| LocalStack | Simulação local de serviços AWS, quando utilizado |

---

## 📖 Referências e Documentação

- [AWS Lambda – Documentação oficial](https://docs.aws.amazon.com/lambda/)
- [Amazon S3 – Documentação oficial](https://docs.aws.amazon.com/s3/)
- [AWS CloudFormation – Documentação oficial](https://docs.aws.amazon.com/cloudformation/)
- [AWS IAM – Documentação oficial](https://docs.aws.amazon.com/iam/)
- [Amazon CloudWatch – Documentação oficial](https://docs.aws.amazon.com/cloudwatch/)
- [AWS S3 Object Lambda – Documentação](https://docs.aws.amazon.com/AmazonS3/latest/userguide/transforming-objects.html)
- [GitHub Markdown](https://docs.github.com/pt/get-started/writing-on-github)

---

## 👨‍💻 Autor

**Wellington Pereira**

Estudante de Tecnologia | Python | AWS Cloud | Automação e DevOps

GitHub: [@welltech-dev](https://github.com/welltech-dev)

---

## 🏁 Considerações Finais

Este projeto representa mais uma etapa na construção de conhecimentos práticos em computação em nuvem, automação e infraestrutura AWS.

A utilização conjunta de serviços como Amazon S3 e AWS Lambda demonstra como é possível desenvolver soluções automatizadas, escaláveis e orientadas a eventos, reduzindo a necessidade de gerenciamento de infraestrutura.

A documentação deste laboratório também faz parte do processo de aprendizagem, permitindo registrar procedimentos, organizar conhecimentos e construir um portfólio técnico para projetos futuros.

**Aprender, implementar, documentar e evoluir.**
