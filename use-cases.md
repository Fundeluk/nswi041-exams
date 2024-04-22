## Use cases

### Queue:

#### Detail:
Happy path - The student is waiting in the queue until vacancy occurs. Then is automatically enrolled on the exam and given a specific time. 
#### Alternatives: 
The student will not be able to enrolled for the exam because the capacity is full.
The student is not able to get to the queue because the student has not fullfilled the requirements for enrolling for the exam.
#### Prerequirements:
The capacity is full.
It is still possible to enroll for the exam.
#### Postrequirement
To be able to see position in the queue. 

### Enroll for exam:

#### Detail:
Happy path - Student is enrolling for a specific date and subject.
#### Alternatives: 
Can happen that there is no way to get enrolled for the specific date or time.
The term can be full.
There is no term that the student will be satisfied with
#### Prerequirements:
To have credit for this subject
The term is opened for enrolling
There is a term that is opened and is not full
#### Postrequirements:
To be succesfully enrolled to the term

### Get credit:

#### Detail:
Happy path - To meet the criteria for acquiring the credit for the subject which is later granted to the student from the teacher
#### Alternatives: 
Not having enough points the acquire the credit for the subject
Not having submitted credit work before deadline
#### Prerequirements:
To meet the criteria for acquiring the credit for the subject
To be enrolled for the subject
#### Postrequirements:
Permission to be able to enroll for the exam

### Filter exams:

#### Detail:
Happy path - to choose from options that are available
#### Alternatives: 
There is no term of exam that meets the criteria
There are no terms for the exam listed yet
#### Prerequirements:
List of terms for the exam
To be enrolled for the subject
#### Postrequirements:
The list of all the terms for the exam that meets the criteria from the options available

### Pass exam:

#### Detail:
Happy path - To pass the exam to be awarded with passing of this course
#### Alternatives: 
Not to have enough points for passing the exam
#### Prerequirement:
To be enrolled for the specific exam date that you are taking
#### Postrequirement:
Completing the subject and passing the exam you enrolled.

### Unenroll from exam:

#### Detail:
Happy path- Successfully unenroll from the exam.
#### Alternatives: 
It is not possible to unenroll from the exam anymore.
#### Prerequirement:
To be enrolled for the exam. 
#### Postrequirement:
Have the oportunity to enroll for another date or time.

### View exam result

#### Detail:
Happy path - User successfully views the result of his exam
#### Alternatives:
The results are not ready yet
The user tries to view results of a different user and is rejected  
#### Prerequirement:
Enroll for the exam
Attend the exam
#### Postrequirement:
None

### Make/create exam

#### Detail:
Happy path - The user with teacher privileges selects a date, time and place and adds the exam into the system
#### Alternatives:
The user does not have teacher privileges and is rejected
The selected place is already booked for selected date&time
The user does not have privileges to create an exam for a course they do not teach
#### Prerequirement:
Have teacher rights
Teach this course
Selected date,time&place is not booked
#### Postrequirement:
Have the ability to change the time,date&place

### Publish Result

#### Detail:
Happy path - The teacher efficiently publishes the exam results into the system, which then become immediately available for students to view.

#### Alternatives:
- The publishing process encounters a technical error, delaying the availability of results.
- The teacher mistakenly publishes incomplete or incorrect results and needs to retract or amend them.

#### Prerequirements:
- The teacher has access to the system with rights to publish results.
- The exams have been graded and the results finalized.

#### Postrequirements:
- Students are able to view their exam results as soon as they are published.
- Notifications might be sent to students alerting them of newly published results.

### Kick Student Out

#### Detail:
Happy path - The teacher uses the system to automatically unenroll students who have not fulfilled the prerequisite criteria (e.g., requisite credits) for the exam.

#### Alternatives:
- The system fails to identify and remove a student who hasn't met the prerequisites.
- A student is mistakenly removed due to incorrect data regarding their prerequisites.

#### Prerequirements:
- The student is currently enrolled in an exam for which they do not meet the necessary criteria.
- The teacher has the appropriate system permissions to manage enrollments and remove students.

#### Postrequirements:
- The student is no longer enrolled in the exam.
- The student and teacher receive notifications about the change in enrollment status.
- The system logs the action for auditing purposes.
