![[Pasted image 20260820132211.png]]


## Domínios de Broadcast e Segmentação

Em uma LAN Ethernet, os dispositivos usam broadcast e o Protocolo de Resolução de Endereços (ARP) para localizar outros dispositivos. O __ARP__ envia broadcasts dea Camada 2 para um endereço IPv4 conhecido na rede local para descobrir o endereço MAC associado. Os dispositivos em LANs Ethernet também localizam outros dispositivos usando serviços. Um host normalmente adquire sua configuração de endereço IPv4 usando o protocolo DHCP (Dynamic Host Configuration Protocol) que envia broadcasts na rede local para localizar um servidor DHCP.

Os switches propagam broadcasts por todas as interfaces, exceto a interface em que foram recebidos. Por exemplo, se um switch na figura recebesse um broadcast, ele o encaminharia para os outros switches e os outros usuários conectados na rede.

![[Pasted image 20260820132329.png]]


Roteadores não propagam broadcasts. Quando um roteador recebe um broadcast, ele não o encaminha por outras interfaces. Por exemplo, quando R1 recebe um broadcast na interface Gigabit Ethernet 0/0, ele não o encaminha por outra interface.

Portanto, cada interface do roteador se conecta a um domínio de broadcast e as transmissões são propagadas apenas dentro desse domínio de broadcast específico.

## Problemas com Domínios de Broadcast Grandes

Um grande domínio de broadcast é uma __rede que conecta vários hosts__. Um problema desse tipo de domínio é que os hosts podem gerar __broadcasts em excesso__ e afetar a rede de forma negativa. Na figura, a LAN 1 conecta 400 usuários que podem gerar uma quantidade excessiva de tráfego de broadcast. Isso resulta em operações de rede lentas devido à quantidade significativa de tráfego que pode causar e operações de dispositivo lentas porque um dispositivo deve aceitar e processar cada pacote de difusão.

![[Pasted image 20260820133012.png]]

## Comunicação entre Redes

A solução é reduzir o tamanho da rede para criar domínios de broadcast menores em um processo denominado divisão em __sub-redes__. __Os espaços de rede menores são chamados de sub-redes.__

Na figura, os 400 usuários da LAN 1 com endereço de rede 172.16.0.0/16 foram divididos em duas sub-redes de 200 usuários cada: 172.16.0.0/24 e 172.16.1.0/24. Os broadcasts são propagados apenas dentro dos domínios de broadcast menores. Portanto, um broadcast em LAN 1 não se propagaria para LAN 2.

![[Pasted image 20260820133310.png]]

Observe como o comprimento do prefixo mudou de /16 para /24. Esta é a base da divisão em sub-redes: usar bits de host para criar sub-redes adicionais.

**Observação**: os termos sub-rede e rede costumam ser usados de maneira intercambiável. A maioria das redes são uma sub-rede de um bloco de endereços maior.

## Razões para Segmentar Redes

A divisão em sub-redes reduz o tráfego total da rede e melhora seu desempenho. Além disso, permite que o administrador implemente políticas de segurança como, por exemplo, quais sub-redes podem ou não se comunicar com quais sub-redes. Outra razão é que reduz o número de dispositivos afetados pelo tráfego anormal de transmissão devido a configurações incorretas, problemas de hardware/software ou intenção mal-intencionada.

Há várias maneiras de usar sub-redes para gerenciar dispositivos de rede.

- __Localização:__ Divisão de Sub-Redes por Local
![[Pasted image 20260820133550.png]]

- __Grupo ou Função:__ Sub-redes por grupo ou função
![[Pasted image 20260820133617.png]]

- __Tipo de Dispositivo:__ Divisão em sub-Redes por Tipo de Dispositivo
![[Pasted image 20260820133643.png]]

Os administradores de rede podem criar sub-redes usando qualquer outra divisão que faça sentido para a rede. Observe nas figuras que as sub-redes usam comprimentos de prefixo para identificar redes.

É fundamental que todos os administradores de redes entendam a divisão da rede em sub-redes. Vários métodos foram criados para ajudar a entender esse processo. Embora um pouco esmagador a princípio, preste muita atenção aos detalhes e, com a prática, a sub-rede se tornará mais fácil.

## Gabarito

![[Pasted image 20260820140211.png]]

