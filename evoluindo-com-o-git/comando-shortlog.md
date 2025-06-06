# Comando shortlog

O `git shortlog` é um comando do Git usado para gerar um **resumo dos commits agrupados por autor**, geralmente com contagem de commits e mensagens em ordem cronológica ou alfabética. Embora seja um comando do **Git local**, seu resultado pode ser usado no GitHub para **gerar changelogs**, **créditos** ou **resumos de contribuições**.

Permte agrupar os commits por autor e mostra quantos commits cada um fez, com as mensagens de cada commit (opcionalmente). Considere o seguinte exemplo:

```
$ git shortlog
Alice Silva (3):
      Corrige erro de layout
      Adiciona componente de login
      Atualiza documentação

Carlos Souza (2):
      Refatora lógica de autenticação
      Melhora testes de integração

```

Resumo com contagem de commits:

```
git shortlog -s
```

```
  //saida
  3  Alice Silva
  2  Carlos Souza
```

Com nomes e emails:

```
git shortlog -sne
```

saída:

```
  3  Alice Silva <alice@example.com>
  2  Carlos Souza <carlos@example.com>
```

Para um intervalo específico  que mostra o resumo de commits entre as _tags_ `v1.0` e `v2.0`.

```
git shortlog v1.0..v2.0
```

Embora o GitHub não tenha um botão "Shortlog", você pode:

* Rodar `git shortlog` localmente e colar na seção de **release notes** do GitHub.
* Usar para gerar **créditos** automáticos de contribuição.
* Integrar em scripts de **CI/CD** para gerar changelogs.
