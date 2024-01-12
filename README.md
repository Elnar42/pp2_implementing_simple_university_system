# Implementing University System
Students will try to implement a simple university system using Java programming language

## Description
This Java project implements a simple University Management System with a focus on the Person, Student, Professor, School, University, and Main classes. Here are the classes, their fields and methods to implement:

### Person class (Abstract)
#### Fields/Properties: 
+ **ID** : **final int** **(automatically generated 6-digit ID)**

+ **name** : **final String**  

+ **surname** : **final String**  

+ **birthday** : **final LocalDate (seach for this class, especially its 'of' method)**

+ **email** : **String** **(automatically generated)**  

+ **address** : **String**  

+ **phoneNumber** : **String**

#### Methods:
+ **Getters for all fields**

+ **Setters for all fields except ID, name, surname, and birthday**

+ **ToString() - this method is overridden to display all fields in a formatted manner, each on a new line**

*NOTE: ID is generated as a 6-digit number (using Random class).Email is generated in lowercase, consisting of the first letter of the name, followed by the surname, followed by "@edu.az". Create a corresponding constructor, considering that ID and email are not required from the user while calling constructor for subclasses*

### Student class
**This class extends Person class**
#### Fields/Properties: 
+ **enrolledCourses** : **ArrayList<Course>**
+ **grades** : **Map<Course, Map<String, Double>>**
+ **permittedCreditPerSemestr** : **int**
+ **currentCredit** : **int**
+ **average** : **double**

#### Methods:
+ **Setters and Getter**
+ **enrollCourse(Course course) : void**
+ **dropCourse(Course course) : void**
+ **getEnrolledCoursesList(): String**
+ **getCurrentGradePerCourse(): String**
+ **averageGrade(): double**
+ **viewEnrolledCourses(): void**
+ **toString()**

*NOTE: Corresponding constructor should be set.By default enrolledCourses are empty list, grades are empty, currentCredit is 0, permittedCreditPerSemester is 30, average is 0. Consider such cases while setting a constructor. ToString() method should return Enrolled Courses, Current Grades Per Course, Permitted Credit, Current Credit and Average each on a new line(You can use corressponding methods for such purposes)*

### Course class
#### Fields/Properties:
+ **courseID** : **String (Automatically generated 8 char long, mixture of both digit and letter)**
+ **lecturer** : **Professor**
+ **courseName** : **String**
+ **description** : **String**
+ **currentEnrolledNumber** : **int**
+ **capacity** : **int** **(Default: 40)**
+ **enrolledStudents** : **List<Student>**
+ **creditNumber** : **int** **(Default: 6)**
+ **term** : **String**
+ **isActive** : **boolean**
+ **gradingSystem** : **String** **(Static, Default: "Based on 100 Scale")**
+ **duration** : **Duration** **(Static, Default: 90 minutes)**
+ **passingScore** : **double** **(Static, Default: 59.5)**
+ **maxScore** : **double** **(Static, Default: 100.0)**
+ **roomNumber** : **String**
+ **assignments** : **Map<String, Double>**

#### Methods:
+ **Getters for all fields**
+ **Setters for all except courseID**
+ **addAssignment(String name, Double grade): void**
+ **getAssignmentMaxGrade(String assignment) : Double**
+ **addEnrollment(Student student): void**
+ **studentPosition(Student student): boolean (return true if student is enrolled)**
+ **getEnrolledStudentsList(): String**
+ **generateRandomID(int length): String (Static) - for courseID**
+ **toString()**

*NOTE: When creating a constructor, the courseID is automatically added to the course, enrolledStudents are empty list, assignments are empty, isActive is false, currentEnrolledNumber is 0*

