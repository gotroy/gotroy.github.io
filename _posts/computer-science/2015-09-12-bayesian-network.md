---
layout: post
title: Notes of Bayesian network (class one)

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

<!----------------------------------------- Example of Bayesian Networks ----------------------------------->
<div>
    <p class="index-image">Example of Bayesian Networks</p>
    <img style="display: block" height="500px" src="https://d1b10bmlvqabco.cloudfront.net/attach/idl50807mpy3uf/idmncuax9e47dh/idmndcbcl5677u/MobilePhotoUpload.jpeg" alt="bayes network img" />
</div>

$$P(I)$$ Distribution of Intelligence: H:(High) A:(Average) L:(Low)  
$$
\begin{array}{|c|c|} \hline
P(I=H) & 0.2\\
\hline
P(I=A) & 0.6\\
\hline
P(I=L) & 0.2\\
\hline
\end{array}
$$

$$P(D)$$ Distribution of Difficulty: L:(Low) H:(High)  
$$
\begin{array}{|c|c|} \hline
P(D=L) & 0.6\\
\hline
P(D=H) & 0.4\\
\hline
\end{array}
$$

$$P(S|I)$$ Distribution of SAT given by Intelligence: H:(High) M:(Middem) L:(Low)  
$$
\begin{array}{|c|c|c|c|} \hline I & P(S=H) & P(S=M) & P(S=L) \\
\hline
H & 0.7 & 0.2 & 0.1 \\
\hline
A & 0.2 & 0.6 & 0.2 \\
\hline
L & 0.2 & 0.4 & 0.4 \\
\hline
\end{array}
$$

$$P(G|I,D)$$ Distribution of Grade given by Intelligence and Difficulty: H:(High) M:(Middem) L:(Low)  
$$
\begin{array}{|c|c|c|c|c|} \hline I & D & P(G=H) & P(G=M) & P(G=L) \\
\hline
H  & L & 0.8 & 0.15 & 0.05 \\
\hline
H  & H & 0.6 & 0.3 & 0.1 \\
\hline
A & L & 0.3 & 0.5 & 0.2 \\
\hline
A & H & 0.2 & 0.7 & 0.1 \\
\hline
L & L & 0.2 & 0.6 & 0.2 \\
\hline
L & H & 0.2 & 0.4 & 0.4 \\
\hline
\end{array}
$$

$$P(L|G)$$ Distribution of Letter given by Grade: G:(Good) A:(Average) B:(Bad)  
$$
\begin{array}{|c|c|c|c|} \hline G & P(L=G) & P(L=A) & P(L=B) \\
\hline
H & 0.9 & 0.09 & 0.01 \\
\hline
A & 0.6 & 0.3 & 0.1 \\
\hline
L & 0.1 & 0.3 & 0.6 \\
\hline
\end{array}
$$

$$P(J|S,L)$$ Distribution of Job given by SAT and Letter: Y:(yes) N:(No)  
$$
\begin{array}{|c|c|c|c|} \hline S & L & P(J=Y) & P(J=N) \\
\hline
H & G & 0.99 & 0.01 \\
\hline
M & G & 0.9 & 0.1 \\
\hline
L & G & 0.8 & 0.5 \\
\hline
H & A & 0.8 & 0.5 \\
\hline
M & A & 0.5 & 0.5 \\
\hline
L & A & 0.4 & 0.6 \\
\hline
H & B & 0.5 & 0.5 \\
\hline
M & B & 0.3 & 0.7 \\
\hline
L & B & 0.1 & 0.9 \\
\hline
\end{array}
$$

<!----------------------------------------- Example of Bayesian Networks ----------------------------------->

<!----------------------------------------- Definition of Bayesian Networks ----------------------------------->
<div>
    <p class="index-image">Definition of Bayesian Networks</p>
    <img style="display: block" height="500px" src="https://d1b10bmlvqabco.cloudfront.net/attach/idl50807mpy3uf/ie7nqxpnv02351/ie7nr3iafxp3ax/MobilePhotoUpload.jpeg" alt="bayes network img" />
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
<!----------------------------------------- Definition of Bayesian Networks ----------------------------------->

