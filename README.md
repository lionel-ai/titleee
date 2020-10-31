import numpy as np
import matplotlib.pyplot as plt

a=0.5

def e(t):
    return np.exp(t)

plt.figure(figsize=(8,5), dpi=80)

plt.xlabel("t") 
plt.ylabel("x(t)=$e^{at}$") 
ax = plt.subplot(111)

ax.spines['right'].set_color('none')
ax.spines['top'].set_color('none')
ax.xaxis.set_ticks_position('bottom')
ax.spines['bottom'].set_position(('data',0))
ax.yaxis.set_ticks_position('left')
ax.spines['left'].set_position(('data',0))

x = np.arange(-3, 3, 0.1 )
y1=e(a*x)
y2=e(-a*x)
y3=e(0*x)
plt.plot(x, y1, color="blue", linewidth=1.5, linestyle="-", label="a>0")
plt.plot(x, y2, color="red",  linewidth=1.5, linestyle="-", label="a<0")
plt.plot(x, y3, color="green",  linewidth=1.5, linestyle="-", label="a=0")

plt.legend(loc='upper left')
plt.show()
