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
É mostrado as adições/remoções naquela branch referente a branch referida
```

4. Escreva uma sequencia de comandos para mesclar o ramo não-master no `master`

```
git checkout master && git merge BRANCH
```


5. Escreva um comando (ou sequência) para (i) criar um novo ramo chamado `math` (do` master`)
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
git commit -a -m MESSAGE
```

8. Volte para o branch `master` e mude B.java adicionando o seguinte código-fonte (confirme sua mudança para` master`):
```java
System.out.println("Hello World")
```

9. Escreva uma sequência de comando para mesclar o branch `math` em` master` e descreva o que aconteceu
```
git checkout master && git merge math
```
  Houve um conflito de merge:

```
Auto-merging handson/B.java
CONFLICT (content): Merge conflict in handson/B.java
Automatic merge failed; fix conflicts and then commit the result.
```


10. Escreva um conjunto de comandos para abortar a mesclagem
```
git merge --abort
```
   
11. Agora repita o item 9, mas prossiga com a mesclagem manual (Editando B.java). Todas as funções implementadas são necessárias. Explique o seu procedimento

Arquivo B.java após o comando `git merge math`: 

```
public class B {


}
<<<<<<< HEAD
System.out.println("Hello World")
=======
System.out.println("I know math, look:")
System.out.println(2+2)
>>>>>>> math

```

Para resolve isso é necessário escolher qual das alterações será efetivada, caso as duas sejam aceitas é necessário alterar o código para que não haja problemas, resultado da alteração:

```
public class B {


}
System.out.println("Hello World")
System.out.println("I know math, look:")
System.out.println(2+2)
```

12. Escreva um comando (ou conjunto de comandos) para prosseguir com a mesclagem e atualizar o branch `master`
```
git commit -a -m "resolve merge master-math"
```


