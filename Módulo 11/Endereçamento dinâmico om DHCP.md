Os endereços IPv4 podem ser atribuídos __estática__ ou __dinamicamente__.

Com uma atribuição estática, o administrador de rede deve configurar manualmente as informações da rede para um host. No mínimo, isso inclui o seguinte:

- **Endereço IP**– Identifica o computador na rede.
- **Máscara de Sub-rede** - Identifica a rede à qual o host está conectado
- **Gateway padrão** – Identifica o dispositivo de rede que o host usa para acessar a Internet ou outra rede remota.

## Endereços Estáticos

| __Vantagens__                                 | __Desvantagens__            |
| --------------------------------------------- | --------------------------- |
| Úteis para impressora e outros dispositivos   | Maior tempo de configuração |
| Controle maior dos recursos de rede           |                             |
| Aumento de probabilidade de que ocorram erros |                             |

![[Pasted image 20260825144351.png]]


## Endereçamento dinâmico

Nas redes locais, geralmente, a população de usuários muda com frequência. Novos usuários chegam com notebooks e precisam de uma conexão. Outros têm novas estações de trabalho que precisam ser conectadas. Em vez de fazer com que o administrador de rede atribua endereços IPv4 em cada estação de trabalho, é mais eficiente ter endereços IPv4 atribuídos __automaticamente.__

> [!abstract]
A atribuição de IP é feita automaticamente pelo __Dynamic Host Configuration Protocol (DHCP)__.


O DHCP fornece um mecanismo para atribuição automática de informações de endereçamento, como endereço IPv4, máscara de sub-rede, gateway padrão e outras informações de configuração, como mostrado na figura.

![[Pasted image 20260825144603.png]]

Outro benefício do DHCP é que o endereço não é permanentemente atribuído a um host, mas é só “alugado” por um período. Se o host é desligado ou retirado da rede, o endereço retorna ao pool para ser reutilizado. Isso é especialmente útil com usuários móveis que vêm e vão em uma rede.

## Servidores DHCP

Se você inserir um hotspot sem fio em um aeroporto ou uma lanchonete, o DHCP possibilitará o acesso à Internet. Ao entrar na área, o cliente DHCP de seu laptop entra em contato com o servidor DHCP local via conexão sem fio. O servidor DHCP atribui um endereço IPv4 ao seu notebook.

Nas redes residenciais, é provável que o servidor DHCP esteja localizado no ISP. Um host na rede residencial recebe a configuração IPv4 diretamente do ISP, como mostrado na figura.

![[Pasted image 20260825144729.png]]

