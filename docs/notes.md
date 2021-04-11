# Notes

Here are writen some notes taken in the early phases of the project:

## Program notes

### Configuration notes

- The number of students is based on the number of enrolled students.
- Program configuration can change in the middle of the course.
- The maximum and minimum number of free slots can change (even between subjects).

### Input notes

- The program must be able to take as input a previous complete list of assignments but without some of the classrooms/laboratories used in it.
- The progam receives as input the list of class groups with their relations and the timetable for the year.
- The program must be able to receive as input a subset of groups already assigned to some laboratories.

### Other

- The program must implement a CLI.
- The program must be able to find a gap in the current list of assignments to include a (mono/multi)-(classroom/laboratory).

## Algorithm notes

### English AND spanish groups notes

- English groups should go to different classrooms/laboratories from the spanish groups.
- English groups and spanish groups must be treated as part of different subjects.

### Classroom notes

- Theory classes of the same course and group have to be in the same classroom.

### Laboratory notes

- A set of groups can be specified to be always in the same laboratory.
- Consecutive laboratory classes of the same subject have to be taught in the same laboratory.
- The laboratories must have some free space defined by the user.
- The program must penalise assignments where the number of students is far below the number of computers.
- In each time slot there must be a minimum number of free laboratories.
- The program must be able to split a laboratory group in two with only one professor (for emergencies).
- There are 12 normal laboratories plus a special one used for TEC.
- The number of groups of the same subject assigned to the same laboratory must be maximised.
- In small laboratories (of 16 computers) there must be at least two free computers.
- Some big laboratories must be empty for emergency reasons.
- Small laboratories should have some margin for broken computers.

### Classroom AND laboratory notes

- A set of classrooms/laboratories of obligatory use can be specified for specific subjects.
- Some initial classroom assignments can be specified before the execution of the program and they must remain the same.
- The number of classrooms/laboratories assigned for an exam must be minimised.
- A set of classrooms/laboratories of obligatory use can be specified for a given exam.
- Using less classrooms and laboratories is not always good for maintenance reasons.
- Students of first course should go in the same group for all subjects, if possible (Student A in group L1 of subjects 1, 2...).

