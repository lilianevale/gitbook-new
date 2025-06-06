# Comando reflog

O **conceito de `reflog`** vem do **Git**, não diretamente do GitHub, mas é muito útil quando você está trabalhando com repositórios que estão no GitHub — especialmente se você **perdeu commits, branches ou fez um `reset` errado** e quer **recuperar um histórico recente**.

É  um **registro local** que guarda o **histórico de movimentações da referência `HEAD`** e de outras referências, como branches. Ele mostra **tudo que o Git fez recentemente**, mesmo que os commits não estejam mais visíveis no log comum.

Com o uso do reflog ele permite:

* Recuperar commits "perdidos" depois de `reset`, `rebase`, `merge` ou `checkout`.
* Ver o histórico de alterações em branches.
* Restaurar um branch deletado acidentalmente.
* Encontrar o hash de um commit antigo.

**Exemplo de uso:**

```
git reflog
```

saída:

```
f3c4e3b HEAD@{0}: reset: moving to HEAD~1
a5b2c2d HEAD@{1}: commit: Corrige bug na autenticação
2e1f998 HEAD@{2}: checkout: moving from main to dev
```

Cada linha  da saída mostra:

* Um commit (`f3c4e3b`)
* A posição no histórico (`HEAD@{0}`)
* O tipo de operação
* Uma descrição



Para recuperar um commit perdido, se foi feito um `git reset --hard` e quer desfazer:

```
git reflog
git checkout <hash_do_commit>
```

```
git reset --hard <hash_do_commit>
```

O `reflog` é **local** e não sincroniza com o GitHub. Ele é automaticamente limpo depois de 90 dias por padrão (ou com `git gc`).

* O GitHub **não tem reflog** — só existe **no seu repositório local**.
* Se você **perder algo e já fez `push` para o GitHub**, o GitHub terá o estado atual, mas **não guarda o histórico "interno" como o reflog faz**.

Quando usar o reflog:

* Quando apagou um branch ou commit por acidente.
* Fez um `git reset` e se arrependeu.
* Precisa entender uma mudança que não aparece no `git log`.
