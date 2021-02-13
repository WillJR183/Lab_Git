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

##### No __Windows__ ( derivado do Shell )

``cd ``: entra em diretórios 

``dir``: lista diretórios

``mkdir`` : cria diretórios

``del`` : remove arquivos / arquivos dentro de pastas

``rmdir`` : remove pastas / diretórios 

``echo`` : exibe no terminal

`` >``  : redirecionador de fluxo

``echo "teste" > teste.txt`` : cria o arquivo teste.txt e preenche com teste

``cls`` : limpa o terminal

##### No __Linux__ ( derivado do bash )

``cd`` : entra em diretórios

``ls`` : lista diretórios

``mkdir`` : cria diretórios

``rm -rf``  : remove pastas

``clear`` : limpa a tela

``echo`` : exibe no terminal

``>`` : redirecionador de fluxo

``echo "teste" > teste.txt`` : cria o arquivo teste.txt e preenche com teste


## Entendendo como o Git funciona por baixo dos panos

### Conceitos Importantes que envolvem o Git

- __SHA1__ ( Secure Hash Algorithm ) 
- __Objetos fundamentais__ (Blobs , Trees e Commits)
- __Sistema distribuído__

#### SHA1

- É um conjunto de __funções hash criptográficas__ projetadas pela NSA.
- A __encriptação__ gera um conjunto de __caracteres identificador__ de __40 dígitos__.
- É uma forma curta de representar um arquivo.
- Comando que gera o __SHA1__ : ` openssl sha1 + arquivo.txt `
- Quando alteramos a informação no arquivo e executamos o comando, ele gera uma nova __chave SHA1__.
- Se alterarmos a informação no arquivo para a que estava anteriormente e executar o comando __SHA1__ novamente, ele retorna para a __chave anterior__.

#### Objetos fundamentais

- Blobs : São os __objetos do Git__ que __guardam__ nossos __arquivos__ realizando o __hash SHA1__, mas também com base em metadados (nome, tipo , tamanho etc) de cada arquivo.
- Trees : São __objetos conhecidos como árvores__ ( estruturas de pastas ) , são responsáveis por __construir toda a estrutura de arquivos__, sendo recursiva. As trees possuem a __própria assinatura hash SHA1__ , além de encapsular os blobs, contendo inclusive o nome de cada blob ( arquivo ). 
 - Commits : São os __principais objetos do Git__ ,  são eles que vão __juntar tudo e dar sentido a alguma alteração__. Os commits apontam para uma árvore, parente (último commit) , autor , mensagem e timing. Os __commits__ também __possuem uma assinatura hash SHA1__.

#### Sistema distribuído seguro

- Seus __objetos__ estão __ligados__ de maneira __encadeada__ e de difícil alteração. Um sistema distribuído é um __sistema que possui múltiplas cópias de si mesmo em diferentes locais__.

### Iniciando o Git e criando um commit

- criando um repositório
    - `git init` : inicializa um repositório Git .
    - `git add` : adiciona arquivos ao repositório.
        - `git add + nome_arquivo` : adiciona um arquivo ao repositório.
        - `git add *`  : adiciona todos os arquivos untracked ao repositório.
        - `git add .`   : adiciona todas as alterações do repositório local para stage area (prontos para commitar).
    - `git commit` : salva arquivos (checkpoint)
        - `git commit -m "algo"` : salva os arquivos (snapshot) e adiciona uma mensagem.
    - `git status` : exibe o estado atual do repositório.

### Ciclo de vida dos arquivos Git 

``git init`` : inicializa um conceito do Git chamado de __repositório Git__.

``tracked`` ou ``untracked`` : basicamente é um conceito que estabelece se o repositório Git __tem ciência da existência (tracked)__ ou __não (untracked)__ sobre os arquivos que estão dentro do repositório.

Os arquivos __tracked__ podem ter __3 diferentes estados__ :

- __unmodified__ : arquivos que ainda não foram modificados.

- __modified__ : arquivos que foram modificados.

- __staged__ : arquivos preparados para o commit.

