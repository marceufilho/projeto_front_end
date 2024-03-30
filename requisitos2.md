# Requisitos do projeto Dosimagem 
### Introdução: 
- ***Proposito do software***: Organizar o fluxo de trabalho interno da dosimagem para a prescrição de laudos. Dando agilidade e organização a empresa.

- ***Usuário do sistama***: Funcionário da dosimagem sem conhecimento de tecnologia. Exemplo: Estagiário de Administração ou uma simples secretária.

- ***Funcionalidades do projeto***: 
    - O usuário deve ser capaz de vizualisar em que estagio está cada cliente no processo de geração de laudo.
    - o usuario deve ser capaz de procurar um cliente especifico no pipeline
    - O usuario deve ser capaz de readequar o cliente no fluxo da dosimagem em caso de algum bug ou má funcionalidade.

- ***Tech Stack***: A aplicação fron-end será desenvovida em React para browser. O front end se conectara com uma Rest API desenvovida pela Dosimage. (Precisamos da documentação da API)

- ***Resposabilidade do time Balança mais não cai***: Fazer o UX do front-end, programar o aplicativo e testa-lo com o uso da API da Dosimagem. No caso da API falhar nos teste deve ser criado apenas um log com a falha e enviado a dosimagem. Uma vez que API está fora do escopo do trabalho.

### Visão geral do sistema: 

- A primeira interface que o usuário terá acesso é uma pagina similar a um kanban.
    - ***Primeiro Quadro do Kanban***: Novos clientes que estão todos processos pendentes.
    - ***Segundo Quadro do Kanban***: Processo de calibração da maquina do cliente realizado.
    - ***Terceiro Quadro do Kanban***: Download dos dados do **PACIENTE DO CLIENTE** e de seus exames anexados. Aqui também terá um quadro com quantos pacientes já foram concluídos e quantos faltam.
    - ***Quarto Quadro do Kanban***: Anexo do relatório da Dosimagem para cada paciente. Finalização do processo.
    - ***Quinto Quadro Kanba***: Finalizado
- Todos os quadros terão links para paginas próprios e ações para passar de um quadro para o outro.
    - ***Primeiro Kanban:*** Ao clicar no nome do cliente será aberto uma pagina com todas as informações de calibração do sistema da Dosimagem e o arquivo para download das imagens de calibração.
        - *Ação necessária para mudar do primeiro quadro pro segundo*: Clicar em um botão que a calibragem foi feita. POP up para confirmação da ação.
    - ***Segundo Kanban:*** A figura da empresa terá um contador embaixo com quantos pacientes já foi feito os downloads dos dados e foram concluídos com confirmação do usuário.
            - *Ação necessária para ir do segundo pro terceiro Kanban*: 100% dos pacientes terem seus downloads feitos.
    - ***Terceiro Kanban:*** Figura igual ao primeiro Kanban mas com a diferença o contador para relatórios entregues para paciente.
            - *Ação necessária para ir do segundo pro terceiro Kanban:* 100% dos pacientes terem seus relatórios anexados.
    - ***Quarto Kanban:*** Processo 100% finalizado.

## Requisitos Funcionais:

#### Interfaces do sistema
- ***Pagina Home***: Pagina principal de controlo onde terá 5 divisões, cada uma sendo um quadro com os respectivos titulos abaixo, dentro de cada titulo tera a onde a empresa se encontra no processo. Seguindo a mesma ordem: Uma empresa pode estar em uma e apenas uma divisão.
    1. **Pendentes**
    2. **Calibração**
    3. **Downloads** : Nesse quadro tambem teremos ao lado do nome do cliente um contador de quantos downloads já foram feitos e quantos faltam. 
    4. **Anexo de relatorios**
    5. **Finalizados**
    - A Pagina tambem contara com um buscador
- **Pagina Pendentes**: Pagina para apenas com um butão para começar o processo.
- **Pagina Calibração**: 
    - Form com todas as informações nescessarias para calibração que foram recebidads da API
    - botão para copiar as informações
    - Abaixo do form os arquivos nescessarios para claibragem tambem fornecidos pela API
    - Botão de concluido 
- **Pagina de Downloads**:
    - Buscador em cima:
    - Dados de maneira tabular as informações e anexo de cada paciente do hospital:Botão de concluido no final
- **Pagina Anexo Relatorio**: 
    - Nome do paciente e botão para anexar o relatorio dosimagem.

#### Interface do usuario
- **Home**: 
    - O usuario pode inputar o nome de uma empresa no buscador e retorna em qual fase se encontra 
    - O usuario pode clicar no nome da empresa nos quadros e deve ser direcionado para pagina de mesmo nome do kanban
- **Pagina Pendentes**: 
    - Usuario pode clicar em começar e o botão passa a empresa para o quadro de calibração na home 
- **Pagina Calibração**:
    - O usuario pode clicar no botão para copiar as informações de calibração
    - o usuario pode clicar no botão de anexo para baixar os arquivos
    - O usuario so pode clicar no botão de concluido apos apertar os outros dois botões. Ao concluir a empresa é atualizada para o proximo kanban
- **Pagina de Downloads**:
    - O usuario pode fazer o download de todas as informações do paciente apenas ao clicar em seu nome.
    - O usuario pode procurar um nome especifico de paciente
    - O usuario o pode concluir o usario após ddownload de suas informções
- **Pagina Anexo Relatorio**: 
     - O usuario pode anexar o relatorio para cada paciente 

#### Rotinas internas do sistema:
- **Pagina de Downloads**: 
    - Após ser concluidas todos downloads de paciente automaticamente é atulizada a fase do cliente para o anexo de relatorio
- **Pagina Anexo Relatorio**: 
    - Após ser anexados todos relatorios a fase do cliente é automaticamente atulizada.



## Requisitos não funcionais:
#### Segurança:
- Perguntar para Dosimagem se tem alguma informção que o usuario do sistema não pode ter acesso.

#### Maintainability:
- CI: ESLint e Jest
- Airbnb React/JSX Style Guide: https://github.com/airbnb/javascript/blob/master/react/README.md

#### Usabilidade:
- Devemos fazer uma pequena explicação do fluxo da dosimagem e testar com pelo menos 5 pessoas diferentes e leigas se conseguem usar e fazer todas as ações nescessarias para dosimagem.
