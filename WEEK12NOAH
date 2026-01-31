# week12assignment
#include <iostream>
using namespace std;

class Student {
public:
    int studentID;
    string name;

    Student(int id, string n) {
        studentID = id;
        name = n;
    }
};

class Course {
public:
    string courseCode;
    string courseName;

    Course(string code, string name) {
        courseCode = code;
        courseName = name;
    }
};

class Department {
public:
    string deptName;
    Course* courses[5];
    int count;

    Department(string name) {
        deptName = name;
        count = 0;
    }

    void addCourse(Course* c) {
        courses[count++] = c;
    }

    void displayCourses() {
        cout << "Department: " << deptName << endl;
        for (int i = 0; i < count; i++) {
            cout << courses[i]->courseCode << " - "
                 << courses[i]->courseName << endl;
        }
    }
};

class Registration {
public:
    void registerStudent(Student& s, Course& c) {
        cout << s.name << " registered for "
             << c.courseName << endl;
    }
};

int main() {
    
    Student s1(101, "Noah");

  
    Course c1("CS101", "Programming Fundamentals");
    Course c2("CS102", "Data Structures");

  
    Department dept("Computer Science");
    dept.addCourse(&c1);
    dept.addCourse(&c2);


    dept.displayCourses();


    Registration reg;
    reg.registerStudent(s1, c1);
    reg.registerStudent(s1, c2);

    return 0;
}
