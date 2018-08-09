# sql_installer

## Pré-requis

Pour Windows, avoir téléchargé et installé MySQL Workbench : https://www.clubic.com/telecharger-fiche430839-mysql-workbench.html

## Introduction

Aujourd'hui, la gestion des données est l'un des enjeux majeurs au sein de l'IT. Afin de pouvoir gérer les données d'utilisateurs, d'applications, de crawls, les systèmes de gestion de base de données (SGBD) doivent être les plus performants et optimisés en terme de temps de réponse mais également de sécurité. Les différentes solutions du marché répondent aux différents besoins des administrateurs, développeurs, ou plus généralement des entreprises. Les gros flux de données seront plutôt gérés par des bases de données non-relationnelles dites noSQL tels que MongoDB, Dynamo, CouchDB (qui stockent les données sous formes de paires clés-valeurs par exemple) comparitivement aux bases de données relationnelles tout aussi performantes, voir plus utilisées, qui répondent à d'autres besoins (MySQL, PostGreSQL, Oracle, SQL Server...)

> Le but est ici de présenter deux solutions gratuites, très connues, qui permettront de designer une base de données relationnelle afin de permettre de gérer par exemple les données d'un petit site, d'une petite application ou encore . Ces solutions sont :

• MySQL : MySQL est un serveur de base de données Open Source.

• MySQL Worbench : GUI permettant de totalement modéliser et de monitorer une base de données MySQL

MySQL Workbench est vraiment pratique puisque son interface user-friendly permet de schématiser à merveille tous les éléments dont on a besoin pour travailler avec une base de données. Nous survolerons donc les possibilités de travail avec Workbench.

## Concevoir votre base de données avec WorkBench

### Pour commencer

> Avant toute chose, la première réflexion est de savoir quels types de données notre application/site aura besoin. Comment va-t-on les organiser ? Comment peut-on les classer sous forme d'entités ? Afin de faire cela, une feuille et un stylo suffiront. L'idée est de faire en sorte de schématiser vos données sous forme de tables, en faisant en sorte que les données soient le plus insécables possible (c'est à dire qu'on ne puisse plus subdiviser la donnée en deux - exemple : mettre le nom et le prénom dans un seul champ est une mauvaise idée). Une fois que vous avez une idée assez fixe du nombre de tables, du nombre de champs et de leur type, la conception sous WorkBench peut alors commencer.

### Instancier une nouvelle connexion

Une fois Workbench ouvert, il faudra configurer une nouvelle connexion (qui nécessite donc d'avoir MySQL installé). Il faudra ensuite créer un nouveau modèle de données (équivalent d'une schéma de base de données), vous pourrez ensuite ajouter toutes les tables qu'il faut.

![alt text](https://www.supinfo.com/articles/resources/158424/1072/1.png "Logo Title Text 1")

### Ajouter et remplir les tables

Une fois qu'une table a été ajouté, Workbench permet d'ajouter un à un des champs aux tables, puis de les typer (lINT, VARCHAR, BOOL) en leur donnant une longueur maximale. Il est intéressant de noter que le typage doit être correctement choisi. Inutile de donner une longueur trop importante au champ "âge" de votre table "utilisateurs", un nombre à 2 chiffres suffira (INT(2)). La case AI signifie "Auto Increment", c'est à dire que si votre champ est de type INT, à chaque nouvel enregistrement dans la table, le champs de type INT sera incrémenté de 1 par rapport à la dernière valeur. La case UN permet d'indiquer si vous souhaitez ajouter une contrainte d'unicité à votre champ. Cochez-là et vous ne pourrez pas avoir deux enregistrements dont l'un des champs a une valeur identique à celui d'un autre enregistrement de la table.

![alt text](https://www.supinfo.com/articles/resources/158424/1072/2.png "Logo Title Text 1")
