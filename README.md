# SAM-AI-Tech-Task
import java.util.ArrayList;
import java.util.Scanner;
 class GradeCalculator
{
    public static void main (String[] args)
    {
        Scanner scanner= new Scanner(System.in);
        ArrayList<Double>marks= new ArrayList<>();
        System.out.print("Enter the number of subjects");
        int totalSubjects=scanner.nextInt();
        for (int i=1;i<=totalSubjects;i++)
        {
            System.out.print("Enter marks for subject"+ i +"(out of 100):");
            double mark=scanner.nextDouble();
            while(mark<0||mark>100)
            {
                System .out .print("Invalid marks! Please enter between 0 and 100");
                mark=scanner.nextDouble();
            }
            marks.add(mark);
        }
        double totalMarks=0;
        for(double m :marks)
        {
            totalMarks+=m;
        }
        double averagePercentage = totalMarks;
        char grade;
        if (averagePercentage>=85)
    {
        grade ='A';
    }
    else if (averagePercentage>=70)
    {
        grade ='B';
    }
    else if (averagePercentage>=50)
    {
        grade = 'C';
    }
    else
    {
        grade='F';
    }
    System.out.println("\n---Final Result---");
    System.out.println("Total Marks Obtained."+ totalMarks+"/"+(totalSubjects*100));
    System.out.printf("AveragePercentage:%2f%%\n",averagePercentage);
    System.out.println("Assigned Grade:"+grade);
    
    scanner.close();
    }
}
