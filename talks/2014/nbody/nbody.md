
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
