# MedFlow

**Sistema de Gestão de Filas e Feedback para UBS**

---

## Sobre o Projeto

Este projeto foi desenvolvido para a disciplina de Usina de Projetos Experimentais I (UPX I). O nosso principal objetivo é desenvolver um sistema que permita aos pacientes acompanhar sua posição na fila da UBS e fornecer feedback sobre o atendimento.

A solução utiliza plataformas *low code/no code* para criar um Produto Mínimo Viável (MVP) que resolve um problema crônico de logística no atendimento público de saúde: a falta de previsibilidade nas filas e a escassez de dados estruturados para a gestão.

## Equipe Click Byte

Este projeto foi desenvolvido pelos alunos:

* Ana Laura
* Celso Toledo
* José Leonardo
* Márcia Regina
* Raphael do Santos
* Vítor Zan

## Funcionalidades do MVP e Tecnologias

Para alcançar nosso objetivo, implementaremos as seguintes funcionalidades:

* **Monitoramento:** Acompanhamento em tempo real da posição na fila para os pacientes.
* **Feedback do Usuário:** Sistema de avaliação ao final do atendimento sobre tempo de espera, infraestrutura, etc.

**Tecnologias Utilizadas:**

* **Plataforma de Desenvolvimento:** Figma (Protótipo Interativo / MVP)
* **Gestão do Projeto:** Metodologias Ágeis utilizando Trello

## Impacto Social (ODS)

O sistema busca humanizar o atendimento e otimizar recursos, alinhando-se aos Objetivos de Desenvolvimento Sustentável (ODS) da ONU:

* **ODS 3:** Saúde e Bem-Estar.
* **ODS 16:** Paz, Justiça e Instituições Eficazes (transparência e eficiência em instituições públicas).

## Protótipo de Interface (UI/UX)

O design das telas e o fluxo de navegação do aplicativo foram desenvolvidos no Figma, que atua como o nosso Produto Mínimo Viável (MVP) para esta etapa do projeto.

 **[Acessar Protótipo no Figma](https://www.figma.com/make/U2mrWrfeIeoJwvnx4yyAb1/Hospital-Check-in-App?p=f&t=5kHQXmxwswEJyfPu-0)**

![Tela de Login](imagem_2026-03-28_192822530.png)
![Tela de Acompanhamento](imagem_2026-03-28_192842956.png)
![Tela de Avaliação](imagem_2026-03-28_192901183.png)

## Fluxo Logístico de Atendimento

```mermaid
graph TD
    A([📍 Paciente chega à UBS]) --> B[Totem / Recepção]
    B --> C(Faz o Check-in)
    C --> D{Recebe Link}
    D -->|Via QR Code ou SMS| E[Entra na Fila Virtual]
    E --> F[📱 Acompanha Posição no MedFlow]
    F --> G{Chegou a vez?}
    G -->|Ainda não| F
    G -->|Sim!| H[Notificação de Chamada]
    H --> I[🩺 Atendimento no Consultório]
    I --> J[Formulário de Feedback Liberado]
    J --> K(Paciente Avalia a Experiência)
    K --> L[(📊 Dashboard do Gestor)]
    E -.->|Atualiza a fila em tempo real| L
