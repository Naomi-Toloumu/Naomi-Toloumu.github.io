---
layout: project
type: project
image: img/GradeCalculator(2.0).tiff
title: "Grade Calculator"
date: 2023
published: true
labels:
  - Java
  - Visual Studio Code
summary: "In ICS 211, I created a GradeCalculator."
---

The GradeCalculator Java program illustrates key programming concepts with a well-organized class structure and a main method as the entry point. It uses final variables for constants, manages user input with Scanner, and includes basic validation. The program calculates percentages for different assessments, caps them at 100%, and computes weighted averages based on student status (UG, G, DL) using conditional logic. Output is formatted for clarity with System.out.printf, and resource management is handled by closing the Scanner. To improve, the code could benefit from refactoring repeated logic into methods, enhancing error handling, and providing clearer user prompts.

[Visual Studio Code]

```
import java.util.Scanner;

public class GradeCalculator {
     public static void main(String[] args) {
      
      final double HOMEWORK_MAX = 800.0;
      final double QUIZZES_MAX = 400.0;
      final double MIDTERM_MAX = 150.0;
      final double FINAL_MAX = 200.0;    
      
      Scanner scnr = new Scanner(System.in);
      
      String student_stat;
      student_stat = scnr.next();
      
      if (!(student_stat.equals("UG") || student_stat.equals("G") || student_stat.equals("DL"))){
         System.out.println("Error: student status must be UG, G or DL");
         scnr.close();
         return;
      }
      
      double homework;
      homework = scnr.nextDouble();
      homework = (homework / HOMEWORK_MAX) * 100;
      if(homework > 100.0){
         homework = 100.0;
      }
      System.out.printf("Homework: %.1f%%", homework);
      System.out.println();
    
      double quizzes;
      quizzes = scnr.nextDouble();
      quizzes = (quizzes / QUIZZES_MAX) * 100;
      if (quizzes > 100.0) {
         quizzes = 100.0;
      }
      System.out.printf("Quizzes: %.1f%%", quizzes);
      System.out.println();
      
      double midterm;
      midterm = scnr.nextDouble();
      midterm = (midterm / MIDTERM_MAX) * 100;
      if(midterm > 100.0){
         midterm = 100.0;
      }
      System.out.printf("Midterm: %.1f%%", midterm);
      System.out.println();
      
      double final_exam;
      final_exam = scnr.nextDouble();
      final_exam = (final_exam / FINAL_MAX) * 100;
      if(final_exam > 100.0){
         final_exam = 100.0;
      }
      System.out.printf("Final Exam: %.1f%%", final_exam);
      System.out.println();
    
      double avg = 0.0;
      
      if (student_stat.equals("UG")) {
         avg = (homework * 0.2) + (quizzes * 0.2) + (midterm * 0.3) + (final_exam * 0.3);
         System.out.printf("UG average: %.1f%%\n", avg);
      }
      
      else if (student_stat.equals("G")){
         avg = (homework * 0.15) + (quizzes * 0.05) + (midterm * 0.35) + (final_exam * 0.45);
         System.out.printf("G average: %.1f%%\n", avg);
         
      }
      else if (student_stat.equals("DL")){
         avg = (homework * 0.05) + (quizzes * 0.05) + (midterm * 0.4) + (final_exam * 0.5);
         System.out.printf("DL average: %.1f%%\n", avg);
      }
    
      if (avg >= 90) {
         System.out.print("Course grade: A");
         System.out.println();
      }
      else if (avg >= 80) {
         System.out.print("Course grade: B");
         System.out.println();
      }
      else if (avg >= 70) {
         System.out.print("Course grade: C");
         System.out.println();
      }
      else if (avg >= 60) {
         System.out.print("Course grade: D");
         System.out.println();
      }
      else {
         System.out.print("Course grade: F");
         System.out.println();
      }
      scnr.close();
   }
}
```

