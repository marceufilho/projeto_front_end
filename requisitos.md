# Requisitos
## Requisitos em linguagem natural
1. *Quem é o usuário?*
    - Funcionário da dosimagem sem conhecimento de tecnologia. Exemplo: Estagiário de Administração
2. *Quem é o cliente?*
    - Hospitais
2. *O problema:*
    - Interface muito pouco amigável. Django default admin site
3. *Objetivo:*
    - tornar mais intuitivo o uso do sistema.
<hr>

### Proposta da equipe balança mas não cai pro software
- A primeira interface que o usuário terá acesso é uma pagina similar a um kanban.
    - ***Primeiro quadro do Kanban***: Novos clientes que estão todos processos pendentes.
    - ***Segundo Quadro do Kanban***: Processo de calibração da maquina do cliente feito.
    - ***Terceiro Quadro do Kanban***: Download dos dados do **PACIENTE DO CLIENTE** e de seus exames anexados. Aqui também terá um quadro com quantos pacientes já foram concluídos e quantos faltam.
    - ***Quarto Quadro do Kanban***: Anexo do relatório da Dosimagem para cada paciente. Finalização do processo.
- Todos os quadros terão links para paginas próprios e ações para passar de um quadro para o outro.
    - ***Primeiro kaban:*** Ao clicar no nome do cliente será aberto uma pagina com todas as informações de calibração do sistema da Dosimagem e o arquivo para download das imagens de calibração.
        - *Ação necessária para mudar do primeiro quadro pro segundo*: Clicar em um botão que a calibragem foi feita. POP up para confirmação da ação.
    - ***Segundo Kanban:*** A figura da empresa terá um contador embaixo com quantos pacientes já foi feito os downloads dos dados e foram concluídos com confirmação do usuário.
        - *Ação necessária para ir do segundo pro terceiro Kanban*: 100% dos pacientes terem seus downloads feitos.
    - ***Terceiro Kanban:*** Figura igual ao primeiro Kanban mas com a diferença o contador para relatórios entregues para paciente.
        - *Ação necessária para ir do segundo pro terceiro Kanban:* 100% dos pacientes terem seus relatórios anexados.
    - ***Quarto Kanban:*** Processo 100% finalizado