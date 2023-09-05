# O que é o Git stash e para que serve? 
### O Git stash arquiva alterações não commitadas do seu local de trabalho, ou seja, ele volta para o estado do seu último **_commit_** guardando as alterações adicionais que você tinha feito. Fazendo uma analogia, é quase como se fizesse um backup das modificações dos seus arquivos.

### Existem algumas situações bem úteis para utilizar o comando, algumas delas listadas abaixo:

+ Você está trabalhando em algumas modificações e precisa fazer um teste desconsiderando o que você fez, mas sem perder tudo.

+ Você começou a desenvolver na branch errada e não quer perder as alterações.
Decidiu que vai criar uma nova branch a partir dessas modificações e não mais vai trabalhar na branch que está.

+ Testará uma nova abordagem para o mesmo problema sem perder a versão que estava trabalhando e também sem precisar fazer um commit.
Precisará fazer uma modificação em um outro branch ou até fazer um conserto rápido, mas não quer perder as alterações que fez até agora e nem fazer um commit. 

Em todas essas situações você pode utilizar o git stash para ajudar você. 

O que acontece na prática é que o Git cria uma branch temporária com todas as alterações que você tinha feito, volta para a branch que você estava trabalhando e desfaz tudo que não estava commitado. Ao longo desse post, vamos explicar melhor como fazer para recuperar essas alterações, como criar novas branches a partir delas, entre outras opções. 

## Como usar o Git stash?

### Para salvar suas alterações no stash, execute o comando:

```
git stash save "mensagem opcional para você mesmo"
```

Isso salvará suas alterações e reverterá o diretório de trabalho ao que parecia anteriormente ao último _commit_. As alterações em stash estão disponíveis para qualquer branch daquele repositório.

### Para ver o que está no seu stash, execute o comando:

```
git stash list
```

Isso retornará uma lista de seus instantâneos salvos no formato `stash@{0}: BRANCH-PARA-A-QUAL-SÃO-AS-ALTERAÇÕES-EM-STASH: MESSAGE`. A parte do `stash@{0}` é o nome do stash, enquanto o número entre chaves (`{ }`) é o índice daquele stash. Se você tiver vários conjuntos de alterações em stash, cada conjunto terá um índice diferente.

### Para obter as alterações do stash e aplicá-las à branch atual, na qual você está, você tem duas opções:

**1.** 
```
git stash apply NOME-DO-STASH
``` 
+ Aplica as alterações e deixa uma cópia no stash

**2.** 
```
git stash pop NOME-DO-STASH
```
+ Aplica as alterações e remove os arquivos do stash

### Se quiser remover alterações do stash sem aplicá-las, execute o comando:

```
git stash drop NOME-DO-STASH
```

### Para limpar todo o stash, execute o comando:

```
git stash clear
```