# Anotações Importantes

Regex, ou expressões regulares, é uma linguagem para encontrar padrões de texto.
Sendo uma linguagem independente, existem interpretadores para a maioria das plataformas de desenvolvimento, como JavaScript, C#, Python ou Ruby.
Uma classe de caracteres predefinida é \d, que significa qualquer dígito.
Existem vários meta-char, como . ou *.
Existem quantifiers que definem quantas vezes um caractere deve aparecer:
{1} é um quantifier que significa uma vez.
* é um quantifier que significa zero, uma ou mais vezes
. é um meta-char que significa qualquer char.
Com \ podemos escapar meta-chars, por exemplo \..

## Capturando Telefone

**(21) 3216-2345**

````js
\(\d{2}\) \d{4}-\d{4}
````

Quebrou a cabeça? O parênteses é um meta caracter de grupo, algo que ainda aprenderemos. Sendo assim, precisamos escapá-lo com um \ quando temos o interesse de encontrá-lo em uma string.

A regex não está perfeita pois o telefone poderia variar, por exemplo ter com 9 números ou um 0 na frente do DDD (além de definir melhor o espaço). Nos próximos capítulos veremos como definir essas possibilidades.

## Capturando <\code>


**No <code>for</code>, o valor de <code>i</code> começa de zero e é incrementado a cada volta enquanto <code>i < 10</code>, portando o bloco de código do for é executado 10 vezes.**

````js
</?code>
````

## Capturando os números entre 1 e 3 E 6 e 9

````js
[1-36-9]
````

## Capturando CPF

## Capturando hora

**19h32min16s**

````js
\[0-9]{2}h\[0-9]{2}min\[0-9]{2}s
````

````js
[0-9]{2}h[0-9]{2}min[0-9]{2}s
````

## Capturando placa de Carro

**KMG-8089**

````js
[A-Z]{3}-\d{4}
````

## Capturando Notas

**9.8 - Robson, 7.1 - Teresa, 4.5 - Armênio, 6.5 - Zulu, 7.7 - Stefania, 7.8 - João, 5.0 - Romeu, 7.2 - Pompilho, 3.1 - Reinaldo, 7.3 - Bernadete, 4.7 - Cinério**

````js
7\.[2-9]\s+-\s+[^,]+
````

## Capturando palavras maiúsculas

**BALEIRO GARROTE SERROTE GOLEIRO ROTEIRO**

````js
[A-Z]*ROT[A-Z]+
````

## Capturando UserName

````js
@POST
@Path("/user")
@Consumes(MediaType.APPLICATION_JSON)
public Response listaDeRestaurantes(@Valid User user) { 
    // codigo omitido
}
````
````js

