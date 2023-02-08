# MAPAS
Semelhantes às keyword list, os mapas são nomalmente utilizados para salvas uma estrutura de informações. Podem ter como chaves, strings e/ou atomos.

Escrito com chaves átomos:
```elixir
iex> mapa = %{a: 1, b: 2}
%{a: 1, b: 2}
```
Escrito com chaves strings:
```elixir
iex> mapa2 = %{"a" => 1, "b" => 2}
%{"a" => 1, "b" => 2}
```

Escrito com chaves strings e átomos(chaves strings sempre são as primeiras):

```elixir
iex> mapa = %{"b" => 2, a: 1}
%{:a => 1, "b" => 2}
```

Uma das diferenças entre Keyword list e mapas é que as chaves de nomes iguais são sobreescritas e somente aultima chave duplicada é guardada dentro desse mapa.

```elixir
iex> mapa = %{a: 1, a: 2, b: 3}
warning: key :a will be overridden in map
  iex:1

%{a: 2, b: 3}
```
## Como acessar mapas
Através das chaves:
```elixir
iex> mapa2 = %{"a" => 1, "b" => 2}
%{"a" => 1, "b" => 2}

iex> mapa2["a"]
1
```

Ou se as chaves do mapa forem atomos, pode-se acessar através de ponto:

```elixir
iex> mapa = %{a: 1, b: 2}
%{a: 1, b: 2}
iex> mapa.a
1

iex> mapa.b
2
```

## Atualizando mapas

Ao atualizar mapas, não importa a ordem das chaves. É necessário seguir uma estrutura específica. Apenas as chaves que já existem nos mapas podem ser atualizadas, não é possível incluir novas chaves por meio de atualização.

```elixir
iex> mapa = %{a: 1, b: 2}
%{a: 1, b: 2}

iex> %{mapa | b: 5, a: 4}
%{a: 4, b: 5}
```
Lembrando que no Elixir as atualizações não alteram os dados originais sem uma reatribuição:

```elixir
iex> mapa = %{a: 1, b: 2}
%{a: 1, b: 2}

iex> %{mapa | b: 5, a: 4}
%{a: 4, b: 5}

iex> mapa
%{a: 1, b: 2}

iex> mapa = %{mapa | b: 5, a: 4}
%{a: 4, b: 5}

iex> mapa
%{a: 4, b: 5}
```
[<<< Tuplas ](tuplas.md)| - - - - - - - - - - - -|[ Início ](/README.md)| - - - - - - - - - - - -|[ Coleções >>>](README.md)