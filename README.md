# CI2024_Lab1
## Lab1 - Set Cover
Given a family of sets, find the subfamily of minimum cost that covers all elements in the universe.\
Solve efficiently these instances customizing a technique discussed.

| Instance | Universe size | Num sets | Density |
|----------|---------------|----------|---------|
| 1        | 100           | 10       | 0.2     |
| 2        | 1,000         | 100      | 0.2     |
| 3        | 10,000        | 1,000    | 0.2     |
| 4        | 100,000       | 10,000   | 0.1     |
| 5        | 100,000       | 10,000   | 0.2     |
| 6        | 100,000       | 10,000   | 0.3     |

## Description 
The algorithm is based on *Hill climbing*. My agent prioritizes improving the current solution. However, in case ther is no improvement, it use all three tecniques to escape the local maxima: **simulated annealing**,  the temperature increases x1.2 times, every time we have no improvement, while doing the square root when there is an improvement; **steepest step**, 10 solution explored in the neighbourhood, then select the best one; **Iterated Local Search**, restart the process from a new position obtained shaffling the best solution so far.

## Performance
The following table shows some sample performance; all solutions are valid. **The number of steps has been fixed to 10000 in every instance.** \
The solution's cost is reported positive, so the lower the better, while during the execution the cost is considered negative. In the process we search always for the maximization.

As we can see from the plot, for the 5-th istances there still room for improvement.

| Instance | Universe size | Num sets | Density |  Cost of solution |
|----------|---------------|----------|---------|----------|
| 1        | 100           | 10       | 0.2     |   283.74556873583543   |
| 2        | 1,000         | 100      | 0.2     |   7492.50920532134    |
| 3        | 10,000        | 1,000    | 0.2     |   179201.05125665627    | 
| 4        | 100,000       | 10,000   | 0.1     |    47446550.337716416      | 
| 5        | 100,000       | 10,000   | 0.2     |          | 
| 6        | 100,000       | 10,000   | 0.3     |          | 