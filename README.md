# push swap

  The project consists in the implementation of sorting algorithm for integers in a data structures; in this project it was required to work with a maximum of two stacks, stack A and stack B. At the beginning the stack A contains a random amount of negative and/or positive input numbers which cannot be duplicated and the stack B is empty. The goal is to sort in ascending order numbers into stack A. </br> </br>

## Rules:
  
  Only specific movements can be used to do this:
    
    • SA (swap A): Swap the first 2 elements at the top of stack A (Do nothing if there is only one or no elements).
    • SB (swap B): Swap the first 2 elements at the top of stack B (Do nothing if there is only one or no elements).
    • SS : SA and SB at the same time.
    • PA (push A): Take the first element at the top of B and put it at the top of A (Do nothing if B is empty).
    • PB (push C): Take the first element at the top of A and put it at the top of B (Do nothing if A is empty).
    • RA (rotate A): Shift up all elements of stack A by 1 (The first element becomes the last one).
    • RB (rotate B): Shift up all elements of stack b by 1 (The first element becomes the last one).
    • RR : RA and RB at the same time.
    • RRA (reverse rotate A): Shift down all elements of stack A by 1 (The last element becomes the first one).
    • RRB (reverse rotate b): Shift down all elements of stack B by 1 (The last element becomes the first one).
    • RRR : RRA and RRB at the same time.

 
  The algothm i chose to implement is the [Mechanical Turk](https://medium.com/@ayogun/push-swap-c1f5d2d41e97).
  
## Installing and running the project:

1- Clone the repo:
  
  ```sh
  git clone https://github.com/startaglia/push_swap.git push_swap
  ```

2- Enter in push_swap dir and compile the program with the `make` command
	
 ```
  cd push_swap
	make
 ```

3- Run the program and then insert the numbers you want to order.

	./push swap 32 12 76 999 -32 54 -61 -9

The program's output will be the moves order. There is a repo-visualizer to see the numbers movements. </br></br>
4- To check if the moves are correct we need a checker, before using it we have to give it the necessary permissions:
    
    for Linux: chmod +x checker_linux
    for Mac: chmod +x checker_mac

5- Now we could run the checker

    ./push_swap 54 43 32 21 | ./checker_linux 54 43 32 21
  
we expected `Error` if the move sequence is not correct or if there are double numbers

### Bonus part:
For the bonus part i recode my own checker:

1- Compile the bonus part :
  
    make bonus

2- Run with my checker :
  
    ./push_swap 54 43 32 21 | ./checker  54 43 32 21
 
### Makefile Available Targets:  
`make` or `make all` - Makes exe file 
`make clean` - Deletes all the resulting object files  
`make fclean` - Deletes the executables and all the resulting object files  
`make re` - fclean + all</br>
`make bonus` - rules for compile the bonus part if required
</br></br>

## Sources
  [Push Swap — A journey to find most efficient sorting algorithm](https://medium.com/@ayogun/push-swap-c1f5d2d41e97).</br>
   
## Technologies Used:

- **Programming Language**: C
- **Operating System**: Linux
- **Compiler**: GCC (GNU Compiler Collection)
- **Build System**: GNU Make
- **C Standard Library**
- **Process Management**: Implementation of Mechanical Turk sorting algorithm
- **Command Line Arguments Handling**: Techniques such as `argc`/`argv`

## Authors:

- **Simone Tartaglia**
  - Email: [startaglia89@gmail.com](mailto:startaglia89@gmail.com)
  - GitHub: [startaglia](https://github.com/startaglia)
  - LinkedIn: [Simone Tartaglia](https://www.linkedin.com/in/simone-tartaglia-134723248/)
