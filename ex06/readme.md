# Dining philosophers

## Objectives

* Using structs
* Using vectros
* Using traits and lifetimes where appropriate
* The main objective of this exercise is to use threads

## TO DO
```
In ancient times, wealthy philanthropists were invited to visit five outstanding philosophers. They are allocated to each of the room in which they can practice their profession - thinking. There was also a common dining room, where there was a large round table and five chairs around it. Each chair had a sign with the name of the philosopher, who was supposed to sit on it. To the left of each philosopher lay golden fork, and in the center of the table was a large bowl of spaghetti, which is constantly updated. As befits philosophers, they spend most of their time in thought. But once they felt hungry and went into the dining room. Everyone sat down on his chair, picked up by a fork and stuck it in a bowl of spaghetti. But the essence of tangled spaghetti is such that there must be a second fork to send the spaghetti into his mouth. That is the philosopher needed more and fork right. Philosophers have laid down their forks and stood up from the table, still thinking. After all, the plug can be used by only one philosopher at the same time. If another philosopher wants to take it, then he would have to wait until it becomes free.
```

This classical problem shows various elements of parallelism. The complexity of the implementation task is that simple realization can go in a hopeless state. Let's look at a simple example of this problem:

* 1.The philosopher takes the fork in your left hand.
* 2.Then he takes a fork in right hand.
* 3.Eating.
* 4.Puts the fork in place.

Now imagine it as a sequence of philosophers:

* 1.Philosopher 1 begins to execute an algorithm, taking the fork in the left hand.
* 2.Philosopher 2 starts executing the algorithm takes the fork in the left hand.
* 3.Philosopher 3 starts executing the algorithm takes the fork in the left hand.
* 4.Philosopher 4 starts executing the algorithm takes the fork in the left hand.
* 5.Philosopher 5 starts performing the algorithm takes the fork in the left hand.
* 6....? All plugs are occupied and no one can start eating! Hopeless condition.

You should find a way to solve this with threads.

