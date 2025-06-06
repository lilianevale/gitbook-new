# Adicionando arquivos no repositório

Adicionar novos arquivos no GitHub pode ser feito de duas formas principais: diretamente pela interface web do GitHub ou usando o Git no seu computador. Vamos  mostrar as duas alternativas.

### Adicionar arquivos usando o Git localmente

Vamos iniciar o processo de _upload_ de arquivos para o repositório remoto. Para isso iremos empregar nossos primeiros comandos Git que são destinados a este fim.

**Passo a passo:**

1. Coloque o novo arquivo dentro da pasta do seu projeto local.
2. Abra o terminal na pasta do projeto e execute:

```
git add nome-do-arquivo.ext
```

3. Faça o commit das mudanças:

```
git commit -m "Adiciona nome-do-arquivo.ext"
```

{% hint style="info" %}
O comando commit será explicado em detalhes nas próximas seções.
{% endhint %}

4. Envie as alterações para o GitHub:

```
git push
```

\
Se quiser adicionar todos os arquivos novos/modificados de uma vez, use:

```
git add .
```

Isso adiciona tudo que mudou na pasta do projeto.&#x20;

### Adicionar arquivos diretamente pelo site do GitHub

Para adicionar arquivos no repositório na página do GitHub, desempenhe as seguintes etapas:

1. Selecione o repositório no GitHub.
2. Clique no botão **Add** file (Adicionar arquivo).
3. Escolha _**Create new file**_ (Criar novo arquivo).
4. Digite o nome do arquivo (ex: novo-arquivo.txt) e escreva o conteúdo.
5. Escreva uma mensagem de _commit_ (ex: “Adiciona novo arquivo”).
6. Clique em _Commit_ new file para salvar.\
