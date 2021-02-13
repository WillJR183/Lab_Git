# Laboratório Git e GitHub

### Visão geral

Estudos e conceitos aprendidos na plataforma Alura, no curso ['Git e GitHub: Controle e Compartilhe seu código.'](https://cursos.alura.com.br/course/git-github-controle-de-versao) E também aprendidos no bootcamp Impulso FullStack Developer pela plataforma Digital Innovation One no curso ['Introdução ao Git e ao GitHub'.](https://web.digitalinnovation.one/course/introducao-ao-git-e-ao-github/learning/75b9fe49-6ed4-4480-83a7-7e37fc356aa9/)

### O que é o Git ?

- O Git é um __sistema de controle de versão distribuído__ (DVCS), que foi criado em __2005__, por __Linus Torvalds__ durante o desenvolvimento do kernel __Linux__ para resolver o problema de __versionamento colaborativo__. 

- O Git não foi o sistema pioneiro no versionamento, porém foi o que __supriu as necessidades__ e hoje é o __sistema padrão do mercado__. 
- Através da sua __arquitetura distribuída__ permite que cada desenvolvedor tenha uma __cópia local do repositório do projeto__, isso permite o __trabalho em equipe de forma segura__. 
- O Git possui um __histórico de modificações__ que podem ser __restauradas__ a qualquer momento. 
- Uma vez que temos um __sistema de versionamento__, precisamos __guardar os códigos__, e assim surgiu as empresas que provém __repositórios online__, como o __GitHub__.

### Benefícios em aprender e dominar o Git e GitHub

- Possibilita o controle de versão ( Git )
- Permite o armazenamento em nuvem ( Git Hub )
- Possibilita o trabalho em equipe ( Git / GitHub )
- Proporciona melhorar o seu código , através de experiências com a comunidade ( GitHub )
- Viabiliza o reconhecimento na comunidade ( GitHub )

### Navegação via command line interface (CLI)

No __Windows__ ( derivado do Shell ) 
``` sh
cd : entra em diretórios 

dir : lista diretórios

mkdir : cria diretórios

del : remove arquivos / arquivos dentro de pastas

rmdir : remove pastas / diretórios 

echo : exibe no terminal

( > ) : redirecionador de fluxo

echo "teste" > teste.txt : cria o arquivo teste.txt e preenche com teste
```

> cls : limpa o terminal

No __Linux__ ( derivado do bash ) : 
``` bash
cd : entra em diretórios

ls : lista diretórios

mkdir : cria diretórios

rm -rf  : remove pastas

clear : limpa a tela

echo : exibe no terminal

( > ) : redirecionador de fluxo

echo "teste" > teste.txt : cria o arquivo teste.txt e preenche com teste
```

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

```git init```: Serve para inicializar um repositório no diretório em que o comando for executado. A partir deste comando, o Git poderá gerenciar as modificações realizadas nos arquivos.

```git status```: Serve para mostrar o estado atual do nosso repositório, ou seja, indica quais arquivos foram alterados, entre outras informações.

```git add```: Serve para incluir os arquivos para que o git possa monitorar.

```git commit -m```: Serve para commitar(realizar um checkpoint) nas mudanças que foram realizadas. O parametro __-m__ serve para adicionar uma mensagem junto ao commit.
por exemplo, ```git commit -m "CSS personalizado adicionado"```.

```git log```: Serve para mostrar um histórico de alterações(commits) em forma de logs, com diversas informações, podendo ter uma série de parametros para que seja customizado
as informações e a maneira que é vizualizado. Utilize __git log --help__ para saber mais sobre os parametros ou acesse: https://devhints.io/git-log


