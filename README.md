# cis165-lab3
  diamond.cpp   game_time.cpp   README.md   AI_REFLECTION.md
CIS-165 Lab 3 — C++ Output and Time Calculations
Name: Jessica Carver
Course Section: CIS-165-W099

Initial Plan
Diamond Pattern
I will create the diamond using seven separate cout statements. Each statement will print one line of the required pattern. I will use spaces before the asterisks to center each line. The number of asterisks will increase from one to three to five to seven and then decrease back to five, three, and one.

Video Game Level Times
I will store 78 minutes for Level 1 and 144 minutes for Level 2 in named integer variables. I will use integer division by 60 to calculate hours and the remainder operator to calculate the remaining minutes. I will calculate the difference between the two levels and convert that difference into hours and minutes before displaying the results.

Compile and Run
diamond.cpp
g++ -std=c++17 -Wall -Wextra diamond.cpp -o diamond
./diamond

game_time.cpp
g++ -std=c++17 -Wall -Wextra game_time.cpp -o game_time
./game_time

## Testing
| Program/test | Values or pattern checked | Expected result before running | Actual output | Match or correction |
|---|---|---|---|---|
| `diamond.cpp` | Seven required lines | 3, 2, 1, 0, 1, 2, 3 leading spaces and 1, 3, 5, 7, 5, 3, 1 asterisks | Seven-line diamond matched the required pattern | Match; no correction was necessary |
| `game_time.cpp` — assigned values | Level 1 = 78 minutes; Level 2 = 144 minutes | Level 1 = 1 hour, 18 minutes; Level 2 = 2 hours, 24 minutes; Difference = 1 hour, 6 minutes | Level 1 time: 1 hours and 18 minutes; Level 2 time: 2 hours and 24 minutes; Level 2 took longer by: 1 hours and 6 minutes | Match |
| `game_time.cpp` — changed values | Level 1 = 125 minutes; Level 2 = 250 minutes | Level 1 = 2 hours, 5 minutes; Level 2 = 4 hours, 10 minutes; Difference = 2 hours, 5 minutes | Level 1 time: 2 hours and 5 minutes; Level 2 time: 4 hours and 10 minutes; Level 2 took longer by: 2 hours and 5 minutes | Match | 


Final Rerun
The assigned values were restored to:

int level_one_minutes = 78;
int level_two_minutes = 144;

Final diamond.cpp output:

   *
  ***
 *****
*******
 *****
  ***
   *

Final game_time.cpp output:

Level 1 time: 1 hours and 18 minutes
Level 2 time: 2 hours and 24 minutes
Level 2 took longer by: 1 hours and 6 minutes

The assigned values were restored and both programs completed their final runs.

Code Explanation
diamond.cpp
The program uses seven separate cout statements to create the seven lines of the diamond. Each line contains a specific number of spaces followed by a specific number of asterisks. The spaces decrease toward the middle of the diamond and then increase again. The asterisks increase toward the middle and then decrease.

I checked the spaces by comparing each line of the program's output with the required pattern line by line. Because spaces are difficult to see, I counted the leading spaces on each line to make sure they were 3, 2, 1, 0, 1, 2, and 3.

game_time.cpp
Integer division by 60 calculates the number of complete hours. The remainder operator calculates the number of minutes left after the complete hours are removed.

For Level 1:

78 / 60 = 1
78 % 60 = 18

Therefore, Level 1 takes 1 hour and 18 minutes.

For Level 2:

144 / 60 = 2
144 % 60 = 24

Therefore, Level 2 takes 2 hours and 24 minutes.

The difference is calculated as:

144 - 78 = 66

Then:

66 / 60 = 1
66 % 60 = 6

Therefore, Level 2 took 1 hour and 6 minutes longer than Level 1.

The calculations are stored in variables before being displayed because this makes the code easier to read, understand, test, and debug. Each variable has a meaningful name that explains what the calculated value represents.
