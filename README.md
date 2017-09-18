# git-demo2

# CSC301 git-demo Sept 18

script of this demo:

we pretend we are working on a couple of features.
Mathew makes f1 and alexei makes f2.

We do it a couple of ways.. including a conflict.

Let's pretend it's a little C program.

include.h, source.c, README.md is all there is.

## Script for simple collab

on branch: take-turns

1. matz pushes f1 in source.c
1. alexei pulls, changes source.c
1. alexei pushes f2

## Script for simple collab that goes wrong

on branch: ff (ff stands for fast forward)

1. alexei, pushes f1 in include.h (NOTE include.h!!)
1. matz, meanwhile writes f2
1. matz tries to push f2.. can't because tip is out of date??
1. matz pulls. merge is fine because changes are to different files
1. matz pushes f1 and f2

## Script for simple collab that goes even more wrong

on branch: conflict

1. alexei pushes f1 (changing first line) in source.c
2. meanwhile, matz writes f2, also changing first line of source.c
3. matz can't push, pulls, conflict!
4. matz resolves conflict and pushes resolved source.c with both f1
   and f2 in source.c
