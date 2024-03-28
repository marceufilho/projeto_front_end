# Casos de Uso Sistema Dosimagem


### Entrar no Sistema:
- **Usuário:** Cliente ou Funcionário
- **Pré-condição:** O usuário acessa a página inicial da plataforma.
- **Ação:** O usuário insere suas credenciais de login (por exemplo, nome de usuário e senha) nos campos apropriados.
- **Pós-condição:** O sistema autentica as credenciais do usuário. Se válidas, o usuário é redirecionado para a página principal da plataforma. Se inválidas, o usuário é notificado sobre o erro de autenticação.

### Visualização de Serviços Disponíveis:
- **Usuário:** Hospital, Clínica
- **Pré-condição:** O cliente acessa a plataforma.
- **Ação:** O cliente explora os diferentes serviços de imagem oferecidos pela empresa.
- **Pós-condição:** O cliente pode revisar informações detalhadas sobre cada serviço e sua aplicabilidade.

### Contratação de Serviços:
- **Usuário:** Hospitais, Clinica
- **Pré-condição:** O cliente revisa e aceita o orçamento fornecido pela empresa
- **Ação:** O cliente seleciona o serviço desejado e confirma a contratação
- **Pós-condição:** O serviço é oficialmente contratado e o cliente recebe uma confirmação de contratação.

### Solicitação de Orçamento:
- **Ator:** Hospital, Clínica.
- **Pré-condição:** O cliente acessa a plataforma e está autenticado.
- **Ação:** O cliente seleciona o serviço desejado e preenche os detalhes para solicitar um orçamento.
- **Pós-condição:** O pedido de orçamento é enviado para a empresa.

### Geração de Orçamento:
- **Ator:**  Empresa de Serviços de Imagem
- **Pré-condição:** A empresa recebe uma solicitação de orçamento.
- **Ação:** A empresa revisa os detalhes da solicitação e calcula o custo do serviço.
- **Pós-condição:** - Um orçamento é gerado e enviado ao cliente.

### Revisão de Solicitações de Orçamento:
- **Ator:** Funcionário do sistema.
- **Pré-condição:** O funcionário acessa a seção de solicitações de orçamento.
- **Ação:** O funcionário revisa as solicitações, avaliando os serviços solicitados e os detalhes fornecidos pelo cliente.
- **Pós-condição:** O funcionário toma uma decisão sobre a viabilidade da solicitação de orçamento.
