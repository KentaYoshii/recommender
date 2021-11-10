# README

## Introduction
This code is a simple implementation of the REPL that takes in a command and outputs the result. The allowed commands and their syntax are:

### _**command**_
- **`add num1 num2`** -- returns the sum of two numbers
- **`subtract num1 num2`** -- returns the result of num2 - num1
- **`stars path/to/file`** -- loads star data (in csv file format) that contains the name of the star, its distance from a certain point.
- **`naive_neighbors k x y z`** -- finds the nearest k stars given the starting <x,y,z> coords
- **`naive_neighbors k star`** -- finds the nearest k stars from the star in arg
- **`API path/to/file`** -- loads in the data in the file path and creates javaobj instances
- **`API <datatype> path/to/URI(S)`** -- API aggregator that finds the best combination of API calls and return the corresponding instances
- **`recommend src x`** -- recommend the best x matches given the source

## Implementation
The implementation of this code can be divided into three parts:
**Data retrieval**, **REPL commands**, and **Algorithms/Data Structure**.

### Data Retrieval
- We retrieve the data by using the `API` command. Given various endpoints, we make a API request and return the result in Json format. We then map that into a Java object and store it in a ArrayList. 
- Another method we use is querying into the database. We use SQL commands to query the database and return the result.

### REPL commands
- The REPL commands are the list of commands stated above. 
- To make the code cleaner, we used triggerAction interface that have a general methods that all commands have (such as execute()).
- Thereafter, we create a class for each command that implements the triggerAction interface.

### Algorithms/Data Structure
- The algorithms/data structure we used for this code is k-d tree. Where each at each depth you compare different attribute of the tree nodes.
- This allowed us to compare different attributes of the user input and return the best matches.


