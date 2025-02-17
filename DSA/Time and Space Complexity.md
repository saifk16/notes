
Algorithmic complexity
time complexity and space complexity

#Note 
Time complexity is a way to analyze an algorithm's efficiency by measuring how the number of operations grows as the input size increases (n).

three different notations
- BIG - O #Worst refers to the behavior of an algo in worst case scenario
- BIG - Ω #Best  (Omega) best case scenario
- BIG - Θ #Average  (Theta) average case scenario 

Common Complexities
- Linear - O(n)
- Constant - O(1)
- Quadratic - O(n<sup>2</sup>)
- Exponential - O(2<sup>n</sup>)
- Logarithmic - O(log n)

```mermaid
--- 
config:
 themeVariables: 
  xyChart: 
   backgroundColor: "#000000"
   titleColor: "#ff7777" 
   xAxisLabelColor: "#ffffff" 
   xAxisTitleColor: "#ffffff" 
   xAxisTickColor: "#ffffff"
   xAxisLineColor: "#ffffff" 
   yAxisLabelColor: "#ffffff" 
   yAxisTitleColor: "#ffffff" 
   yAxisTickColor: "#ffffff"
   yAxisLineColor: "#ffffff" 
   plotColorPalette: "#00ff00" 
---

xychart-beta
  title "Constant O(1)"
  x-axis "Input (n)" [100, 200, 300, 400, 500, 600, 700, 800, 900, 1000]
  y-axis "Time" 0 --> 4.5
  line [1, 1, 1, 1, 1, 1, 1, 1, 1, 1]
```