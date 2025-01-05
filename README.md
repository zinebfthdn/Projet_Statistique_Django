# Projet Django - Statistiques

Ce projet est une application Django dédiée aux statistiques et à la manipulation de données. Il utilise des bibliothèques populaires, afin pour offrir des fonctionnalités analytiques et interactives.


# Guide d'Installation et d'Exécution

## 1. Création et activation de l'environnement virtuel
Création : **python -m venv venv**
Activation : **venv\Scripts\activate**

## 2. Création et activation de l'environnement virtuel
Installez toutes les bibliothèques nécessaires avec la commande suivante :
**pip install -r requirements.txt**

## 3. Configuration du projet Django
### 1.  Lancez les migrations
Vous utilisez les commandes suivantes :

- **python manage.py makemigrations**
- **python manage.py migrate**

### 2.  Créez un superutilisateur
Pour gérer les connexions utilisateur et accéder à l'administration Django :
Utilisez la commande : **python manage.py createsuperuser**

### 3. Lancez le serveur local
Démarrez le serveur pour exécuter l'application :
Utilisez la commande : **python manage.py runserver**

### 4. Lancez le serveur local
Ouvrez votre navigateur et accédez à l'application via **http://127.0.0.1:8000**.


---


## La structure du Projet  


### 1. **`stat_projet/`**
Le répertoire principal du projet Django, contenant les fichiers de configuration comme :
- `settings.py` : Configuration de base (base de données, apps installées, fichiers statiques, etc.).
- `urls.py` : Fichier pour le routage principal.
- `wsgi.py` et `asgi.py` : Points d'entrée pour le déploiement.


### 2. **`stat_app/`**
Le répertoire de l'application principale du projet, contenant :
- `models.py` : Définition des modèles de base de données (par exemple, fichiers importés, résultats, etc.).
- `views.py` : Logique métier et rendu des pages.
- `forms.py` : Gestion des formulaires Django.
- `templates/` : Fichiers HTML pour l'interface utilisateur.
- `urls.py` : Routes spécifiques à cette application.


### 4. **`db.sqlite3`**
Base de données SQLite utilisée pour stocker les données de l'application.

### 5. **`manage.py`**
Outil en ligne de commande pour interagir avec le projet (création de migrations, lancement du serveur, etc.).

### 6. **`requirements.txt`**
Liste des bibliothèques Python nécessaires, installées via `pip`.

![structure](pictures/image.png) 


## Fonctionnalités principales

### 1. **Téléchargement de fichiers et calculs de statistiques**
- Importation de fichiers CSV et Excel.
- Calcul des **tendances centrales** : moyenne, médiane, mode.
- Calcul des **mesures de variabilité** : variance, écart-type, étendue.

### 2. **Loi de probabilités**
- Visualisation et simulation des lois suivantes :
  - **Bernoulli**
  - **Binomiale**
  - **Uniforme**
  - **Poisson**
  - **Exponentielle**
  - **Normale continue**

### 3. **Tests d'hypothèses**
- **Z-Test** (échantillons de grande taille, n > 30).
- **T-Test** (échantillons de petite taille, n < 30).
- Affichage interactif des résultats avec calculs des statistiques et p-values.


## Organisation de l'application

L'application est divisée en ***quatres sections principales*** accessibles via le tableau de bord :

### 1. **Login page**

![login](pictures/login.png) 


### 2. **Importation de fichiers et calculs statistiques**
- Permet de charger des fichiers **CSV** et**Excel**.

![Importation de fichiers](pictures/upload.png) 
![Importation de fichiers](pictures/upload2.png) 


## **Avec l'option de :**

## **Visualisation des données**
L'utilisateur peut choisir différents types de visualisations pour explorer les données importées, comme des barplots, heatmaps, scatterplots, et plus encore.

![Visualisation des données](pictures/visualiser.png)

- Exemple :
![Visualisation des données](pictures/visualiser2.png)
![Visualisation des données](pictures/visualiser3.png)

- Avec une gestion d'erreur :
  
