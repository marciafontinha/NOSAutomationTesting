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

**3. Em automação, com resposta desta API gorest.co.in/public/v2/todos**

3.1. Aplica uma validação de schema ao resultado;

3.2. Valida se todos os resultados têm status completed;

3.3. Interpreta e valida o valor “due_on”

Comenta e publica o código num repositório público de GitHub:

Para realizar automação e validação de respostas da API GoREST para o endpoint `/public/v2/todos`, podemos utilizar o Postman junto com o Newman para executar os testes automatizados.

**3.1. Validação do Schema:** A validação de schema garante que a resposta da API corresponde à estrutura esperada. Utilizaremos a biblioteca `tv4` no Postman para validar o schema.

**3.2. Validação de Status:** Valida se todos os resultados têm o status `completed`.
  
**3.3. Validação do campo `due_on`:** Valida e interpreta se o valor do campo `due_on` é uma data válida no formato ISO 8601.

**Configuração no Postman para implementar estas validações:**

**1. Criar um nova coleção no postam e adicionar um nova request para `GET /public/v2/todos`**
**2. Adicionar os seguintes scripts na tab `testes` da request:**

```
// Import the tv4 library for JSON schema validation
const tv4 = require('tv4');

// Define the expected schema for the response
const schema = {
    "type": "array",
    "items": {
        "type": "object",
        "properties": {
            "id": {"type": "integer"},
            "user_id": {"type": "integer"},
            "title": {"type": "string"},
            "due_on": {"type": "string", "format": "date-time"},
            "status": {"type": "string"}
        },
        "required": ["id", "user_id", "title", "due_on", "status"]
    }
};

// Validate the response schema
pm.test("Schema is valid", function() {
    const result = tv4.validateMultiple(pm.response.json(), schema);
    pm.expect(result.valid).to.be.true;
    if (!result.valid) {
        console.log(result.errors);
    }
});

// Validate all todos have status 'completed'
pm.test("All todos have status 'completed'", function() {
    const todos = pm.response.json();
    todos.forEach(todo => {
        pm.expect(todo.status).to.eql('completed');
    });
});

// Validate the 'due_on' field
pm.test("All todos have a valid 'due_on' date", function() {
    const todos = pm.response.json();
    todos.forEach(todo => {
        pm.expect(new Date(todo.due_on).toString()).not.to.equal('Invalid Date');
    });
}); 
```

**Configurações do Newman:**

Para executamos os testes automaticamente num ambiente CI/CD podemos usar o Newman, a CLI do postman. Primeiro exportamos a coleção do postamn para um ficheiro .JSON e depois usamos o Newman para executar a colection. 

**Passos:**
1. Exportar a colection do Postman:

- No Postman, clicar com o botão direito na coleção e selecione `Export`.
- Salvar o arquivo JSON da coleção.

2. Intalar o Newman:

Instalar o mesmo usando npm:

```
npm install -g newman
```

3. Executar a colection exportada:

```
newman run <path_to_exported_collection.json>
```

4. Publicar a mesma no repositório GitHub

Adicionamos o arquivo .JSON da colection exportada e um arquivo `README.md` como este a explicar a exucação dos testes e publicamos o código no repositório. 

Exemplo da estrutura do repositório: 

```
gorest-api-tests/
├── collections/
│   └── GoREST_Todo_Tests.postman_collection.json
├── README.md
```

Conteudo do `README.md`

```
# GoREST API Tests

Este repositório contém testes automatizados para o endpoint `/public/v2/todos` da API GoREST.

## Configuração

1. Instalar o [Postman](https://www.postman.com/) se ainda não o fez.
2. Instalar o [Newman](https://github.com/postmanlabs/newman) globalmente:
   ```sh
   npm install -g newman
