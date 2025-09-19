NuvemQD - Documentação Técnica

1. Estrutura geral

NuvemQD é composta por uma máquina virtual central que gerencia múltiplos containers Docker.

Cada container atua como um nó independente, capaz de processar tarefas isoladas.

O computador principal executa apenas o código da nuvem; todo o processamento pesado ocorre nos containers.


2. Containers

Containers são criados dinamicamente pelo código.

Cada container possui:

CPU alocada

RAM dedicada

Espaço de armazenamento específico


Containers podem ser reiniciados, parados ou limpos individualmente.

Um container especial, chamado Filasco, recebe prioridade em recursos e é destinado a processamento intenso.


3. Gerenciamento de recursos

O código da nuvem monitora CPU, RAM e storage em tempo real.

Recursos são alocados automaticamente entre containers conforme necessidade.

Containers podem ser criados ou destruídos sem reiniciar a nuvem.


4. Processamento

Tarefas e modelos não ficam carregados na nuvem por padrão; os containers são vazios.

Cada container processa uma tarefa isolada, garantindo que a carga seja distribuída.

O computador principal atua como orquestrador, sem sobrecarga de processamento pesado.


5. Armazenamento

Cada container possui diretório de armazenamento persistente.

Dados podem ser adicionados, removidos ou listados por container individualmente.

Storage é separado para evitar interferência entre containers.


6. Monitoramento e manutenção

Threads de monitoramento observam a saúde da nuvem.

Logs detalhados são gerados sobre o status de containers, CPU e memória.

Funções permitem reiniciar containers, limpar storage ou listar diretórios ativos.
