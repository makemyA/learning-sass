# Guide d'utilisation pour sass et compass

## Installation (On WIndows 10) des composants

<iframe width="560" height="315" src="https://www.youtube.com/embed/wKuGWmX1XPs" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

### Installer [RubyInstaller](https://rubyinstaller.org/)

Ce qui va vous permettre d'installer des modules gem
### Vérifier votre version en tapant dans votre terminal
```
$ gem --version
2.6.14.1
```
### Installation de sass
``` ruby
gem install sass
```
``` ruby
sass --version
Ruby Sass 3.5.6
```
### Installation de compass
``` ruby
gem install compass 
```
``` ruby
compass --version
Compass 1.0.3 (Polaris)
```
## Configuration

### Tuto intéressant en français
<iframe width="560" height="315" src="https://www.youtube.com/embed/DrrVjpMUxxU" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

### configurer sass + compass
``` ruby
compass create myproject
 ```
 Va créer automatiquement un dossier avec les éléments requis pour utiliser le sass et le compass
 ``` ruby
code (votre éditeur de code) myproject
 ```
 Ouvrez votre dossier et configurer dans *config.rb* le chemin d'accès à vos fichiers scss et css si vous avez modifier l'architecture de base du dossier
  ``` ruby
compass watch myproject
>>> Compass is watching for changes. Press Ctrl-C to Stop.
 ```
 Cette commande lance en fond le framework **compass**. Vous pouvez commencer à travailler, il fera automatiquement les liens nécessaires entre vos différents dossiers.

## Utiliser SASS et COMPASS

### SASS

1. Qu'est ce que c'est?

Il s'agit d'une façon d'écrire le css afin de pouvoir réutiliser des élements sans devoir retaper à chaque fois tout le css quand on ouvre un nouveau projet

2. Comment l'utiliser?

Une méthode simple et efficace est de l'utiliser avec le framework *compass* afin d'optimiser au maximum la réutilisation du code. 

* Utilisation des variables

``` scss
$blue: #3bbfce;
$width: 70%;
$margin: 0 auto 0 auto; 

body {
    color: $blue;
    background-color: darken($blue, 9%);
    width: $width;
    margin: $margin;
}
```
Ce qui donnera en css
```css
body {
    color: #3bbfce;
    background-color: #2b9eab;
    width: 70%;
    margin: 0 auto 0 auto;
}
```
En parallèle vous pouvez vérifier si le compilateur compass fonctionne toujours en arrière-plan en allant voir votre terminal.
Vous devriez y voir toutes les modifications faites entre vos fichiers scss et css comme dans l'exemple ci-dessous:

```
compass watch sass
>>> Compass is watching for changes. Press Ctrl-C to Stop.
 modified sass/sass/screen.scss
    write sass/stylesheets/screen.css
 modified sass/sass/screen.scss
    write sass/stylesheets/screen.css
 modified sass/sass/screen.scss
    write sass/stylesheets/screen.css
 ```



