![[Pasted image 20260811132707.png|700]]
# O Modelo TCP/IP

Os modelos em camadas ajudam a visualizar o funcionamento conjunto dos diversos protocolos para possibilitar comunicações de rede. Um modelo de camadas representa a operação dos protocolos ocorrendo dentro de cada camada, bem como a interação com as camadas acima ou abaixo dela:

| __Camada do modelos TCP/IP__ | __Descrição__                                                                  |
| ---------------------------- | ------------------------------------------------------------------------------ |
| Aplicação                    | Representa dados para o usuário, além de codificação e do controle de diálogo. |
| Transporte                   | Permite a comunicação entre vários dispositivos diferentes em redes distintas. |
| Internet                     | Determina o melhor caminho pela rede.                                          |
| Acesso à rede                | Controla os dispositivos de hardware e o meio físico que formam a rede.        |

> [!NOTE]
> O Transport Control Protocol (TCP) é o responsável  por garantir a entrega confiável
> 
> O protocolo Internet (IP) é usado pelos roteadores para encaminhar mensagens.
> 
> As camadas de rede e enlace de dados corrspondem à camada de acesso à rede do modelo TCP/IP.
> 
> Endereçamento IP ocorre na camada de rede.

# O Modelo de Referência OSI

Há dois tipos básicos de modelo para descrever as funções que devem ocorrer para que as comunicações de rede sejam bem-sucedidas: modelos de protocolo e modelos de referência.

- __Modelo de protocolo__: Este modelo corresponde muito bem à estrutura de um conjunto específico de protocolo. Um conjunto de protocolos inclui o conjunto de protocolos relacionados que normalmente fornecem toda a funcionalidade necessária para as pessoas se comunicarem com a rede de dados. __O Modelo TCP/IP__ é um modelo de protocolo que descreve as funções que ocorrem em cada camada de protocolos dentro da suíte TCP/IP.
	
- __Modelo de referência__: Este tipo de módulo descreve as funções que devem ser concluídas em uma determinada camada, mas não especifica exatamente com uma função deve ser realizada. Um modelo de referência não deve fornecer um nível suficiente de detalhes para definir com precisão com cada protocolo deve trabalhar em cada camada.

> Curiosidade: O modelo de referência internetwork mais conhecido foi criado pelo projeto Open Systems Interconnection(OSI) e da ISO(Organização Internacional de Padronização). Ele é usado para projeto de rede de dados, especificações de operação e solução de problemas.

| __Camada de Modelo OSI__ | __Descrição__                                                                                                                                                                                                       |
| ------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 7 - Aplicação            | A camada de aplicação contém protocolos usados para comunicações processo a processo.                                                                                                                               |
| 6 - Apresentação         | A camada de apresentação fornece a representação comum de dados transferidos entre serviços da camada de aplicação.                                                                                                 |
| 5 - Sessão               | A camada de sessão fornece serviços a camada de apresentação para organizar o diálogo e gerenciar a troca de dados.                                                                                                 |
| 4 - Transporte           | A camada de transporte define serviços para segmentar, transferir e reagrupar os dados para comunicações individuais entre os dispositivos finais.                                                                  |
| 3 - Rede                 | A camada de rede fornece serviços para trocar dados individuais pela rede entre dispositivos finais identificados.                                                                                                  |
| 2 - Enlace de dados      | Os protocolos da camada de enlace de dados descrevem métodos para a troca de quadros de dados entre os dispositivos em um meio físico comum.                                                                        |
| 1 - Físico               | Os protocolos da camada física descrevem os meios mecânicos, elétricos, funcionais e procedimentais para ativar, manter e desativar conexões físicas para uma transmissão de bits de e para um dispositivo de rede. |

# Comparação entre os Modelos OSI e TCP/IP

![[Pasted image 20260811154856.png]]