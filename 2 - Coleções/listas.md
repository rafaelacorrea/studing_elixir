# Listas

## Uma lista pode conter elementos de qualquer tipo.

```elixir
iex> [1, :atom, "string", 1.4]
[1, :atom, "string", 1.4]
```
## lista encadeada: o Elixir percorre as listas de forma linear, por isso é indicado adicionar os novos itens na cabeça da lista para facilitar o processamento)

```elixir
iex> lista = [1, :atom, "string", 1.4]
[1, :atom, "string", 1.4]

iex> [0 | lista]
[0, 1, :atom, "string", 1.4]
```
Para adicionar um elemento no final da lista, usamos concatenação de lista(++):

```elixir
iex> lista ++ [5]
[1, :atom, "string", 1.4, 5]
```
Remover itens da lista: É necessário ter lista nos dois termos(se existir dois ou mais elementos iguais na lista, será removido apenas o que vier primeiro na fila)

```elixir
iex> lista = [1,2,2,3]
[1, 2, 2, 3]

iex> lista -- [2]
[1, 2, 3]
```
Elixir faz uma verificação para confirmar se o elemento é identico ao que foi solicitado a exclusão.

```elixir
iex> lista = [1,2,2.0,3]
[1, 2, 2.0, 3]

iex> lista -- [2.0]     
[1, 2, 3]
```

## [head | tail] = lista

Esse é o nosso primeiro exemplo de pattern matching, basicamente aqui estamos guardando as informações da lista em variáveis(podem ter qualquer nome), definindo qual parte é a cabeça e qual parte é a cauda da lista.

```elixir
iex> lista = [1,2,2.0,3]
[1, 2, 2.0, 3]

iex> [cabeca | cauda] = lista
[1, 2, 2.0, 3]

iex> cabeca
1

iex> cauda
[2, 2.0, 3]
```

## Head(hd)
Retorna a cabeça da lista.

```elixir
iex> lista = [1,2,2.0,3]
[1, 2, 2.0, 3]

iex> hd(lista)                        
1
```

## Tail(tl)
Retorna a cauda(resto) da lista.
```elixir
iex> lista = [1,2,2.0,3]
[1, 2, 2.0, 3]

iex> tl(lista)     
[2, 2.0, 3]
```
[<<< Coleções ](README.md)| - - - - - - - - - - - -|[ Início ](/README.md)| - - - - - - - - - - - -|[ Tuplas >>> ](tuplas.md)