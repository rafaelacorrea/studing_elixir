# Introdução ao Elixir

No terminal, esse é o comando para usar o ambiente interativo do Elixir: 
```elixir
> iex
```

Para acessar números através de binários é só incluir "0b" antes dos binários no iex e é retornado o numero referente.
```elixir
iex> 0b0110
6
```
## Tipos básicos

INTEIROS: Números positivos ou negativos incluindo o zero que não possuem partes decimais.
```elixir
iex> -5
-5
```

FLUTUANTES: Números que contém uma parte decimal.
```elixir
iex> 0.6
0.6
```

BOLEANOS: true, false.
```elixir
iex> true
true
iex> false
false
```

ATOMOS: é uma constante, a palavra é seu próprio valor. Não sendo possível iniciar com números.
```elixir
iex> :casa
:casa
```

STRINGS: textos com letras e caracteres especiais dentro de aspas duplas, aceitando quebra de linha por padrão.
```elixir
iex(7)> "Olá, mundo"
"Olá, mundo"
```

## Operações básicas:

### Opredores aritméticos:
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

### Operadores relacionais:
!(Não - retorna o contrário):
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

&&(E - retorna true apenas se as duas parte comparadas forem verdadeiras).
```elixir
iex> true && true
true
iex> true && false
false
```

||(OU - Retorna true se pelo menos umas das partes forem verdadeiras).
```elixir
iex> true || false
true
iex> false || false
false
```

AND, OR(Diferente do && e ||, o and, or e not verificam se a primeira parte da comparação é um boleano para então prosseguir com a verificação. Caso contrário, é retornado um erro):
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

### Operadores Comparativos:

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

Interpolação de strings: Colocar uma string dentro de outra.
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