![Visualisation des données](pictures/visualiser4.png)
![Visualisation des données](pictures/visualiser5.png)



#### **Parcourir les données**
L'utilisateur peut parcourir les données en sélectionnant des colonnes spécifiques ou en appliquant des filtres pour analyser les enregistrements.

![Parcourir les données](pictures/parcourir.png)



- **Calcule les statistiques descriptives :**
  - Moyenne
  - Médiane
  - Mode
  - Variance
  - Écart-type
  - Étendue


![calcules](pictures/calc.png) 

- Voici un exemple :
  
![calculesexmpl](pictures/calc2.png) 



---

### 2. **Lois de probabilités**
Explorez et visualisez différentes lois de probabilité :

- **Bernoulli**
  
  ![bernoulli](pictures/bernoulli.png)
  ![bernoulli](pictures/bernoulli2.png)
  
- **Binomiale**
  
  ![binomiale](pictures/binomial.png)
  ![binomiale](pictures/binomial2.png)


- **Uniforme**
  
  ![uniforme](pictures/uni.png)
  ![uniforme](pictures/uni2.png)


- **Poisson**
  
  ![poisson](pictures/poi.png)
  ![poisson](pictures/poi2.png)

- **Exponentielle**
  
  ![exponentielle](pictures/expo.png)
  ![exponentielle](pictures/expo2.png)

- **Normale continue**
  
  ![normale](pictures/nor.png)
  ![normale](pictures/nor2.png)


---

### 3. **Tests d'hypothèses**
- Effectuez des **tests Z** et **tests T** pour analyser vos données.
- Affichez les résultats avec des visualisations conviviales et des calculs détaillés.
  ![testes](pictures/test.png)

- **Z-Test**


  ![Z](pictures/Z.png)
  ![Z](pictures/Zres.png)

  
- **T-Test**
  ![T](pictures/T.png)
  ![T](pictures/Tres.png)


---

## Bibliothèques utilisées

L'application repose sur des bibliothèques robustes pour offrir des fonctionnalités avancées :

### Backend
- **Django** : Framework backend pour le développement web, incluant des fonctionnalités d'authentification et de gestion de sessions.

### Manipulation de données
- **Pandas** : Manipulation et analyse des données tabulaires.
- **NumPy** : Calculs numériques avancés.

### Visualisation
- **Plotly** : Visualisations interactives, y compris des graphiques comme barplots, scatterplots, histogrammes, etc.
- **Matplotlib** : Génération de graphiques statiques.
- **Seaborn** : Visualisation des données avec des graphiques esthétiques.

### Statistiques et calculs probabilistes
- **SciPy** : Tests statistiques (z-test, t-test, etc.) et distributions probabilistes (binomiale, normale, exponentielle, etc.).
- **Scipy.stats** : Fournit des outils supplémentaires pour les calculs statistiques.

### Outils additionnels
- **Statistics** : Calcul de mesures statistiques telles que la moyenne, la médiane, la variance et l'écart-type.
- **Plotly Figure Factory** : Génération avancée de graphiques spécifiques, comme les distributions KDE.
- **Base64** : Encodage d'images en Base64 pour une intégration dans le frontend.
- **BytesIO** : Manipulation d'objets en mémoire pour gérer des images générées par Matplotlib.

### Authentification et gestion des utilisateurs
- **Django.contrib.auth** : Authentification, connexion et déconnexion des utilisateurs.
- **Django.contrib.messages** : Affichage des messages de validation ou d'erreur à l'utilisateur.


## Conclusion

Ce projet offre une plateforme interactive et intuitive pour l'analyse statistique et probabiliste. Grâce à l'utilisation de bibliothèques puissantes comme Django, Pandas, NumPy, et Plotly, il permet de manipuler des données, d'explorer des lois de probabilité, et de réaliser des tests statistiques avec facilité. Que ce soit pour des besoins académiques, professionnels ou personnels, cette application constitue un outil polyvalent pour comprendre et interpréter vos données. 
