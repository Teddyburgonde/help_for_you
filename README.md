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
ft_ft(....);
```
5. apres avoir appeler la fonction , imprime sa valeur 

## **C01 ex01** 

1. Dans l'exo d'avant tu avais UN(1) pointeur qui pointer sur un int 
```c
void   ft_ft(int *nbr)
{
   *nbr = 42;
}
```
la tu dois fais la meme chose mais avec plusieurs etoile, 
*nbr = 42 la il y a une seule etoile car il y avait juste un pointeur qui pointe sur int.
exemple :
```
*nbr -> c'est un pointeur
**nbr -> c'est un pointeur de pointeur
***nbr -> c'est un pointeur de pointeur de pointeur
etc...
```

Main

1. creer 9 pointeurs

```c
int *ptr1;
int **ptr2;
etc...
```
2. Faire pointer le pointer vers le pointeur inferieur
Quand tu veux faire pointer un pointeur vers le variable tu fais
```c
ptr = &nomdelavariable
```
la c'est la meme chose mais tu fais pointer le pointeur vers le pointeur inferieur et ainsi de suite
```c
ptr9 = &ptr8;
```
le dernier pointeur doit pointer vers une variable que tu auras donner la valeur 42;
```c
ptr1 = &nomdelavariable
```
3. imprime la valeur de ptr1
4. appel la fonction et en parametre donne lui ptr9
```c
ft_ultimate_ft(...);
```
5. imprime de nouveau la valeur
