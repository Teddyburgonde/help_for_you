# help_for_you


![Screenshot from 2024-03-30 13-23-52](https://github.com/Teddyburgonde/help_for_you/assets/93845046/46413029-f80c-477c-9a9b-2bc6fde14733)

❌❌❌❌❌❌❌❌❌❌❌❌❌❌❌❌❌❌❌❌❌❌❌❌❌❌❌❌❌❌❌❌❌❌❌❌❌❌❌❌❌❌




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
3. imprime la valeur de la variable nombre
4. appel la fonction et en parametre donne lui ptr9
```c
ft_ultimate_ft(...);
```
5. imprime de nouveau la valeur de nombre

## c01 ex03

## **Un peu de math** 

## **La division** 

```
11 diviser par 2 = 5,5
```
Mais en informatique 
```
5 = 11 diviser par 2
```
2 choses : 
   1. Vous voyez en informatique il y a pas de virgule.
   2. la variable qui va stocker le resultat est au debut , exemple    result = 11 / 2; et donc resultat contiendra la valeur 5.

## **Le modulo** 

Définition : Le modulo c'est le reste de la division. 
En informatique % cela veut dire modulo et non pas pourcentage.
par exemple : 
```
result = 11 % 2

result est egal a 1
```

Voila un lien pour faire des calcul avec du modulo
```
https://www.dcode.fr/calculatrice-modulo-n 
```

## **Le prototype** 

```
void    ft_div_mod(int a, int b, int *div, int *mod)
```

## **Commençons**

1. Tu dois diviser a par b et le stocker dans le pointeur div;
2. Tu dois faire modulo de a par b et le stocker dans le pointeur mod;


## **Le main**

Regarde ce que prends en parametre ta fonction 
- un int
- un autre int
- Un pointeur 
- Un autre pointeur

> ![IMPORTANT]
> Dans ta fonction ft_div_mod, Ta un pointeur qui pointe sur un int     ->    int *div

> ![IMPORTANT]
> Dans ta fonction ft_div_mod, Ta un pointeur qui pointe sur un int     ->    int *mod

Donc si il pointe sur des int il faut creer des int. 

Aussi pour les permettres de pointer sur les int il faut leurs donner l'adresse.
On donne l'adresse avec &

La valeur sera stocker dans une variable ( un int ) qui aura stocker la division de tes deux int.


La valeur sera stocker dans une variable ( un int ) qui aura stocker le modulo de tes deux int.

## **Print les valeurs**

pritnf les variables qui ont stocker les resultats et voit si cela te semble juste. 




