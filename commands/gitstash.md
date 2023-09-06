# Git Stash: Uma Ferramenta Poderosa para o Gerenciamento de Alterações

O Git stash é uma funcionalidade essencial para o controle de alterações não confirmadas em seu ambiente de trabalho. Ele permite que você retorne ao estado do seu último **_commit_**, enquanto armazena cuidadosamente as modificações adicionais que você realizou. Pode-se pensar nele como uma espécie de backup das suas alterações de arquivo.

## Por que Usar o Git Stash?

Há várias situações úteis em que o Git stash pode ser aplicado:

- Quando você está trabalhando em modificações e deseja realizar testes temporários, sem comprometer as mudanças existentes.
- Se você começou a desenvolver na branch errada e deseja salvar as alterações para criar uma nova branch ou continuar em outra.
- Ao testar uma nova abordagem para um problema, sem perder a versão atual e sem precisar fazer um commit temporário.
- Quando é necessário fazer uma correção rápida em outro branch sem perder as alterações feitas até o momento ou criar um commit adicional.

O Git stash é a solução para todas essas situações.

## Como Utilizar o Git Stash

Para armazenar suas alterações no stash, execute o seguinte comando:

```bash
git stash save "mensagem opcional para referência"
```

Isso preservará suas modificações e reverterá o diretório de trabalho ao estado anterior ao último commit. As alterações no stash podem ser acessadas a partir de qualquer branch no mesmo repositório.

## Visualizando os Instantâneos do Stash

Ao executar o seguinte comando:

```bash
git stash list
```
Você receberá uma lista dos seus instantâneos armazenados no seguinte formato: 


`stash@{0}:BRANCH-DESTINO-DAS-ALTERAÇÕES-EM-STASH: MENSAGEM.`

O termo `stash@{0}` é o identificador do stash, enquanto o número entre chaves (`{ }`) indica o índice daquele stash. Em caso de múltiplos conjuntos de alterações armazenados no stash, cada um terá um índice único.

## Aplicando Alterações do Stash à Branch Atual
Para aplicar as alterações do stash à branch atual, você tem duas opções:

1. Utilize o seguinte comando:

```bash
git stash apply NOME-DO-STASH
```

Esta opção aplica as alterações do stash à branch atual e mantém uma cópia no stash para uso posterior.

2. Use o seguinte comando:

```bash
git stash pop NOME-DO-STASH
```

Esta alternativa aplica as alterações do stash à branch atual e remove os arquivos do stash, deixando-a limpa.

## Removendo Alterações do Stash Sem Aplicá-las
Se desejar descartar as alterações do stash sem aplicá-las, utilize o comando a seguir:

```bash
git stash drop NOME-DO-STASH
```

## Limpando Completamente o Stash
Para realizar uma limpeza completa do stash, execute o seguinte comando:

```bash
git stash clear
```
Estas operações permitem um controle preciso das suas alterações com o Git stash.