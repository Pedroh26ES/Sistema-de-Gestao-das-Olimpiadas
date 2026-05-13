<h1 align="center">Sistema de Gestão das Olimpíadas</h1>

<p align="center">
  <strong>SGO - Modelagem UML para gestão de competições, atletas, locais, resultados e medalhas olímpicas.</strong>
</p>

<p align="center">
  <img alt="Projeto de Software" src="https://img.shields.io/badge/Projeto%20de%20Software-SGO-1f6feb">
  <img alt="UML" src="https://img.shields.io/badge/UML-Diagramas-2ea043">
  <img alt="PlantUML" src="https://img.shields.io/badge/PlantUML-Modelagem-f97316">
  <img alt="Status" src="https://img.shields.io/badge/Status-Completo-8250df">
</p>

---

## Visão geral

O **Sistema de Gestão das Olimpíadas (SGO)** foi modelado para apoiar a organização de eventos olímpicos, permitindo controlar competições, inscrições de atletas, alocação de locais, registro de resultados e relatórios de medalhas por país.

Este repositório contém os diagramas UML solicitados no trabalho da disciplina **Projeto de Software**, com os arquivos de origem em **PlantUML** e as respectivas imagens em PNG.

## Nome

| Integrantes |
| --- |
| Nome do aluno 1 |
| Nome do aluno 2 |

## Entregáveis

| Item | Descrição | Arquivo |
| --- | --- | --- |
| Caso de Uso | Atores e principais funcionalidades do SGO. | [`diagrama-de-caso-de-uso.puml`](codigos/diagrama-de-caso-de-uso.puml) |
| Classes | Diagrama de classes de projeto com fronteira, controle, domínio e persistência. | [`diagrama-de-classes.puml`](codigos/diagrama-de-classes.puml) |
| Pacotes | Organização lógica do sistema em responsabilidades. | [`diagrama-de-pacotes.puml`](codigos/diagrama-de-pacotes.puml) |
| Componentes | Arquitetura em serviços, API, bancos, filas e workers. | [`diagrama-de-componentes.puml`](codigos/diagrama-de-componentes.puml) |
| Implantação | Distribuição física em infraestrutura de nuvem. | [`diagrama-de-implantação.puml`](codigos/diagrama-de-implantação.puml) |

## Regras de negócio

| Código | Regra | Descrição |
| --- | --- | --- |
| RN01 | Cadastro de competições | O sistema deve permitir cadastrar competições com modalidade, data, horário, local e lista de atletas inscritos. |
| RN02 | Inscrição de atletas | Atletas de diferentes países podem se inscrever em competições específicas. Cada atleta pode participar de várias competições. |
| RN03 | Representação por país | Um atleta só pode representar um país em cada modalidade. |
| RN04 | Alocação de locais | Um local só pode receber uma competição por vez, evitando conflitos de horário. |
| RN05 | Controle de resultados | Após a realização da competição, devem ser registrados ouro, prata e bronze. |
| RN06 | Relatório de medalhas | O sistema deve gerar relatórios de medalhas por país, consolidando ouro, prata e bronze. |

## Histórias de usuário

| ID | História |
| --- | --- |
| US01 | Como administrador do SGO, quero cadastrar competições com modalidade, data, horário, local e atletas inscritos, para organizar a agenda oficial das Olimpíadas. |
| US02 | Como administrador do SGO, quero atualizar os dados de uma competição, para corrigir informações de agenda, local ou modalidade quando necessário. |
| US03 | Como atleta, quero me inscrever em uma ou mais competições, para participar das modalidades nas quais estou apto. |
| US04 | Como sistema, quero validar que um atleta represente apenas um país por modalidade, para cumprir as regras de participação. |
| US05 | Como gestor de locais, quero alocar uma competição em um local disponível, para evitar conflitos de horário e uso do espaço. |
| US06 | Como usuário do sistema, quero consultar a agenda de competições, para acompanhar datas, horários, locais e modalidades. |
| US07 | Como oficial de competição, quero registrar o resultado final de uma competição, para definir os atletas classificados em primeiro, segundo e terceiro lugares. |
| US08 | Como comitê olímpico, quero gerar relatórios de medalhas por país, para acompanhar o desempenho das delegações. |
| US09 | Como usuário do sistema, quero consultar o quadro de medalhas, para visualizar a classificação geral por ouro, prata e bronze. |
| US10 | Como comitê olímpico, quero exportar relatórios em arquivo, para divulgar e arquivar os resultados oficiais. |

