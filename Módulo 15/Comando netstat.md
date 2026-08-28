Conexões TCP desconhecidas podem representar uma grande ameaça à segurança. Elas podem indicar que algo ou alguém está conectado ao host local. Às vezes é necessário conhecer quais conexões TCP ativas estão abertas e sendo executadas em um host de rede. O netstat é um utilitário de rede importante que pode ser usado para verificar essas conexões. Como mostrado abaixo, digite o comando **netstat** para listar os protocolos em uso, o endereço local e os números de porta, o endereço externo e os números de porta e o estado da conexão.

```
C:∖> netstat

Active Connections

  Proto Local Address           Foreign Address             State

  TCP   192.168.1.124:3126      192.168.0.2:netbios-ssn     ESTABLISHED

  TCP   192.168.1.124:3158      207.138.126.152:http        ESTABLISHED

  TCP   192.168.1.124:3159      207.138.126.169:http        ESTABLISHED

  TCP   192.168.1.124:3161      sc.msn.com:http             ESTABLISHED

  TCP   192.168.1.124:3166      www.cisco.com:http          ESTABLISHED

(output omitted)

C:∖> netstat
```

Por padrão, o comando **netstat** tentará resolver os endereços IP para os nomes de domínio e os números de porta para aplicações bem conhecidas. A opção **n** pode ser usada para exibir endereços IP e números de porta em sua forma numérica.