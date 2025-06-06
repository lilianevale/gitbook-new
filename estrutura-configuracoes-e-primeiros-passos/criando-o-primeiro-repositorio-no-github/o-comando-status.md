# O comando Status

É possível obter  informações sobre o estado atual do  diretório de trabalho e da área de preparação (staging). Isso proporciona uma visão das alterações que foram realizadas, mas ainda não estão preparadas para serem registradas.

Suponha que desejamos adicionar um arquivo de extensão markdown a área de preparação (staging). Qual seria o status de um arquivo? Para saber a resposta precisamos digitar o sequinte comando no terminal do computador:

```
$ git status
```

```
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   001-1.md
```

> Neste exemplo, pode-se notar que  o arquivo `001-1.md` foi modificado e está pronto para  um _upload_ para o repositório local, ou seja, fazer o `commit`.

Outras possibilidades são usadas para visualizar o _status_ da modificação. Isso pode ser feito usando

&#x20;`git status --short`.&#x20;

Este comando fornece informações de forma compacta, mostrando o estado dos arquivos na área de preparação (_staging_) e no diretório de trabalho. A saída do `git status --short` é geralmente apresentada em duas colunas. A primeira coluna, mostra o status dos arquivos na área de preparação, e a segunda coluna mostra o status dos arquivos no diretório de trabalho.\
\
No caso do exemplo anterior apenas o arquivo `001-1.md` esta preparado.

```
M  001-1.md
M 002-1.md
M 002-2.md
```
