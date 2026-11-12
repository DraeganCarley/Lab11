# Lab11
# Lab 11 - Counters and Dividers


In this lab, we learned how to make clock dividers from two types of counters.


## Rubric


| Item | Description | Value |
| ---- | ----------- | ----- |
| Summary Answers | Your writings about what you learned in this lab. | 25% |
| Question 1 | Your answers to the question | 25% |
| Question 2 | Your answers to the question | 25% |
| Question 3 | Your answers to the question | 25% |


## Names
Group 7 - Aaron Ray and Draegan Carley
## Summary
In this lab, we learned how to use modulo counters and ripple counters to divide clock signals into lower frequencies. We learned that modulo counters use D-flip-flops, adders, and a comparator to count to a specific value before resetting. Ripple counters use T-flip-flops connected together, with each one dividing the clock frequency by 2. We also learned how to add reset pins to our flip-flops and how these counters can be used to slow down clock signals.


## Lab Questions


### 1 - Why does the Modulo Counter actually divide clocks by 2 * Count?
The modulo counter divides the clock by 2 times the count because it toggles its output every time it reaches the set count. Since it takes two toggles to complete a full clock cycle, it has to count twice. For example, our modulo counter counts to 6, so it takes 12 clock cycles to complete one full output cycle.


### 2 - Why does the ripple counter's output go to all 1s on the first clock cycle?
In our ripple counter, each T-flip-flop toggles its output when it receives the correct clock edge. If the counter starts at 000, the first clock pulse can cause all three flip-flops to toggle to 1 as the changes ripple through the circuit. This depends on how the flip-flops are connected and which clock edge they respond to.


### 3 - What width of ripple counter would you use to get to an output of ~1KHz?
Since the Basys 3 board has a 100 MHz clock, we would need to divide it by about 100,000 to get 1 KHz. Each T-flip-flop divides the frequency by 2, so we can use 17 flip-flops to get approximately 763 Hz. This would be the closest we could get to 1 KHz using a ripple counter.
