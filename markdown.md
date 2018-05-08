
un guide pour bien commencer avec markdown



Markdown est un système de publication et de formattage de texte minimaliste. Il est de plus en plus utilisé et je vais faire de mon mieux pour vous aider à l’apprendre rapidement.
Contenus

    Qu’est-ce que Markdown ?
    Un peu d’histoire
    Outils
    La syntaxe de markdown
    Les titres
    Les paragraphes
    Les sauts de ligne simple
    L’emphase
    Les citations
    Les listes non ordonnée
    Les listes ordonnées
    Le bloc de code
    Le code dans la ligne
    Les filets ou barres de séparation
    Les liens
    Les images
    Les tableaux
    Échappement des caractères
    Séparer des blocs
    Et après ?

Qu’est-ce que Markdown ?

Markdown est un système d’édition et de formatage de texte ; c’est à la fois une syntaxe, un script de conversion texte → HTML et un format de fichier. Il est couramment utilisé pour les fichiers de documentation d’un projet ou d’un jeu de données -souvent nommé readme.md. Il est stocké au format texte classique et est plus léger que sa version interprétée puisqu’il ne contient pas les balises html.

La philosophie du système veut que le texte écrit soit lisible sans interpréteur particulier en mode texte. Il est léger et épuré de l’essentiel de la verbosité d’un language balisé. Les éléments de syntaxe sont des caractères de ponctuation qui font sens visuellement même non convertis. Une fois converti, le navigateur web (qui joue alors le rôle d’interpréteur) en rendra la lecture plus claire.

Les fichiers sont généralement enregistrés avec l’extension .md (ou .markdown ) pour indiquer aux interpréteur la nature du texte qu’il vont lire ; mais ça n’a rien d’obligatoire.

Comme le résultat sera exporté en HMTL, vous pouvez tout à fait introduire directement des balises HTML dans votre texte ; mais celui-ci deviendra moins lisible et ne pourra plus être édité par quelqu’un ne maîtrisant pas le HTML. Attention, le formatage markdown ne sera pas appliqué à l’intérieur de ces balises.
Un peu d’histoire

Ce language a été créé en 2004 par John Gruber et Aaron Swartz et n’a pas évolué depuis. Même si de nombreuses extensions et “extras” sont venues se greffer au projet originel. Le projet initial avec sa documentation est sur daringfireball.

Dès le départ, Gruber a écrit un script Perl pour convertir du texte markdown en XHTML. C’est tout l’intérêt du système : éditer un fichier texte simple avec quelques caractères spéciaux supplémentaires, puis le faire passer dans un script qui va l’enrichir des balises requises pour l’afficher mise en forme dans le navigateur.

Il existe aujourd’hui de très nombreuses implémentations dans divers langages et des variantes augmentées de ce script pour générer du contenu lisible avec une mise en forme plus riche à partir du markdown. Vous utiliserez au minimum celles de GitHub -pour les fichiers de documentation des projets- et Stack Overflow -pour écrire vos questions et vos réponses.

Ces implémentations ne sont pas forcément compatibles et introduisent chacune leur lots d’idiome. Sauf en cas de besoin très spécifiques, il est donc conseillé de s’en tenir aux possibilités de l’implémentation originelle.

Le guide de l’implémentation de GitHub. Le guide de l’implémentation de Stack Overflow.
Outils

Pour découvrir markdown et voir un peu ce qu’il peut faire, vous pouvez essayer un des nombreux éditeurs en ligne comme markable, l’éditeur original de Gruber, dingus ou encore le très puissant stack edit que vous pouvez synchroniser avec google docs.

Il existe de nombreux éditeurs offline. Ce tutoriel est rédigé avec l’un d’entre eux: Mou, mouapp.com pour Mac OS, gratuit. Byword bywordapp.com est également une bonne applications; Mac Os, payant. À noter que byword se synchronise sur vos différents devices. Pour Windows, il existe Write Monkey writemonkey.com, un peu austère à mon goût, mais très fonctionnel et gratuit. Pour Windows également, Markdown Pad markdownpad.com, gratuits. Pour Linux, il existe ReText ReText.

