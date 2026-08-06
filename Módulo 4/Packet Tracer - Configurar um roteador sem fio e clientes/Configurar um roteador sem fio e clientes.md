# Objetivos

Parte 1: Conectar os Dispositivos

Parte 2: Configurar o roteador sem fio

Parte 3: Configurar o endereçamento IP e testar a conectividade

# Instruções

## Parte 1: Conecte os dispositivos

A área de trabalho mostra o interior da casa de sua amiga. Role a janela para ter uma ideia do layout da casa e da localização dos dispositivos. Nesta parte, você conectará todos os dispositivos com lable.

### Etapa 1: Conecte os cabos coaxiais.

A empresa de serviços a cabo de Natsumi oferece serviços de Internet e vídeo em sua casa por meio de um cabo coaxial. O cabo está conectado a uma tomada em sua casa. Um dispositivo divisor separa o serviço de dados da Internet do serviço de vídeo. Isso permite que os dois serviços sejam conectados aos dispositivos apropriados. Você conectará o serviço de Internet ao modem a cabo e o serviço de vídeo à televisão.

a.  Em Network Components, clique em Connections (raio).

b.  Localize e clique no ícone do cabo coaxial. É o ícone azul em zigue-zague.

c.  Clique no Cable Splitter (divisor de cabo) e selecione a porta Coaxial1.

d.  Clique no Cable Modem e selecione Port 0.

e.  Repita as etapas anteriores para conectar o Coaxial2 no Cable Splitter à Port 0 na TV.

f.   Clique na TV e clique em ON em Status. Se as conexões estiverem corretas, será exibida uma imagem que representa um programa de TV.

### Etapa 2: Conecte os cabos de rede.

Há dois PCs na casa de Natsumi. Eles não têm adaptadores de LAN sem fio, então eles serão conectados com cabos Ethernet. O roteador sem fio doméstico é o centro da rede. Ele permite que os dispositivos configurados na rede doméstica se comuniquem entre si e com a Internet. O roteador inclui um switch de rede que aceita conexões com fio com até quatro hosts. Você conectará os PCs a essas portas.

Para que o **Home Wireless Router** acesse a Internet pela rede do provedor de TV a cabo, o cable modem deve estar conectado à porta Internet do roteador sem fio doméstico. Isso é feito com um cabo direto (straight-through) de cobre.

a.  Clique **Connections**, e depois no cabo **Copper Straight-Through**. Se parece com uma linha preta sólida.

b.  Conecte a **Port 1** no **Cable Modem** à porta **Internet** do **Home Wireless Router**.

c.  Clique no **Office PC** e conecte o cabo à porta **FastEthernet0**. Localize o **Home Wireless Router** e clique nele. Conecte a outra extremidade do cabo à porta **GigabitEthernet 1** para concluir a conexão.

d.  Repita as etapas anteriores para conectar o **Bedroom PC** à porta **GigabitEthernet 2** no **Home Wireless Router**.

A rede doméstica com fio agora está totalmente conectada à Internet pela rede do provedor de TV a cabo.

## Parte 2: Configurar o roteador sem fio (Wireless Router)

A maioria dos roteadores sem fio domésticos são configurados usando uma interface gráfica de usuário (GUI) que é acessada através do navegador Web do computador. Nesta parte, você acessará o roteador sem fio doméstico através do navegador no **Office PC** e configurará a rede doméstica da Natsumi.

### Etapa 1: Acesse a GUI do roteador sem fio doméstico.

a.  Clique **Office PC** > guia **Desktop**, e depois **IP Configuration**.

b.  Clique em **DHCP**. O DHCP configurará automaticamente o **Office PC** para estar na mesma rede IP do **Home Wireless Router**.

c.  Após um breve atraso, os valores da **IP Configuration** deverão ser atualizados automaticamente. O endereço IPv4 deve começar com o número 192. Caso contrário, clique em **Fast Forward Time** (Tempo de avanço rápido), que fica logo abaixo da topologia de rede no canto inferior esquerdo. Isso vai acelerar a simulação do DHCP.

d.  Anote o endereço do gateway padrão. O gateway padrão é o dispositivo que fornece aos dispositivos na rede doméstica acesso a redes externas, como a Internet. Nesse caso, o endereço de gateway padrão é o endereço do **Home Wireless Router.**

e.  Mantendo a janela do **Office PC** aberta, feche a janela **IP Configuration**, e depois clique em **Web Browser**. Insira o endereço IP do **Home Wireless Router** (o endereço de gateway padrão) na caixa **URL** e clique em **Go**.

f.   Os roteadores domésticos recém-instalados são configurados com credenciais padrão. Entre com **admin** em ambos campos: **User Name** e **Password**. Você deve ver a GUI do **Home Wireless Router** sendo exibida e pronta para configurar a rede de Natsumi. Ajuste o tamanho da janela, conforme necessário, para ver mais da interface.

**Observação: as senhas padrão em dispositivos do mundo real devem ser alteradas imediatamente, pois são amplamente conhecidas, inclusive por agentes de ameaças.**

### Etapa 2: Defina as configurações básicas.

Nesta etapa, você configurará um novo nome de usuário e senha para o roteador sem fio e limitará o número de endereços IP que o DHCP fornecerá aos hosts conectados à rede.

Natsumi tem apenas alguns dispositivos para conectar a rede, e ela não terá muitos amigos visitando. Ela acredita que não mais de 10 dispositivos se conectariam à rede ao mesmo tempo. Você decide diminuir o número de usuários para 10. Sua amiga mora em uma parte densamente povoada da cidade, então é possível que muitas pessoas possam ver a rede sem fio dela.

