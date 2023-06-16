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

## Part 2:

#### Changements apportés à Date.java

#### setDay(int)

AVANT

![image](https://github.com/Daizon99/Lab3/assets/114030630/03b1f95f-8717-4388-8952-aa0a69018197)

APRÈS

![image](https://github.com/Daizon99/Lab3/assets/114030630/ab00c759-0965-4d87-a6ba-9b66f40974bb)

#### isEndOfMonth()

AVANT

![image](https://github.com/Daizon99/Lab3/assets/114030630/9e39baea-f039-4615-9b10-1a1c4bfa8a93)

APRÈS

![image](https://github.com/Daizon99/Lab3/assets/114030630/8553d077-5ea7-4703-a0d8-9a8a7e767350)

#### isThirtyDayMonth()

AVANT

![image](https://github.com/Daizon99/Lab3/assets/114030630/4a3785fe-7fd1-45f4-bc8e-86c1904bbce6)

APRÈS

![image](https://github.com/Daizon99/Lab3/assets/114030630/d32e81da-a74e-4e75-871d-ab270e2c11bb)

#### isLeapYear()

AVANT

![image](https://github.com/Daizon99/Lab3/assets/114030630/21850dfe-dda2-49c6-8bdc-b50473396a91)

APRÈS

![image](https://github.com/Daizon99/Lab3/assets/114030630/33cc3afb-ce5b-4d16-b224-4046e120b5c9)

####Resultats
Si nous devions conserver les tests unitaires ajoutés dans la première partie, les taux de couverture seraient les mêmes après  refactoring, comme prévu.

![image](https://github.com/Daizon99/Lab3/assets/114030630/a40a031e-e360-472b-8cef-3011e9820d3d)

En fait, l'écrasement des instructions (if/switch) ou d'autres opérations similaires n'augmentera en aucun cas le taux de couverture des branches. Cependant, cela pourrait contribuer à réduire le nombre d'instructions manquées. Cela peut être observé si on supprime les tests ajoutés dans la partie 1.

![image](https://github.com/Daizon99/Lab3/assets/114030630/4e2fd3b4-4709-488b-a515-053e4c0a0d30)

En conclusion,  refactoring peut aider à réduire le nombre d'instructions sans affecter les branches. Il est intuitif de refactoriser correctement la logique avant de la tester.











