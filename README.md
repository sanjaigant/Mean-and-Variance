Exp 1: Mean and variance of a discrete distribution
Date:16/12/2024
Aim :
To find mean and variance of arrival of objects from the feeder using probability distribution

Software required :
Python and Visual components tool

Theory:
The expectation or the mean of a discrete random variable is a weighted average of all possible values of the random variable. The weights are the probabilities associated with the corresponding values. It is calculated as,

image

The variance of a random variable shows the variability or the scatterings of the random variables. It shows the distance of a random variable from its mean. It is calcualted as

image

Procedure :
Construct frequency distribution for the data

Find the probability distribution from frequency distribution.

Calculate mean using

image

Find

image

Calculate variance using

image

Experiment :
image

Program :
Developed by : sanjai ganth.B
Register number : 24006814
import numpy as np
L=[int(i) for i in input().split()]
N=len(L); M=max(L) 
x=list();f=list()
for i in range (M+1):
    c = 0
    for j in range(N):
        if L[j]==i:
            c=c+1
    f.append(c)
    x.append(i)
sf=np.sum(f)
p=list()
for i in range(M+1):
    p.append(f[i]/sf) 
mean=np.inner(x,p)
EX2=np.inner(np.square(x),p)
var=EX2-mean**2 
SD=np.sqrt(var)
print("The Mean arrival rate is %.3f "%mean)
print("The Variance of arrival from feeder is %.3f "%var) 
print("The Standard deviation of arrival from feeder is %.3F "%SD)
Output :
280447313-1d674464-ec27-4123-8846-d5dc93e392b8

Results :
The mean and variance of arrivals of objects from feeder using probability distribution are calculated.
