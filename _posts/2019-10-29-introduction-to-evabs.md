---
layout: post
title: "[PART 2] Introduction to EVABS"
tags: [EVABS]

---
This blog post is a very basic introduction to how EVABS works and how to solve it.

> NOTE: If you have not completed the setup for solving the labs, please refer to [Part 1: Getting Started with EVABS](https://www.hawkspawn.com/blog/getting-started-with-evabs/).

Once EVABS has been installed, open the application. Input your name and you'll be greeted with the landing page.

<a style="text-align:center;" href="https://ibb.co/PCHwkwj"><img src="https://i.ibb.co/bd9ztzm/newui.jpg" alt="newui" border="0" height="500" width="250"></a>

---
### Challenges
The `Challenges` button navigates to a list of all the challenges in EVABS. There are 12 levels (as of when this article was written) and each level introduces the user to one of the vulnerabilities that exist in the Android platform. With each level, the difficulty linearly increases and every level is provided with a hint as to how to solve the level. 

<a style="text-align:center;"><img src="https://i.ibb.co/hmj8s39/ss2.jpg" alt="ss2" border="0" height="500" width="250"></a>

Successfully solving a level with or without the help of the hint gifts the player with a flag. This flag can be submitted and checked against a flag checking service that is accessible from within EVABS. EVABS has been made vulnerable in such a way that there are multiple ways to solve a particular level which the players can explore. The final goal is to exploit the level and find the flag.

All the flags in EVABS are of the format:

```java
EVABS{s0m3_l33t_t3xt_h3r3}
```

---
### Submitting Flags

Once you have found a flag successfully, submit the flag using the `Flag Check` feature of the application. If you see a success message, congratulations, you have solved the level! 

<a href="https://ibb.co/PMbpJ3p"><img src="https://i.ibb.co/XDdB6NB/flagcheck.jpg" alt="flagcheck" border="0" height="500" width="250"></a>

Hopefully, this gives some idea on how EVABS works. 
Let's move on to our next section where we start solving the levels. 
