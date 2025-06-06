# Comando .gitignore

Por padrão, o Git possui um arquivo chamado [_.gitignore_](https://docs.github.com/pt/get-started/getting-started-with-git/ignoring-files), que serve para manter arquivos ou pastas fora do rastreamento do Git. Esta funcionalidade é útil quando queremos utilizar um arquivo/pasta apenas de forma local.\
\
Para utilizar essa funcionalidade basta criar um arquivo com o nome `.gitignore` (caso ele não exista) no diretório em que deseja ocultar o arquivo/pasta. Então, todos os nomes de arquivos ou extensões que forem adicionados nele, não serão adicionados ao sistema de controle. Vamos aos exemplos:



\


> É necessário usar a nomenclatura completa com o `.` antes do nome `gitignore`.

Para  ignorar arquivos no Git/GitHub deve-se criar um arquivo .gitignore na raiz do projeto\
Se ainda não existir, crie um arquivo chamado .gitignore dentro da pasta principal do  projeto.

**Exemplo 1:** _Vamos supor que desejemos ignorar todos os arquivos com a extensão `.log`. Como ficaria o arquivo `.gitignore`?:_

Entrando dentro do arquivo `.gitignore` editamos da seguinte forma:

```shell
*.log
```

**Exemplo 2:** _Vamos supor que desejemos ignorar todos as pastas com a nomenclatura `logs`. Como ficaria o arquivo `.gitignore`?:_

Entrando dentro do arquivo `.gitignore` editamos da seguinte forma:

```shell
**logs/
```

**Exemplo 3:** _Vamos supor que desejemos ignorar todos os arquivos com a extensão `.log`. Porém esse arquivo `.log` tem variações do tipo `debugA.log`, `debug10.log`. . Como ficaria o arquivo `.gitignore`?:_

Entrando dentro do arquivo `.gitignore` editamos da seguinte forma:

```shell
debug?.log
```

##

**Exemplo 4:** _Vamos supor que desejemos &#x69;_&#x67;norar pasta node\_modules e ignorar arquivos de ambiente, neste caso os comandos são o seguinte, respectivamente:

```
 node_modules/
 .env

```

{% hint style="info" %}
#### Arquivos já versionados não serão ignorados automaticamente
{% endhint %}

Se um arquivo já foi enviado para o Git (já está no histórico), o .gitignore não vai removê-lo automaticamente. Para isso:

```
git rm --cached nome-do-arquivo.ext
git commit -m "Remove arquivo ignorado"
```

Além disso, o .gitignore pode ter comentários (linhas que começam com #) e pode usar curingas, ex: \*.log ignora todos arquivos com extensão .log.\
\


Use um gerador online para criar .gitignore específico para seu projeto:\
[https://www.toptal.com/developers/gitignore\
](https://www.toptal.com/developers/gitignore)
