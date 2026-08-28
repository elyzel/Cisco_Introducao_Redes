
São muitos os serviços que acessamos pela Internet ao longo do dia. DNS, Web, E-mail, FTP, Mensagem instantânea e VoIP são apenas alguns desses serviços que são disponibilizados por sistemas cliente/servidor em todo o mundo. Eles podem ser fornecidos por um único servidor ou por vários servidores em grandes datacenters.

Quando uma mensagem é entregue usando o TCP ou o UDP, os protocolos e os serviços são identificados por um número de porta. Uma porta é um identificador numérico dentro de cada segmento que é usado para rastrear conversas específicas entre um cliente e um servidor. Cada mensagem que um host envia contém uma porta origem e destino.

![[Pasted image 20260828112434.png]]

Quando uma mensagem e recebida por um servidor, e necessário que o servidor consiga determinar qual serviço esta sendo solicitado pelo cliente. Os clientes são reconfigurados para usar uma porta de destino que foi registrada na Internet para cada serviço. Um exemplo disso são os clientes de navegador da Web, que são configurados previamente para enviar solicitações para servidores da Webpela porta 80, a porta usada normalmente para serviços da Web em HTTP.

As portas são atribuídas e gerenciadas por uma organização conhecida como ICANN (Internet Corporation for Assigned Names andNumbers, Corporação da Internet para Atribuição de Nomes e Números). As portas foram divididas em três categorias e variam em número de 1 a 65.535.

. Portas bem conhecidas - As portas de destino que estão associadas a aplicativos de rede comuns são identificadas como portas bem conhecidas. Elas estão no intervalo de 1 a 1.023.
· Portas registradas - As portas 1.024 a 49.151 podem ser usadas como portas de destino ou de origem. Elas podem ser usadas por empresas para registrar aplicativos específicos, como os de mensagem instantânea.
. Portas privadas - As portas de 49.152 a 65.535 são geralmente utilizadas como portas de origem. Elas podem ser usadas por qualquer aplicativo.

A tabela exibe alguns números de porta conhecidos comuns e seus aplicativos associados.

| Número da Porta | Transporte | Protocolo de aplicação |
| :--- | :--- | :--- |
| 20 | TCP | Protocolo de Transferência de Arquivos (FTP) - Dados |
| 21 | TCP | FTP -Controle |
| 22 | TCP | Secure Shell(Shell seguro) - SSH |
| 23 | TCP | Telnet |
| 25 | TCP | Protocolo SMTP |
| 53 | UDP, TCP | Protocolo DNS |
| 67 | UDP | Dynamic Host Configuration Protocol (DHCP) - Servidor |
| 68 | UDP | Cliente DHCP |
| 69 | UDP | Protocolo de Transferência Trivial de Arquivo (TFTP) |
| 80 | TCP | Protocolo HTTP |
| 110 | TCP | Protocolo POP3 (Post Office Protocol - Protocolo dos Correios) |
| 143 | TCP | Protocolo IMAP |
| 161 | UDP | Protocolo de Gerenciamento Simples de Rede (SNMP) |
| 443 | TCP | HTTPS (Secure Hypertext Transfer Protocol - Protocolo de Transferência de Hipertexto Seguro) |

Algumas aplicações podem usar tanto TCP quanto UDP. Por exemplo, o DNS usa o protocolo UDP quando os clientes enviam requisições a um servidor DNS. Contudo, a comunicação entre dois servidores DNS sempre usa TCP.

Pesquise no site da IANA o registro de portas para visualizar a lista completa de números de portas e aplicativos associados.

# Pares de Soquetes

As portas origem e destino são colocadas no segmento. Os segmentos são encapsulados em um pacote IP. O pacote IP contém o endereço IP de origem e destino. A combinação do endereço IP de origem e o número de porta de origem, ou do endereço IP de destino e o número de porta de destino é conhecida como um socket.

No exemplo na figura, o PC está solicitando simultaneamente serviços FTP e Web do servidor de destino.

![[Pasted image 20260828112713.png]]


No exemplo, a solicitação FTP gerada pelo PC inclui os endereços MAC da Camada 2 e os endereços IP da Camada 3. A solicitação também identifica o número da porta de origem 1305 (ou seja, gerado dinamicamente pelo host) e a porta de destino, identificando os serviços de FTP na porta 21. O host também solicitou uma página da Web do servidor usando os mesmos endereços de Camada 2 e Camada 3. No entanto, ele está usando o número da porta de origem 1099 (ou seja, gerado dinamicamente pelo host) e a porta de destino identificando o serviço Web na porta 80.

O socket é usado para identificar o servidor e o serviço que está sendo solicitado pelo cliente. Um socket do cliente pode ser assim, com 1099 representando o número da porta de origem: 192.168.1.5:1099

O soquete em um servidor da web pode ser 192.168.1.7:80

Juntos, esses dois sockets se combinam para formar um par de sockets: 192.168.1.5:1099, 192.168.1.7:80

Os sockets permitem que vários processos em execução em um cliente se diferenciem uns dos outros, e várias conexões com um processo no servidor sejam diferentes umas das outras.

Este número de porta age como um endereço de retorno para a aplicação que faz a solicitação. A camada de transporte rastreia essa porta e a aplicação que iniciou a solicitação, de modo que quando uma resposta é retornada, ela pode ser encaminhada para a aplicação correta.

# Resumo

Quando uma mensagem é entregue usando o TCP ou o UDP, os protocolos e os servicos sao identificados por um numero de porta. Uma porta é um identificador numérico dentro de cada segmento que é usado para rastrear conversas específicas entre um cliente e um servidor. Cada mensagem que um host envia contem uma porta origem e destino.

Quando uma mensagem e recebida por um servidor, e necessario que o servidor consiga determinar qual servico esta sendo solicitado pelo cliente. Os clientes sao pré-configurados para usar uma porta de destino que foi registrada na Internet para cada serviço.

As portas sao atribuídas e gerenciadas por uma organizacao conhecida como ICANN (Corporacao da Internet para Atribuicao de Nomes e Numeros). As portas foram divididas em tres categorias e variam em numero de 1 a 65.535.

- __Portas bem conhecidas__ - As portas de destino que estao associadas a aplicativos de rede comuns sao identificadas como portas bem conhecidas. Elas estao no intervalo de 1 a 1.023.
- __Portas registradas__ - As portas 1.024 a 49.151 podem ser usadas como portas de destino ou de origem. Elas podem ser usadas por empresas para registrar aplicativos específicos, como os de mensagem instantanea.
- __Portas privadas__ - As portas de 49.152 a 65.535 sao geralmente utilizadas como portas de origem. Elas podem ser usadas por qualquer aplicativo.

O número da porta de origem é gerado dinamicamente pelo dispositivo de envio para identificar uma conversação entre dois dispositivos. Este processo permite que várias conversações ocorram simultaneamente. É comum que um dispositivo envie várias solicitaçoes de serviço HTTP para um servidor Web ao mesmo tempo. Cada conversa HTTP separada e rastreada com base em portas origem.

O cliente preenche um número de porta destino no segmento para informar o servidor destino qual serviço está sendo solicitado. Um servidor pode oferecer mais de um servico simultaneamente como servicos Web na porta 80, ao mesmo tempo que oferece o estabelecimento de uma conexao FTP na porta 21.