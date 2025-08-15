# Leetcode :rocket:
These are some of my solutions to Leetcode questions. As a Cybersecurity Education professional trying to become better at writing code and math, I will be using this repository to explain my thought processes, diagram my solutions, and explain the time complexity of each solution. For these solutions I will specifically be using Golang or Typescript to solve these solutions. If this is used as a reference you do not need to use Typescript or Golang to solve these problems because leetcode gives several other language options. 

## Big O Notation 
It is imperative to determine whether each algorithm we use to solve these problems is the "Best Approach" to address the leetcode problem. We can use Big O notation to determine whether the solution we came up with is actually effective for the problem we have solved. This notation allows us to determine whether a program will struggle in the most strunuous cases and where that struggle will likely occur. In my solutions we will delve into the time and space complexity of the solutions. 

### Time Complexity Calculation :hourglass:
Time complexity measures how the runtime of an algorithm scales with the size of its input, `n`.

1.  **Identify the Input**: First, determine what n represents. It's usually the size of the data structure you're working with, like the number of elements in an array.

2. **Count the Operations**: Count the number of basic operations the algorithm performs in terms of `n`. Focus on the operations inside loops, as they are typically the most significant.

    -   A single statement or a block of statements without loops is `O(1)` (constant time).
    -   A single loop that iterates n times is `O(n)` (linear time).
    -   A loop nested inside another loop, where both iterate n times, is `O(n^2)` (quadratic time).

3. **Simplify with Big O Rules**: Simplify the operation count to find the final Big O expression.

    -  *Find the Dominant Term*: Keep the term that grows the fastest. For example, in `n^2 + n`, the `n^2` term is dominant.

    -  *Drop Constants*: Remove any constant multipliers. For instance, `2n` becomes `O(n)`, and `4n^2` becomes `O(n^2)`.

### Space Complexity Calculation :milky_way:
Space complexity measures the extra memory an algorithm requires, not including the space taken up by the input itself. This extra memory is called auxiliary space.

1. **Identify Auxiliary Space**: Look for any new data structures or variables your algorithm creates. This includes variables, arrays, or objects created within the function.

2. **Measure Memory in Terms of**`n`: Determine how the size of that extra memory scales with the input size, n.

    -   `O(1)` **Space (Constant Space)**: The algorithm uses a fixed amount of memory, regardless of the input size. Creating a few simple variables falls into this category.

    -   `O(n)` **Space (Linear Space)**: The algorithm creates a new data structure whose size is proportional to the input size. For example, creating a copy of an input array of size n requires O(n) space.

    -   `O(log n)` **Space (Logarithmic Space)**: The extra memory grows logarithmically. This often occurs in recursive algorithms where the recursion depth is `log n`.

3. **Simplify with Big O Rules**: Just like with time complexity, drop any constants and non-dominant terms to find the final Big O expression.


## Diagramming :arrow_up_down:
Diagramming is an essential part to understanding the flow of data within an algorithm or short program. One thing I have not seen often when I look through Leetcode problems and solutions is diagramming to help undertand the high level flow and operation of an algorithm. So for this specific repository I will be using MermaidJS within my Markdown to demonstrate the logical flow of the Leetcode solutions. 

## Cybersecurity Tie In :necktie:
As a person working in Cybersecurity education it would not be fruitful to do all of this work building and working through Leetcode problems if I am not going to tie it back into the Cybersecurity industry. I will demonstrate where the logic in the Leetcode problems exists within the industry and I will show examples on this. 