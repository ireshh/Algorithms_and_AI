# Project Specification: Heads-Up Poker AI

**Degree Program**: Bachelor of Science (BSc)  
**Project Language**: Python  
**Project Documentation Language**: English

---

## Project Overview

The purpose of this project is to develop an AI agent that can play a simplified two-player (heads-up) version of Texas Hold'em Poker. The AI will evaluate hand strength, calculate probabilities, and utilize strategies that include bluffing and reacting dynamically to the opponent’s moves. This project will use probability-based decision-making and basic pattern recognition to simulate realistic and competitive poker play.

## Problem Definition

This project addresses the challenge of developing an AI for heads-up poker that can make competitive, intelligent decisions in real time. The AI will need to:
1. **Analyze Hand Strength**: Evaluate the potential of the AI’s hand against possible community cards.
2. **Calculate Winning Probabilities**: Assess the likelihood of winning based on current hand strength and potential outcomes.
3. **Incorporate Adaptive Strategy**: Implement strategic elements like bluffing and opponent modeling to counter human-like or pre-programmed opponents effectively.

## Inputs and Usage

The program will receive the following inputs:
- **Card Deal Information**: The initial two cards dealt to the AI and the subsequent community cards (flop, turn, river).
- **Game State Data**: Current bets, actions taken by the opponent (bet, call, fold, raise), and remaining chips.
- **Opponent Action History**: Track previous moves by the opponent to model their behavior (e.g., likelihood of bluffing, calling frequency).

These inputs will be used to:
1. **Calculate Hand Strength**: Assess whether the AI’s hand is likely to win based on probability.
2. **Decide on Moves**: Use a decision tree to evaluate betting, calling, folding, or raising.
3. **Adapt Strategy**: Adjust decisions based on observed opponent tendencies, such as bluffing or conservative play.

## Algorithms and Data Structures

This project will implement the following algorithms and data structures:

1. **Monte Carlo Simulation**:
   - **Purpose**: Used to calculate winning probabilities by simulating potential outcomes based on the community cards and AI’s hand.
   - **Complexity**: Estimated time complexity \(O(N \cdot S)\), where \(N\) is the number of simulations and \(S\) the average number of states evaluated per simulation.

2. **Decision Tree for Move Selection**:
   - **Purpose**: Based on the game state, this decision tree will evaluate the optimal move by weighing probabilities, hand strength, and game context.
   - **Complexity**: Expected time complexity is approximately \(O(d)\), where \(d\) is the depth of decision evaluations per move.

3. **Opponent Modeling**:
   - **Purpose**: A simple tracking model that records opponent behavior (e.g., fold, call, raise frequencies) to help predict future actions.
   - **Data Structure**: Dictionary-based history tracking for frequencies of opponent actions.
   - **Complexity**: Expected time complexity \(O(1)\) for recording actions and constant space complexity \(O(c)\), where \(c\) is the constant number of possible opponent actions.

4. **Bluffing Mechanism**:
   - **Purpose**: Introduces a probabilistic model to occasionally simulate bluffing and create a less predictable AI. This is based on a probability threshold, which can change based on the game context.
   - **Data Structure**: Randomized probability thresholding.
   - **Complexity**: Constant time \(O(1)\) for bluff decisions.

## Desired Time and Space Complexities

- **Monte Carlo Simulation**: \(O(N \cdot S)\) time complexity, where \(N\) is the number of simulations and \(S\) is the average number of states per simulation. This could potentially require large memory if extensive simulations are conducted.
- **Decision Tree for Move Selection**: Target time complexity \(O(d)\), assuming limited tree depth for efficient move selection.
- **Opponent Modeling and Bluffing**: Expected time complexity \(O(1)\) per recorded action, with low space complexity \(O(c)\), where \(c\) represents possible opponent actions.

## References

1. Billings, D., Burch, N., Davidson, A., Holte, R., Schaeffer, J., Schauenberg, T., & Szafron, D. (2003). *Approximating Game-Theoretic Optimal Strategies for Full-scale Poker*. University of Alberta.
2. Johanson, M. (2007). *Robust Strategies and Counter-strategies: Building a Champion Level Computer Poker Player*. University of Alberta.
3. Monte Carlo Method – [Monte Carlo Simulation Explanation](https://en.wikipedia.org/wiki/Monte_Carlo_method).
4. Texas Hold'em Probability Calculations – [Poker Hand Probabilities](https://en.wikipedia.org/wiki/Poker_probability).

---

This document outlines the scope, methodologies, and key algorithms for the project. Feedback would be appreciated.
