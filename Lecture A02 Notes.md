##Lecture 02 Notes

##Week 12th Jan 2026

Source: https://youtu.be/pGVkCWlXnlg?si=Jv64YaiYYMToCYfx

Garden of Forking Data 

For a 4-sided globe 
```
Ways for `p` to produce `W`, `L` = (4p)^W * (4 - 4*p)^L

```
`p` : probability of finding water for a globe with  

`W` : number of times water is found (win)\

`L` : number of times land is found (loss)


Prior distribution and Posterior distribution 

Increasing the sides increases the number of p values

4-side: 0, 0.25, 0.5, 1 
10-sided: 0, 0.1, 0.2 ....0.8,0.9,1.0 


If there is a globe of infinite posibilities (a polyhedron) 

The posterior probability of any side `p` is proportional to: 

`p^W*(1-p)^L `


for a continous space where p can have any value from 0 to 1 the posterior probability can be calculated by multiplying the above by a ratio. This is the integral of the curve for different p values 

```
(1 + L +1)! / (W! L!)  * [p^W * ( 1-p)^L] 

```