Os arquivos "commitados" voltam ao estado de unmodified, __isso é um ciclo__. O commit é uma espécie de __snapshot__ do momento dos arquivos.

O repositório basicamente é onde está armazenado todo o seu projeto, com todas as branches e arquivos. Esse repositório fica armazenado em um servidor Git, geralmente na nuvem, em serviços como o GitHub. Quando vamos trabalhar nesse projeto, devemos antes fazer uma cópia local do repositório na nossa máquina. __Repositórios são divididos em 2 tipos__ : 

- Servidor (GitHub) 
- Ambiente de desenvolvimento (Git)

No ambiente de desenvolvimento temos __3 níveis de repositórios__ (Working Directory, Staging Area e Local Repository) . Os __arquivos ficam se alternando entre os 3 níveis__.

Quando temos uma pasta e arquivos sem inicializar um repositório Git , estamos no nível __working directory (diretório de trabalho)__.

Quando inicializamos um repositório Git naquele working directory, os arquivos passam para a __staging area (área de preparação)__ , onde podemos __modificar os arquivos e commitar__. Basicamente os arquivos vão estar na staging area quando criados, modificados ou adicionado ao repositório Git

Quando realizamos um commit, basicamente o Git pega o snapshot dos arquivos e joga no __local repository (repositório local)__, ou seja, o repositório local é __composto por commits__, onde podemos envia-los para um repositório remoto.

## Introdução ao GitHub

#### Visão geral

O GitHub é uma plataforma de hospedagem de código fonte e arquivos, e usa como controlador de versionamento o sistema Git.

#### Configuração 

- Comandos para configurar seu perfil no Git :
    - ``git config --global --unset user.email`` : para limpar o seu e-mail no perfil.
    - ``git config --global --unset user.nickname`` : para limpar o seu username no perfil.
    - ``git config --list`` : para ver a lista de configurações
    - ``git config --global user.email "seu email"`` : para adicionar o seu e-mail no perfil
    - ``git config --global user.nickname "seu nome"`` : para adicionar o seu username no perfil

- Configuração do seu repositório no Git :
    - Copiamos o caminho HTML do nosso repositório, que o GitHub vai dar e colocamos no Git.
    - ``git remote add origin`` : ( origin -> link do seu repositório GitHub) : comando para adicionar seu repositório do GitHub à sua maquina local.
    - ``origin`` : apelido do seu link repositório.
    - ``git remote -v`` : lista seus repositórios remotos.
    - ``git push origin master`` : empurra seu repositório local para o remoto.

#### Resolvendo conflitos

Como os conflitos acontecem no GitHub e como resolve-los :
   - Os conflitos ocorrem quando duas ou mais pessoas editam a mesma linha de código, dessa maneira é necessário analisarmos as alterações e fazer correções manuais.
        - ``git pull origin master`` : puxa o conteúdo do seu repositório remoto
        - Assim que puxamos o conteúdo , devemos verificar as modificações e fazer as devidas alterações e depois podemos subir ( push ) as alterações para o GitHub novamente.

- Como clonar um repositório público do GitHub na sua maquina : 

     - Entre em algum repositório público e clique no botão CODE

     - Copie esse link e vá no seu terminal Git e faça :  ``git clone ( link )``

### Outros comandos e complementos

``git log``: Serve para mostrar um histórico de alterações (commits) em forma de logs, com diversas informações, podendo ter uma série de parâmetros para que seja customizado, as informações e a maneira que é visualizado. Utilize ``git log --help`` para saber mais sobre.

__Árvore do Git__: quando inicializamos um repositório Git, automaticamente é criada uma __árvore (tree)__. Sendo que o código inicial do projeto é conhecido como __galho (branch)__. Ao trabalhar no projeto, podemos criar outras branches a partir da branch inicial, e toda modificação realizada, será refletida somente na branch estendida, sem modificar a branch pai (main/master).

__Commits__: são uma espécie de checkpoints, que servem para indicar que houve mudanças em nosso código. É uma boa prática acompanhar o commit uma pequena mensagem descritiva, que informa exatamente o que foi alterado.