Il reste possible d’ouvrir et d’éditer des fichiers markdown avec n’importe quel éditeur de code ou éditeur textuel (le notepad ou le textedit livré avec votre système d’exploitation). Mais vous êtes alors privé de la coloration syntaxique et de la prévisualisation en temps réel de ce que vous êtes en train d’écrire.

La voie de la maîtrise étant la pratique, je vous conseille fortement d’utiliser Mardown Here. Une extension pour Chrome, Firefox et Safari qui converti le markdown tapé en html. Vous l’utiliserez pour formater vos emails. Ces étant lus au format html par les client mail, le format sera bien transmis. Vous enverrez des emails de meilleur qualité -surtout si des tableaux sont de la partie- et améliorerez rapidement votre compétence avec markdown.
La syntaxe de markdown
Les titres

Il existe deux syntaxes pour les titres. Elles produisent le même résultat et vous pouvez donc utilisez l’une ou l’autre indifféremment. Essayez simplement d’être cohérent à travers vos documents.

Le format Export HTMLé des titres est hx où x est le niveau de titre. Les titres de niveau 1 sont les plus importants, et l’importance décroît avec le nombre.

La méthode par soulignement permet deux niveaux de titre. Il faut souligner votre ligne de texte par deux caractères ou plus -sans limite supérieure. Les = pour un titre 1 et les - pour un titre 2.

Il est également possible de titrer en ajoutant des dièses au début de la ligne. Il n’y a alors pas de limite au nombre de niveaux de titres qu’il est possible d’utiliser (mais n’allez pas au delà de 7). Pour cette raison, c’est cette seconde syntaxe que je vous conseille.

Il est également possible de fermer les titres par un ou plusieurs dièses, mais c’est purement esthétique.

*** Code Markdown ***
*********************

<pre>Title 1
==
Title 2
-
### Title 3 #
####  Title 4
</pre>

*** Export HTML ***
*******************
<pre>
<h1>Title 1</h1>
<h2>Title 2</h2>
<h3>Title 3</h3>
<h4>Title 4</h4>
</pre
Les paragraphes

Pour afficher un paragraphe, sautez deux ligne et de taper son texte. Un seul saut de ligne correspond à un retour chariot et pas à un changement de paragraphe.

Le formatage HTML sera le suivant :

*** Export HTML ***
*******************

<pre><p>a paragraph</p></pre>

Les sauts de ligne simple

Effectuer un saut de ligne simple dans votre texte markdown n’aura aucun effet sur le Export HTMLé. Sauf si vous terminez votre ligne par un double espace (ou plus que ça). Un retour chariot sera alors exporté ; c’est la balise <br/>;.

*** Code Markdown ***
*********************

Ligne sans espace à la fin
Ligne avec 2 espaces à la fin
Troisième ligne

*** export HTML ***
*******************

Ligne sans espace à la fin Ligne avec 2 espaces à la fin
<br/>Troisième ligne

L’emphase

Pour formater une partie de votre texte comme emphase, entourez le par des astérisques ou des underscores. Entourer par un signe unique passe en italique (emphase faible : *;) et par un double signe en gras (emphase forte: **;). Il est possible de combiner les deux. Un double tildes vous permettent de barrer le texte. À titre personnel, j’utilise plutôt les astérisques, mais c’est une question de goût. La seule chose importante est d’être cohérent dans vos documents.

*** Code Markdown ***
*********************

<pre>Texte _dont_ certains __éléments__ sont formatés **pour _être_** en *italique*, en **bold** ou ~~barrés~~.</pre>

*** export HTML ***
*******************

<pre><p>Texte <em>dont</em> certains <strong>éléments</strong> sont formatés <strong>pour <em>être</em></strong> en <em>italique</em>, en <strong>bold</strong> ou <del>barrés</del>.</p></pre>

Les citations

Pour afficher un bloc de citation, commencez le paragraphe par un chevron fermant. Si votre bloc contient plusieurs lignes, vous pouvez faire des sauts de lignes à la main et toutes les ouvrir par un chevron fermant, mais ce n’est pas nécessaire. Ces bloc peuvent contenir d’autres éléments markdown comme des titres ou des listes.

*** Code Markdown ***
*********************

> une citation est un paragraphe ouvert par un chevron fermant

*** export HTML ***
*******************

<blockquote>une citation est un paragraphe ouvert par un chevron fermant</blockquote>

