## Use cases

### Queue:

**Happy Path:**
1.The student loggs into their account. 
2.The system displays the home page.
3.The student clicks on the icon to sign up for exams.
4.The system presents a list of upcoming exams with filtering options.
5.The student selects an exam with full capacity to enroll in. 
6.The system places the student in the waiting queue.

**Potential Issues:**
-In step 1, the student encounters difficulty logging into the system.
-In step 4, no exams are available for enrollment. 
-In step 6, the deadline for enrolling in the exam has passed.
-In step 6, the exam's capacity is not full, so the system automatically enrolls the student.
-In step 6, the student cannot enroll in the waiting queue due to unfulfilled exam requirements.

**Preconditions:**
-The selected exam has reached full capacity.
-Enrollment for the exam is still open.
**Postconditions:**
-The student can view their position in the queue.

### Enroll for Exam:

**Happy Path:**
1. The student logs into their account.
2. The system displays the home page.
3. The student clicks on the icon to sign up for exams.
4. The system presents a list of upcoming exams with filtering options.
5. The student selects an exam with a specific date to enroll in.
6. The system confirms the student's enrollment in the exam and assigns them a time slot.

**Potential Issues:**
- In step 1, the student encounters difficulty logging into the system.
- In step 4, no exams are available for enrollment.
- In step 5, there are no suitable exam dates for the student.
- In step 6, the deadline for enrolling in the exam has passed.
- In step 6, the exam's capacity is full, so the system automatically places the student on the waiting list.
- In step 6, the student cannot enroll in the exam due to unfulfilled exam requirements.

**Preconditions:**
- The student has the necessary credit for the subject.
- Enrollment for the exam is still open and has available slots.

**Postconditions:**
- The student is successfully enrolled in the exam for the selected term.


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
