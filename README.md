# AI-Based_Number_Guessing_Game

## Problem Statement
The AI-based Number Guessing Game is a simple yet efficient implementation of a searching algorithm. The goal of the game is to enable an AI to correctly guess a randomly chosen number within a given range (e.g., 1 to 100) using the **Binary Search Algorithm**. Instead of making random guesses, the AI follows a structured approach to minimize the number of attempts needed to find the correct number.

## Approach and Explanation
### 1. **Understanding the Problem**
- A random number is generated within a specific range.
- The AI has to guess this number using an efficient approach.
- Feedback is provided to the AI after each guess:
  - "Too High" → The AI should guess a lower number next time.
  - "Too Low" → The AI should guess a higher number next time.
  - "Correct" → The game ends successfully.

### 2. **Optimal Strategy: **
- The AI starts by selecting the **middle number** of the given range.
- If the guessed number is **correct**, the game ends.
- If the guess is **too high**, the AI eliminates the upper half and focuses on the lower range.
- If the guess is **too low**, the AI eliminates the lower half and focuses on the upper range.
- The process repeats until the AI finds the correct number.

### 3. **Example Execution**
Let's assume the randomly chosen number is **42**.

| Attempt | AI Guess | Feedback | New Range |
|---------|---------|----------|-----------|
| 1       | 50      | Too High | [1, 49]   |
| 2       | 25      | Too Low  | [26, 49]  |
| 3       | 37      | Too Low  | [38, 49]  |
| 4       | 43      | Too High | [38, 42]  |
| 5       | 40      | Too Low  | [41, 42]  |
| 6       | 41      | Too Low  | [42, 42]  |
| 7       | 42      | Correct! | -         |

The AI successfully finds the number in just **7 attempts**!

### 4. **Complexity Analysis**
Since the AI is halving the search space at each step, the time complexity of this approach is **O(log N)**, making it highly efficient. For example:
- A range of **1 to 100** requires at most **7 guesses**.
- A range of **1 to 1,000,000** requires at most **20 guesses**.

### 5. **Possible Enhancements**
- Allow the **user** to choose a number while the AI tries to guess it.
- Implement a **GUI-based version** using Python’s Tkinter or Pygame.
- Add difficulty levels by modifying the range of numbers.

## Conclusion
The AI-based Number Guessing Game demonstrates how simple algorithms can make intelligent decisions efficiently. 
---
**Technologies Used:** Python, Random Module, Binary Search Algorithm


