# Commits

O comando "commit" é de extrema importância no Git, pois é responsável por preparar as alterações locais para o repositório local. Além disso, possibilita a inclusão de uma mensagem descritiva que documenta o propósito das mudanças realizadas. Dessa forma o comando usado para comitar as alterações feitas em arquivo é o seguinte:

```
$ git commit
```

> Um editor de texto será aberto e sua mensagem poderá ser escrita no seguinte padrão:

```
<titulo>

<corpo 1>
<corpo 2>
<corpo 3>
# E assim conforme a demanda
```

Você também pode efetuar a transmissão direta da mensagem do `commit` via o próprio comando para isso utilize:

```
$ git commit -m <"msg descritiva da alteracao">
```

{% hint style="info" %}
> Este comando não altera o repositório do GitHub remoto. Além disso somente é realizado o `commit` nos arquivos que já foram preparados por meio do comando `add`.
{% endhint %}

Caso seja feita um `commit` prematuro e você necessite fazer alterações no seu último _update_ utilize o comando `git commit --amend -m <"msg nova">`. A seguir mostramos a sequência exemplo:

```
# Edita o hello
$ git add hello.py
$ git commit -m "novo arquivo" 
# Você esqueceu o arquivo main como fazemos?
$ git add main.py 
$ git commit --amend -m "adicionou novo arquio"
# Pronto commit realizado!
```

{% hint style="info" %}
Para não alterar a menssagem no `commit` pode ser utilizada a sintaxe `git commit --amend --no-edit`.
{% endhint %}

É possível adicionar emojis  (reactions) ao `commits` e isso melhora a compreensão e a comunicação do time de desenvolvimento. Para adicionar o emoji basta fazer isso em formato de código. Para verificar a lista de emoji podemos checar a [documentação](https://gist.github.com/rxaviers/7360908). Considere um exemplo:

```
git commit -m ":bulb: botão na página inicial"
```

Em alguns casos, pode-se combinar o add e commit. Esta opção faz automaticamente o commit de todos os arquivos (incluindo os novos) rastreados, modificados ou excluídos.

```
git commit -a -m "adiciona e faz commit das mudanças"
```

É possível listar os _commits_ que foram realizados mostrando detalhes de cada um deles para isso vamos usar o seguinte comando:

```
$ git log
```

```
commit c4aaf9d736eedba04f88b9909287dde10638ba98 (HEAD -> main, origin/main, origin/HEAD)
Author: wmpjrufg <wanderlei_junior@ufcat.edu.br>
Date:   Tue Oct 24 09:31:49 2023 -0300

    fix: colocação do conceito de repo e branch

commit 4c6160b3e346146a2f640ae1671dc1d216659925
Author: wmpjrufg <wanderlei_junior@ufcat.edu.br>
Date:   Mon Oct 23 22:54:23 2023 -0300
```

Veja que o comando mostra informações adicionais sobre o _commit,_  como por exemplo,   data/hora, hash (identificador) e nome do autor do _commit_.

Adicionalmente, para mostrar commits resumidos, podemos digitar no terminal:

```
git log --oneline
```

Por fim, para mostrar com gráficos (visualizar branches), podemos digitar no terminal:

```
git log --graph --oneline --all
```

Tambem é possível acessar commits pela interface web do GitHub, para isso desempenhe os seguintes passos:\
1- Vá até o repositório no GitHub.

2- Clique na aba Commits (geralmente fica perto de “Code”).

3- Você verá a lista de commits, com:

&#x20;    \- Mensagens

&#x20;    \- Autor

&#x20;    -Data e hora

Clique em qualquer commit para ver os detalhes e as alterações feitas.

Em algumas situações pode-se  modificar um arquivo mas que ainda não fez o  commit e quer voltar para a última versão salva no Git, neste caso, pode-se digitar o sequinte comando para desempenhar esta operação:

```
git checkout -- nome-do-arquivo.ext
```

Isso descarta todas as alterações feitas no arquivo desde o último commit.\
Agora, considere o caso em que o usuário queira reverter todos os arquivos modificados \


```
git checkout -- .
```

Este comando permite desfazer todas as alterações locais que não foram comitadas.

Caso queira desfazer um commit já enviado, mas mantendo as alterações no arquivo (modo "_unstaged_"):

```
git reset --soft HEAD~1
```

Para desfazer o último commit e apagar as alterações:

```
git reset --hard HEAD~1
```

Adicionalmente, pode-se aplicar o comando _**restore**_ que permite reverter as alterações:

```
git restore nome-do-arquivo.ext
```

Mas atenção, antes de executar o comando tenha certeza de que não irá perder conteído relevante!
