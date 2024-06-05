# NOS Automation Testing

**1. Escolher uma ferramenta para automatizar testes à seguinte Api REST, explica o porquê dessa escolha. https://gorest.co.in/**
Para este caso a minha escolha seria a ferramenta de Postman pelas seguintes razões:

**1.1. Facilidade de uso:** pela interface ser "friendly" e de uso mais simples que nos permite criar, guardar e organizar solicitações de API com facilidade. Esta ferramenta acaba por ser o ideal tanto para a equipa de DEV quanto para a equipa de Testers e mesmo para quem não tenha muita experiência com scripts de teste.

**1.2. Criação e execução dos testes:** Esta ferramenta permite a criação de testes automáticos com base de liguagem JavaScript diretamente nas solicitações. Conseguimos também adicionar scripts de teste que validam as resposta da API como por exemplo: status codes, headers e conteudo do body da resposta.
 
**1.3. Criação de coleções de API**
 
**1.4. Integrações com CI/CD através do newman que é a CLI do postman.**
  
**1.5. Obtenção de relatórios e feedback.**
  
**1.6. Gratuito**
  
**1.7. Simulações de APIs antes mesmo da API estar completamente desenvolvida o que facilita testes inciais e desenvolvimento em paralelo.**

**2. Explica os use case de teste**:

**Criação de novos usuários:**
- Descrição do caso: Verificar a criação de um novo usuário.
- Cenários de teste:
  
  a) Criar um usuário com todos os campos obrigatórios preenchidos corretamente.
  
  b) Criar um usuário com campos opcionais adicionais.
  
  c) Tentar criar um usuário com dados inválidos (ex.: e-mail inválido, nome vazio)
  
  d) Criar um usuário com um e-mail já existente para verificar o comportamento do erro.
  
**Obter informações de um usuário**:

- Descrição do caso: Verificar a recuperação dos dados de um usuário específico.
- Cenários de teste:
  
  a) Atualizar um ou mais campos de um usuário existente.
  
  b) Tentar atualizar um usuário com dados inválidos.
  
  c) Atualizar um usuário inexistente e verificar o comportamento do erro.
  
**Excluir um usuário:**

- Descrição do caso: Verificar a exclusão de um usuário.
- Cenários de teste:
  
  a) Excluir um usuário existente.
  
  b) Tentar excluir um usuário inexistente e verificar o comportamento do erro.
  
**Criar um novo post:**
  
- Descrição do caso: Verificar a criação de um novo post.
- Cenários de teste:
  
  a) Criar um post com todos os campos obrigatórios preenchidos.
  
  b) Criar um post com dados inválidos.
  
  c) Criar um post associado a um usuário inexistente e verificar o comportamento do erro.
  
**Obter posts:**

- Descrição do caso: Verificar a recuperação de posts.
- Cenários de teste:
  
  a) Obter todos os posts.
  
  b) Obter posts de um usuário específico.
  
  c) Obter posts com filtros aplicados (ex.: título, stauts)
  
**Atualizar um Post:**

- Descrição do caso: Verificar a atualização de um post.
- Cenários de Teste:
  
  a) Atualizar um post existente.
  
  b) Atualizar um post com dados inválidos.
  
  c) Tentar atualizar um post inexistente e verificar o comportamento de erro.
  
**Excluir um Post:**

- Descrição do caso: Verificar a exclusão de um post.
- Cenários de Teste:
  
  a) Excluir um post existente.
  
  b) Tentar excluir um post inexistente e verificar o comportamento de erro.
  
**Adicionar um Comentário a um Post:**

- Descrição do caso: Verificar a adição de um novo comentário a um post.
- Cenários de Teste:
  
  a) Adicionar um comentário válido a um post existente.
  
  b) Adicionar um comentário a um post inexistente e verificar o comportamento de erro.
  
  c) Adicionar um comentário com dados inválidos.
  
**Obter Comentários de um Post:**

- Descrição do caso: Verificar a recuperação de comentários de um post.
- Cenários de Teste:
  
  a) Obter todos os comentários de um post existente.
  
  b) Tentar obter comentários de um post inexistente.
  
**Criar uma Nova Tarefa:**

- Descrição do caso: Verificar a criação de uma nova tarefa.
- Cenários de Teste:
  
  a) Criar uma tarefa com todos os campos obrigatórios preenchidos.
  
  b) Criar uma tarefa com dados inválidos.
  
  c) Criar uma tarefa associada a um usuário inexistente e verificar o comportamento de erro.
  
**Obter Tarefas:**

- Descrição do caso: Verificar a recuperação de tarefas.
- Cenários de Teste:
  
  a) Obter todas as tarefas.
  
  b) Obter tarefas de um usuário específico.
  
  c) Obter tarefas com filtros aplicados (ex.: por status).
  
**Atualizar uma Tarefa:**

- Descrição do caso: Verificar a atualização de uma tarefa.
- Cenários de Teste:
  
  a) Atualizar uma tarefa existente.
  
  b) Atualizar uma tarefa com dados inválidos.
  
  c) Tentar atualizar uma tarefa inexistente e verificar o comportamento de erro.
  
**Excluir uma Tarefa:**

- Descrição: Verificar a exclusão de uma tarefa.
- Cenários de Teste:
  
  a) Excluir uma tarefa existente.
  
  b) Tentar excluir uma tarefa inexistente e verificar o comportamento de erro.
  
**Considerações Gerais:**

 **- Autenticação:** Testar o comportamento da API quando o token de autenticação está ausente, inválido ou expirado. Verificar se a API respeita as permissões do usuário para diferentes operações.
 
  **- Paginação:** Testar a funcionalidade de paginação passando parâmetros como page e per_page. Verificar as respostas quando os limites de paginação são excedidos.
  
  **- Validação de Dados:** Testar a validação de dados em todos os campos obrigatórios e opcionais. Verificar mensagens de erro detalhadas para entradas inválidas.
  
  **- Respostas HTTP**: Verificar se a API retorna os códigos de status HTTP apropriados (200, 201, 204, 400, 401, 403, 404, 405, 422, 429, 500) para cada cenário de teste.
  
  **- Taxa de Limite:** Testar o comportamento da API ao exceder os limites de taxa (rate limits) para garantir que o cabeçalho de resposta contenha as informações corretas sobre os limites e o tempo de redefinição.
  
Ao seguirmos estes casos de uso de teste, serão garantidas umas coberturas abrangentes das funcionalidades da API GoREST, validando não apenas os cenários de sucesso, mas também os cenários de erro e edge case.
