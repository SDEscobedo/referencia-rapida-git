# Git Log

O comando `git log` é usado para visualizar o histórico de commits em um repositório Git. Ele exibe informações detalhadas sobre cada commit, como código do commit, autor, data e comentário associado.

## Sintaxe

```
git log
```

## Parâmetros Comuns

- `--oneline`: Exibe cada commit em uma única linha, com a mensagem resumida.
- `--author=<autor>`: Filtra os commits pelo autor especificado.
- `--since=<data>`: Mostra commits feitos após a data especificada.
- `--until=<data>`: Mostra commits feitos antes da data especificada.

## Exemplos

### Exibir log completo

```
git log
```

### Exibir log com detalhes abreviados

```
git log --oneline
```

### Exibir log por autor

```
git log --author="Nome do Autor"
```

### Exibir log desde uma determinada data

```
git log --since="2023-01-01"
```

### Exibir até uma determinada data

```
git log --until="2023-08-30"
```

### Exibir log por comentário

```
git log --grep="<texto_do_comentário>"
```
