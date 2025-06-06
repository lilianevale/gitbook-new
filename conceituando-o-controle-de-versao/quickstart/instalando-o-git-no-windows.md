# Instalando o Git no Windows

A seguir, é descrito os principais para a instalaçao do git:

* Acesse: [https://git-scm.com/download/win](https://git-scm.com/download/win) para fazer o download do instalador
* Execute o instalador (.exe).
* Durante a instalação, deixe as opções padrão, exceto quando aparecer "Choose the default editor used by Git", que pode ser por exemplo: Visual Studio Code software.
  * Na opção "Adjusting your PATH environment", escolha: "Git from the command line and also from 3rd-party software"
* Finalize a instalação.
* No terminal do computador, verifique se o git foi instalado corretamente:

```
$ git --version
```

O que deve retornar algo como: git version 2.xx.x



Após fazer o _donwload_ e instalação das aplicações precisamos configurar nosso Git na máquina.\
\
Este passo é fundamental, já que a ferramenta de versionamento, precisa reconhecer a máquina e o autor das alterações que serão posteriormente agregadas ao repositório remoto.\
\
Este passo pode ser feito de duas formas diferentes, sendo uma configuração global, ou seja, valida para qualquer repositório que está na máquina ou de forma individual. Inicialmente vamos configurar apenas duas informações, que já serão suficiente para prosseguirmos com nosso curso.\


Após a instalação, é necessário criar uma conta no repositório _online_ [GitHub](https://github.com/). Após a criação do login, você pode configurar seu nome e email para usar com Git/GitHub:

````
 ```bash $ git config --global user.name "Seu Nome" $ git config --global user.email "seu@email.com" ``` 
````

Pronto nosso ambiente Git já está configurado e preparado para o uso para verificar as credenciais utilize o comando:

```
$ git config --list
```
