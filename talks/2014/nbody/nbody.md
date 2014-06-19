
class: center, middle

# Milkyway@Home N-Body

---

# Overview

1. 2D Histograms
2. Lua Integration

---

# Introduction

---

# Lua Integration

##1. What is Lua?
- Embeddable scripting language
- Interpreted bytecode runs on VM
- C API for exchanging data

##2. Why do we use it?
- Small footprint
- Easy to embed in our application
- Allows complete control of intial state

---

# Lua Integration

##3. How does it work?
- Lua file is downloaded along with the nbody binary
- Lua file contains several functions required for setting up the simulation
- milkyway_nbody is executed, initializing a lua intepreter and loading the lua script specifed with the -f argument

---

# Forwarded Arguments

```bash
x1arch% milkyway_nbody -e 0 -f EMD_10k_isotropic2.lua -z out.hist  2 1 1 0.5 10 0.5
```

Command line arguments unused by milkyway_nbody are forwarded to the lua script, and can be accessed as command line arguments within the lua script.

```lua 
evolveTime       = arg[1]
reverseOrbitTime = arg[1] / arg[2]
r0  = arg[3]
light_r_ratio = arg[4]
```

This is used by BOINC to pass the work unit parameters to the application

---

```lua
function makeHistogram()
   return HistogramParams.create{
     phi = 128.79,
     theta = 54.39,
     psi = 90.70,
     lambdaStart = -50,
     lambdaEnd = 50,
     lambdaBins = 50,
     betaStart = -25,
     betaEnd = 25,
     betaBins = 50 
}
end
```
