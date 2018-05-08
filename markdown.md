## Les tableaux

Rien de plus facile que de créer des tableaux avec MarkDown. Il suffit juste de mettre des \| à la place des *bareaux* du tableau. Il faut savoir que la premiere ligne sert d'entete, la seconde sert à indiquer l'allignement du texte a l'interieur des *cases* du tableau, a gauche: ':-', au centre: ':-:', a droite: '-:'.  

    | Entete 1      |     Entete 2    |   Entete 3 |  
    | :------------ |:--------------: | ---------: |  
    | Ligne 1       |        1        |      value |  
    | Ligne 2       |        2        |      value |  
    | Ligne 3       |        3        |      value |  

*ou bien*  

    |Entete 1|Entete 2|Entete 3|  
    |:-|:-:|-:|  
    Ligne 1|1|value  

(notez que | ne sont pas nécessaires au debut ou a la fin) vont donner le meme tabeau:

Entete 1|Entete 2|Entete 3  
:-|:-:|-:  
Ligne 1|1|value  

Oubliez pas de **séparer** le tableau d'une **ligne au dessus et au desous** et surtout n'oubliez pas les deux espaces a la fin de chaque ligne, **le retour a la ligne**.  


## Partager du code avec MarkDown

Le partage du **code** grace au MarkDown est d'une simplicité à toute epreuve, il suffit de **quatre espaces** qui se suivent pour creer ce *block-code*.  On peut egalement utiliser le symbole **\`**, l'*anti-apostrophe* ou bien the *backticks*, pour les anglophones, ou bien la *contre-apostrophe*. Il suffit d'en mettre une au debut et la fin du code pour que ca donne une integration dans le texte, exemple\`code\` donne `code`. Grace a **\`** ont peut se passer des espaces, il suffit de deux lignes avec trois **\`** avec le *bloc-code* a l'interieur, exemple:  
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