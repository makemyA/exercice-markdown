# **Documentation Markdown**

##### Pour plus d'informations concernant ce projet rendez-vous sur le [README](https://github.com/SammuelJ/exercice-markdown/tree/master)
----------

# Titre - Headers

Pour convertir un texte en titre, il suffit d'ajoute un ```#``` avant.


**Exemple**:

```
# Ceci est un <h1>
# Ceci est un <h2>
# Ceci est un <h3>
# Ceci est un <h4>
# Ceci est un <h5>
# Ceci est un <h6>
```
*Veuillez à bien laisser un espace entre le ```#``` et le texte !*


# Accentuation - Emphasis

## Texte en *Italique*

Afin de convertir un bout de texte en *italique*, utilisez un ```*``` ou ```_``` aux extremit&eacute;s du texte.
**Exemple**:
```
*Ce texte est en italique*
_Ce texte est en italique_
```
*R&eacute;sultat*
*Ce texte est en italique*
_Ce texte est en italique_

## Texte en **Gras**

Afin de convertir un bout de texte en **gras**, utilisez un ```*``` ou ```_``` aux extremit&eacute;s du texte.

**Exemple**:
```
**Ce texte est en gras**
__Ce texte est en gras__
```
*R&eacute;sultat*
**Ce texte est en gras**
__Ce texte est en gras__

# Les listes

## Listes simples


Il est très facile de cr&eacute;er des listes en Markdown. Il suffit de d'ajouter un *'*'* avant chaque liste


**Exemple:**
```
* Une puce
* Une autre puce
* Une troisième puce
```

*R&eacute;sultat*

* Une puce
* Une autre puce
* Une troisième puce

## Listes imbriqu&eacute;es

De la même manière, nous pouvons cr&eacute;er des *listes imbriqu&eacute;es* les unes dans les autres

En voici **un exemple**:
```
* Une puce
     * Une  puce imbriqu&eacute;e
     * Une deuxième puce imbriqu&eacute;e
* Une deuxième puce
* Une dernière puce 
```
*R&eacute;sultat*

* Une puce
     * Une  puce imbriqu&eacute;e
     * Une deuxième puce imbriqu&eacute;e
* Une deuxième puce
* Une dernière puce 

## Listes num&eacute;rot&eacute;es

Dans ce cas il suffit de commencer les puces par des num&eacute;ros

**Exemple:**
```
1. Puce 1
1. Puce 2
1. Puce 3  
``` 
*R&eacute;sultat*
1. Puce 1
1. Puce 2
1. Puce 3  

# Lien - Link

Pour partager des **liens** avec MarkDown il suffit de suivre la synthaxe suivante : 

```[texte du lien](url_du_lien "texte pour le titre, facultatif")```

Donc, le texte du lien, tel qu'il apparaitra cliquable, entre crochets.
Et l'url du lien (ex: https://fr.wikipedia.org/wiki/Markdown) entre parenthèses.
On peut &eacute;galement rajouter un texte descriptif du lien entre guillemets, après l'url, qui apparaitra lorsque l'on survole le lien avec la souris.

# [Image](https://github.com/SammuelJ/exercice-markdown/blob/master/markdown-insertions.md#images)

# [Video](https://github.com/SammuelJ/exercice-markdown/blob/master/markdown-insertions.md#vid&eacute;os)

# Tableaux - Table

Rien de plus facile que de cr&eacute;er des tableaux avec MarkDown. Il suffit juste de mettre des \| à la place des *bareaux* du tableau. Il faut savoir que la premiere ligne sert d'entete, la seconde sert à indiquer l'allignement du texte a l'interieur des *cases* du tableau, a gauche: ':-', au centre: ':-:', a droite: '-:'.  

    | Entete 1      |     Entete 2    |   Entete 3 |  
    | :------------ |:--------------: | ---------: |  
    | Ligne 1       |        1        |      value |  
    | Ligne 2       |        2        |      value |  
    | Ligne 3       |        3        |      value |  

*ou bien*  

    |Entete 1|Entete 2|Entete 3|  
    |:-|:-:|-:|  
    Ligne 1|1|value  

(notez que | ne sont pas n&eacute;cessaires au debut ou a la fin) vont donner le meme tabeau:

Entete 1|Entete 2|Entete 3  
:-|:-:|-:  
Ligne 1|1|value  

Oubliez pas de **s&eacute;parer** le tableau d'une **ligne au dessus et au desous** et surtout n'oubliez pas les deux espaces a la fin de chaque ligne, **le retour a la ligne**.  


# Partager du code avec MarkDown

Le partage du **code** grace au MarkDown est d'une simplicit&eacute; à toute epreuve, il suffit de **quatre espaces** qui se suivent pour creer ce *block-code*.  On peut egalement utiliser le symbole **\`**, l'*anti-apostrophe* ou bien the *backticks*, pour les anglophones, ou bien la *contre-apostrophe*. Il suffit d'en mettre une au debut et la fin du code pour que ca donne une integration dans le texte, exemple\`code\` donne `code`. Grace a **\`** ont peut se passer des espaces, il suffit de deux lignes avec trois **\`** avec le *bloc-code* a l'interieur, exemple:  
    \`\`\`  
    code  
    \`\`\`  
Si jamais on veut mettre en evidence la syntaxe du language utilise dans le *block-code* il suffit de le preciser apres les trois premier \`,  
**Exemple**:  
```python  
    ```python  
    def addition(a,b):
      return(a+b)
    ```
```  
N'oubliez pas le saut a la ligne, cad **les deux espaces** à la fin de chaque ligne.

# Bloc de citation(s) - Blockquotes

Afin de convertir un bout de texte en une citation, utilisez un ```>``` au d&eacute;but du texte.

**Exemple**:
```
> Ceci est une citation
```
*R&eacute;sultat*
> Ceci est une citation



# Lignes horizontaux

Les lignes horizontaux peuvent être cr&eacute;&eacute;s en tapant trois ou quatre ast&eacute;risques (```*```), tirets (```-```) ou caractères soulign&eacute;s (```_```) tous seuls sur une ligne.

Le code suivant fonctionnera :

 ``` *** ```

mais vous pouvez ajouter des espaces ou plus de mêmes caractères pour rendre plus visible un saut de section dans la fenêtre d'&eacute;dition du texte.
**Exemple**
``` * * * * * ```

``` ------------------------- ```

``` _ _ _ _ _ ```
 
Toutes ces m&eacute;thodes donneront exactement le même r&eacute;sultat :

_ _ _ _ _ 
Exemple :arrow_up:
