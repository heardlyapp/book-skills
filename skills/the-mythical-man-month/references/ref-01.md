# Reference: Brooks's Law

## Overview
Brooks's law is the most famous insight in software engineering: "Adding manpower to a late software project makes it later."

## Case: The Communication Overhead
If N people work on a project, the number of communication channels is N(N-1)/2. Adding two people to a team of ten increases communication channels from 45 to 66. Each new person must be trained, learn the codebase, and be integrated into the team. During this period, the new people produce little while consuming the time of existing team members. Brooks concluded that adding people to a late project is counterproductive.

## Case: The OS/360 Experience
Brooks's experience managing the IBM System/360 operating system development showed him that the conventional wisdom about adding people was wrong. The OS/360 project was one of the largest software projects of its time. Brooks tried adding people to keep the schedule. He learned that it did not work. The Mythical Man-Month was written to explain why.

## Case: Partitioning
Some tasks can be partitioned (divided among workers with no communication) and others cannot. Planting crops can be partitioned: 10 people can plant 10 times as much as 1 person. Writing software cannot be partitioned because the parts must work together. Brooks argues that most software tasks are inherently non-partitionable.

## Case: The Man-Month Myth
The assumption that work can be partitioned and that men and months are interchangeable is the "mythical man-month." Brooks argues this fallacy causes more project failures than any other single error. A task that requires 10 person-months cannot be completed by 10 people in 1 month. The sequential nature of software development and the communication overhead make this impossible.
