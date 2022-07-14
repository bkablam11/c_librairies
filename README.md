# C static and dynanimic librairies

# Creating and Linking Static Libraries

(Creating and Linking Static Libraries)[https://www.youtube.com/watch?v=t5TfYRRHG04]

1. gcc -c addNumbers.c subNumbers.c

compile in file.o all c files

3. ar cr libmath.a addNumbers.o subNumbers.o

create an archive for all file .o named libmatch.a and put into lib folder and create an include folder also

on prend deux fichier.o et on les fusionnent en un fichier libmath.a

4. ar t libmath.a

to see all files.o archived in the librairy

5. deplacer tous les prototype (file.h) dans le dossier include et toute les librairy (file.a) dans le dossier lib



6. gcc doMath.c -lmath -o doMath -I include -L lib

dire a la machine oû charger les fichiers à inclure et les lib

or

gcc doMath.c -lmath -o doMath -I include -L lib -no-pie -static


[link](https://forums.commentcamarche.net/forum/affich-27310766-fonction-de-la-longueur-d-une-chaine-de-caractere#answers)

7. reecrire une fonction _strlen

Soit tu définies la fonction toi-même, soit tu calcules avec strlen, mais pas les deux à la fois. Et si tu veux que ta fonction retourne un nombre,
int sup_car(char *S) {
     int i=0;
     while (*(S+i))
     {
          i++;
     } 
     return i;
}