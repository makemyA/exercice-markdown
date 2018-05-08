
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


Le bloc de code

Pour afficher un bloc de code, sautez deux lignes comme pour un paragraphe, puis indentez avec 4 espaces ou une tabulation. Dans le navigateur, la touche tabulation vous fait changer de champ et il n’est généralement pas possible de l’utiliser. Le bloc se terminera dès qu’il arrivera sur un ligne non indentée.
code
<pre>
<code>
import numpy as np
import tensorflow as tf


num_data = 64
feat_dim = 6
A_feature = np.random.randn(10, feat_dim).astype(np.float32)
P_feature = np.random.randn(5, feat_dim).astype(np.float32)

#Python Version for each feature
out = np.zeros((len(P_feature),1))
for i in range(len(P_feature)):
    t = (A_feature-P_feature[i])
    t1 = t**2
    t2 = np.sum(t1,axis=1)
    t3 = np.sum(t2**2.0)**(1/2.0)
    out[i]=t3

#Half Tensorflow Version with only one feature result
P_dist2 = tf.norm(tf.reduce_sum(tf.square(tf.subtract(A_feature, P_feature[0])), 1),ord=2)
with tf.Session() as sess:
        pos_dist2_np = sess.run(P_dist2)
</code>
</pre>

