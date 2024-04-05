# HELP

**C02 ex00 ft_strcpy**

**Analyse du prototype**

```c
char *ft_strcpy(char *dest, char *src)
// il y a deux tableaux
// un tableau destination
// et un tableau source
```

**Ce qu'on doit faire** 

```
- On doit copier tout ce qui se trouve dans le tableau de src et le mettre dans dest.
- On copie element par element.
```

**Exemple de copie** 

```
int a;
int b;

a = 10;
b = 50;


a = b;
// la nouvelle valeur de a est de 50.

```

** Attention **

```
- Encore une fois la copie se fais element par element
dest = src , Cela ne fonctionnera pas !
```

**Définition dun tableau de char**

```
C'est un ensemble de charactere et qui se termine par un '\0'
```

Si tu decides de copier tab_denvoi dans tab_de_reception
tab_denvoi contient "salut"
tab_de_reception est vide. ( pas vraiment , il faut pas oublier que dedans il y a le '\0')

pendant la copie 
le "s" entrera dans tab_de_reception et ecrasera le '\0'.
Donc a la fin il y a le mot "salut" a l'interieur de tab_de_reception
mais le '\0' n'a pas eté copié.

**Rajouter un '\0'**

Apres la boucle ecrire 

```
dest[i] = '\0';
```






**c01 ex07 ft_rev_int_tab**

## **Explication du resultat attendu** 

Tu auras un tableau de int et dans ce tableau il y aura des valeurs , comme par exemple
```
1, 2, 3, 4, 5
```
et ton but c'est inverser l'ordre des elemens pour que au final cela te donne
```
5, 4, 3, 2, 1
```
## **Une fonction qui inverse deux elements**

- Est ce que tu te rappelle d'une fonction qui inverse deux élements ?

## Utilisation d'une fonction que tu as deja coder 

tu fais un copier coller dans ton code de la fonction
puis tu l'appel dans la fonction que tu es en train de faire.

![Screenshot from 2024-04-02 22-29-32](https://github.com/Teddyburgonde/help_for_you/assets/93845046/802109ed-74ad-4070-8a43-be476a735576)


## deux iterateurs 

- Une bonne strategie c'est d'avoir deux itérateurs, un qui commence au debut
et l'autre a la fin.

![Screenshot from 2024-04-02 22-18-35](https://github.com/Teddyburgonde/help_for_you/assets/93845046/66805d79-af0a-4cad-8771-822d0314c742)


- Le but c'est d'échanger les valeurs qui sont a index de i avec celui de index j
- Puis faire monter le i en faisant i++ et faire decendre le j en faisant j--

![Screenshot from 2024-04-02 22-19-55](https://github.com/Teddyburgonde/help_for_you/assets/93845046/782f84d9-df93-439f-b848-7c0d1749e185)

## condition d'arret du while
```c
while (i < j)
```
A force de faire monter le i et faire descendre le j , les deux vont se rejoindre et donc la boucle
s'arretera.

## **comment placer le j a la fin ?**

```c
j = size - 1;
```
prends un tableau de int avec 5 elements 
la size sera egal a 5
et pour placer le j a la fin on fait size - 1 car il faut pas oublier que dans un tableau le premier
element est a l'index 0. 


## **Main**

## **Différence entre un tableau de char et de int**

un tableau de char tu l'ecris
```c
char str[] = "salut";
```
à la fin d'un tableau de char il y a un '\0'
Tu ne le vois pas mais l'ordinateur le met automatiquement dans la memoire et c'est comme cela qu'il
sait que c'est la fin du mot.

Un tableau de int il y a pas de '\0'.
Un tableau de int il faut utiliser une size.
Par exemple ton tableau contient :
```
1, 2, 3, 4, 5
```
il a une size de 5 car il a 5 element a l'interieur.

## **Déclarer un tableau de int**

```c
// le type,  le nom et on met les valeurs dans des {} separer par une virgule
int tab[] = {1, 2, 3, 4 , 5};
```

## **Imprimer un tableau de int**

Si tu as 10 elements dans ton tableau 
tu met size = 10;

```c
while (i < size)
{
	printf("%d", tab[i]);
	i++;
}
```

---------------------------------------------------------------------------------------------------------------





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
- Un pointeur sur un int
- Un autre pointeur sur un int

> [!IMPORTANT]
> Dans ta fonction ft_div_mod, Ta un pointeur qui pointe sur un int     ->    int *div

> [!IMPORTANT]
> Dans ta fonction ft_div_mod, Ta un pointeur qui pointe sur un int     ->    int *mod

- Dans ton main tu ne dois pas crée des pointeurs mais des int car ta fonction en haut , elle a deja deux pointer qui pointe vers des int donc tu dois crée des int dans le main.


- Pour les permettres de pointer sur les int il faut leurs donner l'adresse quand tu fais appelle à ta fonction dans le main.
On donne l'adresse avec &

- La valeur sera stocker dans une variable ( un int ) qui aura stocker la division de tes deux int.

- La valeur sera stocker dans une variable ( un int ) qui aura stocker le modulo de tes deux int.

- Pour résumé dans ton main tu dois avoir que des int. 

## **Print les valeurs**

printf les variables qui ont stocker les resultats et voit si cela te semble juste. 


## **c01 ex05**

## **Revision des bases**

## **write**

```c
// 1 c'est la où tu veux que write ecris , 1 coresponds au terminal

// & c'est adresse de la variable que tu veux ecrire

// 1 le nombre de caractere que tu veux ecrire
write (1, &..., 1);
```
garde en tête que write imprime un caractere.

## **Boucle**

Une boucle permet de repeter un ou des instructions.
Elle est composé de 3 parties :
```c
while (1. // condition d'arret)
{
   2. // une instruction
   3. //  un incrementateur i++;
}
```

## **Comment parcourir tout un tableau**

```
while (str[i] != '\0')
```
La il vas parcourir chaque lettre que contient le tableau str ,
par exemple si il y a "SALUT" a linterieur
str[i] sera d'abord egal à  S
puis le i++ (il augmente ) donc str[i] sera egal à  A
et si str[i] est egal a '\0' (a la fin de chaque tableau de char il y a ce caractere la ) ben la boucle s'arrete.

La on parcours tant que str[i] est different de '\0'

## Analyse du prototype 
```c
void ft_putstr(char *str);
```

en argument d'entrer c'est un pointeur.
Mais pour l'instant dit toi que quand tu vois un char * c'est un tableau. 

donc on a un tableau en argument d'entrer.

## **Le main**

Tu as juste a appeler ta fonction est ecrire dedans un mot ou une phrase

```c
ft_putstr("salut");
```

![Screenshot from 2024-03-30 13-23-52](https://github.com/Teddyburgonde/help_for_you/assets/93845046/46413029-f80c-477c-9a9b-2bc6fde14733)












