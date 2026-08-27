# Domínios de Broadcast

Quando um host recebe uma mensagem endereçada ao endereço de broadcast, ele aceita e processa a mensagem como se ela tivesse sido endereçada diretamente a ele. Quando um host envia uma mensagem de broadcast, os switches encaminham a mensagem para cada host conectado na mesma rede local. Por esse motivo, uma rede local (ou seja, uma rede com um ou mais switches Ethernet) também é conhecida como domínio de broadcast.

Se muitos hosts estiverem conectados ao mesmo domínio de broadcast, o tráfego de broadcast poderá ficar excessivo. O número de hosts e a quantidade de tráfego de rede que pode ser suportada na rede local são limitados pelos recursos dos switches usados para conectá-los. À medida que a rede cresce e mais hosts são adicionados, o tráfego de rede aumenta, inclusive o tráfego de broadcast. Para melhorar o desempenho, geralmente é necessário dividir uma rede local em várias redes (ou seja, domínios de broadcast), como mostrado na figura. Os roteadores são usados para dividir a rede em vários domínios de broadcast.

![[Pasted image 20260827163809.png]]


# Comunicação na camada de Acesso

Em uma rede Ethernet local, uma NIC só aceitará um quadro se o endereço de destino for o endereço MAC de broadcast ou corresponder ao endereço MAC da NIC.

A maioria dos aplicativos de rede, entretanto, baseiam-se no endereço IP lógico de destino para identificar a localização de servidores e clientes. A figura ilustra o problema de um host emissor ter apenas o endereço IP lógico do host de destino. Como o host emissor determina o endereço MAC de destino a ser colocado no quadro?

O host emissor pode usar um protocolo IPv4 chamado ARP (Address Resolution Protocol) para descobrir o endereço MAC de qualquer host na mesma rede local. O IPv6 usa um método semelhante conhecido como Descoberta de Vizinhos (Neighbor Discovery).

![[Pasted image 20260827163833.png]]

