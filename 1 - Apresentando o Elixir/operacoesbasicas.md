# Operações básicas:

* [Operadores aritiméticos](#operadores-aritméticos)

* [Operadores relacionais](#operadores-relacionais)

* [Operadores Comparativos](#operadores-comparativos)

* [Interpolação de Strings](#interpolação-de-strings-colocar-uma-string-dentro-de-outra)


## Operadores aritméticos:
```elixir
iex> 2 + 2
4

iex> 3 - 5
-2

iex> 2 * 5
10

iex> 20 / 3   
6.666666666666667
```

FUNÇÃO DIV: Retorna a parte inteira da divisão, ao contrário do resultado do operador "/" que retorna um boleano.
```elixir
iex> div(20,3)
6
```

FUNÇÃO REM: Retorna o resto da divisão.
```elixir
iex> rem(20,3)
2
```

## Operadores relacionais:
! (Não - retorna o contrário):
```elixir
iex> true
true

iex> !true
false

iex> false
false

iex> !false
true
```

&& (E - retorna true apenas se as duas parte comparadas forem verdadeiras).
```elixir
iex> true && true
true

iex> true && false
false
```

|| (OU - Retorna true se pelo menos umas das partes forem verdadeiras).
```elixir
iex> true || false
true

iex> false || false
false
```

AND, OR (Diferente do && e ||, o and, or e not verificam se a primeira parte da comparação é um boleano para então prosseguir com a verificação. Caso contrário, é retornado um erro):
```elixir
iex> 1 and true
** (BadBooleanError) expected a boolean on left-side of "and", got: 1

iex> true and 1
1

iex> false or true
true

iex> false or 3
3
```

## Operadores Comparativos:

Maior que:
```elixir
iex> 1 > 2
false
```

Menor que:
```elixir
iex> 1 < 2
true
```


Menor ou igual:
```elixir
iex> 1 <= 2
true
```


Maior ou igual:
```elixir
iex> 2 >= 2
true
```


Igual a:
```elixir
iex> 2 == 2
true
```


Diferente de:
```elixir
iex> 2 != 2
false
```


Identico a:
```elixir
iex> 2 === 2.0
false
```

## Interpolação de strings: 
Colocar uma string dentro de outra.
```elixir
iex> nome = "Rafaela"
"Rafaela"

iex> "Meu nome é #{nome}"
"Meu nome é Rafaela"
```

Concatenação de strings:
```elixir
iex> nome = "Rafaela"
"Rafaela"

iex> "Meu nome é " <> nome
"Meu nome é Rafaela"
```

 [<<< Tipos Básicos](tiposbasicos.md) | - - - - - - - - - - - - - -| [ Início](/README.md) |- - - - - - - - - - - - - -|[ Apresentando o Elixir >>>](operacoesbasicas.md)