a.  No momento, você está visualizando opções de configuração na guia **Setup**. Localize a área **Network Setup**. É onde você pode definir as configurações do servidor DHCP do roteador. Localize o campo **Maximum Number of Users**, digite **10**. Role a tela até a parte inferior da página e clique em **Save Settings**. Você deve salvar as configurações em todas as páginas da GUI nas quais fizer alterações.

**Observação:** é possível que você perca a conexão com o roteador. Clique em **Go** no navegador Web para recarregar a página da GUI. Talvez seja necessário fechar o **Web Browser**, clicar em **IP Configuration**, e alternar entre **DHCP** e **Static** para atualizar o endereçamento IP do **Office PC**. Em seguida, verifique se o Office PC tem uma configuração de endereço IP que comece com 192, abra o **Web Browser** novamente, insira o endereço IP do roteador e autentique novamente com **admin** como credenciais padrão.

b.  Clique na guia **Administration**. Aqui, você pode alterar a senha de **admin** padrão. Digite e confirme **MyPassword1!** como a nova senha. Vá até o final da página e clique em **Save Settings** (Salvar Configurações).

Você será solicitado a fazer login novamente. Insira **admin** como o nome de usuário e **MyPassword1!** como a nova senha e clique em **Continue**.

### Etapa 3: Configure a LAN sem fio.

Neste ponto, você está pronto para configurar a rede sem fio de Natsumi para que ela possa conectar seus dispositivos sem fio à Internet por Wi-Fi.

a.  Role até a parte superior da janela e clique na guia **Wireless**.

b.  Para a rede de **2,4 GHz**, clique em **Enable** para ativar o rádio da rede.

c.  Altere o **Network Name** **(SSID)** de **Default** para **MyHome**. Quando as pessoas procurarem redes Wi-Fi para se conectar, elas verão esse nome de rede. O nome da rede pode estar oculto, mas isso pode dificultar um pouco a conexão dos convidados à rede. Vá até o final da página e clique em **Save Settings** (Salvar Configurações).

d.  Agora você vai configurar a segurança na rede **MyHome**. Isso impedirá que pessoas não autorizadas se conectem à rede sem fio. Role até a parte superior da janela e clique em **Wireless Security** na guia **Wireless**.

e.  Observe que a segurança está desativada no momento em todas as três redes sem fio. Você só está usando a rede de 2,4 GHz. Clique no menu suspenso da rede de **2,4 GHz** e selecione **WPA2 Personal**. Essa é a segurança mais forte que esse roteador oferece para redes sem fio.

f.   Mais configurações são reveladas. O WPA2 Personal exige uma senha que deve ser inserida por qualquer pessoa que queira se conectar à rede sem fio. Insira **MyPassPhrase1!** como a **senha**. Observe que a capitalização é importante.

g.  Role até a parte inferior da página, clique em **Save Settings** e feche o **Web Browser** do PC.

## Parte 3: Configurar o endereçamento IP e testar a conectividade

Agora que o roteador está configurado, nesta parte você vai configurar o endereçamento IP para PCs e laptops e verificar se eles podem se conectar à Internet.

### Etapa 1: Conecte o laptop à rede sem fio.

a.  Clique no **Laptop** em living room, e depois na guia **Desktop** > **PC Wireless**.

b.  Clique na guia **Connect**. Após um breve atraso, a rede sem fio configurada deve aparecer anteriormente na lista de nomes de redes sem fio.

c.  Clique no nome da rede que você criou e, em seguida, clique no botão Connect.

d.  Insira a senha que você configurou anteriormente para a rede sem fio no campo Pre-shared Key e clique em Connect.

e.  Clique na guia **Link Information**. Você deverá ver a mensagem: **You have successfully connected to the access point**.

f.   Clique no botão **More Information** para ver detalhes sobre a conexão. Se o endereço IP não começar com **192**, clique em **Fast Forward Time** várias vezes para acelerar a simulação.

g.  Feche o app **PC Wireless** e abra o **Web Browser**. Verifique se o **Laptop** agora pode se conectar a **skillsforall.srv**, clicando em **Fast Forward Time** (Tempo de avanço rápido) até que a página carregue. Isso verifica se o **Laptop** tem conectividade com a Internet.

### Etapa 2: Teste a conectividade do Office PC.

Você sabe que o Office PC pode se conectar à rede porque você o usou para configurar o roteador. No entanto, ele também pode acessar a Internet? Se conseguir, você saberá que a rede com fio está conectada e configurada corretamente.

a.  Clique em **Office PC** > guia **Desktop**  > **Web Browser**.

b.  Insira **skillsforall.srv** e clique em **Go**. Após um breve intervalo de tempo, a página da Web será exibida. Se necessário, clique em **Fast Forward Time** várias vezes para acelerar a convergência.

O carregamento de um site externo verifica a conectividade do **Office PC** com a Internet.

### Etapa 3: Configure o bedroom PC.

a.  Em **Bedroom PC**, abra **IP Configuration** e configure para **DHCP**. Verifique se o Bedroom PC recebeu um endereço IP que começa com **192**.

b.  Feche a janela **IP Configuration** e abra **Web Browser**. Verifique se o **Bedroom PC** agora pode se conectar a **skillsforall.srv**, clicando em **Fast Forward Time** (Tempo de avanço rápido) até que a página carregue. Isso verifica se o **Bedroom PC** tem conectividade com a Internet.