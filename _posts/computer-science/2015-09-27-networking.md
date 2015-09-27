---
layout: post
title: Mininet for Advantaged Networking

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

- Course Name: Advantaged Networking
- Processor: Dr. Kumar

---

##### Mininet Setup Directions

https://troy.blackboard.com/bbcswebdav/pid-9688805-dt-content-rid-65070941_2/courses/T01-CS6649TRAB-15FA/Mininet%20Setup.pdf

1. Download and install the latest Virtualbox for your platform and you can find it [here](https://www.virtualbox.org/wiki/Downloads).
2. Download the latest Mininet virtual machine image from [here](https://github.com/mininet/mininet/wiki/Mininet-VM-Images). 
3. In Virtualbox select File -> Import Appliance and select the .ova you just downloaded. Virtualbox will show you the VM settings and you can then click Import.
4. Next, setup a bridged network by selecting the VM in the left side bar and then Settings -> Network and ensure that Adapter 1 is enabled and attached to a Bridged Adapter
5. Start the VM by clicking Start.
6. Log in to the VM using mininet for both username and password.
7. Type sudo ifconfig on command line. This will display the IP addresses of the connected network interfaces and find for eth0 inet IP. 
8. Open a terminal on your desktop (Terminal on Mac OSX, Putty on Windows and xterm on Linux) and type ssh mininet@ip_address where ip_address is the IP address under the eth0 output from the ifconfig command. Use the password mininet.
9. To ensure Mininet is working correctly run this test : sudo mn --test pingpair.

##### Project Describe:

https://troy.blackboard.com/bbcswebdav/pid-9653630-dt-content-rid-65243017_2/courses/T01-CS6649TRAB-15FA/CS6649MiniProject1%281%29.pdf

Mininet Wiki: https://github.com/mininet/mininet/wiki/Documentation

Pox Wiki: https://openflow.stanford.edu/display/ONL/POX+Wiki

<div>
    <p class="index-image">Use Dynamic Programming to optimize Bayesian Networks</p>
    <img style="display: block" height="500px" src="https://d1b10bmlvqabco.cloudfront.net/attach/idl50807mpy3uf/ie7nqxpnv02351/ie7nqzbp7fvpw/MobilePhotoUpload.jpeg" alt="bayes network img" />
</div>


1. seperate whole file to 20% and 80% and save as cvs
2. random choose 1000 case

More training and less overfitting
Less testing set will less acurry

<script src="/js/jquery-2.1.3.min.js"></script>
<script type="text/javascript">
$(".index-image").click(function(){
    $(this).next().toggle() ;
});
</script>
