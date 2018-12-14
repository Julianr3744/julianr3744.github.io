---
layout: post
title: "Flag Project- In progress"
date: 2018-12-14
---

```
(define size 100)
(define width (* 3 size))
(define height (* 2 size))
(define stripeheight (/ height 9))
(define stripewidth (/ width 5))

(define stripe1 (rectangle width stripeheight "solid" "white"))

(define stripe2 (rectangle stripeheight (* stripewidth 2) "solid" "white"))

(define stripe3(rotate 90 stripe2))

(define base(rectangle width height "solid" "RoyalBlue"))

(define canton(rectangle (* 5.5 stripeheight) (* 5.5 stripeheight) "solid" "Royalblue"))

(define stage1(put-image stripe1 150 (* 1.5 stripeheight) base))
  
(define stage2(put-image stripe1 150 (* 3.5 stripeheight) stage1))

(define stage3(put-image stripe1 150 (* 5.5 stripeheight) stage2))

(define stage4(put-image stripe1 150 (* 7.5 stripeheight) stage3))

(define stage5(put-image canton 55 150 stage4))

(define stage6(put-image stripe2 60 148 stage5))

(define GreeceFlag(put-image stripe3 56 145 stage6))
```
![FlagImage](/images/flagV2.png)

So currently, i have the base program set as you can see above, where the flag image is produced, but currently i have alot of numbers that have to start fitting in with the scale. So currently, it looks like it fits in with the scale size of 100, as you can see the first line of code with size, but if i changed that to 150, or another number, the enitre flag is messed up. A challenge for me was trying to think about this in the form of layers. When we made the flags with paper, we had to have layers. I then encorperated that into my project with the different stages. But now i gotta first fix the size problem, which adds on to the positioning problem.