Les listes non ordonnée

Pour afficher une liste, commencez la ligne par une astérisque *, un moins - ou un plus +. Là encore, le choix n’a pas d’importance, mais il faut rester cohérent dans votre document. Pour ma part, j’ai tendance à utiliser l’astérisque qui se rapproche un peu plus de la puce affichée au final.

*** Code Markdown ***
*********************

* item
* item
* item

-

+ item
+ item
+ item

-

- item
- item
- item

*** Export HTML ***
*******************
<ul>
    <li>item</li>
    <li>item</li>
    <li>item</li>
</ul>

Les listes ordonnées

Pour afficher une liste ordonnée, commencez la ligne par un nombre suivit d’un point. Pour que votre markdown soit plus lisible, je vous conseille d’ordonner proprement votre liste. Mais ce n’est pas nécessaire pour le rendu HTML. Comme vous pouvez le voir dans l’export html, la seule différence avec la liste non ordonnée est que la balise englobant les éléments est ol et plus ul. C’est le navigateur qui se charge d’ajouter les nombre pour ordonner la liste.

*** Code Markdown ***
*********************

1. Item
1234. Item
3. Item
4. Item

*** Export HTML ***
*******************

<ol>
    <li>item</li>
    <li>item</li>
    <li>item</li>
</ol>

Le bloc de code

Pour afficher un bloc de code, sautez deux lignes comme pour un paragraphe, puis indentez avec 4 espaces ou une tabulation. Dans le navigateur, la touche tabulation vous fait changer de champ et il n’est généralement pas possible de l’utiliser. Le bloc se terminera dès qu’il arrivera sur un ligne non indentée.
code

code

*** Export HTML ***
*******************

<pre><code>code</code></pre>

Le code inliné

