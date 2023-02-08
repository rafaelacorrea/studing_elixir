# Tuplas
São parecidas com as listas. Suas informações são armazenadas inteiras na memória, tornando o resgate dessa informação mais rápido, por esse motivo é uma boa prática é utilizar tuplas pequenas. 

```elixir
iex> {:ok, "mensagem de sucesso"}
{:ok, "mensagem de sucesso"}
iex> {:erro, "mensagem de erro"}
{:erro, "mensagem de erro"}
```

## FUNÇÃO ELEM
Recebe como parâmetro a tupla e o índice da posição desejada e retorna o elemento que está presente nela.
```elixir
iex> tupla = {1.2, 1, :atom, "string", 'cadeia'} 
{1.2, 1, :atom, "string", 'cadeia'}
iex> elem(tupla,0)
1.2
iex> elem(tupla,3)
"string, 'cadeia'}\n"
```

## Keyword list
É um a lista  contém uma tupla. Dentro dessa tupla há um atomo como chave e o valor pode ser qualquer elemento. Lembrando de deixar um espaço entre eles.

```elixir
iex> {:a, "valor"}
{:a, "valor"}
iex> [{:a, "valor"}]
[a: "valor"] 
```
A keyword list suporta chaves e valores repetidos, o que importa é a ordem que foram colocados:
```elixir
iex> [a: 1, a: 2, b: 1, b: 1]
[a: 1, a: 2, b: 1, b: 1]
iex> [chave1: "valor1", chave2: "valor2", chave4: "valor4", chave3: "valor3"]
[chave1: "valor1", chave2: "valor2", chave4: "valor4", chave3: "valor3"]
```

[<<< Listas ](listas.md)| - - - - - - - - - - - -|[ Início ](/README.md)| - - - - - - - - - - - -|[ Mapas >>> ](mapas.md)