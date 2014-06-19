
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

1. What is Lua?
- Embeddable scripting language
- Interpreted bytecode runs on VM

2. Why do we use it?
- Powerful C API for exhanging data between lua script and C program
- 

--

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
