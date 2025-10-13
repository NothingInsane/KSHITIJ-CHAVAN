# Key Concepts in STA

## Setup and Hold Checks :

### Setup Time :-
It is the minimum time a data signal must be stable before the active clock edge to be reliably captured by a flip-flop. A setup violation occurs when the data arrives too late, missing the setup window. This is also known as a max time violation. <br>

### Hold Time : 
It is the minimum time a data signal must be stable after the active clock edge. A hold violation occurs when the data signal changes too soon after the clock edge, which can corrupt the data. This is also known as a min time violation.

<img width="1063" height="388" alt="image" src="https://github.com/user-attachments/assets/7c12ee9f-3243-412c-ad15-cb6459a0b65c" />

## Slack :-

**Slack** is the difference between the required arrival time (RAT) and the actual arrival time (AAT) of a signal at a node in a circuit. It tells you how much "margin" a path has.

A **positive slack** means the timing constraint is met, with the signal arriving earlier than required.

A **negative slack** indicates a timing violation, meaning the signal arrived too late. The path must be sped up to fix this violation.

<img width="374" height="135" alt="image" src="https://github.com/user-attachments/assets/075faedc-1cab-49af-b35a-ab8df3ae3180" />

## Clock Definitions :-

**Clock Skew** is the difference in the arrival time of the clock signal at two different sequential elements. It is caused by varying path lengths in the clock network.

**Clock Latency** is the total delay from the ideal clock source to a flip-flop's clock pin. It is the sum of source latency (delay from the clock origin) and network latency (delay through the clock distribution network).

**Clock Uncertainty** is the deviation of the actual clock edge from its ideal time, often due to factors like jitter (temporal fluctuations).

<img width="574" height="298" alt="image" src="https://github.com/user-attachments/assets/a40ee9eb-01da-446f-8e9c-8646bffa34a8" />

## Path Based Analysis :-

Most STA tools use a fast but often pessimistic **Graph-Based Analysis (GBA)** first.

**Path-Based Analysis (PBA)** is a more accurate method used to reduce this pessimism. It is slower than GBA but calculates delays by propagating path-specific timing information, which provides a more precise slack value.

<img width="1213" height="325" alt="image" src="https://github.com/user-attachments/assets/c25da434-116a-45e6-ba3c-71d6e98bdbbf" />

This was what I inculcated from the provided course and would look forward to learn the STA in detail .
