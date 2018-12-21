---
layout: post
title: "Flag Project - Final Submission"
date: 2018-12-21
---

## Flag of _Greece_ by _Julian R._

## Describe your program

-   What country did you design for? I designed the greece flag
-   What grade do you expect? I expect a 3, a practitioner

## Current output

* * *
![Flag](/images/finalflag.png)
* * *

## Describe your process.

-  I started off with the collage, thinking about the different layers. The base is where I started off, and I thought of the function ```put-image``` and thought of that blue paper i used as the base, then putting the stripes on as layers. The last layer I did was the canton, just like the code. The collage really helps out when you think about it, it tells you the process you have to perform, but instead of with paper, you use different functions to create the output of the flag

## Explain your code.

-  So this is basically the backbone of my flag. Each part is in here. I first started off with a size function, which makes my entire flag code to a certain scale. And this is where i take everything and it depends on that function to fit all the parts together. the width and height functions are part of the size, the Greece Flag has a 3:2 scale, meaing the width is going to be longer than the height, and i made sure of that to happen with these two functions. The next two lines is where i take those definitions, and put them so they can scale a certain stripe. The last function i have in that top section is the gblue function, i basically made a color using 3 different number values to get the cetain color i needed for the flag. The next part is essentially the diffent cutouts of paper i did with the collage. stripe1 is the horizontal stripes i had in my flag. The stripeheight now specifically ties in with this because there are 9 exactly equal stripes on the flag. The next stripe is stripe2, in which i used this for my canton to make the plus sign on my canton. I then take that stripe, stripe 2 and rotate it to create stripe3, so i can make the canton on my flag. The next part is my base, a basic rectangle function that uses my height and width function along with gblue and solid to give it its certain shape. And lastly the canton, this is only the base of the canton, I looked at the flag and tried to make the canton to its size, so i had to make it a square with the stripeheight and stripeheight again. This was the basis of my canton, i later put stripe2 and stripe3 on it to make the plus. 
* * *

```
(define size 200)
(define width (* 3 size))
(define height (* 2 size))
(define stripeheight (/ height 9))
(define stripewidth (/ width 5))
(define gblue (make-color 13 94 175))

(define stripe1(rectangle width stripeheight "solid" "white"))

(define stripe2(rectangle stripeheight (* stripewidth 2.11) "solid" "white"))

(define stripe3(rotate 90 stripe2))

(define base(rectangle width height "solid" gblue))

(define canton1(rectangle (* 5.5 stripeheight) (* 5.5 stripeheight) "solid" gblue))
```

* * *


## Program code
```
(define size 300)
(define width (* 3 size))
(define height (* 2 size))
(define stripeheight (/ height 9))
(define stripewidth (/ width 5))
(define gblue (make-color 13 94 175))

(define stripe1(rectangle width stripeheight "solid" "white"))

(define stripe2(rectangle stripeheight (* stripewidth 2.11) "solid" "white"))

(define stripe3(rotate 90 stripe2))

(define base(rectangle width height "solid" gblue))

(define canton1(rectangle (* 5.5 stripeheight) (* 5.5 stripeheight) "solid" gblue))

(define canton2(put-image stripe2 (/ (* 5.5 stripeheight)2) (/ (* 5.5 stripeheight)2) canton1))

(define canton3(put-image stripe3 (/ (* 5.5 stripeheight)2) (/ (* 5.5 stripeheight)2.2) canton2))





(define stage1(put-image stripe1 (/ width 2) (* 1.5 stripeheight) base))
  
(define stage2(put-image stripe1 (/ width 2) (* 3.5 stripeheight) stage1))

(define stage3(put-image stripe1 (/ width 2)  (* 5.5 stripeheight) stage2))

(define stage4(put-image stripe1 (/ width 2) (* 7.5 stripeheight) stage3))

(define FinalFlag(put-image canton3 (/(* 5.5 stripeheight)2) (/ width 2) stage4))
```