Pour afficher du code dans une ligne, il faut l’entourer par des guillemets simples : (`).

`code`

*** Export HTML ***
*******************

<code>code</code>

Les filets ou barres de séparation

Pour afficher un filet de séparation, entrez <hr/>; dans votre texte ou au moins 3 astérisques *ou moins - sur une ligne entourée de sauts de lignes. Il est possible de les séparer par des espaces. Faites en fonction de ce qui fait le plus de sens pour vous visuellement et restez cohérent dans votre document.

*** Code Markdown ***
*********************

***
---
- - -
*    *    *

*** Export HTML ***
*******************
<hr/>

Les liens

Il y a deux façons d’afficher un lien. De manière automatique en encadrant un lien par des chevrons. Il est alors cliquable et affiche l’url indiquée entre chevrons.

*** Code Markdown ***
*********************

<http://www.google.com>

*** Export HTML ***
*******************

<a href="http://google.com">http://www.google.com</a>

Ou en ajoutant des paramètres. Le texte à afficher est alors indiqué entre crochets suivit de l’adresse du lien entre parenthèses. Dans les parenthèses, à la suite du lien, on peut indiquer un titre entre guillemets. Ce titre sera affiché lors du survol du lien dans le navigateur. Il sera également lu par les navigateurs textuels pour les déficients visuels. Cette méthode est plus verbeuse lors de l’édition du document, mais plus élégante lors de sont export. Elle sera donc préférée à la première.

*** Code Markdown ***
*********************

[google] (http://www.google.com "link to google")

*** Export HTML ***
*******************

<a href="http://www.google.com" title="link to google">google</a>

Les images

Pour afficher une image, commencez par un point d’exclamation. Puis indiquez le texte alternatif entre crochets. Ce dernier sera affiché si l’image n’est pas chargé et lu par les moteurs de recherche. Terminez par l’URL de l’image entre parenthèses. Cette URL peut être un lien vers le web ou un chemin local de ce type : /dossier_images/nom_de_mon_image.jpg. Après le lien vers l’image, il est possible d’ajouter un titre lu par les navigateurs textuels et affiché au survol de l’image par les autres.

*** Code Markdown ***
*********************

![Google logo](https://www.google.fr/images/srpr/logo11w.png "google logo")

*** Export HTML ***
*******************

<img src = "https://www.google.fr/images/srpr/logo11w.png" title = "google logo" alt = "Google logo">

Google logo
Les tableaux

Les tableaux n’existent pas dans la spécification markdown originale, mais ils sont présent dans la plupart des implémentations récentes. Et il ont vraiment une utilité très forte dans certains cas.

L’idée globale est de “dessiner” des colonnes en les entourant avec des pipes |. Le nombre de colonnes est défini dans la première ligne du tableau et vous devez pour chaque ligne avoir le même nombre de colonnes, même si certaines sont vides.

La première ligne sera votre en-tête. La seconde ligne sépare cet en-tête du corps du tableau et définit l’alignement du texte dans les colonnes. Elle ne contient que des tiret - et des deux points : sont utilisés pour définir cet alignement. Pas de : ou juste un à gauche signifie que le texte sera aligné à gauche. Si la ligne de - est entourée de 2 :, le texte sera centré et si un seul : est présent à droite de a ligne, le texte sera aligné à droite.

*** Code Markdown ***
*********************

| Header 1      |     2 header    |   header 3 |
| ------------- |: -------------: | ---------: |
| 1 Online      |        1        |      value |
| Line 2        |        2        |      value |
| 3 Online      |        3        |      value |

Résultat affiché dans le navigateur :

Header 1 	2 header 	header 3
1 Online 	1 	value
Line 2 	2 	value
3 Online 	3 	value

*** Export HTML ***
*******************

<table>
    <thead>
        <tr>
            <th>header 1</th>
            <th align="center">header 2</th>
            <th align="right">header 3</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>line 1</td>
            <td align="center">1</td>
            <td align="right">value</td>
        </tr>
        <tr>
            <td>row 2</td>
            <td align="center">2</td>
            <td align="right">value</td>
        </tr>
        <tr>
            <td>line 3</td>
            <td align="center">3</td>
            <td align="right">value</td>
        </tr>
    </tbody>
</table>

Vous pouvez avoir un tableau très propre comme dans l’exemple précédent pour mieux lire en mode édition. Mais ce n’est pas obligatoire. Les | en début et en fin de ligne sont optionnels. Il est possible d’imbriquer des éléments d’emphase ou de code dans les tableaux. Il n’y a besoin que d’un seul - par colonne pour la séparation entre l’en-tête et le corps du tableau.

*** Code Markdown ***
*********************

1 header | header 2 | 3 header
- |:-: | -:
line `1` | **1** | **_valeur_**
Line 2 | 2 | *Value*

Résultat affiché dans le navigateur :
1 header 	header 2 	3 header
line 1 	1 	valeur
Line 2 	2 	Value

Comme on le voit, ça fonctionne encore une fois exporté, mais toute la lisibilité est perdue dans le markdown.
Échappement des caractères

Les caractères spéciaux ayant un sens en HTML et en markdown doivent être échappés. Pour les esperluètes &amp;, chevrons < et autres caractères HTML, markdown se charge de les convertir en entités HTML lors de l’export. Mais si vous souhaitez utiliser dans votre texte des astérisques, accolades, dièses… à une position indiquant à markdown que vous désirer un formatage particulier, vous devez les échapper en les faisant précéder d’un antislash \. Sinon markdown les masquera et appliquera le formatage correspondant. Les caractères suivants sont à échapper :

\ * ` - _ [] () {} # + . !

Séparer des blocs

Une petite chose peut se révéler agaçante : deux blocs consécutifs se verront fusionnés. Ce sera le cas de deux blocs de citation ou de code par exemple. Et ce quel que soit le nombre de lignes que vous sauterez. Une solution simple est d’ajouter des commentaires html entre deux blocs. La syntaxe des commentaire est la suivante : <!-- texte en commentaire -->;. Le texte sera ignoré par le navigateur. Votre commentaire peut tout à fait être vide.

*** Code Markdown ***
*********************

> Citation 1

> Citation 2

Résultat affiché dans le navigateur :

    Citation 1

    Citation 2

*** Code Markdown ***
*********************

> Citation 1
<!-- -->
> Citation 2

Résultat affiché dans le navigateur :

    Citation 1

    Citation 2

Et après ?

Une fois un markdown édité, l’utilisation la plus fréquente est de le mettre en ligne. Dans un repo Git par exemple. Mais vous pouvez également l’imprimer en pdf ou l’enregistrer au format HTML pour en faire une page web. C’est très pratique pour documenter un projet ou un jeu de données.

