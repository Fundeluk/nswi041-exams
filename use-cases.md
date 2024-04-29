## Use cases

### Queue:

**Happy Path:**
1. The student loggs into their account. 
2. The system displays the home page.
3. The student clicks on the icon to sign up for exams.
4. The system presents a list of upcoming exams with filtering options.
5. The student selects an exam with full capacity to enroll in. 
6. The system places the student in the waiting queue.

**Potential Issues:**
- In step 1, the student encounters difficulty logging into the system.
- In step 4, no exams are available for enrollment. 
- In step 6, the deadline for enrolling in the exam has passed.
- In step 6, the exam's capacity is not full, so the system automatically enrolls the student.
- In step 6, the student cannot enroll in the waiting queue due to unfulfilled exam requirements.

**Preconditions:**
- The selected exam has reached full capacity.
- Enrollment for the exam is still open.
**Postconditions:**
- The student can view their position in the queue.

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

### Unenroll from Exam

#### Happy Path:

1. The student logs into their account on the Student Information System.
2. The system displays the home page.
3. The student clicks on the icon where exams they are enrolled in are listed.
4. The system presents a list of exams the student is enrolled for.
5. The student selects an exam by clicking the specific name and icon to unenroll from the exam.
6. The system confirms the student's unenrollment from the exam.

#### Potential Issues:

- In step 1, the student encounters difficulty logging into the system.
- In step 4, the system fails to display a list of enrolled exams.
- In step 5, the deadline for unenrolling from the exam has already passed.

#### Preconditions:

- The student is enrolled in the exam.
- The unenrollment option is still available for the exam.

#### Postconditions:

- The student has the opportunity to enroll for another date or time.
- The student is successfully unenrolled from the exam.

### View Exam Result

#### Happy Path:

1. The student logs into their account on the Student Information System.
2. The system displays the home page.
3. The student clicks on the icon where their exam results are listed.
4. The system presents the results of exams the student has taken.
5. The student views the results from their exams.

#### Potential Issues:

- In step 1, the student encounters difficulty logging into the system.
- In step 4, the exam results are not yet available.

#### Preconditions:

- The student has taken an exam for which they wish to see the results.

#### Postconditions:

- There are no postconditions; the student has simply accessed and viewed their results.

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

#### Happy Path:

1. The teacher logs into their account on the Student Information System.
2. The system displays the teacher's dashboard.
3. The teacher selects the course for which they want to publish exam results.
4. The system displays a list of completed exams along with options to enter or upload results.
5. The teacher inputs or uploads the finalized exam results.
6. The system verifies the accuracy and completeness of the uploaded data.
7. The teacher confirms the publication of the results.
8. The system publishes the results, making them visible to the students.
9. Students receive notifications that their exam results are available for viewing.

#### Potential Issues:

- In step 1, the teacher encounters difficulty logging into the system.
- In step 4, the system fails to display the correct exams, showing exams that are not yet ready for result publication.
- In step 5, the teacher inputs incomplete or incorrect results, requiring revision.
- In step 6, the system encounters an error during data verification, delaying the process.
- In step 7, the teacher inadvertently publishes the wrong results, necessitating a retraction and correction.
- In step 8, the results do not appear for students due to a delay or error in the publication process.
- In step 9, students do not receive notifications due to an issue with the notification system.

#### Preconditions:

- The exams have been completed and graded.
- The teacher has the necessary permissions to publish results for the course.

#### Postconditions:

- Exam results are accurately published and visible to students.
- Notifications are sent out to all relevant students about the availability of their results.
- The system logs the publication event for auditing and compliance purposes.

### Kick Student Out

#### Happy Path:

1. The teacher logs into their account on the Student Information System.
2. The system displays the teacher's dashboard.
3. The teacher accesses the enrollment list for a specific course.
4. The system presents a list of all enrolled students along with their eligibility status.
5. The teacher selects a student who has not met the necessary prerequisites for the exam.
6. The system processes the removal of the student from the enrollment list.
7. The student receives a notification of their removal due to unmet prerequisites.

#### Potential Issues:

- In step 1, the teacher encounters difficulty logging into the system.
- In step 3, the system fails to load the enrollment list due to a technical error.
- In step 5, the system shows incorrect data, leading to the wrongful selection of a student who actually meets the prerequisites.
- In step 6, the system fails to remove the student from the list due to a processing error.
- In step 7, the student does not receive the notification due to an issue with the notification system.

#### Preconditions:

- The student is currently enrolled in an exam for which they have not fulfilled the necessary criteria.
- The teacher is authorized to manage course enrollments.

#### Postconditions:

- The student is removed from the exam enrollment list.
- Both the student and the teacher receive confirmation of the enrollment change.
- The system updates its records to reflect the removal for auditing and tracking purposes.
