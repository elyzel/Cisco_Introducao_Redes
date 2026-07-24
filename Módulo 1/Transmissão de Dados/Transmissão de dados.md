
# Tipos de Dados

## Dados Voluntários

Dados voluntários são dados que você mesmo fornece e concorda em compartilhá-los para armazenar em alguma rede.

## Dados Inferidos

Dados inferidos são dados que você gera por suas atividades  e não percebe.

Exemplo:

Se você mora nos Estados Unidos e compra alguma coisa em um país estrangeiro, o registro feito na momento da compra informar a sua localização e qual loja ou pessoa está comprando, logo, denominamos como __dados inferidos__.

## Dados Observados

Dados observados são dados compartilhados e armazenados passivamente para uma grande "Big Data", ou seja, uma grande nuvem armazenando dados a todo momento sem ninguém a partir do momento de uma ativação de um recurso que o usuário esqueceu, como: localização

<div style="page-break-after: always;"></div>
---
# O Bit

Computadores utilizam dígitos binários para se comunicar, ou seja, são compostos por 0 e 1. O bit é uma abreviação de "dígito binário" e representa a menor parte de dados.

Os computadores utilizam código binários para representar letras, números e caracteres especiais com bits. Um código muito usado é o ASCII (American Standard Code for information), sendo usado para representar praticamente qualquer tipo de informação digital.

> [!NOTE]
> Letra Maiúscula: A = 0100001
> Número: 9 = 00111001
> Caractere especial: # = 00100011

## Como converter um número, letra ou caractere especial em binário

Exemplo:

Vamos converter a letra "A" em binário:

__Passo 1: Encontrar o valor decimal__

Na tabela [ASCII](https://www.binaryhexconverter.com/ascii-text-to-binary-converter), a letra **A** equivale ao número **65**. 

__Passo 2: Fazer divisões sucessivas por 2__

Divida o número por 2 repetidamente e anote o resto de cada operação (que sempre será 0 ou 1):

- **65 ÷ 2** = 32 (resto **1**)
- **32 ÷ 2** = 16 (resto **0**)
- **16 ÷ 2** = 8 (resto **0**)
- **8 ÷ 2** = 4 (resto **0**)
- **4 ÷ 2** = 2 (resto **0**)
- **2 ÷ 2** = 1 (resto **0**)
- **1 ÷ 2** = 0 (resto **1**)

Passo 3: Ler os restos de baixo para cima

Junte os restos começando do último resultado até o primeiro:

- Resultado: **`1000001`** (7 dígitos)

Passo 4: Preencher com 8 bits

Como um byte padrão possui 8 bits, adicionamos um zero à esquerda para completar o bloco:

- Resultado final: **`01000001`**

<div style="page-break-after: always;"></div>
---

# Métodos comuns de transmissão de dados

Após os dados são transformados em uma série de bits, devem ser convertido em sinais que são enviados até o destino através de suas mídas.

> [!INFO]
> Mídias são qualquer tipo de meio físico responsável por transmitir os sinais.

Exemplos de sinais:
- Sinais Elétricos: representação de dados em forma de pulsos elétricos
- Sinais Ópticos: conversão de sinais elétricos em pulsos de luz
- Sinais sem fio: transmissão é feita por uso de infravermelho, micro-ondas ou ondas de rádio pelo ar.

![[Pasted image 20260724134614.png]]


