# Biblioteca Poe

Sistema de gerenciamento de biblioteca desenvolvido em linguagem C como projeto acadêmico da disciplina de Programação. A aplicação permite administrar livros e usuários, controlar empréstimos e devoluções e gerar relatórios por meio de uma interface interativa no terminal.

## Funcionalidades

### Gerenciamento de usuários
- Cadastrar usuários com matrícula, nome e curso.
- Buscar usuários por matrícula ou nome.
- Listar usuários cadastrados.
- Atualizar dados de usuários.
- Remover usuários.
- Consultar empréstimos associados a um usuário.

### Gerenciamento de livros
- Cadastrar livros com código, título, autor, ano, gênero e quantidade de exemplares.
- Listar livros cadastrados.
- Buscar livros por código ou título.
- Atualizar informações dos livros.
- Remover livros.
- Consultar usuários que possuem empréstimos de determinado livro.

### Empréstimos e devoluções
- Registrar empréstimos de livros.
- Registrar devoluções.
- Consultar registros de empréstimos.
- Armazenar informações sobre retirada, prazo previsto e data de devolução.
- Identificar empréstimos devolvidos e pendentes.

### Relatórios
- Listar usuários com empréstimos em atraso.
- Identificar os livros mais emprestados.
- Consultar o acervo disponível.
- Consultar o histórico de empréstimos de um usuário.

### Persistência de dados
O sistema utiliza arquivos para armazenar e recuperar os dados, permitindo manter registros entre execuções do programa.

## Tecnologias utilizadas
- **Linguagem C**
- **Makefile** 

## Como executar


```bash
git clone https://github.com/yhsww/biblioteca_poe.git
cd biblioteca_poe
```

### 3. Compilar o programa

```bash
make
```

O comando compila os arquivos `.c` encontrados em `src/`, utilizando os cabeçalhos de `include/`, e gera o executável `biblioteca-poe.out`.

### 4. Executar a aplicação

```bash
make run
```

O programa exibirá o menu principal no terminal, com as opções de usuários, livros, empréstimos, relatórios e saída.

### 5. Limpar arquivos gerados

Para remover o executável e os arquivos `.dat` e `.txt` abrangidos pela regra `clean` do Makefile:

```bash
make clean
```

## Menu principal

Ao iniciar a aplicação, o usuário encontrará as seguintes opções:

```text
Usuários    [1]
Livros      [2]
Empréstimos [3]
Relatórios  [4]
Sair        [0]
```

Cada seção possui um menu próprio para acessar suas operações. Para encerrar o programa, selecione a opção `0` no menu principal.

### Organização dos módulos

| Arquivo | Responsabilidade |
|---|---|
| `main.c` | Inicialização e menus principais da aplicação. |
| `livros.c` | Operações de cadastro, consulta, atualização e remoção de livros. |
| `usuarios.c` | Operações de gerenciamento de usuários. |
| `emprestimos.c` | Registro e consulta de empréstimos e devoluções. |
| `relatorios.c` | Geração dos relatórios do sistema. |
| `utilitarios.c` | Funções auxiliares para entrada de dados, strings e interface do terminal. |

Os arquivos `.h` em `include/` declaram as estruturas de dados e as funções utilizadas pelos módulos.

## Formatação do código

Para formatar os arquivos C e os cabeçalhos com `clang-format`, execute:

```bash
make format
```

Esse comando aplica a formatação aos arquivos `src/*.c` e `include/*.h`.

## Objetivo acadêmico

O projeto exercita conceitos fundamentais de programação em C, incluindo:

- Modularização por meio de arquivos `.c` e `.h`.
- Estruturas (`struct`) para representação de livros, usuários e empréstimos.
- Alocação e liberação dinâmica de memória.
- Manipulação de arquivos para persistência de dados.
- Validação de entradas do usuário.
- Organização de menus e fluxo de controle.
- Separação de responsabilidades entre módulos.

