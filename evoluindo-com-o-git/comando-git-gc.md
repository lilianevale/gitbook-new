# Comando git gc

O comando `git gc` (abreviação de **garbage collect**) é uma ferramenta de manutenção do Git que **otimiza o repositório**, limpando e compactando arquivos internos para melhorar o desempenho e economizar espaço em disco.

1.  Remove arquivos desnecessários: Exclui objetos órfãos (dados de commits ou blobs que não são mais referenciados).

    Remove arquivos temporários antigos.
2. Compacta objetos soltos em pacotes (packfiles): Em vez de guardar cada objeto como um arquivo separado, o Git agrupa vários objetos em arquivos compactados, mais eficientes.
3. Remove reflogs antigos: Os reflogs armazenam o histórico de movimentações de referências (como HEAD), e entradas muito antigas podem ser descartadas.

🛠️ Quando usar git gc?

<pre><code><strong>- Quando seu repositório está ficando lento.
</strong>
<strong>- Quando o diretório .git/ está ocupando muito espaço.
</strong>
<strong>- Depois de muitas operações (merge, rebase, reset, etc.).
</strong>
- Em repositórios muito grandes ou antigos.
</code></pre>

### Comando sbásico:

Isso roda a coleta de lixo padrão.

```
git gc
```

### Comando agressivo:

Faz uma compactação mais profunda, mas é mais lenta. Ideal para grandes otimizações esporádicas.

```
git gc --aggressive
```



O Git roda `git gc` automaticamente em segundo plano depois de um certo número de operações (por padrão, 670 commits, 50 mudanças de refs, etc.), **mas nem sempre de forma agressiva**.

{% hint style="info" %}
* Não interrompa o processo no meio — pode corromper o repositório.
* Não é necessário usar com frequência em repositórios pequenos ou com poucos colaboradores.
{% endhint %}

#### Exemplo de uso: <a href="#comando-agressivo" id="comando-agressivo"></a>

Ver o tamanho atual do repositório:

```
du -sh .git
```

Rode este comando para verificar o tamanho total dos dados internos do Git. Isso mostra o tamanho da pasta `.git`, que armazena todos os dados versionados.



**Executar o git gc**

```
git gc --aggressive --prune=now
```

* `--aggressive`: tenta otimizar ao máximo (mais lento).
* `--prune=now`: remove imediatamente objetos órfãos



Ver o tamanho após o `git gc:`

```
du -sh .git
```

Compare o valor antes e depois. Em repositórios grandes, a diferença pode ser significativa (vários MBs ou até GBs).

Para ver estatísticas com `git count-objects`  digite o seguinte comando:

```
git count-objects -vH
```

Isso mostra:

* Objetos soltos (`loose objects`)
* Tamanho ocupado
* Número de pacotes (`packs`)
