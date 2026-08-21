# Sistema Hexadecimal

Antes de abordar o endereçamento IPv6, é importante que você saiba que os endereços IPv6 são representados usando __números hexadecimais__. Este sistema numérico, de base dezesseis, usa os dígitos de 0 a 9 e as letras de A a F:

**0 1 2 3 4 5 6 7 8 9 A B C D E F**

Nos endereços IPv6, esses 16 dígitos são representados por hextetos (discutidos a seguir), permitindo representar esses endereços enormes em um formato muito mais legível.

# Segmentos ou Hextets de 16 bits

Os endereços IPv6 têm 128 bits e são escritos como uma sequência de valores hexadecimais. Cada 4 bits são representados por um único dígito hexadecimal, totalizando 32 valores hexadecimais, como mostra a Figura 1. Os endereços IPv6 não diferenciam maiúsculas e minúsculas e podem ser escritos tanto em minúsculas como em maiúsculas.

![[Pasted image 20260821112941.png]]

Formato preferencial significa que o endereço IPv6 é gravado usando __todos os 32 dígitos hexadecimais__. Isso não significa necessariamente que é o método ideal para representar o endereço IPv6. Existem duas regras que ajudam a reduzir o número de dígitos necessários para representar um endereço IPv6.

# Regras do IPv6

## Regra 1 - Omitir os zeros à esquerda

A primeira regra para ajudar a reduzir a notação de endereços IPv6 é omitir os 0s (zeros) à esquerda de qualquer seção de 16 bits ou
hexteto. Aqui estão quatro exemplos de maneiras de omitir zeros à esquerda:

. 01AB pode ser representado como 1AB
· 09f0 pode ser representado como 9f0
· 0a00 pode ser representado como a00
. 00ab pode ser representado como ab

## Regra - 2 - Dois pontos duplos

10.2.5 Regra 2- Dois pontos duplos

A segunda regra para ajudar a reduzir a notaçao de endereços IPv6 é que dois pontos duplos ( :: ) podem substituir qualquer string única
e contigua de um ou mais hextetos de 16 bits consistindo em zeros. Por exemplo, 2001:db8:cafe: 1:0:0:0:1 (Os iniciais omitidos) poderia
ser representado como 2001:db8:cafe:1 :: 1. Os dois-pontos duplos ( :: ) sao usados no lugar dos tres hextetos compostos por zeros
(0:0:0).

Os dois-pontos duplos ( :: ) so podem ser usados uma vez dentro de um endereco, caso contrario, haveria mais de um endereço
resultante possível. Quando associada à tecnica de omissao dos Os à esquerda, a notaçao do endereço IPv6 pode ficar bastante
reduzida. E o chamado formato compactado.

Aqui esta um exemplo do uso incorreto dos dois pontos duplos: 2001:db8 :: abcd :: 1234.

Os dois pontos duplos sao usados duas vezes no exemplo acima. Aqui estao as possiveis expansoes possíveis deste endereço de
formato compactado incorretamente:

. 2001:db8 :: abcd:0000:0000:1234
. 2001:db8 :: abcd:0000:0000:0000:1234
. 2001:db8:0000:abcd :: 1234
. 2001:db8:0000:0000:abcd :: 1234

Se um endereço tiver mais de uma string contígua de hextetos com zero, a melhor prática é usar dois pontos duplos ( :: ) na string mais
longa. Se as strings forem iguais, a primeira string deve usar dois pontos duplos ( :: ).

