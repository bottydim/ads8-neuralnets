# ADS Template Repository

**Note to editors**: make sure you have `nbstripout` installed on your machine so that you don't clog the repository with Jupyter outputs!

This folder has the structure that all ADS modules are expected to have.

## Generic schedule

* 1.50 - 1.50 (0930-1100) *Block 0*
* 0.25 - 1.75 (1100-1115) *Coffee break*
* 1.50 - 3.25 (1115-1245) *Block 1*
* 1.00 - 4.25 (1245-1345) *Lunch*
* 1.50 - 5.75 (1345-1515) *Block 2*
* 0.25 - 6.00 (1515-1530) *Coffee break*
* 1.50 - 7.30 (1530-1700) *Block 3*

Note *Block 0* for all modules on day 1 will be a discussion (either of code, or about the programme or some such).

## Side stuff

* Type A questions: "exact" questions (implement code that does X)
* Type B questions: "open" questions (do something that answers a generic question)

### Presentation

- For each module starting after module 2, every team has to prepare a short presentation (10 minutes).
- Three teams are randomly selected (tweak to have everyone present a bit).  
- These teams present one after the other.
- 10-15 minutes questions / comments directly addressed to teams.
- We present our comments, a standard solution, also discuss Type A questions

### Leaderboard concept

They get points for every module following:

**If present**
- `+10` for presenting
- `+10a` where `a` is the ratio of people present (non jury) who voted for the presentation as the best one
- `+10` if jury voted it the best

**All**
- points for code cleanness (`1..10`)
- points for code quality (`1..10`) (*test A questions*)
- points for model quality (`3-5-10`) (*test B questions, top three of model accuracy leaderboard if relevant. If ties, all people tying get the maximum score available to them.*)

### Team randomisation

For 28 people:

```julia
s = shuffle(15:28)
[(i, s[i]) for i in 1:14]
```

yields

```
 (1, 23)
 (2, 17)
 (3, 28)
 (4, 16)
 (5, 21)
 (6, 22)
 (7, 25)
 (8, 15)
 (9, 20)
 (10, 26)
 (11, 19)
 (12, 24)
 (13, 18)
 (14, 27)
```

this is an assignment for the first module. Then you just cycle up one for each module. No overlap in 9 weekends. Don't pre-announce everything, just say it's randomly drawn every time and announce it 2nd day.
