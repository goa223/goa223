# k-means clustering – initial data

import random
import math

# importing numpy
import numpy as np

from matplotlib import pyplot

jet=pyplot.get_cmap('coolwarm')

numtrials=50

list1=[]

for i in range(numtrials):
    list1.append([random.random(),random.random()])

vec1=np.array(list1)

list2=[]

for i in range(numtrials):
    list2.append([random.random(),random.random()+0.5])

vec2=np.array(list2)

list3=[]

for i in range(numtrials):
    list3.append([-1*random.random(),random.random()])
    
vec3=np.array(list3)

# plot
pyplot.scatter(*zip(*list1), s=100, cmap=jet, vmin=0, vmax=4)
pyplot.scatter(*zip(*list2), s=100, cmap=jet, vmin=0, vmax=4)
pyplot.scatter(*zip(*list3), s=100, cmap=jet, vmin=0, vmax=4)
pyplot.show()


