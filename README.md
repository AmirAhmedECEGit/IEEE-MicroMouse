# IEEE-MicroMouse
we are a team of engineers that dedicated our time to solving a challenge concerning maze solver of an unknown maze based on both embedded systems and AI

## Design flow and tasks
### 0- universal internal peripherals modules (MCAL)
    all designers are submitting to a certain preference of internal modules.
    this includes GPIO modules, Standard macros, and some other 
    needed internal peripherals like timers and delays.
### 1- Power and Voltage regulators
    Designer of this stage is responsible for determining the needed power for motors.
    He is also responsible for designing a voltage regulator circuit that can provide
    for microcontroller voltage and other 5V devices.
    He is responsible for power tracks on PCB and layout.
### 2- Motors/Motor drivers (HAL)
    Designers in this stage are responsible for creating a hardware abstraction layer
    between motors and degrees of motion.
    This is done by choosing motor types then motor drivers then understanding the mechanism
    of rotation and writing a driver module for different types of motion
    (rotating right, rotating left, moving forward, rotate 180')
### 3- Sensors and Transmitters (HAL)
    Designers of this stage are responsible for choosing sensor types based on maze description.
    then writing driver modules for sensors and creating an abstraction layer so that
    later on we can check on sensors in main program easily.
    The driver/module should contain function that gets reading of 1 sensor at a time.
    then we can use time multiplexing to get 3 readings at nearly same time.
    then the function should indicate the surrounding environment somehow in its returned values. 
### 4-  AI Solver (Main Application)
   The team should first write a function based on sensors that indicates whether
   the current position in maze needs "taking action" or "Decision" or not.
   such function will be essential in decision making later on as 
   each decision represents a node in graph.
   
   Designers of this stage should be familiar with AI, Graph, and maze-solving algorithms.
   The main application can be divided into two main functions. one of them is the "discovery"
   function which can scan maze and know its locations then create a graph data, it should have
   some sort of positioning (N,S,E,W) to solve for complicated algorithms as maze loops.
   it should be able to adapt graph data, delete, edit, then export the graph in sort of an array.
   
    other function is the "follower" function which will take the array from previous
    function then follows it each time it faces a decision making chance.





    EECE2024    MAKE THE DIFFERENCE, LEAVE A TRACE
