# Abstract :-
Our project involves a Verilog HDL simulation that replicates the logic of a vending machine. This simulation doesn't aim to build the complete vending machine structure. 
Instead, it focuses on the internal mechanisms such as user interaction, coin validation, product selection, and dispensing.

## 1. INTRODUCTION
 ### 1.1 INTRODUCTION OF THE PROJECT

- A vending machine is an automated machine that provides items such as snacks, beverages, and lottery tickets to consumers after cash, a credit card, or other form of payment is inserted into the machine or otherwise made.
- After payment has been tendered, a product may become available by:
- The machine releasing it, so that it falls in an open compartment at the bottom, or into a cup, either released first, or put in by the customer, or the unlocking of a door, drawer, or turning of a knob.
- Some products need to be prepared to become available. For example, tickets are printed or magnetized on the spot, and coffee is freshly concocted. One of the most common forms of vending machine, the snack machine, often uses a metal coil which when ordered rotates to release the product. The main example of a vending machine giving access to all merchandise after paying for one item is a newspaper vending machine (also called vending box) found mainly in the U.S. and Canada. It contains a pile of identical newspapers.

## 2. FINITE STATE MACHINE :-
- The finite state machines (FSMs) are significant for understanding the decision making logic as well as control the digital systems. In the FSM, the outputs, as well as the next state, are a present state and the input function. This means that the selection of the next state mainly depends on the input value and strength lead to more compound system performance. 
- As in sequential logic, we require the past inputs history for deciding the output. Therefore FSM proves very cooperative in understanding sequential logic roles. Basically, there are two methods for arranging a sequential logic design namely mealy machine as well as more machine. 4.1 What is an FSM (Finite State Machine)? The definition of a finite state machine is, the term finite state machine (FSM) is also known as finite state automation. FSM is a calculation model that can be executed with the help of hardware otherwise software. This is used for creating sequential logic as well as a few computer programs. FSMs are used to solve the problems in fields like mathematics, games, linguistics, and artificial intelligence. In a system where specific inputs can cause specific changes in state that can be signified with the help of FSMs. 4.2 Types of Finite State Machine The finite state machines are classified into two types such as
  
