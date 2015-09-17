---
layout: post
title: Notes of Bayesian network (class Three)

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

<div>
    <p class="index-image">Use Dynamic Programming to optimize Bayesian Networks</p>
    <img style="display: block" height="500px" src="https://d1b10bmlvqabco.cloudfront.net/attach/idl50807mpy3uf/ie7nqxpnv02351/ie7nqzbp7fvpw/MobilePhotoUpload.jpeg" alt="bayes network img" />
</div>

In some senario, we could use dynamic programming to optimize Bayesian Networks calcultion.

<div>
    <p class="index-image">Use Maximum likelihood Estimation to training data</p>
</div>

In Machine Learning, the Size of trainning set must larger than the variables, otherwise result could be overfitting!

In the training process, we should calculate the distance between y and f(x), we could use:

- **Squares Error** in Linear Regression or 
- **Maximum likelihood** in Logistic Regression

In Bayesian Networks, we also use **Maximum likelihood** to measure the distance between y and f(x)

<div>
    <p class="index-image">Use NeticaJ library to implement Bayesian Networks</p>
    <!--
    <img style="display: block" height="500px" src="https://d1b10bmlvqabco.cloudfront.net/attach/idl50807mpy3uf/ie7nqxpnv02351/ie7nr3iafxp3ax/MobilePhotoUpload.jpeg" alt="bayes network img" />
    -->
</div>

It is a Java library to implement calculation of Bayesian Networks.

In the Eclipse, config the Run Configuration:

Run configuration: VM arguments:

-Djava.library.path=/Users/dongdong/Downloads/NeticaJ_504/bin

<script src="/js/jquery-2.1.3.min.js"></script>
<script type="text/javascript">
$(".index-image").click(function(){
    $(this).next().toggle() ;
});
</script>
