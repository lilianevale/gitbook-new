# Clonando um repositório remoto e atualizando a versão local

O comando `clone` é utilizado para "copiar" um repositório online para uma pasta local. Lembrando que o comando `clone` já trás consigo as configurações `.git` que estabelecem que aquela pasta é monitorada pelo Git. Portanto não é necessário aplicar o `git init`.\
\
Para aplicar o clone basta executar o seguinte comando:

```
$ git clone https://github.com/nome_de_usuario/nome_do_repositorio
```

Após o `git clone` é comum que o desenvolver necessite fazer o _download_ de modificações efetuas por outros usuários no REPO. Para isso é necessário utilizar o comando `git pull`.\
\
Aqui é válido observar que o comando `pull` é executado na versão local, logo o que está acontecendo é um _download_ dos arquivos no computador e  a mesclagem dos mesmos no repositório local.