1. Mealy State Machine
2. Moore State Machine  

  ### 2.1.1 Mealy State Machine
  - When the outputs depend on the current inputs as well as states, then the FSM can be named to be a mealy state machine. The following diagram is the mealy state machine block diagram. The mealy state machine block diagram consists of two parts namely combinational logic as well as memory. The memory in the machine can be used to provide some of the previous outputs as combinational logic inputs.
  
  ![Mealy state machine BG](https://github.com/kesarsheth/Sequence-detector-Vending-Machine-/assets/131940649/b6f4f6e3-580b-4c5f-bd2e-97f056d9af19)

        Fig 1. Mealy State Machine Block Diagram

- Based on the current inputs as well as states, this machine can produce outputs. Thus, the outputs can be suitable only at positive otherwise negative of the CLK signal. The mealy state machine’s state diagram is shown below.

![mealy state machine state diagram](https://github.com/kesarsheth/Sequence-detector-Vending-Machine-/assets/131940649/4137379f-4265-4bce-bdd7-4fc345e67318)

      Fig 2. State Diagram of Mealy State Machine

- The state diagram of mealy state machine mainly includes three states namely A, B, and C. These three states are tagged within the circles as well as every circle communicates with one state. Conversions among these three states are signified by directed lines. In the above diagram, the inputs and outputs are denoted with 0/0, 1/0, and 1/1. Based on the input value, there are two conversions from every state. Generally, the amount of required states in the mealy machine is below or equivalent to the number of required states in Moore state machine. There is an equal Moore state machine for every Mealy state machine. As a result, based on the necessity we can employ one of them.

#### 2.1.2 Moore State Machine
- When the outputs depend on current states then the FSM can be named as Moore state machine. The Moore state machine’s block diagram is shown below. The Moore state machine block diagram consists of two parts namely combinational logic as well as memory. Fig

 ![moore state machine BG](https://github.com/kesarsheth/Sequence-detector-Vending-Machine-/assets/131940649/daa64f43-6fbc-41c6-b1fe-70f6279b15d6)
  
     Fig 3. Moore State Machine Block Diagram

- In this case, the current inputs, as well as current states, will decide the next states. Thus, depending on further states, this machine will generate the outputs. So, the outputs of this will be applicable simply after the conversion of the state. The Moore state machine state diagram is shown below. In the above state, the diagram includes four states like a mealy state machine namely A, B, C, and D. the four states as well as individual outputs are placed in the circles.

![moore state machine state diagram](https://github.com/kesarsheth/Sequence-detector-Vending-Machine-/assets/131940649/1d89c331-15b1-4b4b-a996-cb6738ae07ae)

        Fig 4. State Diagram of Moore State Machine

- In the above figure, there are four states, namely A, B, C & D. These states and the respective outputs are labeled inside the circles. Here, simply the input worth is marked on every conversion. In the above figure includes two conversions from every state depending on the input value. Generally, the amount of required states in this machine is greater than otherwise equivalent to the required number of states in the mealy state machine Generally, the number of required states in this machine is more than otherwise equivalent to the required states in MSM (Mealy state machine). For every Moore state machine, there is a corresponding Mealy state machine. Consequently, depending on the necessity we can utilize one of them. There is an equal mealy state machine for every Moore state machine. As a result, based on the necessity we can employ one of them.

### 2.2 Finite State Machine Applications:-
- The finite state machine applications mainly include the following.
-FSMs are used in games; they are most recognized for being utilized in artificial intelligence, and however, they are also frequent in executions of navigating parsing text, input handling of the customer, as well as network protocols.
-These are restricted in computational power; they have the good quality of being comparatively simple to recognize. So, they are frequently used by software developers as well as system designers for summarizing the performance of a difficult system.
- The finite state machines are applicable in vending machines, video games, traffic lights, controllers in CPU, text parsing, analysis of protocol, recognition of speech, language processing, etc.

### 2.3 Advantages of Finite State Machine:-
The advantages of Finite State Machine include the following.
• Finite state machines are flexible
• Easy to move from a significant abstract to a code execution
• Low processor overhead
• Easy determination of reachability of a state

### 2.4 Disadvantages of Finite State Machine:-
The disadvantages of the finite state machine include the following
• The expected character of deterministic finite state machines can be not needed in some areas like computer games
• The implementation of huge systems using FSM is hard for managing without any idea of design.
• Not applicable for all domains
• The orders of state conversions are inflexible.

## 3. STATE DIAGRAM

 ![state digarm V_Machine](https://github.com/kesarsheth/Sequence-detector-Vending-Machine-/assets/131940649/7fa6222c-653d-451c-80bb-cd0d48f3a300)

## 4. STATES TRANSITIONS
**S0 : 0 Rs in Vending Machine :–**

• if nothing added: Stay on State 0, OUTPUT = 0, CHANGE= 0.
• If 5 Rs added: Move to State 1, OUTPUT = 0, CHANGE = 0.
• If 10 Rs added: Move to State 2, OUTPUT = 0, CHANGE = 0.

**S1 : 5 Rs in Vending Machine :–**

• If nothing added: Here, This means the vending machine waited some time but no money was added signifying an incomplete transaction, thus the vending machine should return back the money added as CHANGE (5 Rs). No bottle given.
Move to State 0, OUTPUT = 0, CHANGE = Rs 5 (01).
• If 5 Rs added: Move to State 1, OUTPUT = 0, CHANGE = 0.
• If 10 Rs added: Adding 10 Rs means the vending machine now has 15 Rs total thus, a bottle will be returned with no CHANGE.
Move to State 0, OUTPUT = 1, CHANGE = Rs 0.

**S2 : 10 Rs in Vending Machine :–**

• If nothing added: Again, incomplete transaction thus vending machine returns the money added as CHANGE (10 Rs). No bottle given.
Move to State 0, OUTPUT = 0, CHANGE = Rs 10 (10). 
• If 5 Rs added: Signifies a complete transaction, a bottle is returned with no CHANGE.
Move to State 0, OUTPUT = 1, CHANGE = Rs 0. 
•If 10 Rs added: Here the customer over paid, thus a bottle should be returned but with CHANGE (5 Rs).
Move to State 0, OUTPUT = 1, CHANGE = Rs 5 (01)

## 5. SCHEMATIC DIAGRAM

![schemetic diagram](https://github.com/kesarsheth/Sequence-detector-Vending-Machine-/assets/131940649/93fdbb44-53cb-4c85-af97-797cb2b96b03)


## 6. RESULTS

     Fig 1. ADDING 5 RS THREE TIMES CONSECUTIVELY

  ![adding 3Time's 5RS](https://github.com/kesarsheth/Sequence-detector-Vending-Machine-/assets/131940649/e0aac825-4c69-4030-943e-bd0cb25514e0)


     Fig 2. ADDING 5 RS AND THEN 10 RS

 ![Adding 5RS   10RS](https://github.com/kesarsheth/Sequence-detector-Vending-Machine-/assets/131940649/b3933a27-14e1-4973-b15c-334a2b2eb580)


     Fig 3. ADDING 10 RS TWO TIMES

 ![adding 10 RS TWO times](https://github.com/kesarsheth/Sequence-detector-Vending-Machine-/assets/131940649/5ae199ca-62cc-4613-b688-c89e6aa20d65)


    Fig 4. ADDING 5 RS AND THEN NOTHING

 ![Adding 5RS   then nothing](https://github.com/kesarsheth/Sequence-detector-Vending-Machine-/assets/131940649/c35aaea0-2483-42be-86af-df800c64de02)


     FIG 5. ADDING 10 RS AND THEN NOTHING

  ![adding 10RS   nothing](https://github.com/kesarsheth/Sequence-detector-Vending-Machine-/assets/131940649/6b291485-7229-44a3-8785-b4f8ae0b9ad8)


## 7. CONCLUSION
- We successfully implemented a software simulation of a vending machine. This endeavor allowed us to understand the intricacies of digital system emulation and provided hands-on experience in creating a functioning simulation.
Properly controlling the transitions between states within our virtual vending machine was critical to accurately emulate real-world vending machine behavior.
- Through this project, we've not only learned about Verilog but also gained insights into the complexities of designing and simulating real-world systems. It underscores the importance of thorough testing, verification, and the potential for future advancements in vending machine technology. Our understanding of digital design practices has grown significantly.
