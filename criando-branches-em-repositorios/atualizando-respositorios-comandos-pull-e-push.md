# Atualizando respositórios: comandos pull e push

Nessa seção serão discutidas possibilidades de atualização de um repositório remoto. O comando `push` permite  fazer o _upload_ dos arquivos do repositório local para o repositório remoto.&#x20;

```
$ git push
```

{% hint style="info" %}
O comando completo necessita de especificação da _branch_ para que o upload seja feito na ramificação correta. O comando completo é: git push `<remote>` `<branch>`. Normalmente a especificação `<remote>` para um repositório é remoto é a expressão `origin`. Conforme o exemplo que faz o _upload_ para _branch_ remota `main`.
{% endhint %}

```
$ git push origin main
```

_**Exemplo**: Qual seria uma sequência completa de três modificações (3 `commits`) para fazer o upload para uma branch remota denominada joao._

```
$ git add . 
$ git commit -m "modificação 1"
$ git add main.py schema.py
$ git commit -m "modificação 2"
$ git add .
$ git commit -m "modificação 3"
$ git push origin joao
```

Além da atualização do repositório remoto é necessário fazer a atualização do repositório local. Para isso precisamos sempre executar o comando `git pull`. Esse comando tem muito importância por atualizaremos o nosso repositório local com todas as modificações do repositório remoto. Isso é essencial para mitigação de futuros erros no processo de mesclagem de branchs e desatualização não planejada do algoritmo.

```
$ git pull
```

Vantagens do Pull Request

1. Processo organizado e colaborativo
2. Permite revisão de código antes de unir
