# Comando merge

&#x20;O comando **`merge`** no Git (e, consequentemente, no GitHub) serve para **juntar duas branches (ramificações) diferentes** em uma só.

Quando você cria uma branch para desenvolver uma nova funcionalidade ou corrigir um erro, o `git merge` serve para combinar essa branch com outra (geralmente a branch principal, chamada `main` ou `master`).

**Exemplo 1:**  Você está na branch `main`  e quer criar uma nova branch chamada `feature` para desenvolver algo novo:

```
git checkout -b feature
```

Feito as alterações, queremos fazer um commit:

```
git add .
git commit -m "Nova funcionalidade"
```



Em seguida, queremos voltar para a branch main:

```
git checkout main
```

e fazer a operação de merge:

```
git merge feature
```

Se as duas branches tiverem alterações nos mesmos trechos de um arquivo, o Git irá gerar um **conflito**. Você precisará resolver manualmente, editar o arquivo, salvar e depois fazer:

```
git add .
git commit -m "Resolvendo conflitos"
```

Alternativamente, pode fazer o **merge diretamente no GitHub**, usando **Pull Requests sem terminal:**

Inicialment&#x65;**,** vamos criar uma branch. Para isso, no seu repositório, clique no menu suspenso onde está escrito **`main`** (ou o nome da branch principal). Digite um nome para a nova branch, como **`feature`**, e clique em **"**_**Create branch: feature**_**"**.

Em seguida faça as devidas alterações na nova branch, editando arquivos diretamente no GitHub (ou envie arquivos via upload). Após editar, clique em **"**_**Commit changes"**_, adicione uma mensagem e confirme.

**Crie um Pull Request (PR)**

* O GitHub irá sugerir: **"Compare & pull request"** — clique nesse botão.
* Ou vá até a aba **"Pull requests"** e clique em **"New pull request"**.
* Verifique se a base está em **`main`** e a branch de comparação é a sua, como **`feature`**.
* Escreva um título e uma descrição (opcional).
* Clique em **"Create pull request"**.
* Em seguida, faça o merge:&#x20;
  * Na tela do Pull Request, clique no botão verde **"Merge pull request"**.
  * Confirme clicando em **"Confirm merge"**.
  * (Opcional) Após o merge, clique em **"Delete branch"** para apagar a branch que não é mais necessária.

Caso ocorra conflitos, o GitHub avisará com uma mensagem como **"This branch has conflicts":**

* Clique em **"Resolve conflicts"**.
* Edite os arquivos para remover os sinais de conflito (`<<<<<<<`, `=======`, `>>>>>>>`).
* Clique em **"Mark as resolved"**, depois em **"Commit merge"**.
* &#x20;Finalize clicando em **"Merge pull request"**.