```

Agora executamos os testes: 

1. Clone do repositório:

```
git clone https://github.com/<seu-usuario>/gorest-api-tests.git
cd gorest-api-tests
```

2. Execução de testes com o Newman:

```
newman run collections/GoREST_Todo_Tests.postman_collection.json
```

**Testes incluídos:**
- Validação do Schema da resposta
  
- Verificação se todos têm o status `completed`.
  
- Validação do campo `due_on` para garantir que seja uma data válida.

**4. DevOps, CI/CD.**

4.1. Explica e justifica uma implementação de testes de carga a esta API: 

Os testes de carga são cruciais para garantir que a API GoREST possa lidar com um alto volume de solicitações em simultâneo sem comprometer a performance e a funcionalidade. A implementação de testes de carga permite identificar e prever o 

comportamento sob diferentes nível de tráfego e melhorar a escalibilidade. 

Passos para Implementação:

1. Configuração do Teste:

- Definir Objetivos: Estabelecer métricas chave como tempo de resposta, taxa de transferência e número máximo de usuários simultâneos.
  
- Cenários de Teste: Criar cenários que simulem operações comuns na API, como criação, leitura, atualização e exclusão de usuários, posts, comentários e todos.

2. Desenvolvimento do Script de Teste:

- Ferramenta Escolhida: Configurar scripts em JMeter, Gatling ou Artillery.
  
- Simulação de Usuários: Definir diferentes perfis de usuários e simular suas interações com a API.
  
- Validação de Respostas: Incluir verificações para garantir que as respostas da API estejam corretas.

3. Execução do Teste:

- Ambiente de Teste: Realizar os testes em um ambiente de staging que seja representativo do ambiente de produção.
  
- Aumento Gradual de Carga: Iniciar com uma carga leve e aumentar gradualmente até atingir ou ultrapassar a carga esperada em produção.

4. Análise dos Resultados:

- Identificação de Gargalos: Analisar métricas e relatórios para identificar pontos de falha ou degradação de desempenho.
  
- Ajustes Necessários: Fazer ajustes na API ou na infraestrutura com base nos resultados dos testes.

5. Justificativa:
   
Os testes de carga são essenciais para garantir que a API GoREST possa suportar o tráfego esperado em produção, identificando e mitigando riscos antes que eles impactem os usuários finais.

4.2. Como implementarias uma solução de Continuous Testing, justifica;

Continuous Testing (CT) integra testes automatizados em todas as fases do ciclo de desenvolvimento, proporcionando feedback contínuo e garantindo a qualidade desde o início até a produção. Esta abordagem é vital para manter a qualidade e a 

confiabilidade do software num ambiente de desenvolvimento ágil e DevOps.

Passos para Implementação:

1. Configuração do Pipeline de CI/CD:

- Repositório de Código: Configurar um repositório Git para o código-fonte e scripts de teste.
  
- Pipeline de Integração Contínua: Configurar um pipeline de CI para executar testes unitários, de integração e de API a cada commit.

2. Integração de Testes Automatizados:

- Testes Unitários: Executar testes unitários em cada build para validar a lógica do código.
  
- Testes de Integração: Verificar a interação entre diferentes módulos e serviços.
  
- Testes de API: Utilizar ferramentas como Postman/Newman para executar testes de API automatizados.

3. Testes de Carga e Desempenho:

- Integração de Scripts de Teste de Carga: Configurar scripts de testes de carga (JMeter, Gatling, Artillery) no pipeline para execução periódica.
  
- Monitoramento Contínuo: Utilizar ferramentas como Grafana e Prometheus para monitorar métricas de desempenho em tempo real.

4. Ambientes de Staging e Produção:

- Ambiente de Staging: Implementar testes automatizados no ambiente de staging antes de promover para produção.
  
- Deploy Automatizado: Automatizar o deploy para produção somente após a aprovação dos testes em staging.
  
5. Monitoramento e Feedback:

- Monitoramento Contínuo: Utilizar ferramentas de monitoramento para observar o desempenho da API em produção.
  
- Feedback Rápido: Configurar notificações para alertar a equipe sobre falhas ou degradações de desempenho.

6. Justificativa:
   
A implementação de Continuous Testing garante feedback contínuo e rápido sobre a qualidade do software, permitindo que a equipe identifique e resolva problemas rapidamente. Isso melhora a eficiência, reduz o tempo de lançamento e aumenta a

confiabilidade do software, proporcionando uma experiência de usuário final melhorada e mais consistente.
