# Search space

What follows is an early draft of the search space:

## Assignment definition

In this problem, an assignment can be represented by the following elements:

- `Si`: Subject.
- `Gij`: Subject's group.
- `Ck`: Classroom or laboratory for that group.

An assignment is therefore a 3-tuple in the form:

    (Si, Gij, Ck)

A real example could be:

    (Comp, T1, A-S-02)

The total assignments to be made is calculated by:

    /* This should be represented as a mathematical expression in the final documentation */
    int i, j;
    int assignments;
    for (i = 0; i < numberOfSubjects(); i++) {
        for (j = 0; j < numberOfGroupsForSubject(i); j++) {
            assignments++;
        } 
    }
    return assignments; 

## State definition

The problem starts with an empty solution (normally), with 3-tuples in the form of `(Si, Gij, -)`. A partial solution is a state that occurs in the middle of the program execution, which contains complete assignments but still has some unassigned 3-tuples. After the execution of the program all the assignments are made and the state changes to a complete solution.

## State expansion

When an assignment of a classroom to an incomplete assignment is produced, the state is expanded. For an assignment `(Si, Gij, -)`, the number of new states that can be derived from it is calculated by:

    Number of derived states = sum(C)

Where `C` is the complete set of classrooms and laboratories.

