---
layout: post
title: "Final Video Game Project - Final Submission"
date: 2019-03-07
---

## Link to Video Game
- https://www.wescheme.org/view?publicId=v8hiKt37au

## Game Title
- Get The Cheese Jerry!

## Rundown Of Game
- My game takes place in a household where Tom the cat and Jerry the mouse live. Jerry is who you are playing as and your objective is to get as many pieces of cheese as you can to increase your score. But watch out, tom will be coming for you, avoid tom and collect as many cheese as possible. 

## Image Of Function I Am Explaining 

* * *
![Code](/images/code1.png)
* * *

## Description of the Collide Function
- So first I start off with the contract for this function, what it's going to do. It takes in 4 data types, which are numbers, and produces a boolean (a true or false statement.) Next looking at my examples, on line 140, the collide function takes in the numbers 1 2 1 2, and with these numbers, the collide? example uses the less than function and the distance function to see if the numbers which represent coordinates (1,2) (1,2) are 50 pixels appart. Same thing in line 141 but with different numbers to represent different coordinates. Now we start with defining the collide function, to actually turn this word into a function. So collide? will take in 4 numbers, px, py, cx, and cy. And then the result of giving those numbers, the less than and distance function will check if the numbers which represent coordinates (px,py) (cx,cy) are less than 50 pixels appart.  

## The role of the function
- So the role of the collide function is to see how close the player is to either the target or the danger. In this case, it checks if jerry is less than 50 pixels from either the cheese, or tom. 
