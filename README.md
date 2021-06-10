#!/usr/bin/env python
# coding: utf-8

# In[2]:


import matplotlib.pyplot as plt
import numpy as np


# In[3]:


get_ipython().run_line_magic('matplotlib', 'notebook')


# In[5]:


xmin = input('Xmin=')


# In[6]:


xmin = int(xmin)


# In[7]:


xmax = input('Xmax=')


# In[8]:


xmax = int(xmax)


# In[9]:


xmin = -2*np.pi
xmax = 2*np.pi


x = np.arange(xmin , xmax , 0.1)

y1 = -np.sin(x)*np.cos(x)
y2 = np.sin(x)/x


# In[10]:


x


# In[11]:


get_ipython().run_line_magic('matplotlib', 'Notebook')

plt.figure(figsize = (10,5))
plt.xlabel('X')
plt.ylabel('Y')
plt.plot(x,y1,'-.',lw=2) 
#1st term is x defined in above box
#2nd term is y defined in above box
#3rd term is '-' defines the view of graphic signal.
#4th term is line width.

plt.show()


# In[12]:


get_ipython().run_line_magic('matplotlib', 'Notebook')

plt.figure(figsize = (10,5))
plt.xlabel('X')
plt.ylabel('Y')
plt.title("Two functions in one graph")
plt.plot(x,y1,'-.',lw=2)
plt.plot(x, y2, '+' , lw=2)
#1st term is x defined in above box
#2nd term is y defined in above box
#3rd term is '-' defines the view of graphic signal.
#4th term is line width.

plt.grid()
plt.show()
plt.savefig("twofunc.pdf")


# # Plotting Subplots 

# In[17]:


xmin=-5; xmax=5; Npoints=500
dx = (xmax-xmin)/Npoints

x1 = np.arange(xmin, xmax, dx)
x2 = np.arange(xmin, xmax, dx/20)

y1 = -np.sin(x1)*np.cos(x1*x1)
y2 = np.exp(-x2/4)*np.sin(x2)

y3 = np.exp(-x1**2/4)
y4 = np.log(x2)


# In[24]:


get_ipython().run_line_magic('matplotlib', 'Notebook')

plt.figure(1,figsize = (10,5))
#plt.figure(1)
plt.subplot(2,2,1)
plt.plot(x1,y1,'r',lw=2)
plt.show()

#plt.figure(figsize = (10,5))
#plt.figure(2)
plt.subplot(2,2,2)
plt.plot(x2,y2,'-',lw=2)
plt.show()

plt.subplot(2,2,3)
plt.plot(x1,y3, '.-',lw=2)
plt.show()

plt.subplot(2,2,4)
plt.plot(x2, y4, '-',lw=2)
plt.show()


# In[ ]:




