Download Link: https://assignmentchef.com/product/solved-csci-4300-operating-systems-hw3-in-the-lab-chapter-5-project-2-sleeping-ta-problem
<br>
A university computer science department has a teaching assistant (TA) who helps undergraduate students with their programming assignments during regular office hours. The TA’s office is rather small and has room for only one desk with a chair and computer. There are three chairs in the hallway outside the office where students can sit and wait if the TA is currently helping another student. When there are no students who need help during office hours, the TA sits at the desk and takes a nap. If a student arrives during office hours and finds the TA sleeping, the student must awaken the TA to ask for help. If a student arrives and finds the TA currently helping another student, the student sits on one of the chairs in the hallway and waits. If no chairs are available, the student will come back at a later time.

Using Pthreads (section 4.4.1), begin by creating n students.  Each student, as well as the TA, run as a separate thread. Student threads alternate between programming for a period of time and seeking help from the TA. If the TA is available, they obtain help. Otherwise, they either sit in a chair in the hallway, or if no chairs are available, resume programming and seek help at a later time. If a student arrives and notices that the TA is sleeping, the student notifies the TA using a semaphore. When the TA finishes helping a student, the TA checks to see if there are students waiting for help in the hallway. If so, the TA helps each of these students in turn. If no students are present, the TA returns to napping.

The TA and each student thread print their state and the relevant student ids whenever an action is taken.

The program will request the total number of students working on the programming assignment at the start of the program.  Also, to simulate students programming –as well as the TA providing help to a student- the program will have the appropriate threads sleep for a random period of time.

You will receive a starter version of the code that contains a completed main function and a function to handle the random sleep/waiting times.  You will need to complete the code to handle the TA thread and the student threads.

You are expected to submit your code for this project at the end of the class period in whatever state that it is in.  You will have until Tuesday 11/20 @ 11:59pm to submit the code with any adjustments or changes that you want.  Note that you should work with a partner while in class, but you are both expected to submit your own version of the code to blackboard.

Compile with the following: gcc sleepTA.c –o sleepTA –lpthread -lrt


