

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

