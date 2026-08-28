# Telnet

Muito antes dos computadores desktop com interfaces gráficas sofisticadas, as pessoas utilizavam sistemas com base em texto que frequentemente eram apenas terminas de exibição fisicamente acoplados a um computador central. Depois que as redes se tornaram disponíveis, as pessoas precisavam de uma maneira para acessar remotamente os sistemas de computador da mesma maneira que faziam com os terminais conectados diretamente.

O Telnet foi desenvolvido para atender a essa necessidade. O Telnet data do início da década de 70 e está entre um dos protocolos e serviços da camada de Aplicação mais antigos da suite TCP/IP. O Telnet fornece um método padrão de emulação de dispositivos terminais baseados em texto na rede de dados. O protocolo e o software cliente que implementa o protocolo são comumente chamados de Telnet. Os servidores Telnet escutam solicitações de clientes na porta TCP 23.

Apropriadamente, uma conexão usando Telnet é chamada de sessão ou conexão de terminal virtual (vty) Em vez de usar um dispositivo físico para se conectar ao servidor, o Telnet utiliza software para criar um dispositivo virtual que fornece os mesmos recursos de uma sessão de terminal com acesso à interface de linha de comando (CLI) do servidor.

Na figura, o cliente se conectou remotamente ao servidor via Telnet. Agora o cliente pode executar comandos como se estivesse conectado localmente ao servidor.

**Observação:** o Telnet não é considerado um protocolo seguro. O SSH deve ser usado na maioria dos ambientes, no lugar do Telnet. O Telnet é utilizado em vários exemplos neste curso pela simplicidade de sua configuração.

![[Pasted image 20260828114559.png]]


## Problemas de Segurança com Telnet

Quando uma conexão Telnet é estabelecida, os usuários podem executar qualquer função autorizada no servidor, como se estivessem usando uma sessão de linha de comando no próprio servidor. Se autorizados, podem iniciar e parar processos, configurar o dispositivo e até mesmo desligar o sistema.

Embora o protocolo Telnet possa exigir o login de um usuário, ele não suporta o transporte de dados criptografados. Todos os dados trocados durante as sessões Telnet são transportados como texto simples pela rede. Isso significa que os dados podem ser facilmente interceptados e compreendidos.

O protocolo Secure Shell (SSH) oferece um método alternativo e seguro para acesso ao servidor. O SSH fornece a estrutura para proteger login remoto e outros serviços de rede segura. Ele também fornece autenticação mais forte do que o Telnet e suporta o transporte de dados de sessão usando criptografia. Como melhor prática, os profissionais de rede sempre devem utilizar o SSH em vez do Telnet, quando possível.

A figura ilustra como o SSH é mais seguro que o Telnet. Observe como são claramente legíveis os dados capturados pelo hacker quando o Telnet é usado, enquanto que os dados, capturados quando o SSH está em uso, estão criptografados, tornando assim a comunicação mais segura.

![[Pasted image 20260828114629.png]]


