# Lab_Git

Estudos e conceitos aprendidos na plataforma Alura, no curso de 'Git e Github: Controle e Compartilhe seu código.'

link: https://cursos.alura.com.br/course/git-github-controle-de-versao

O Git é um __sistema de controle de versão__ (VCS), que tem por objetivo gerenciar o versionamento de repositórios. Através da sua arquitetura
distribuída permite que cada desenvolvedor tenha uma cópia local do repositório do projeto, isso permite o trabalho em equipe de forma segura
e também o trabalho de modo offline. O Git possui um histórico de modificações que podem ser restauradas a qualquer momento. Existem outros
sistemas de controle de versão, como por exemplo o Mercurial e o SVN, porém o Git é o mais usado.

__Características do Git:__

- Permite organizar o trabalho em equipe, mantendo as alterações nos arquivos em um servidor específico.
- Permite o armazenamento e acesso a um histórico de modificações.

__Instalação do Git:__

link: https://git-scm.com/downloads

__Conceitos do Git:__

Repositório: basicamente é onde está armazenado todo o seu projeto, com todas as branches e arquivos. Esse repositório fica armazenado
em um servidor Git, geralmente na nuvem, em serviços como o GitHub. Quando vamos trabalhar nesse projeto, devemos antes fazer uma cópia local do
repositório na nossa máquina.

Árvore do Git: quando inicializamos um repositório Git, automaticamente é criada uma árvore(tree). Sendo que o código inicial do projeto é conhecido
como galho(branch). Ao trabalhar no projeto, podemos criar outras branches a partir da branch inicial, e toda modificação realizada, será refletida
somente na branch estendida, sem modificar a branch pai(main).

Commit: são uma espécie de checkpoints, que servem para indicar que houve mudanças em nosso código. É uma boa prática acompanhar o commit uma pequena
mensagem descritiva, que informa exatamente o que foi alterado.

Merge:

__Comandos do Git:__

```git init```: Serve para inicializar um repositório no diretório em que o comando for executado. A partir deste comando, o Git poderá gerenciar
as modificações realizadas nos arquivos.

```git status```: Serve para mostrar o estado atual do nosso repositório, ou seja, indica quais arquivos foram alterados, entre outras informações.

```git add```: Serve para incluir os arquivos para que o git possa monitorar.

```git commit -m```: Serve para commitar(realizar um checkpoint) nas mudanças que foram realizadas. O parametro __-m__ serve para adicionar uma mensagem junto ao commit.
por exemplo, ```git commit -m "CSS personalizado adicionado"```.

```git log```: Serve para mostrar um histórico de alterações(commits) em forma de logs, com diversas informações, podendo ter uma série de parametros para que seja customizado
as informações e a maneira que é vizualizado. Utilize __git log --help__ para saber mais sobre os parametros ou acesse: https://devhints.io/git-log


