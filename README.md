# Relatório aulas práticas Redes de Computadores

- Para atender às necessidades dos departamentos, foram criadas quatro sub-redes
diferentes com a máscara que permite a configuração de 24 hosts em cada
sub-rede.
- Em seguida, foi criada uma topologia em estrela utilizando quatro switches Cisco
2950-24, conectados entre si por cabos Ethernet. Cada departamento está em uma
sub-rede e foi configurada duas VLANs com 12 portas cada. A VLAN 1 utiliza as
portas 1 a 12 e a VLAN 2 utiliza as portas 13 a 24 em cada switch. Cada VLAN tem
10 estações, 1 servidor e 1 impressora.
Foram então seguidos os seguintes passos:
1. Primeiro foi criado as sub-redes de acordo com a máscara que permite a
configuração de 24 hosts em cada sub-rede, que é 255.255.255.224 (ou /27 em
notação CIDR):
- Engenharia: 192.168.1.0/27
- Compras: 192.168.1.32/27
- TI Interno: 192.168.1.64/27
- Infraestrutura: 192.168.1.96/27
2. Observe que para cada sub-rede, temos um total de 32 endereços IP, sendo 30
deles para hosts. O primeiro endereço IP válido é o endereço da rede e o último é o
endereço de broadcast. Portanto, temos:
Engenharia: primeiro IP válido 192.168.1.1, último IP válido 192.168.1.30,
broadcast 192.168.1.31;
Compras: primeiro IP válido 192.168.1.33, último IP válido 192.168.1.62,
broadcast 192.168.1.63;
TI Interno: primeiro IP válido 192.168.1.65, último IP válido 192.168.1.94,
broadcast 192.168.1.95;
Infraestrutura: primeiro IP válido 192.168.1.97, último IP válido
192.168.1.126, broadcast 192.168.1.127.
3. Por fim, cada departamento deve estar em uma sub-rede e configurar duas VLANs
com 12 portas cada. Da porta 1-12, teremos a VLAN 1 - que foi adicionada também
como default, e da porta 13-24, teremos a VLAN 2. Cada VLAN terá 10 estações, 1
impressora e 1 servidor. Como os departamentos entre si não estão ligados foi
atribuído o mesmo nome para as VLANs;
4. Além disso, na configuração das redes, foi possível utilizar dois tipos de atribuição
de endereços IP: estático e dinâmico.

![image](https://github.com/sstephanier/Projeto_Redes/assets/117938105/ef1a2f53-50cc-4ce9-a006-a99d761acc3b)

 - No endereço IP estático foi atribuído manualmente ao dispositivo de rede. Esse tipo de
configuração é recomendado para dispositivos que precisam ter um endereço IP fixo, como
servidores ou roteadores, e em situações em que é necessário ter um controle rigoroso
sobre a rede. No caso do trabalho foi somente para aprendizado na prática de seu
funcionamento. Já ao usar o endereço IP dinâmico foi atribuído automaticamente pelo
servidor DHCP (Dynamic Host Configuration Protocol), que é responsável por gerenciar o
pool de endereços disponíveis na rede.

- Link do arquivo criado no Cisco Packet Tracer:
https://drive.google.com/file/d/1Sy3vIfYlql09hOntHzl4QD768Q8QjlWp/view?usp=sharing

- Link de Tutorial do Projeto no Youtube:
https://youtube.com/playlist?list=PLAp37wMSBouB__-47L4Y8jSsIUzqJIIMz
