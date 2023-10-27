# Here is my HackerRank Solutions

>The repository contains the solutions to various HackerRank problems. Each solution includes a reference to the problem statement and is well-documented to explain the logic and approach.



## Solution Approach

>In the "Solution Approach" section, provide a detailed explanation of your approach to solving the problem. Describe the algorithm, data structures, and any key insights that led to your solution. This helps others understand your thought process and learn from your solutions.

### Problem 1


  - [Problem](https://www.hackerrank.com/challenges/angry-children/problem)(navigate to the Problem)
  - [Solution](https://github.com/Ashif-coder/HackerRank_Solution_20k-10k/blob/main/Max-Min) (navigate to the Solution file)
  - Explanation:
  - Sort the input array arr in ascending order.
  - Initialize the min_unfairness to positive infinity.
  - Iterate through the sorted array and calculate the unfairness for each possible subarray of length k.
  - Update min_unfairness with the minimum unfairness found during the iterations.
  - Return the min_unfairness as the result, which represents the minimized unfairness when choosing a subarray of length k from the sorted array.
  
### Problem 2

  - [Problem](https://www.hackerrank.com/challenges/largest-permutation/problem)(navigate to the Problem)
  - [Solution](https://github.com/Ashif-coder/HackerRank_Solution_20k-10k/blob/main/largest_permutation)(navigate to the Solution file)
  - Explanation:
1. The function `largestPermutation` takes two parameters: `k` (the maximum number of swaps allowed) and `arr` (the input array).
2. It calculates the length of the array `n` and initializes a dictionary `index_map` where each element in the array is a key, and the value is the index of that element in the array. This dictionary allows for quick lookups of an element's index.
3. `largest_num` is initialized to `n`, which is the largest number that can be in the array.
4. The code enters a loop to perform swaps and build the largest permutation. It continues until either `k` becomes zero or the loop reaches the end of the array.
5. Inside the loop, the current number is stored in the `current_num` variable from the `arr[i]`.
6. It checks if the `current_num` is not equal to the `largest_num`. If they are not equal, it means the current number is not the largest in the array, so a swap is needed to make it the largest. 
7. The swap involves updating the `arr` by setting `arr[i]` to the `largest_num` and updating the index of `current_num` to point to the index where the `largest_num` used to be. This effectively swaps the current number with the largest number.
8. The dictionary `index_map` is updated to reflect the new indices of `current_num` and `largest_num`.
9. `k` is reduced by 1 since a swap has been performed.
10. `largest_num` is decremented by 1 to keep track of the next largest number to be swapped in the subsequent iterations.
11. The loop continues until either `k` is zero or the loop reaches the end of the array.
12. Finally, the function returns the modified array, which is the largest permutation possible after making the required swaps.
if `k` is 2 and `arr` is `[4, 2, 3, 5, 1]`, the function will swap the two largest elements to create the largest possible permutation. The output will be the largest permutation of the array.

### Problem 3


  - [Problem](https://www.hackerrank.com/challenges/pylons/problem?isFullScreen=true)(navigate to the Problem)
  - [Solution](https://github.com/Ashif-coder/HackerRank_Solution_20k-10k/blob/main/goodland%20electricity) (navigate to the Solution file)
  - Explanation:
1. `result` is initialized to 0. This variable will keep track of the number of power plants needed to cover all cities optimally.
2. `i` is initialized to 0. This variable represents the index of the current city being considered.
3. The code enters a `while` loop that runs as long as `i` is within the bounds of the array `arr`.
4. `benefited` is initialized to `False`. It's used to track whether a city `i` can be benefited by a power plant.
5. Inside the loop, a nested `for` loop iterates through a range of indices. The range starts from `i + k - 1` and goes backward to `i - k`. This represents a search window around the current city `i`, with a width of `2k - 1`.
6. The code checks if the index `j` is within the bounds of the array `arr` and if the city at index `j` is already powered (i.e., `arr[j] == 1`). If these conditions are met, it means a power plant can benefit the city at index `i`.
7. If a powered city is found within the search window, `result` is incremented by 1, indicating that a power plant is placed at the current city `i`. The variable `i` is then updated to the index `j + k`, moving to the farthest right city that can be benefited within the availability range.
8. The `benefited` flag is set to `True`, indicating that a city within the range can be powered.
9. The `break` statement is used to exit the inner `for` loop because the farthest right city within the availability range has been found.
10. After the inner loop, there's a check to see if `benefited` is still `False`. This means that no city within the range can be powered, and as a result, the function returns -1, indicating that it's impossible to power all cities under the given constraints.
11. If a city within the range was benefited, the outer `while` loop continues, and the process is repeated for the next city.
12. Finally, when the `while` loop finishes, the function returns the value of `result`, which represents the minimum number of power plants needed to cover all cities optimally.

### Problem 4


  - [Problem](https://www.hackerrank.com/challenges/coin-change/problem?isFullScreen=true)(navigate to the Problem)
  - [Solution](https://github.com/Ashif-coder/HackerRank_Solution_20k-10k/blob/main/the_coin_change_proplem) (navigate to the Solution file)
  - Explanation:
1. Initialize a list ways with zeros, where each index represents an amount from 0 to n.
2. There is one way to make change for the amount 0, which is by not using any coins. Therefore, set ways[0] = 1.
3. Iterate through each coin denomination in the list c.
4. For each coin, update the ways list to calculate the number of ways to make change for each amount from the coin value to n. This is done by adding the number of ways to make change for amount - coin to the number of ways to make change for amount.
5. The last element of the ways list, ways[n], contains the number of ways to make change for the given amount.

### Problem 5


  - [Problem](https://www.hackerrank.com/challenges/sherlock-and-anagrams/problem)(navigate to the Problem)
  - [Solution](https://github.com/Ashif-coder/HackerRank_Solution_20k-10k/blob/main/sherlock_anagram) (navigate to the Solution file)
  - Explanation:
1. Initialize a dictionary substring_freq to store the frequency of substrings as sorted tuples.
2. Initialize a count variable to keep track of the number of anagram pairs.
3. Iterate through all possible substrings in the input string s. For each substring, sort its characters, and convert the sorted substring into a tuple.
4. Increment the frequency of the sorted substring in the substring_freq dictionary.
5. After processing all substrings, loop through the values in substring_freq and count the number of anagram pairs using the formula (freq * (freq - 1)) // 2, where freq is the frequency of a sorted substring.
6. Return the total count, which represents the number of unordered anagrammatic pairs of substrings in the string.

### Problem 6


  - [Problem](https://www.hackerrank.com/challenges/the-quickest-way-up/problem)(navigate to the Problem)
  - [Solution](https://github.com/Ashif-coder/HackerRank_Solution_20k-10k/blob/main/snakes_and_ladder) (navigate to the Solution file)
  - Explanation:
1. Two dictionaries, ladder_map and snake_map, are created to represent the start and end points of ladders and snakes. This allows for easy lookup of where a ladder takes you and where a snake sends you.
2. The visited set is initialized to keep track of the cells that have already been visited. This is essential to avoid revisiting cells and potentially entering into an infinite loop.
3. A queue called queue is set up for performing a breadth-first search (BFS). The queue initially contains a tuple (1, 0), where the first element represents the current cell (starting at cell 1), and the second element represents the number of moves (initially 0).
4. The main loop runs as long as there are cells in the queue to explore.
5. Inside the loop, it dequeues the first element of the queue, which represents the current cell and the number of moves taken to reach that cell.
6. The code checks if the current cell is cell 100 (the destination). If it is, the function returns the number of moves taken to reach cell 100.
7. The code simulates rolling a fair 6-sided die by looping through possible roll values from 1 to 6.
8. For each roll, a new_cell is calculated by adding the roll value to the current cell.
9. The code checks if the new_cell is within bounds (i.e., less than or equal to 100). This ensures that the player doesn't move beyond the end of the board.
10. If the new_cell is on a ladder, it checks if new_cell is in the ladder_map. If it is, the player moves to the ladder's end point specified in the ladder_map.
11. If the new_cell is on a snake, it checks if new_cell is in the snake_map. If it is, the player moves to the snake's end point specified in the snake_map.
12. The code then checks if the new_cell has been visited before. If it hasn't, it adds the new_cell to the visited set, and a tuple (new_cell, moves + 1) is added to the queue, where moves + 1 represents the incremented number of moves.
13. This process continues until the BFS explores all possible paths or until the destination (cell 100) is reached.
14. If there is no way to reach cell 100 after exploring all possible paths, the function returns -1, indicating that it's impossible to reach the destination.





