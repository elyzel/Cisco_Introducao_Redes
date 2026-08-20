## Private IPv4 Addresses and Network Address Translation (NAT)

A maioria das redes internas, de grandes empresas a redes domésticas, usa endereços IPv4 privados para endereçar todos os dispositivos internos (intranet), incluindo hosts e roteadores. No entanto, os endereços privados não são globalmente roteáveis.

![[Pasted image 20260820115620.png]]

Antes que o ISP possa encaminhar esse pacote, ele deve traduzir o endereço IPv4 de origem, que é um endereço privado, para um endereço IPv4 público usando a Conversão de Endereços de Rede (NAT). __O NAT__ é usado para converter entre endereços IPv4 privados e IPv4 públicos. Isso geralmente é feito no roteador que conecta a rede interna à rede ISP. Os endereços IPv4 privados na intranet da organização serão traduzidos para endereços IPv4 públicos antes do encaminhamento para a Internet.

## Endereços IPv4 de Uso Especial

Existem determinados endereços, como o endereço de rede e o endereço de broadcast, que não podem ser atribuídos aos hosts. Há também endereços especiais que podem ser atribuídos a hosts, mas com restrições quanto ao modo como interagem na rede.

**Endereços de loopback**

Os endereços de loopback (127.0.0.0 / 8 ou 127.0.0.1 a 127.255.255.254) são comumente identificados apenas como 127.0.0.1. Eles são endereços especiais usados por um host para direcionar tráfego para ele mesmo Por exemplo, o comando **ping** é comumente usado para testar conexões com outros hosts. Mas você também pode usar o comando **ping** para testar a configuração de IP do seu próprio dispositivo, como mostrado na figura.

```powershell
C:∖Users∖NetAcad> ping 127.0.0.1

Pinging 127.0.0.1 with 32 bytes of data:

Reply from 127.0.0.1: bytes=32 time<1ms TTL=128

Reply from 127.0.0.1: bytes=32 time<1ms TTL=128

Reply from 127.0.0.1: bytes=32 time<1ms TTL=128

Reply from 127.0.0.1: bytes=32 time<1ms TTL=128

Ping statistics for 127.0.0.1:

    Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),

Approximate round trip times in milli-seconds:

    Minimum = 0ms, Maximum = 0ms, Average = 0ms

C:∖Users∖NetAcad> ping 127.1.1.1

Pinging 127.1.1.1 with 32 bytes of data:

Reply from 127.1.1.1: bytes=32 time<1ms TTL=128

Reply from 127.1.1.1: bytes=32 time<1ms TTL=128

Reply from 127.1.1.1: bytes=32 time<1ms TTL=128

Reply from 127.1.1.1: bytes=32 time<1ms TTL=128

Ping statistics for 127.1.1.1:

    Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),

Approximate round trip times in milli-seconds:

    Minimum = 0ms, Maximum = 0ms, Average = 0ms

C:∖Users∖NetAcad>
```

>[!abstract]
>Endereços Locais de Link: Os endereços locais de link (169.254.0.0 / 16 ou 169.254.0.1 a 169.254.255.254) são mais conhecidos como endereços APIPA ( endereçamento IP privado automático ) ou endereços auto-atribuídos. Eles são usados por um cliente Windows para se autoconfigurar caso o cliente não consiga obter um endereçamento IP por outros métodos. Endereços de link local podem ser usados em uma conexão ponto a ponto, mas não são comumente usados para esse fim.


## Endereçamento Classful Legado

Em 1981, os endereços IPv4 foram atribuídos usando o endereço classful, conforme definido na RFC 790 ([https://tools.ietf.org/html/rfc790](https://datatracker.ietf.org/doc/html/rfc790)), Números Atribuídos Os clientes receberam um endereço de rede com base em uma das três classes, A, B ou C. A RFC dividiu os intervalos de unicast em classes específicas da seguinte maneira:

- **Classe A (0.0.0.0/8 to 127.0.0.0/8)** – Projetado para suportar redes extremamente grandes com mais de 16 milhões de endereços de host. A Classe A usou um prefixo fixo /8 com o primeiro octeto para indicar o endereço de rede e os três octetos restantes para endereços de host (mais de 16 milhões de endereços de host por rede).
- **Classe B (128.0.0.0 / 16 - 191.255.0.0 / 16)** - Projetada para oferecer suporte às necessidades de redes de tamanho moderado a grande com até aproximadamente 65.000 endereços de host. A Classe B usou um prefixo fixo /16 com os dois octetos de alta ordem para indicar o endereço de rede e os dois octetos restantes para endereços de host (mais de 65.000 endereços de host por rede).
- **Classe C (192.0.0.0 / 24 - 223.255.255.0 / 24)** - Projetado para oferecer suporte a pequenas redes com no máximo 254 hosts. A Classe C usou um prefixo fixo / 24 com os três primeiros octetos para indicar a rede e o octeto restante para os endereços de host (apenas 254 endereços de host por rede).

**Observação:** Há também um bloco multicast Classe D consistindo de 224.0.0.0 a 239.0.0.0 e um bloco de endereço experimental Classe E consistindo de 240.0.0.0 - 255.0.0.0.

Na época, com um número limitado de computadores usando a internet, o endereçamento clássico era um meio eficaz para alocar endereços. Como mostrado na figura, as redes de classe A e B têm um número muito grande de endereços de host e Classe C tem muito poucos. As redes de classe A representaram 50% das redes IPv4. Isso fez com que a maioria dos endereços IPv4 disponíveis não fossem utilizados.

![[Pasted image 20260820131251.png]]


## Atribuição de Endereços IP

__Endereços IPv4 públicos são endereços roteados globalmente pela Internet__. Endereços IPv4 públicos devem ser exclusivos.

Os endereços IPv4 e IPv6 são gerenciados pela __IANA (Internet Assigned Numbers Authority)__. A IANA gerencia e aloca blocos de endereços IP aos registros regionais de Internet (RIRs). Os cinco RIRs são mostrados na figura.

Os __RIRs__ são responsáveis por alocar endereços IP aos __ISPs__ que fornecem blocos de endereços IPv4 para organizações e ISPs menores. As organizações também podem obter seus endereços diretamente de um RIR (sujeito às políticas desse RIR).

![[Pasted image 20260820131442.png]]