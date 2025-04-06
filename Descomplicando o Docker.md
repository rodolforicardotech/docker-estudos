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


PARA FAZER: <br>
[X] Instalar o git no linux<br> 
[X] Criar um repositório para o estudo do Docker<br>
[X] Clonar o repositório na minha máquina
