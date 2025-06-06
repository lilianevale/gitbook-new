# Tags no GitHub

As _tags_ no GitHub (e no Git, de forma geral) são usadas principalmente para marcar versões específicas do seu projeto, como lançamentos (`v1.0`, `v2.1.3`, etc.). Elas são muito úteis, especialmente quando combinadas com o sistema de _releases_ do GitHub. Abaixo explico como criar e usar tags localmente com Git e como usá-las no GitHub.

Existem dois tipos de _tags_ no Git:

* **Leves (lightweight)**: apenas um marcador para um commit.
* **Anotadas (annotated)**: guardam informações extras como autor, data, e mensagem, sendo mais recomendadas para versões.

### Criar uma tag anotada:

```
git tag -a v1.0 -m "Versão 1.0 estável"
```

### Criar uma tag resumida:

```
git tag v1.0
```



### Ver detalhes de uma tag:

```
git show v1.0
```

### Ver todas as tags:

```
git tag
```

### Subir uma tag específica para o GitHub:

```
git push origin v1.0
```

### Subir todas tags:

```
git push origin --tags
```

### Usar Tags para Releases no GitHub:

Depois que a _tag_ está no GitHub,  pode usá-la para criar uma **release**:

1. Vá até o repositório no GitHub.
2. Clique em **"Releases"** no menu do repositório.
3. Clique em **"Draft a new release"**.
4. Escolha a tag existente (ou crie uma nova).
5. Preencha o título e a descrição.
6. Clique em **"Publish release"**.



### Atualizar ou Deletar Tags:

Para excluir tag local execute o seguinte comando:

```
git tag -d v1.0
```

### Excluir tag no remoto (GitHub):

```
git push origin --delete tag v1.0
```
