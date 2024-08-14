# Teste Técnico - Sistema de Cadastro de Produtos e Variações

## Descrição Geral
Este teste técnico consiste em desenvolver um sistema simples para cadastro e gestão de produtos, onde cada produto pode ter múltiplas variações (ex: cor, tamanho). O sistema deve permitir a criação, leitura, atualização e exclusão (CRUD) de produtos e variações de produtos.

## Requisitos Funcionais
1. **Cadastro de Produtos:**
   - O produto deve ter os seguintes campos: `Id`, `Nome`, `Preço Base`.
   - O sistema deve permitir criar, visualizar, editar e excluir produtos.

2. **Cadastro de Variações de Produtos:**
   - Cada produto pode ter múltiplas variações.
   - A variação deve ter os seguintes campos: `Id`, `ProdutoId` (chave estrangeira para o produto), `Nome da Variação`.
   - O sistema deve permitir criar, visualizar, editar e excluir variações de produtos.

## Requisitos Técnicos

1. **Arquitetura em Camadas usando DDD:**
   - **API:** Contém os controladores e a interface de comunicação com o mundo externo.
   - **Domain:** Contém as entidades, agregados, repositórios, serviços de domínio e regras de negócio.
   - **Infra.Data:** Responsável pela persistência de dados utilizando Entity Framework Core.
   - **Infra.IoC:** Responsável pela configuração de injeção de dependência, incluindo o AutoMapper.
   - **Shared:** Contém objetos ou utilitários compartilhados entre as camadas, como DTOs e exceções personalizadas.

2. **Injeção de Dependência:**
   - Utilize injeção de dependência em `Infra.IoC` para gerenciar a criação de instâncias de serviços, repositórios, e outras dependências.

3. **Entity Framework Core:**
   - Use o Entity Framework Core na camada `Infra.Data` para persistir os dados no banco de dados.
   - Configure corretamente o mapeamento das entidades para as tabelas do banco.

4. **Automapper:**
   - Utilize o AutoMapper em `Infra.IoC` para mapear as entidades de domínio para os DTOs usados na API.

5. **Validações e Tratamento de Erros:**
   - Implemente validações básicas no domínio (ex: nome do produto é obrigatório).
   - Utilize middleware para tratamento de erros globais na API.

## Tarefas
1. Crie o projeto base usando .NET e configure as camadas conforme descrito.
2. Implemente o CRUD completo para o cadastro de produtos na camada `API`, utilizando os serviços e repositórios definidos no domínio e `Infra.Data`.
3. Implemente o CRUD completo para o cadastro de variações de produtos.
4. Configure a injeção de dependências em `Infra.IoC` e certifique-se de que todas as dependências necessárias estejam corretamente registradas.
5. Implemente as validações necessárias na camada de domínio e o tratamento de erros na camada `API`.

## Expectativas
- **Código:** Estruturado de acordo com os princípios de DDD, com camadas bem definidas.
- **Validações:** Simples e diretas, focadas na obrigatoriedade de campos.
- **Automapper:** Implementado para mapeamento entre entidades e DTOs.
- **Injeção de Dependência:** Corretamente configurada em `Infra.IoC`.
- **Documentação:** README simples explicando como configurar e rodar o projeto.