## Diagramas UML

### Diagrama de Caso de Uso

Representa os atores do SGO e suas interações com os principais casos de uso, como cadastrar competição, inscrever atleta, alocar local, registrar resultados e consultar medalhas.

<p align="center">
  <img width="100%" src="imagens/diagrama-de-caso-de-uso.png" alt="Diagrama de Caso de Uso">
</p>

Arquivo PlantUML: [`codigos/diagrama-de-caso-de-uso.puml`](codigos/diagrama-de-caso-de-uso.puml)

### Diagrama de Classes

Modela o SGO como um **Diagrama de Classes de Projeto**, separando classes de fronteira, controle, domínio e persistência. Inclui entidades, interfaces, atributos, operações, multiplicidades e navegabilidade.

<p align="center">
  <img width="100%" src="imagens/diagrama-de-classes.png" alt="Diagrama de Classes">
</p>

Arquivo PlantUML: [`codigos/diagrama-de-classes.puml`](codigos/diagrama-de-classes.puml)

### Diagrama de Pacotes

Organiza o sistema em pacotes responsáveis por apresentação, aplicação, domínio, persistência e infraestrutura.

<p align="center">
  <img width="100%" src="imagens/diagrama-de-pacotes.png" alt="Diagrama de Pacotes">
</p>

Arquivo PlantUML: [`codigos/diagrama-de-pacotes.puml`](codigos/diagrama-de-pacotes.puml)

### Diagrama de Componentes

Demonstra a arquitetura de componentes do SGO com navegador, API central, serviços independentes, bancos AWS por serviço, filas SQS e workers para processamento assíncrono.

<p align="center">
  <img width="100%" src="imagens/diagrama-de-componentes.png" alt="Diagrama de Componentes">
</p>

Arquivo PlantUML: [`codigos/diagrama-de-componentes.puml`](codigos/diagrama-de-componentes.puml)

### Diagrama de Implantação

Apresenta a distribuição física da solução em infraestrutura de nuvem, incluindo dispositivos dos usuários, CloudFront, API Gateway, Load Balancer, VPC, sub-redes, cluster de aplicação, banco de dados, filas, armazenamento, observabilidade, notificações e backup.

<p align="center">
  <img width="100%" src="imagens/diagrama-de-implantação.png" alt="Diagrama de Implantação">
</p>

Arquivo PlantUML: [`codigos/diagrama-de-implantação.puml`](codigos/diagrama-de-implantação.puml)

## Estrutura do repositório

```text
.
+-- README.md
+-- codigos
|   +-- diagrama-de-caso-de-uso.puml
|   +-- diagrama-de-classes.puml
|   +-- diagrama-de-componentes.puml
|   +-- diagrama-de-implantação.puml
|   +-- diagrama-de-pacotes.puml
+-- imagens
    +-- diagrama-de-caso-de-uso.png
    +-- diagrama-de-classes.png
    +-- diagrama-de-componentes.png
    +-- diagrama-de-implantação.png
    +-- diagrama-de-pacotes.png
```

## Ferramenta utilizada

Os diagramas foram modelados com **PlantUML**, conforme solicitado no enunciado do trabalho.

Links úteis:

- [PlantUML](https://plantuml.com/)
- [Guia PlantUML](https://plantuml.com/guide)

---

<p align="center">
  <strong>Trabalho de Projeto de Software</strong><br>
  Sistema de Gestão das Olimpíadas
</p>
