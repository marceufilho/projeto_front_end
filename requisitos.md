# Requisitos
## Requisitos em linguagem natural 
1. *Quem é o usuario?*
    - Funcionario da dosimagem sem conhecimento de tecnologia. Exemplo: Estagiario de Administração
2. *Quem é o cliente?* 
    - Hospitais 
2. *O problema:*
    - Interface muito pouco amigavel. Django default admin site 
3. *Objetivo:* 
    - tornar mais intuitivo o uso do sistema.

### Proposta da equipe balança mas não cai pro software
- A primeira interface que o usuario terá acesso é uma pagina simailar a um kanban. 
    - ***Primerio quadro do Kanban***: Novos clientes que estão todos processos pendentes.
    - ***Segundo Quadro do Kanban***: Processo de calibração da maquina do cliente feito.
    - ***Terceiro Quadro do Kanban***: Dowload dos dados do **PACIENTE DO CLIENTE** e de seus exames anexados. Aqui tambem tera um quadro com quantos pacientes ja foram concluidos e quantos faltam.
    - ***Quarto Quadro do Kanban***: Anexo do relatorio da Dosimagem para cada paciente. Finalização do processo.
- Todos os quadros teram links para paginas proprios e ações para passar de um quadro para o outro.
    - Primeiro kaban: Ao clicar no nome do cliente será aberto uma pagina com todas as informações de calibração do sistema da Dosimagem e o arquivo para download das imagens de calibração.
        - Ação nescessaria para mudar do primeiro quadro pro segundo: Clicar em um butão que a calibragem foi feita. POP up para confirmação da ação.
    - Segundo Kanban: A figura da empresa tera um contador embaixo com quantos pacientes ja foi feito os downloads dos dados e foram concluidos com confirmação do usuario.
        - Ação nescessaria para ir do segundo pro terceiro Kanban: 100% dos pacientes terem seus downloads feitos.
    - Terceiro Kanban: Figura igual ao primeiro Kanban mas com a diferença o contador para relatorios entregues para paciente.
        - -Ação nescessaria para ir do segundo pro terceiro Kanban: 100% dos pacientes terem seus relatorios anexados.
    - Quarto Kanban: Processo 100% finalizado



    