<!----------------------------------------- Relations in Bayesian Networks ----------------------------------->
<div>
    <p class="index-image">Relaionships in Bayesian Networks 1</p>
    <img style="display: block" height="500px" src="https://d1b10bmlvqabco.cloudfront.net/attach/idl50807mpy3uf/idmncuax9e47dh/idmnd7ivqs7776/MobilePhotoUpload.jpeg" alt="marginal bayesions" />
</div>
<div>
    <p class="index-image">Relaionships in Bayesian Networks 2</p>
    <img style="display: block" height="500px" src="https://d1b10bmlvqabco.cloudfront.net/attach/idl50807mpy3uf/idmncuax9e47dh/idmnd3gunug5tg/MobilePhotoUpload.jpeg" alt="relations of bayesions" />
</div>

Mathematical Definition:

Unconditional Independent:
$$ X \bot Y \ \Leftrightarrow \ P(Y|X) = P(Y) $$

Conditional Dependence:
$$ X (\lnot \bot) Y \ \Leftrightarrow \ P(Y|X) \ne P(Y) $$

$$P(X,Y) = P(X) \times P(Y)$$ `if` $$ X \bot Y$$

<div>
    <p class="index-image">Relaionships in Bayesian Networks 3</p>
    <img style="display: block" height="500px" src="https://d1b10bmlvqabco.cloudfront.net/attach/idl50807mpy3uf/idmncuax9e47dh/idmncyw3u9t75v/MobilePhotoUpload.jpeg" alt="relations of bayesians" />
</div>

Unconditional Dependence:
$$P(Y|Z) \ne P(Y) $$ where both $$Z$$ and $$Y$$ denpent on $$X$$

Conditional Independence:
$$Y \bot Z \ | \ X $$ [ $$Y$$ and $$Z$$ are independent when given by X ].

<!----------------------------------------- Relations in Bayesian Networks ----------------------------------->

<!----------------------------------------- Mariginal Distributions 1 ----------------------------------->
<div>
    <p class="index-image">Marginal Distributions 1 </p>
    <img style="display: block" height="500px" src="https://d1b10bmlvqabco.cloudfront.net/attach/idl50807mpy3uf/idmncuax9e47dh/idmndd62fly7g9/MobilePhotoUpload.jpeg" alt="marginal distributions" />
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
<!----------------------------------------- Mariginal Distributions 1 ----------------------------------->

<!----------------------------------------- Mariginal Distributions 2 ----------------------------------->
<div>
    <p class="index-image">Marginal Distributions 2</p>
    <img style="display: block" height="500px" src="https://d1b10bmlvqabco.cloudfront.net/attach/idl50807mpy3uf/idmncuax9e47dh/idmndcxnql781/MobilePhotoUpload.jpeg" alt="marginal distributions" />
</div>
$$
\sum_{I}P(I) = 1 \\ 
P(I=H) = \cfrac{\#  of \ instance \ in (I=H)}{\# of \ instances \ in \ \sum} \\
P(I=A) = \cfrac{\#  of \ instance \ in (I=A)}{\# of \ instances \ in \ \sum} \\
P(I=L) = \cfrac{\#  of \ instance \ in (I=L)}{\# of \ instances \ in \ \sum} \\
P(I=H) + P(I=A) + P(I=L) = \cfrac{\#  of \ instance \ in (I=H) + \#  of \ instance \ in (I=A) + \#  of \ instance \ in (I=L)}{\# of \ instances \ in \ \sum}
= \cfrac{\# of \ instances \ in \ \sum}{\# of \ instances \ in \ \sum} = 1
$$
<!----------------------------------------- Mariginal Distributions 2 ----------------------------------->

<!----------------------------------------- Mariginal Distributions 3 ----------------------------------->
<div>
    <p class="index-image">Marginal Distributions 3</p>
    <img style="display: block" height="500px" src="https://d1b10bmlvqabco.cloudfront.net/attach/idl50807mpy3uf/idmncuax9e47dh/idmnd3n9o5c7ez/MobilePhotoUpload.jpeg" alt="marginal distributions" />
</div>
$$
\hat X = \operatorname{arg}\max(P(X))
$$

Find the arguments of X, let the $$P(X)$$ to be maximize:   
<!----------------------------------------- Mariginal Distributions 3 ----------------------------------->


<script src="/js/jquery-2.1.3.min.js"></script>
<script type="text/javascript">
$(".index-image").click(function(){
    $(this).next().toggle() ;
});
</script>
