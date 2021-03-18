# Git Assignment
## Como entregar
Copie o arquivo em um repositorio que seja seu e coloque as respostas nas caixas abaixo

Abra uma issue nesse repositório aqui indicando o link para o arquivo no seu repo.

1. Descreva qual é a saída dos seguintes comandos
    -  `git branch` 
    -  `git checkout BRANCH_NAME` (USE THE NAME OF AN EXISTING BRANCH)
    -  `git log --decorate`

```
git branch > Mostra a branch atual do projeto;
git checkout BRANCH_NAME (USE THE NAME OF AN EXISTING BRANCH) > Muda a branch atual;
git log --decorate > Mostra o histórico de commit no projeto (branch atual); 
```

2. Tente usar `git log --graph --all`. O que acontece?
```
O histórico de commits é mostrado com apenas o commit inicial do projeto
```

3. Use `git diff BRANCH_NAME`  para ver as diferenças de um ramo e do ramo atual.
   Sumarize as diferenças do master e do outro ramo.

```
É mostrado as adiç?es/remoç?es naquela branch referente a branch referida
```

4. Escreva uma sequencia de comandos para mesclar o ramo n?o-master no `master`

```
git checkout master && git merge BRANCH
```


5. Escreva um comando (ou sequ?ncia) para (i) criar um novo ramo chamado `math` (do` master`)
e (ii) mudar para este ramo

```
git checkout master && git checkout -b math
```
   
6. Edite B.java adicionando o código abaixo ao conteúdo do arquivo
```java
System.out.println("I know math, look:")
System.out.println(2+2)
```

7. Escreva o comando (ou sequencia) para realizar o commit de suas mudanças
```


```

8. Volte para o branch `master` e mude B.java adicionando o seguinte código-fonte (confirme sua mudança para` master`):
```java
System.out.println("Hello World")
```

9. Escreva uma sequ?ncia de comando para mesclar o branch `math` em` master` e descreva o que aconteceu
```


```
   
10. Escreva um conjunto de comandos para abortar a mesclagem
```


```
   
11. Agora repita o item 9, mas prossiga com a mesclagem manual (Editando B.java). Todas as funç?es implementadas s?o necessárias. Explique o seu procedimento
```


```

12. Escreva um comando (ou conjunto de comandos) para prosseguir com a mesclagem e atualizar o branch `master`
```


```


