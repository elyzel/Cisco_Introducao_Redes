# Finalidade do IPV4

__O endereço IPV4 é um endereço de rede lógico que identifica um host específico.__ Ele deve ser configurado corretamente e de forma exclusiva no mundo, para fornecer comunicação remota. É assim que um host se comunica com outros dispositivos na internet.

Um endereço IPv4 é atribuído à conexão de interface de rede um host. __Essa conexão geralmente é uma placa de interface de rede (NIC) instalado no dispositivo__. Estações de trabalho, servidores, impressoras de rede e telefones IP são exemplos de dispositivos de usuário final com interfaces de rede.

__Cada pacote enviado pela Internet tem um endereço IPv4 de origem e de destino__. Essa informação é necessária para os dispositivos de rede garantirem que os dados cheguem ao destino e que as respostas sejam retornadas à origem.

![[Pasted image 20260819110811.png]]


# Octetos e notação decimal com ponto

O limite máximo de um IPV4 é de 32 bits de comprimento. Aqui está um endereço IPV4 em binário:
**11010001101001011100100000000001**

Imagine ter que configurar dispositivos com uma série de 32 bits! Por esse motivo, os 32 bits são agrupados em quatro bytes de 8 bits chamado __octetos__:
**11010001.10100101.11001000.00000001**

Está melhor, mas ainda assim difícil de ler. É por isso que convertemos cada octeto em seu __valor decimal__, separados por um ponto decimal ou por um período. O IPv4 binário acima torna-se esta representação decimal com ponto:
**209.165.200.1**

# A estrutura do endereço IPV4

O endereço lógico IPv4 de 32 bits é hierárquico e contém duas partes, a rede e o host Na figura, a porção de rede é azul e a porção de host é vermelha. As duas partes são necessárias em um endereço IPv4:

![[Pasted image 20260819112651.png]]

Ambas as redes têm a máscara de sub-rede 255.255.255.0. __Máscara de sub-rede é usada para identificar a rede à qual o host está conectado.__

Como exemplo, um host com o endereço IPv4 __192.168.18.99__ e a máscara de sub-rede 255.255.255.0. __Os três primeiros octetos (192.168.18)__ identificam a __porção de rede do endereço__ e o __último octeto (11)__ identifica o __host__. Isso é conhecido como endereçamento hierárquico porque a porção de rede indica a rede na qual está localizado cada endereço exclusivo de host.

Com o endereçamento IPv4, poderão existir diversas redes lógicas em uma rede física se a porção de rede dos endereços de hosts de rede lógica for diferente. 

Por exemplo: três hosts em uma única rede local física têm a mesma porção de rede do endereço IPv4 (192.168.18) e outros três hosts têm porções de rede diferentes de seus endereços IPv4 (192.168.5). __Os hosts com o mesmo número de rede em seus endereços IPv4 poderão se comunicar entre si__, mas não com os outros hosts sem o uso de roteamento. Neste exemplo, há uma rede física e duas redes IPv4 lógicas.

![[Pasted image 20260819113049.png]]


1. O Host-A tem o endereço IPv4 e a máscara de sub-rede 10.5.4.100 __255.255.255.0__. Qual é o endereço de rede do Host-A?

	10.5.4.0

2. O Host-A tem endereço IPv4 e máscara de sub-rede 172.16.4.100 __255.255.0.0__. Qual é o endereço de rede do Host-A?

	172.16.0.0

3. 