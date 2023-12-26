### Diagrama de Casos de Uso

```mermaid
graph TD
    A[Usuário] -- Realiza Cadastro --> B(Cadastro de Usuários)
    A -- Realiza Pedido --> C(Aplicativo)
    B -- Gerencia Dados --> D(Painel Administrativo)
    D -- Controla Catálogo --> E(Cadastro de Itens)
    D -- Gerencia Usuários --> B
    D -- Gera Relatórios --> C
    D -- Acessa Dados --> F(Banco de Dados)
``` 
  
# Casos de Uso Detalhados

### Diagrama de Caso de Uso - Cadastro de Usuários

```mermaid
graph TD
    A[Usuário] -- Insere Dados --> B(Cadastro de Usuários)
```

#### Descrição Detalhada:
- **Ator Principal:** Usuário
- **Descrição:** O usuário insere dados pessoais no formulário de cadastro. Esses dados são processados e salvos no sistema.

### Diagrama de Caso de Uso - Realiza Pedido

```mermaid
graph TD
    A[Usuário] -- Seleciona Itens --> B(Aplicativo)
    B -- Gera Pedido --> C(Emite Pedido em PDF)
```

#### Descrição Detalhada:
- **Ator Principal:** Usuário
- **Descrição:** O usuário utiliza o aplicativo para selecionar os itens desejados. Após a seleção, o sistema gera um pedido em PDF contendo informações de identificação da empresa requerente, do fornecedor e a lista de itens com códigos e quantidades.

### Diagrama de Caso de Uso - Gerência de Dados

```mermaid
graph TD
    A[Administrador] -- Acesso --> B(Painel Administrativo)
    B -- Controla Catálogo --> C(Cadastro de Itens)
    B -- Gerencia Usuários --> D(Cadastro de Usuários)
    B -- Gera Relatórios --> E(Emite Relatórios)
    B -- Acessa Dados --> F(Banco de Dados)
```

#### Descrição Detalhada:
- **Ator Principal:** Administrador do Sistema
- **Descrição:** O administrador acessa o Painel Administrativo para controlar o catálogo de itens, gerenciar usuários, gerar relatórios e acessar informações no banco de dados.

### Diagrama de Caso de Uso - Cadastro de Itens

```mermaid
graph TD
    A[Administrador] -- Insere Dados --> B(Cadastro de Itens)
```

#### Descrição Detalhada:
- **Ator Principal:** Administrador do Sistema
- **Descrição:** O administrador insere dados dos itens no sistema, incluindo descrição, imagem, código, entre outros campos, para compor o catálogo de materiais.

### Diagrama de Caso de Uso - Geração de Relatórios

```mermaid
graph TD
    A[Administrador] -- Gera Relatórios --> B(Emite Relatórios)
```

#### Descrição Detalhada:
- **Ator Principal:** Administrador do Sistema
- **Descrição:** O administrador, por meio do Painel Administrativo, gera relatórios com informações relevantes do sistema, como pedidos realizados, usuários cadastrados, entre outros dados.

### Diagrama de Caso de Uso - Acesso a Dados

```mermaid
graph TD
    A[Painel Administrativo] -- Consulta/Edição --> B(Banco de Dados)
```

#### Descrição Detalhada:
- **Ator Principal:** Painel Administrativo
- **Descrição:** Através do Painel Administrativo, é possível consultar e editar informações armazenadas no Banco de Dados para manter a integridade e a segurança dos dados do sistema.