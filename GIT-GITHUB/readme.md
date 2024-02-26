# Gerenciamento de código com git e gitHub

## O que é git ?

* Git, basicamente são comandos utilizados pelo terminal, onde gerenciamos o histórico de mudanças usando um sistema de controle de versão desenvolvido por Linus Torvalds (o criador do Linux). Isso significa que qualquer desenvolvedor numa equipe pode gerenciar o repositório local (código que está no nosso computador) e o repositório remoto (pasta do nosso projeto que está no gitHub)

Exemplos:
* git add .
* git status
* git push origin main

## O que é terminal ?

* É uma famosa tela preta, conhecida pelos programadores, na qual você digita comandos para dar instruções para um computador e visualizar informações dessa máquina. Ou seja, ele serve para você executar tarefas no computador sem utilizar a interface gráfica, com pastinhas e ícones, ou o bom e velho mouse

Exemplos:
* CMD
* PowerShell
* GitBash

## O que é gitHub ?
* GitHub é uma espécie de "rede social para programadores". Sendo um repositório remoto (código que está na nuvem) utilizado com um serviço de publicação e compartilhamento de códigos de programação. Lançada em 2008, a plataforma é usada mundialmente e é, desde 2018, de propriedade da Microsoft

<hr>

## Principais comandos git

```
git init
```
* Este comando cria um repositório Git vazio, basicamente uma pasta oculta ".git", responsável pelo gerenciamento dos repositórios e arquivos contidos na pasta criada no computador onde o comando foi executado

* Comando sendo executado<p>
<img src="./img/git_init.png">

* Imagem da pasta .git no computador<p>
<img src="./img/repo_git.png">

<hr>

### A primeira coisa que você deve fazer após instalar o Git é configurar seu nome de usuário e endereço de e-mail. Isto é importante porque cada commit usa esta informação, e ela é carimbada de forma imutável nos commits que você começa a criar

```
git config -l
```
* Este comando "git config" obtem e define opções globais ou do repositório

```
git config --global user.name "DIGITE_SEU_NOME_AQUI"
```
* Altere o campo 'DIGITE_SEU_NOME_AQUI' e coloque o seu nome

```
 git config --global user.email "DIGITE_SEU_EMAIL_AQUI"
```
* Altere o campo 'DIGITE_SEU_EMAIL_AQUI' e coloque o seu email do gitHub

<hr>

```
git clone
```
* O comando é executado junto com a URL do repositório do gitHub em uma pasta criada no computador

* Imagem do comando "git clone" sendo executado
<img src="./img/git_clone.png">

<hr>


