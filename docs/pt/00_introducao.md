# Introdução ao Projeto Ouroboros HPC

Bem-vindo ao início da sua jornada na criação de um cluster de Computação de Alta Performance (HPC) pessoal. Este projeto, apelidado de "Ouroboros", foi concebido para ser um guia completo e prático, desde a preparação do seu computador até a execução de um pipeline de bioinformática distribuído e o monitoramento profissional do seu ambiente.

## Filosofia

O nome **Ouroboros** foi escolhido por sua representação do ciclo e da autossuficiência. Nosso objetivo é criar um ecossistema de computação que é:
-   **Autocontido:** Vive inteiramente dentro do seu computador host, sem custos de nuvem.
-   **Autorreferencial:** Os nós do cluster se conhecem e trabalham em conjunto, gerenciados por uma mente central (Slurm).
-   **Cíclico:** A comunicação flui do host para o cluster (para gerenciamento) e do cluster para o host/mundo (para baixar dados e softwares), completando um ciclo.

## Para Quem é Este Guia?

Este material foi pensado para estudantes, pesquisadores e profissionais das áreas de bioinformática, biologia computacional, ciência de dados e áreas correlatas que desejam:
-   Entender na prática como um cluster HPC é estruturado.
-   Aprender a instalar e configurar um gerenciador de jobs como o Slurm.
-   Ganhar experiência na submissão de jobs e no uso de gerenciadores de pipeline como o Nextflow em um ambiente distribuído.
-   Ter um ambiente de desenvolvimento local e robusto para criar e testar pipelines antes de enviá-los para supercomputadores reais.

## Arquitetura Final

Ao final deste guia, você terá construído a seguinte arquitetura:

-   **1 Nó Mestre (`master`):** Responsável por gerenciar a fila de jobs (Slurm Controller), servir arquivos compartilhados (NFS Server) e hospedar os serviços de monitoramento (Prometheus + Grafana).
-   **3 Nós de Trabalho (`workers`):** Responsáveis por executar os cálculos e tarefas dos pipelines (Slurm Daemons).
-   **Rede Virtual Privada:** Uma rede interna onde todos os nós se comunicam de forma isolada e eficiente.
-   **Armazenamento Compartilhado:** Um diretório central acessível por todos os nós, garantindo que dados, softwares e resultados sejam consistentes em todo o cluster.

Vamos começar!

➡️ **Próximo passo: [Fase 1: Preparação do Host](01_preparacao_host.md)**
