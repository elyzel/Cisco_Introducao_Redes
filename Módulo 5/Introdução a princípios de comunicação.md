# O que são Protocolos?

Protocolos são as regras que regem as comunicações de rede, incluindo o formato, o tamanho, a temporização e o encapsulamento da mensagem.

# Protocolos de Comunicação

- __Método__:
	Antes que a comunicação possa começar, talvez tenhamos que chegar a um acordo sobre o idioma usado. (Anotações, Linguagem de Sinais, Oratória)
- __Idioma__:
	Antes que a comunicação possa começar, talvez tenhamos que chegar a um acordo sobre o idioma usado. (Inglês, português, espanhol)
- Confirmação
	A comunicação é bem-sucedida quando a mensagem pretendida foi recebida.

# Por que os protocolos são importantes?

Assim como os seres humanos, os computadores usam regras para para se comunicarem. Os protocolos são necessários para que os computadores se comuniquem corretamente na rede. Em ambiente com fio ou sem fio, uma rede local é definida como uma área onde todos os hosts devem "falar a mesma linguagem", ou seja, __"compartilhar um protocolo em comum"__.

| **Características de procolo** | **Descrição**                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| ------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Formato de mensagem            | Quando uma mensagem e enviada, ela deve usar um formato ou estrutura específica. Os formatos da<br>mensagem dependem do tipo de mensagem e do canal usado para entregá-la.                                                                                                                                                                                                                                                                                   |
| Tamanho da mensagem            | As regras que regem o tamanho das partes transmitidas por meio da rede sao muito rigidas. Eles tambem<br>podem ser diferentes, dependendo do canal usado. Quando uma mensagem longa é enviada de um host<br>para outro em uma rede, pode ser necessario dividir a mensagem em partes menores para garantir que<br>ela seja entregue de forma confiável.                                                                                                      |
| Temporização                   | Muitas funções de comunicação de rede dependem de temporização. A temporização determina a<br>velocidade com que os bits sao transmitidos na rede. Tambem afeta quando um host individual pode<br>enviar dados e a quantidade total de dados que pode ser enviada em qualquer transmissão.                                                                                                                                                                   |
| Codificação                    | As mensagens enviadas pela rede sao convertidas primeiramente em bits pelo host emissor. Cada bit e<br>codificado em um padrao de sons, de ondas de luz ou de impulsos elétricos, dependendo da mídia de<br>rede em que os bits sao transmitidos. O host de destino recebe e decodifica os sinais para interpretar a<br>mensagem.                                                                                                                            |
| Encapsulamento                 | Cada mensagem transmitida em uma rede deve incluir um cabeçalho com informações de<br>endereçamento que identifique os hosts de origem e destino. Caso contrário, ela não poderá ser<br>entregue. Encapsulamento e o processo de adicionar essas informacoes aos dados que compoem a<br>mensagem. Além do endereçamento, podem existir outras informações no cabeçalho que garantem que<br>a mensagem foi entregue ao aplicativo correto no host de destino. |
| Padrão de mensagem             | Algumas mensagens exigem uma confirmação antes que a próxima mensagem possa ser enviada. Esse<br>tipo de padrão de solicitação/resposta é um aspecto comum em muitos protocolos de rede. No entanto,<br>existem outros tipos de mensagens que podem ser simplesmente transmitidas pela rede, sem a<br>preocupação de chegarem ao seu destino.                                                                                                                |


