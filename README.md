# CodeAlpha_CGPA-_alculator
c++ program cgpa calculator
#include <iostream>
#include <vector>

using namespace std;

int main() {
    int numCourses;
    cout << "Enter the number of courses: ";
    cin >> numCourses;

    vector<double> grades(numCourses);
    vector<int> credits(numCourses);
    double totalCredits = 0;
    double totalGradePoints = 0;

    for (int i = 0; i < numCourses; ++i) {
        cout << "Enter grade for course " << i + 1 << " (e.g., 4.0 for A): ";
        cin >> grades[i];

        cout << "Enter credits for course " << i + 1 << ": ";
        cin >> credits[i];

        totalCredits += credits[i];
        totalGradePoints += grades[i] * credits[i];
    }

    double cgpa = totalGradePoints / totalCredits;
    cout << "Your CGPA is: " << cgpa << endl;

    return 0;
}
