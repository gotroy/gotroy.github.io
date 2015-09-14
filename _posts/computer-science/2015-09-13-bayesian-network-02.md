---
layout: post
title: Notes of Bayesian network (class Two)

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

<!----------------------------------------- Definition of Bayesian Networks ----------------------------------->
<div>
    <p class="index-image">Definition of Bayesian Networks</p>
    <img style="display: none" height="500px" src="https://d1b10bmlvqabco.cloudfront.net/attach/idl50807mpy3uf/ie7nqxpnv02351/ie7nr3iafxp3ax/MobilePhotoUpload.jpeg" alt="bayes network img" />
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

$$|D_A| = 3$$

$$|D_B| = 5$$

$$|D_C| = 2$$

Distribution size of: 
$$\{P(A),P(B|A),P(C|A)\}$$

$$P(A) \leftarrow 1 \times |D_A|$$

$$P(B|A) \leftarrow |D_B| \times |D_A| $$

$$P(C|A) \leftarrow |D_C| \times |D_A| $$

Find the arguments of c, let the $$P(C)$$ to be maximize:   

$$
\hat c = \operatorname{arg}\max(P(C))
$$

<!----------------------------------------- Definition of Bayesian Networks ----------------------------------->

<!----------------------------------------- joint probability 1 ----------------------------------->
<div>
    <p class="index-image">Joint Probability one</p>
    <img style="display: none" height="500px" src="https://d1b10bmlvqabco.cloudfront.net/attach/idl50807mpy3uf/ie7nqxpnv02351/ie7nr1xgni53ak/MobilePhotoUpload.jpeg" alt="joint probability" />
</div>

$$
P(A,B,C) = P(A|B,C) \cdot P(B|C) \cdot P(C)
$$

Becuase we know the structure, we could optimize the probilities:

$$
P(A,B,C) = P(B|A) \cdot P(C|A) \cdot P(A)
$$

We also know that:

$$
P(A,B) = P(A) \cdot P(B|A) \\
P(A,B) = P(B) \cdot P(A|B) \\
P(A) \cdot P(B|A) = P(B) \cdot P(A|B) \\
P(A|B) = \frac{P(A,B)}{P(B)}\\
P(A|B) = \frac{P(B|A) \cdot P(A)}{P(B)}
$$

Also:

$$
P(A=1,B=0) = \frac{| (A=1) \ \& \ (B=0) |}{\sum} \\
P(A=1 | B=0) = \frac{| (A=1) \ \& \ (B=0) |}{\sum B=0}
$$

<!----------------------------------------- joint peobability 1 ----------------------------------->

<!----------------------------------------- joint probability 2 ----------------------------------->
<div>
    <p class="index-image">Joint Probability two</p>
    <img style="display: none" height="500px" src="https://d1b10bmlvqabco.cloudfront.net/attach/idl50807mpy3uf/ie7nqxpnv02351/ie7nqzbp7fvpw/MobilePhotoUpload.jpeg" alt="joint probability" />
</div>

$$
P(A_1,A_2,A_3,...,A_n) = P(A_1 | A_2,A_3,...,A_n) \times P(A_2 | A_3,...A_n) \times ... \times P(A_{n-1} | A_n)
$$

Becuase we know the structure, we could optimize the probilities:

$$
P(A,B,C,D,E) = P(E|C,D) \cdot P(C|A,B) \cdot P(D|B) \cdot P(B|A) \cdot P(A)
$$

We could rewrite to:

$$
P(X_1,X_2,...,X_n) = \prod_{i=1}^n P(X_i|\operatorname{par}(X_i))
$$

<!----------------------------------------- joint peobability 2 ----------------------------------->

<!----------------------------------------- joint probability 3 ----------------------------------->
<div>
    <p class="index-image">Others</p>
    <img style="display: none" height="600px" src="https://d1b10bmlvqabco.cloudfront.net/attach/idl50807mpy3uf/ie7nqxpnv02351/ie7nqz34yz1aw/MobilePhotoUpload.jpeg" alt="joint probability" />
</div>

$$\sum_c:$$ over all values of $$C$$

$$
P(A,B) = \sum_C P(A,B,C)
$$ 

$$
P(A,B) = P(A,B,C=C_1) + P(A,B,C=C_2) + P(A,B,C=C_3) = \sum_c P(A,B,C)
$$

$$
P(A,C) = \sum_B P(A,B,C)
$$

$$
P(C) = \sum_A \sum_B P(A,B,C) \
\\ or \\
P(C) = \sum_{A,B} P(A,B,C)
$$

<!----------------------------------------- joint peobability 3 ----------------------------------->



<script src="/js/jquery-2.1.3.min.js"></script>
<script type="text/javascript">
$(".index-image").click(function(){
    $(this).next().toggle() ;
});
</script>
