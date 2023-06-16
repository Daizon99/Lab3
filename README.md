# seg3503_playground
| Outline | Value |
| --- | --- |
| Course | SEG 3503 |
| Date | Summer 2023 |
| Professor | Mohamed Ali Ibrahim |
| TA | Abonasara Joseph / Kasumba Joseph | 

# Lab 3
## Part 1:

Le rapport suivant apparaîtera pour Date.java

![173232852-f592a0d9-4afb-4e95-b14e-c7e96633b7b1](https://github.com/Daizon99/Lab3/assets/114030630/6a043e54-9e94-4211-ab90-222afe2fc641)

Notre objectif pour la première partie était d'atteindre une couverture de 100% pour les instructions et les branches de Date.java.

#### setDay(int)
![image](https://github.com/Daizon99/Lab3/assets/114030630/e7d6eaba-6fa7-4e4c-91a8-12b1ab25f0d9)

On a pu couvrir toutes les branches et instructions manquantes en ajoutant les cas de test suivants à DateTest.java :
![image](https://github.com/Daizon99/Lab3/assets/114030630/71bd1e96-12d0-4186-bfca-721f428afa0a)

#### toString()
![image](https://github.com/Daizon99/Lab3/assets/114030630/853ecac2-5d44-4d10-b467-7c1b40e83af4)

toString() n'a pas de branches (if/switch statements). Il suffit donc d'ajouter le cas de test suivant :
![image](https://github.com/Daizon99/Lab3/assets/114030630/6ba5cd43-910d-4033-9ec5-5370b8f5c4cd)

#### equals(Object)
![image](https://github.com/Daizon99/Lab3/assets/114030630/992436fd-176d-402e-8590-acc007c26e25)

equals(Object) comporte quatre branches manquantes et une instruction au total. Notre tâche consistait à déterminer celles qui n'étaient pas couvertes par les cas de test déjà mis en œuvre :
![image](https://github.com/Daizon99/Lab3/assets/114030630/5e951a10-f5b2-4f43-b12a-436be0746e98)

#### isEndOfMonth()
![image](https://github.com/Daizon99/Lab3/assets/114030630/f4c367e4-3f93-44aa-98f3-61a4d5dd08ef)

isEndOfMonth() avait trois branches manquantes et une instruction. La seule branche qu'on a  pas pu couvrir est le cas où l'année n'est pas bissextile, le mois est février, et le jour est supérieur à 28 (Ex. : 2015/02/29). Ce qui est tout à fait logique puisqu'une telle date n'est pas valide, càd qu'une exception d'argument illégal sera levée par le constructeur.
![image](https://github.com/Daizon99/Lab3/assets/114030630/f5641bb4-e145-495c-8d03-07391e5195ad)

#### isLeapYear()
![image](https://github.com/Daizon99/Lab3/assets/114030630/f889ba93-94f1-4b4f-8fdd-ca56b217043b)

La branche manquante a été couverte par le cas de test suivant :
![image](https://github.com/Daizon99/Lab3/assets/114030630/106cf77b-64fc-4eec-8c0f-5ab5d3b15b54)

#### isThirtyDayMonth()
![image](https://github.com/Daizon99/Lab3/assets/114030630/6087af56-80a9-4abc-a9d4-65d2e924bd64)
Cette méthode a été entièrement couverte après l'ajout de cas de test pour isEndOfMonth().

#### setMonth(int)
![image](https://github.com/Daizon99/Lab3/assets/114030630/1ee5ec67-cf95-4329-95cc-3b6263b2338e)

Pour SetMonth la branche manquante a été couverte par :
![image](https://github.com/Daizon99/Lab3/assets/114030630/0d9804fa-f90d-4a97-a5f2-f0de4d4e5f8d)

#### Conclusion
Après avoir ajouté tous les cas de test précédents, le rapport JaCoCo généré était le suivant :
![image](https://github.com/Daizon99/Lab3/assets/114030630/8479b87f-ad7f-4fa5-b201-6e97411f8d40)





