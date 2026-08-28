# IP Packet Encapsulated in an Ethernet Frame

Na maioria das situações, queremos que os nossos dispositivos possam se conectar além da rede local: a outras residências, a empresas e à Internet. Os dispositivos que estão além do segmento de rede local são conhecidos como hosts remotos. Quando um dispositivo de origem envia um pacote a um dispositivo de destino remoto, é necessária a ajuda de roteadores e do roteamento. O roteamento é o processo de identificação do melhor caminho até um destino.

Um roteador é um dispositivo de rede que conecta várias redes IP de Camada 3. Na camada de distribuição da rede, os roteadores direcionam o tráfego e realizam outras funções essenciais em uma operação de rede eficiente. Os roteadores, como switches, conseguem decodificar e ler as mensagens que são enviadas para eles. Ao contrário dos switches, que tomam uma decisão de encaminhamento com base no endereço MAC da Camada 2, os roteadores fundamentam suas decisões de encaminhamento no endereço IP da Camada 3.

O formato do pacote contém os endereços IP dos hosts de destino e de origem, assim como os dados da mensagem que está sendo enviada entre eles. O roteador lê a porção de rede do endereço IP de destino e a utiliza para descobrir qual das redes conectadas é a melhor forma de encaminhar a mensagem para o destino.

Sempre que a porção de rede dos endereços IP dos hosts de origem e de destino não coincidir, deverá ser usado um roteador para encaminhar a mensagem. Quando um host localizado na rede 1.1.1.0 precisa enviar uma mensagem para um host na rede 5.5.5.0, ele encaminha a mensagem ao roteador. O roteador recebe a mensagem, desencapsula o quadro Ethernet e lê o endereço IP de destino no pacote IP. Em seguida, ele determina para onde deve encaminhar a mensagem. Ele reencapsula o pacote de volta em um novo quadro e encaminha o quadro para o destino.

**Clique em Play para ver como são usados os endereços MAC e IP.**

### Pacote IP Encapsulado em um Quadro Ethernet

![[Pasted image 20260828104310.png]]


# Entradas da Tabela de Roteamento

Os roteadores movem informações entre redes locais e remotas. Para fazer isso, eles têm que usar tabelas de roteamento para armazenar informações. As tabelas de roteamento não estão relacionadas aos endereços de hosts individuais. Tabelas de roteamento contêm endereços de redes e o melhor caminho para acessar essas redes. As entradas podem ser feitas na tabela de roteamento de duas maneiras: atualizadas dinamicamente por informações recebidas de outros roteadores na rede ou inseridas manualmente por um administrador de rede. Os roteadores usam as tabelas de roteamento para determinar qual interface deve ser usada para encaminhar uma mensagem para o destino desejado.

Se o roteador não conseguir determinar para onde encaminhar uma mensagem, ele a descartará. Os administradores de rede podem configurar uma rota padrão que é inserida na tabela de roteamento para evitar que o pacote não seja descartado pelo fato do caminho para a rede de destino não estar na tabela de roteamento. Uma rota padrão é a interface através da qual o roteador encaminha um pacote contendo um endereço de rede IP de destino que é desconhecido. Essa rota padrão normalmente se conecta a outro roteador que pode encaminhar o pacote para a rede de destino final.

![[Pasted image 20260828104526.png]]

- **Tipo -** O tipo de conexão C para diretamente conectado
- **Rede -** O endereço de rede
- **Porta -** Interface usada para encaminhar pacotes para a rede

# Gateway Padrão

O método que um host utiliza para enviar mensagens para um destino em uma rede remota difere da forma como um host envia mensagens na mesma rede local. Quando um host precisa enviar uma mensagem para outro host localizado na mesma rede, ele pode encaminhar a mensagem diretamente. Um host usará o ARP para descobrir o endereço MAC do host de destino. O pacote IPv4 contém o endereço IPv4 de destino, encapsula o pacote em um quadro com o endereço MAC de destino e o encaminha para fora.

Quando um host precisa enviar uma mensagem para uma rede remota, ele deve usar o roteador. O host inclui o endereço IP do host de destino dentro do pacote, exatamente como antes. Entretanto, quando ele encapsula o pacote em um quadro, usa o endereço MAC do roteador como destino do quadro. Dessa forma, o roteador receberá e aceitará o quadro baseado no endereço MAC.

Como o host de origem determina o endereço MAC do roteador? Um host conhece o endereço IPv4 do roteador por meio do endereço de gateway padrão configurado em suas configurações de TCP/IP. O endereço do gateway padrão é o endereço da interface do roteador conectada à mesma rede local do host de origem. Todos os hosts na rede local usam o endereço do gateway padrão para enviar mensagens ao roteador. Quando o host conhece o endereço IPv4 do gateway padrão, ele pode usar o ARP para determinar o endereço MAC. O endereço MAC do roteador é colocado no quadro, destinado a outra rede.

É importante que o gateway padrão correto esteja configurado em cada host na rede local. Se não houver um gateway padrão definido nas configurações TCP/IP do host ou se estiver especificado um gateway padrão incorreto, não será possível entregar as mensagens endereçadas aos hosts nas redes remotas.

![[Pasted image 20260828104607.png]]