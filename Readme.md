# SPIDER MONKEY OPTIMIZATION

Social behavior of spider monkeys inspired authors to develop an stochastic optimization technique that mimics the foraging behavior of spider monkeys. The foraging behavior of spider monkeys shows that these monkeys fall in the category of fission-fusion social structure (FFSS) based animals. Thus the proposed optimization algorithm, which is based on foraging behavior of spider monkeys, can be explained better in terms of FFSS. Following are the key features of the FFSS.
1.	The fission-fusion social structure based animals are social and live in groups of 40-50 individuals. The FFSS of swarm may reduce the foraging competition among group members by dividing them into sub-groups in order to search food.
2.	A female (global Leader) generally leads the group and is responsible for searching food sources. If she is not able to get enough food for the group, she divides the group into smaller subgroups (size varies from 3 to 8 members) that forage independently.
3.	Sub-groups are also supposed to be led by a female (local leader) who becomes decision-maker for planning an efficient foraging route each day.
4.	The group members communicate among themselves and with other group members, to maintain social bonds and territorial boundaries.

In the developed strategy, foraging behavior of FFSS based animals (e.g. spider monkeys) is divided into four steps. First, the group starts food foraging and evaluates their distances from the food. In the second step, based on the distance from the foods, group members update their positions and again evaluate distance from the food sources. Furthermore, in the third step, local leader updates its best position within the group and if the position is not updated for a specified number of times then all members of that group start searching of the foods in different directions. Next, in the fourth step, global leader, updates its ever best position and in case of stagnation, it splits the group into smaller size subgroups. All the four steps, mentioned aforesaid, are continuously executed until the desired output is achieved. There are two important control parameters necessary to introduce in the proposed strategy, one is GlobalLeaderLimit and another is LocalLeaderLimit which help local and global leaders to take appropriate decisions.

#### Algorithm
<pre>
1. Initialize Population, LocalLeaderLimit, GlobalLeaderLimit, pr.
2. Calculate fitness (i.e. the distance of individuals from food sources).
3. Select global leader and local leaders by applying greedy selection. 
**while** (Termination criteria is not satisfied) **do** 
&nbsp;&nbsp;(i)	For finding the objective (Food Source), generate the new positions 
&nbsp;&nbsp;&nbsp;for all the group members by using self experience, local leader experience 
&nbsp;&nbsp;&nbsp;and group members experience.
&nbsp;&nbsp;(ii) Apply the greedy selection process for all the group members based on their fitness;
&nbsp;&nbsp;(iii) Calculate the fitness probability for all the group members. 
&nbsp;&nbsp;(iv) Produce new positions for the all the group members, selected based on the fitness probability, by using self experience, global leader experience and group members’ experiences.
&nbsp;&nbsp;(v)	Update the position of local and global leaders, by applying the greedy selection process on all the groups.
&nbsp;&nbsp;(vi) If any Local group leader is not updating her position after a specified number of times (LocalLeaderLimit) then re-direct all members of that particular group for foraging.
&nbsp;&nbsp;(vii) If Global Leader is not updating her position for a specified number of times (GlobalLeaderLimit) then she divides the group into smaller groups. 
**end while**
</pre>

# SMO-in-python
Python code of Spider-Monkey Optimization (SMO)

Coded by: Mukesh Saraswat (emailid: saraswatmukesh@gmail.com), Himanshu Mittal (emailid: himanshu.mittal224@gmail.com) and Raju Pal (emailid: raju3131.pal@gmail.com)

Reference: Jagdish Chand Bansal, Harish Sharma, Shimpi Singh Jadon, and Maurice Clerc. "Spider monkey optimization algorithm for numerical optimization." Memetic computing 6, no. 1, 31-47, 2014.
@link: http://smo.scrs.in/

The C++ version of the SMO at link: http://smo.scrs.in/

The code template used is similar to code given at link: https://github.com/himanshuRepo/CKGSA-in-Python

This code is available for non-commercial purposes. We would appreciate an acknowledgment if you use it in your work.

* Command to run:

	python Main.py
