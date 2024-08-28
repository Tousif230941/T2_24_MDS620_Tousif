# Import libraries
import numpy as np
import math
import random
import matplotlib.pyplot as plt

# Visualize the figure
x = np.arange(0, 1.05, 0.05)
y = - x * x + 1
plt.plot(x, y, color='g')

# plot x = 0
x1 = [0] * 11
y1 = np.arange(0, 1.1, 0.1)
plt.plot(x1, y1, color='g')

# plot y = 0
x3 = np.arange(0, 1.05, 0.05)
y3 = [0] * 21
plt.plot(x3, y3, color='g')

# display the figure
plt.show()

# Implement the Monte Carlo Method
def MonteCarl(TRIES):
    num_in_area = 0

#### implement your code here ####
def MonteCarl(TRIES):
    num_in_area = 0
   
    for _ in range(TRIES):
        x = random.uniform(0, 1)
        y = random.uniform(0, 1)
       
        if y <= -x**2 + 1:
            num_in_area += 1
   
    shadow_area = num_in_area / TRIES
    return shadow_area
##################################
    
    #return shadow_area

# Conduct some experiments
experiments = [10, 100, 1000, 10000, 100000]
res = {}
# Call MonteCarl() for a few times
for exp in experiments:
    res[exp] = MonteCarl(exp)
print(res)
