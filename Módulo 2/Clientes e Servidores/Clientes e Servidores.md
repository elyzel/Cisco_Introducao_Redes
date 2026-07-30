
# Funções de Clientes e Servidores

Todos os computadores conectados a uma rede que participam diretamente na comunicação de rede são classificados como `hosts`.
Os hosts podem enviar e receber mensagens na rede. No entanto, o software instalado no computador determina qual a função o computador desempenha.

![[Pasted image 20260729092756.png]]

`Servidores` são hosts que têm um software instalado que os permite fornecer informações, como o e-mail ou páginas Web. Por exemplo, um servidor exige um software de servidor Web para que forneça serviços web à rede.

`Clientes` são computadores host que têm um software instalado que permite solicitar ou exibir as informações obtidas do servidor. Exemplo: Navegador Web -> Safari.

# Redes Ponto-a-Ponto

Os softwares de cliente e de servidor geralmente são executados em computadores separados, mas também é possível que um computador execute duas funções ao mesmo tempo.

Em pequenas empresas e rede doméstica, muitos computadores funcionam como servidores e clientes na rede. Esse tipo de rede é chamada de `rede ponto a ponto (P2P)`. Ambos computadores conectados podem trocar dados e informações entre si, atuando como cliente ou servidor conforme o necessário.

> [!INFO]
> A desvantagem de um ambiente ponto a ponto, é o desempenho reduzido de um host se estiver atuando como cliente e servidor.

| __Vantagens__                                                                                  | __Desvantagens__                                                                                  |
| ---------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| Fácil de configurar                                                                            | Nenhuma administração centralizada                                                                |
| Menos complexo                                                                                 | Não é tão segura                                                                                  |
| Menor custo porque os dispositivos de rede e os servidores dedicados podem não ser necessários | Não é escalável                                                                                   |
| Pode ser usada para tarefas simples como transferir arquivos e compartilhar impressoras.       | Todos os dispositivos podem atuar como clientes e servidores, podendo deixar seu desempenho lento |

# Aplicações Ponto-a-Ponto

Uma aplicação P2P permite que um dispositivo atue como cliente e servidor na mesma comunicação, como mostra a figura:

![[Pasted image 20260729135937.png]]

Nesse modelo, todo cliente é um servidor e todo servidor é um cliente. Aplicações P2P exigem que cada dispositivo final forneça uma interface de usuário e execute um serviço em segundo plano.

# Múltiplas Funções na Rede

Um computador com software de servidor pode fornecer serviços simultaneamente a um ou vários cliente, como demonstrado na imagem abaixo:

![[Pasted image 20260729140320.png]]

Além disso, um único computador pode executar vários tipos de software de servidor. Em cassa ou em uma empresa pequena, pode ser necessário que um computador atue como um servidor de arquivos, um servidor Web e um servidor de e-mail.




