---
layout: post
title: Understanding of combinatorics
---

Combinatorics

 In many people's minds, mathematics is a complex world full of unreadable equations and notations that that hardly anyone understands. What if I told you that resolving a problem or demonstrating a formula can also be done with (almost) no numbers and no equations, just by using some words, your logic and your ability to count? Counting elements (cows, cards or balls for instance) to solve a problem is a real area of mathematics called **combinatorics**. If you don't understand how counting elements can help us with solving mathematical problems, no worries, that is the purpose of this blog post. To make you understand what combinatorics is, we are going to demonstrate a statistic formula. You will see how useful counting can be.
 <br>
 <br>
    The formula we will prove is called **Pascal's formula** : <b> $ {n}\\choose{k}$ = ${n-1}\\choose{k}$ + ${n-1}\\choose{k-1} $ </b>,
 
<br>
<br>
 
    First of all, we have to understand what this symbol $ {n}\\choose{k}$, termed as a **binomial coefficient**, means :  
   
   <br>
 <br>
    Understanding of binomial coefficients,
 <br>
 <br>
    Imagine you have 2 extra tickets for a concert (let's say Beyonce's). After listing all the people you could take with you, you managed to reduce the list to 3 people. You still hesitate between 3 of your friends, called Alice, Betty and Caro. How many different groups of 2 people can you make with your 3 friends?
 <br>
 <br>
    You can invite either :,
 <br>
 <br>
    * Alice and Betty
     <br>
    * Alice and Caro 
     <br>
    * Betty and Caro
 <br>
 <br>
    We can see that there are 3 different ways to choose the 2 friends coming with you to the concert among your 3 friends. The number of different groups of 2 people you can make with 3 people is  called \"3 choose 2\". It is represented by this symbol $3\\choose 2$ and it is equal to 3 here.
 <br>
 <br>
    This notion can easily be generalized. The size of the sample we want to isolate is usually called \"k\" (in our case, 2 friends). The total amount of elements we have is often named \"n\" (3 friends in our example).
 <br>
 <br>
    As we can see, a binomial coefficient is represented by $n\\choose k$ and is read \"n choose k\". It represents the number of ways you can chose k elements among n elements.
 <br>
 <br>
    Now that we all know what a binomial coefficient is, let's demonstrate Pascal's formula using combinatorics.
    <br>
 <br>
    *Pascal's formula*
 <br>
 <br>
    The formula we are going to demonstrate is the following one : ${n}\\choose{k}$ = ${n-1}\\choose{k}$ + ${n-1}\\choose{k-1} $.
 <br>
 <br>
    Let's say we have 6 (here n=6) marbles in front of us.
  <br>
 <br>
    <img src=\"https://github.ubc.ca/MDS-2019-20/DSCI_542_lab2_chahma/blob/master/Pictures/6%20circles%20beginning.JPG?raw=true\" width=\"300px\"/>
    <br>
 <br>
    We can only keep 3 of those 6 marbles (k=3), and put them in a bag. The number of possibilities we have to choose those 3 marbles among the 6 we have is ${6}\\choose{3}$ = ${n}\\choose{k}$. 
 <br>
 <br>
    First of all, we take one marble in our hand, whichever we want, the green one for instance.
 <br>
 <br>
    <img src=\"https://github.ubc.ca/MDS-2019-20/DSCI_542_lab2_chahma/blob/master/Pictures/choose%20one%20marble.JPG?raw=true\" width=\"300px\"/>
   <br>
 <br>
    We have two possible choices : keep it and put it in the bag or don't keep it and throw it away.
  <br>
 <br>
    * First choice : keeping the green marble and put it in the bag
     <br>
 <br>
    Let's imagine that we put the green marble in the bag.
    <br>
 <br>
    <img src=\"https://github.ubc.ca/MDS-2019-20/DSCI_542_lab2_chahma/blob/master/Pictures/marble%20kept.JPG?raw=true\" width=\"300px\"/>
  <br>
 <br>
   Now, we only have to choose 2 (here, 2=k-1) more marbles among the 5 remaining (here 5=n-1). So we still have ${5}\\choose{2}$ = ${n-1}\\choose{k-1}$ ways to choose the 2 last marbles. 
     <br>
 <br>
    * Second choice : not keeping the green marble
    <br>
 <br>
    Imagine that this time we don't decide to keep the green marble and throw it away.
    <br>
 <br>
    <img src=\"https://github.ubc.ca/MDS-2019-20/DSCI_542_lab2_chahma/blob/master/Pictures/Marble%20not%20kept.JPG?raw=true\" width=\"300px\"/>
 <br>
 <br>
    We still have to choose 3 (here k=3) marbles, but there are only 5 (here n-1=5) remaining marbles on the table. Therefore, we now have ${5}\\choose{3}$ = ${n-1}\\choose{k}$ ways to choose 3 marbles.
    
 <br>
 <br>
    Overall, in order to find out the number of ways we have to choose 3 marbles among 6, we just have to sum the number of possibilities we had when we kept the green marble and the number of possibilities we had when we didn't keep the green marble. In a more formal way, we can write it : ${6}\\choose{3}$ = ${5}\\choose{3}$ + ${5}\\choose{2}$. If we keep using this relation on each term of the sum, it gives : ${6}\\choose{3}$ = ${4}\\choose{3}$ + ${4}\\choose{2}$ + ${4}\\choose{1}$ + ${4}\\choose{2}$. Or :
   <br>
 <br>
    * ${4}\\choose{3}$ = ${3}\\choose{3}$ + ${3}\\choose{2}$ = 1 + 3 = 4 (there is one way to choose 3 elements among 3, and we showed before that ${3}\\choose{2}$ = 3)
    * ${4}\\choose{2}$ = ${3}\\choose{2}$ + ${3}\\choose{1}$ = 3 + 3 = 6 (we showed before that ${3}\\choose{2}$ = 3 and there are 3 ways to choose 1 element among 3)
    * ${4}\\choose{1}$ = 4 (there are 4 ways to choose 1 element among 4) 
    <br>
 <br>
    So ${6}\\choose{3}$ = 4 + 6 + 4 + 6 = 20 
   <br>
 <br>
    The general formula we demonstrated is ${n}\\choose{k}$ = ${n-1}\\choose{k}$ + ${n-1}\\choose{k-1} $.
     <br>
 <br>
    This is it, we have proved Pascal's formula! You can notice that we did it without writing any complicated equations, just by understanding the formula and counting the elements we had. The way we demonstrated this formula is combinatorics and and it is totally valid to do that. 
    <br>
 <br>
    This demonstration is just an example to show you how combinatorics works and how powerful and easy it can be. Combinatorics can be used in statistics (as shown before), but also in several other mathematical areas dealing with counting a finite number of elements. 