# DDIA page 391

## Batch Processing with Unix Tools

### Simple Log Analysis&#x20;

Use unix tools to deal with logs like cat, awk, sort, uniq, sort, head

#### Chain of commands versus custom program

We can also use a program to achieve similliar goal, like using ruby. It will use in memory data structure like hashmap.



GNU sort utility automatically handles larger-than-memory datasets by spilling to disk, and paralellize sorting acoss multiple CPU cores.



### The Unix Philosophy

Make each program do one thing well.

Expect the output of every program to become the input to another.

Design and build software, even operating systems, to be tried early, ideally within weeks.

Use tools in preference to unskilled help to lighten a programming task.



Down side: Unix tools run on a single machine
