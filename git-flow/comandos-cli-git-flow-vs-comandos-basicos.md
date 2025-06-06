# Comandos CLI Git Flow vs Comandos básicos

Segue abaixo a lista de comandos referentes ao CLI do Git Flow, que já esta imbutido na versão do git já insatalada na sua maquina.

### Iniciando o Git Flow

```bash
#Comando básico
$ git checkout -b develop
```

```bash
#Comando CLI Git Flow
$ git flow init
```

### Criação de uma feature

```bash
#Comando básico
$ git checkout develop
$ git checkout -b feature/NOME_FEATURE
```

```bash
#Comando CLI Git Flow
$ git flow feature start feature/NOME_FEATURE
```

### Finalização de uma feature

```bash
#Comando básico
$ git checkout develop
$ git merge feature/NOME_FEATURE
```



```bash
#Comando CLI Git Flow
$ git flow feature finish  feature/NOME_FEATURE
```

### Criação de um Hotfix

```bash
#Comando básico
$ git checkout master
$ git checkout -b hotfix/NOME_HOTFIX
```



```bash
#Comando CLI Git Flow
$ git flow hotfix start hotfix/NOME_HOTFIX
```

### Finalização de um Hotfix

```bash
#Comando básico
$ git checkout master
$ git merge hotfix/NOME_HOTFIX
$ git checkout develop
$ git merge hotfix/NOME_HOTFIX
$ git tag hotfix/NOME_HOTFIX
```



```bash
#Comando CLI Git Flow
$ git flow hotfix finish hotfix/NOME_HOTFIX
```

### Criação de uma Release

```bash
#Comando básico
$ git checkout develop
$ git checkout -b release/1.0.0
```



```bash
#Comando CLI Git Flow
$ git flow release start 1.0.0
```

### Finalização de uma Release

```bash
#Comando básico
$ git checkout master
$ git merge release/1.0.0
$ git checkout develop
$ git merge release/1.0.0
$ git tag 1.0.0
```



```bash
#Comando CLI Git Flow
$ git flow release finish 1.0.0
```
