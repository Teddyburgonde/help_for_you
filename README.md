# help_for_you

## C01 ex00

ceci est le prototype de la fonction 
```c
void	ft_ft(int *nbr)
```
etape 1 :
Ce que tu dois faire c'est mettre la valeur dans la variable qui est entre parametre 

```c
*nbr = 10;
```

Erreur a eviter : 
si tu ecris 
```c
nbr = 10; ❌
```
C'est une erreur car nbr sans * c'est juste une variable qui n'a pas de type.

Par contre si tu ecris ceci 

```c
*nbr = 10;
```
La c'est correct car * devant une variable permet de detuire que c'est un pointeur. 

rappel 
```
int nbr -> nbr c'est un int
int *nbr -> nbr c'est un pointeur
```
## le main 

Maintenant que tu as ecris ta fonction tu veux la testé : 
1. Cree un pointer et une variable de type int

```c
int *ptr;
int  nombre;
```
2. Donne une valeur a int et accede a cette valeur grace au pointeur.
tu ne peux pas assigner directement une valeur a un pointeur tu dois ABSOLUMENT passer par une variable.

```c
int  nombre;
int  *ptr;
nombre = 5;
// la tu dis a ton pointeur que tu veux qu'il pointe vers adresse(&) de la variable nombre.
// comme il a l'adresse il peut avoir acces a la valeur; 
ptr = &nombre;
```

3.Imprime la valeur du pointeur 
```c
// * permet d'avoir access a la valeur de ptr, si tu aurais mit & devant ptr tu aurais access a son adresse
printf("%d\n", *ptr);
```

4. appel la fonction puis re imprime la valeur
   La fonction prends quoi en paramettre ? un int ou un pointeur ?
```c
ft_ft(&....);
```
5. apres avoir appeler la fonction , imprime sa valeur 



