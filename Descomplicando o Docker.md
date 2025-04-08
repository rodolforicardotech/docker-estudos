# Descomplicando o Docker

## Dia 01 - Aula 01
- O container é isolado na máquina (o cercadinho)
- eu consigo especificar os recursos da máquina para cada container
- CONTAINER NÃO É MÁQUINA VIRTUAL!
- Não existe só o Docker para isso, ele popularizou. O docker foi baseado no LXC (Linux Container)

Isolamento Logico (usuários, rede, permissões) -> namespaces<br>
Isolamento Fisico (memória, recursos, etc) -> cgroups

## Dia 01 - Aula 02
- O dockerfile possui instruções run
- cada vez que rodamos o run, ele cria uma nova camada
- SOMENTE A ÚTLIMA CAMADA tem a possibildiade de escrita
- Caso queira alterar algo da anterior, é preciso criar uma cópia na camada mais atual e com isso, alterar
- O ideal é agilizar todos os runs em um só comando!
- NÃO É POSSÍVEL INTERAGIR COM AS CAMADAS READ- ONLY

## Dia 01 - Aula 03
- O container utiliza o kernel do próprio host (exemplo: um prédio de 100 apartamentos e cada um com o porteiro? Não rola!)
- IPTABLE e NETFILTER -> tudo relacionado à rede. Como a internet se conecta ao container
- CGROUPS: Cpu, memória, recursos
- NAMESPACE: Usuários, rede, permissões

## Dia 01 - Aula 06
Alguns comandos:
> docker version<br>
> docker container ls<br>
> docker container run hello-world (roda e para)<br> 
> docker container run -ti hello-world (roda e mantém em execução e interativo)
> docker container ls -a (mostra os containers que estão em execução e os que já pararam)
> docker container run -ti ubuntu (rodou o Ubuntu e já abriu o terminal, por conta do -ti. Perceba que o nome root muda para o ID daquele container)
> docker container **attach** ID_OU_NOME (para voltar para um container ativo)

<br>
OBS: Todo container tem um entry-point. Se esse cara morrer, o container morre.<br>
OBS 2: Se quiser sair do container sem matar, é preciso apertar CTRL + P + Q
<br>
OBS 3: Quando você roda um container que precisa ser rodado em primeiro plano, para evitar o erro de ficar preso, é preciso rodar com o **-d** para que ele se conecte com o DAEMON, ou seja, em segundo plano (-d -> DESANEXADO). Para executar alguma coisa nesse container, utilize o **EXEC**:<br>
> docker container exec -ti ID_OU_NOME O_QUE_QUER_RODAR

## Dia 01 - Aula 07
> docker container **stop** ID<br>
> docker container **start** ID<br>
> docker container **restart** ID<br>
> docker container **inspect** ID (retorna todas as informações do container)<br>  
> docker container **pause** ID  
> docker container **unpause** ID  
> docker container logs -f ID (mostra os logs do container. Legal para aqueles que precisam rodar em primeiro plano)  
> docker container **rm** ID (remove o container. Se for um container que roda em primeiro plano, tem que parar primeiro OU forçar o rm. Esse comando também remove o container lá do ls -a)  
> 

OBS: O curl é uma ferramenta para fazer requisições URL.



### PARA FAZER: <br>
[] Realizar o curl do arquivo nginx  
[X] Instalar o git no linux<br> 
[X] Criar um repositório para o estudo do Docker<br>
[X] Clonar o repositório na minha máquina
