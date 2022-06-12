1 - 🚀 No Docker Hub, utilizando a caixa de busca ("Search for great content"), busque pela imagem da Distribuição Linux Debian.


2 - 🚀 Uma vez que encontrar a imagem oficial, acesse-a (clicando em seu card) e verifique na página de detalhes. Confira se existe algum comando para baixar a imagem localmente sem ter que criar um contêiner para isso.


3 - 🚀 Baixe a imagem utilizando a tag: stable-slim, que é uma versão reduzida da distribuição.

docker pull:stable-slim

4 - 🚀 Após baixar a imagem para seu computador local, crie e execute um contêiner no modo interativo utilizando essa imagem como referência — não esqueça referenciar a tag.

docker container run -it debian:stable-slim

5 - 🚀 No terminal, você deve conseguir rodar o comando cat /etc/*-release, que vai retornar os dados da distribuição Debian que está sendo rodada dentro do contêiner.
🚀 Encerre o terminal.

cat /etc/*-release

6 - 🚀 Verifique na sua lista de contêiners qual contêiner se refere ao exercício que acabou de praticar.

exit

7 - 🚀 Inicie o mesmo contêiner novamente, sem criar outro. Valide se ele está ativo na lista de contêiners.

docker container ls -l

8 - 🚀 Retome o contêiner que foi criado anteriormente neste exercício.

docker container start <CONTAINER ID || NAMES>

9 - 🚀 Rode o comando cat /etc/debian_version que deve retornar a versão atual do sistema do contêiner.

docker container attach <CONTAINER ID || NAMES>

10 - 🚀 Encerre o terminal.

cat /etc/debian_version

11 - 🚀 Remova somente o contêiner criado para esse exercício.

docker container rm <CONTAINER ID || NAMES>

12 - [BÔNUS] Crie e rode de modo interativo em modo 'Cleanup', a imagem andrius/ascii-patrol.

docker run -it --rm andrius/ascii-patrol

13 - [BÔNUS] **Encerre o contêiner utilizando os botões [ctrl] + [c].

docker container ls -a
