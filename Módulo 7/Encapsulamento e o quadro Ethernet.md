
# Encapsulamento e o quadro Ethernet

Ao enviar uma carta, quem a escreve usa um formato aceito para garantir que ela seja entregue e compreendida pelo destinatário. Da mesma forma, a mensagem enviada por uma rede de computadores segue regras específicas de formato para que seja entregue e processada.

O processo de colocar um formato de mensagem (a carta) em outro formato de mensagem (o envelope) é chamado de __encapsulamento__.

Cada mensagem de computador é encapsulada em um formato especifico, chamado de __quadro__, antes de ser enviado pela rede. Um quadro atua como um envelope: ele fornece o endereço do destino desejado e o endereço do host de origem.

### Analogia

Um envelope tem o endereço do remetente e do destinatário, cada um localizado no local apropriado do envelope. Se o endereço de destino e a formatação não estiverem corretos, a carta não será entregue.

O processo de colocar um formato de mensagem (a carta) em outro formato de mensagem (o envelope) é chamado __encapsulamento__. O desencapsulamento ocorre quando o processo é invertido pelo destinatário e a carta é retirada do envelope.

![[Pasted image 20260818143731.png]]

### Rede

Internet Protocol (IP) é um protocolo com uma função semelhante ao exemplo de envelope. Na figura, os campos do pacote IPv6 (Internet Protocol versão 6) identificam a origem do pacote e seu destino. O IP é responsável por enviar uma mensagem da origem para o destino através de uma ou mais redes.

![[Pasted image 20260818143844.png]]


# Camadas de Acesso

1. __Os switches Ethernet tomam a decisão de encaminhamento com base em qual campo do quadro Ethernet?__

Os switches Ethernet tomam sua decisão de encaminhamento com base no endereço MAC de destino.

2. __Os switches Ethernet adicionam entradas à tabela de endereços MAC com base em qual campo do quadro Ethernet?__

Os switches Ethernet adicionam entradas à sua tabela de endereços MAC com base no endereço MAC de origem.

3. __Quando um switch recebe um quadro Ethernet e o endereço MAC de destino desse quadro não está em sua tabela de endereços MAC, o switch:__

Ao receber um quadro de entrada com um endereço MAC de destino que não está listado na tabela de endereços MAC, o switch encaminha o quadro para todas as portas, exceto para a porta de entrada do quadro.

4. __Os hubs Ethernet são considerados:__

