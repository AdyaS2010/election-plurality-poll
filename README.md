# Voting Systems: Plurality and Runoff

This repository contains implementations of two voting systems: **Plurality** and **Runoff**. I mean for it to be utilized as an integration, a step that I am currently working on (as of now, this is a WIP, and one of my first project in C)! These systems are designed to handle elections with multiple candidates and voters, ensuring a fair and transparent voting process, inspired by our StuCo and Class Elections for School!

## Plurality Voting System

The plurality voting system is a simple and widely-used method where each voter selects one candidate, and the candidate with the most votes wins (no runoffs or additional tiebreakers)! 

### Features
- **Maximum Candidates**: Supports up to 9 candidates.
- **Vote Counting**: Accurately counts votes for each candidate.
- **Winner Declaration**: Declares the candidate(s) with the highest votes as the winner(s).

### Code Overview
The `plurality.c` file contains the implementation of the plurality voting system. Key components include:
- **Candidate Structure**: Defines a candidate with a name and vote count.
- **Vote Function**: Updates vote totals given a new vote.
- **Print Winner Function**: Prints the winner(s) of the election.

### Usage
To run the plurality voting system:
1. Compile the code using a C compiler.
2. Execute the program with the candidate names as command-line arguments.
3. Enter the number of voters and their votes.
4. The program will display the winner(s).

```bash
gcc plurality.c -o plurality
./plurality Alice Bob Charlie
```
*Using the candidates 'Emma', 'Bob', and 'Charlie', the following are different example cases of elections and results according to 'voter input'!*
![image](https://github.com/user-attachments/assets/5f5ec1dd-8286-4e1b-a644-8b2e5e74e96c)

![image](https://github.com/user-attachments/assets/36fddd42-e29d-424b-bb72-be9ea088d308)

![image](https://github.com/user-attachments/assets/2b969b48-684e-47c4-a55b-de2d88fe7f59)
*The Winners name(s) will be printed at the end of the program after all votes are inputted!*

## Runoff Voting System

The runoff voting system is a more complex method where voters rank candidates in order of preference. If no candidate wins a majority, the candidate with the fewest votes is eliminated, and their votes are redistributed until a winner is found.

### Features
- **Maximum Voters and Candidates**: Supports up to 100 voters and 9 candidates.
- **Preference Recording**: Records voter preferences for each candidate.
- **Vote Tabulation**: Tabulates votes for non-eliminated candidates.
- **Elimination Process**: Eliminates candidates with the fewest votes and redistributes their votes.
- **Winner Declaration**: Declares the candidate with a majority of votes as the winner.

### Code Overview
The `runoff.c` file contains the implementation of the runoff voting system. Key components include:
- **Candidate Structure**: Defines a candidate with a name, vote count, and elimination status.
- **Vote Function**: Records preferences if the vote is valid.
- **Tabulate Function**: Tabulates votes for non-eliminated candidates.
- **Print Winner Function**: Prints the winner if there is one.
- **Elimination Functions**: Finds the minimum votes, checks for ties, and eliminates candidates.

### Usage
To run the runoff voting system:
1. Compile the code using a C compiler.
2. Execute the program with the candidate names as command-line arguments.
3. Enter the number of voters and their ranked preferences.
4. The program will display the winner after necessary runoffs.

```bash
gcc runoff.c -o runoff
./runoff Alice Bob Charlie
```

![image](https://github.com/user-attachments/assets/6b9682ec-7d38-4fdc-adec-c6d2e350be70)
*The runoff system utilizes a ranking system, as shown!*

## License
This project is not currently licensed under anything.
