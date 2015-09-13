---
layout: post
title: Notes of Bayesian network

---

<style type="text/css">
    .index-image{
        color: blue;
    }
    .index-image:hover{
        cursor: pointer;
    }
</style>
<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML"></script>

---

##### Course Info:

- Course Name: [Probabilistic Graphical Models](/2015/09/12/probabilistic-graphical-models.html)
- Processor: Karen Hovsepian

---

<!----------------------------------------- Bayesian Networks ----------------------------------->
<div>
    <p class="index-image">Definition of Bayesian Networks</p>
    <img style="display: none" width="100%" src="https://d1b10bmlvqabco.cloudfront.net/attach/idl50807mpy3uf/ie7nqxpnv02351/ie7nr3iafxp3ax/MobilePhotoUpload.jpeg" alt="bayes network img" />
</div>
$$
BN = \{\{A,B,C \},\{D_A,D_B,D_C\},\{P_{aB}=\{A\},P_{aA}=\varnothing,P_{aC}=\{A\}\}, \{P(A),P(B|A),P(C|A)\} \}
$$

$$\{A,B,C\}$$ means: This net network has **3** nodes(variables) which were $$ A,B,$$ and $$C$$

$$\{D_A,D_B,D_C\} $$ means: Different variables could have different size of dimensions.

$$\{P_{aB}=\{A\},P_{aA}=\varnothing,P_{aC}=\{A\}\} $$: Distribution of variables' values depend on parents distribution.

$$\{ P(A), P(B|A), P(C|A) \}$$
Calculat the distribution values of different variables.

Dimensions of $$A,B,C$$:  
$$|D_A| = 3$$,  
$$|D_B| = 5$$,  
$$|D_C| = 2$$

Distribution size of 
$$\{P(A),P(B|A),P(C|A)\}$$:  
$$P(A) \leftarrow 1 \times |D_A|$$,  
$$P(B|A) \leftarrow |D_B| \times |D_A| $$,  
$$P(C|A) \leftarrow |D_C| \times |D_A| $$

Find the arguments of c, let the $$P(C)$$ to be maximize:   
$$
\hat c = \operatorname{arg}\max(P(C))
$$
<!----------------------------------------- Bayesian Networks ----------------------------------->

<!----------------------------------------- Mariginal Distributions ----------------------------------->
<div>
    <p class="index-image">Marginal Distributions (SHOULD CHECK WITH PROCESSOR)</p>
    <img style="display: none" width="100%" src="https://d1b10bmlvqabco.cloudfront.net/attach/idl50807mpy3uf/idmncuax9e47dh/idmndd62fly7g9/MobilePhotoUpload.jpeg" alt="marginal distributions" />
</div>
$$P(X)$$ means probability distribution of X for every value of X

$$\sum_{x}P(x)=1$$ which means:

<pre>
total = 0
for each X in (sum):
    total += P(X)
total == 1 (True)
</pre>

Distribution of X and Y:
$$
\begin{array}{|c|c|c|} \hline & y=Y & y=N \\
\hline
x=Y & 0.3 & 0.2\\
\hline
x=N & 0.1 & 0.4\\
\hline
\end{array}
$$

Marginal Distributions:
$$
P(x=Y) = 0.3 + 0.2 = 0.5 \\
P(x=N) = 0.1 + 0.4 = 0.5 \\
P(y=Y) = 0.3 + 0.1 = 0.4 \\
P(y=N) = 0.2 + 0.4 = 0.6
$$

<script src="/js/jquery-2.1.3.min.js"></script>
<script type="text/javascript">
$(".index-image").click(function(){
    $(this).next().toggle() ;
});
</script>
