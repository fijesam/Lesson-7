# Lesson-7
//four dimensional array
using System;

namespace four_dimensional_array
{
    class Program
    {
        static void Main(string[] args)
        {
            //lesson 7 exercise 1
            int[,,,] matrixG = new int[2, 3, 5, 4]
                                    { {{{1,2,3,4 },{1,2,3,4},{1,2,3,4},{1,2,3,4},{1,2,3,4}},
                                    {{1,2,3,4 },{1,2,3,4},{1,2,3,4},{1,2,3,4},{1,2,3,4}},
                                    {{1,2,3,4 },{1,2,3,4},{1,2,3,4},{1,2,3,4},{1,2,3,4}}},{ { { 1,2,3,4 },{ 1,2,3,4},{ 1,2,3,4},{ 1,2,3,4},{ 1,2,3,4} },
                                    { { 1,2,3,4 },{ 1,2,3,4},{ 1,2,3,4},{ 1,2,3,4},{ 1,2,3,4} },
                                    { { 1,2,3,4 },{ 1,2,3,4},{ 1,2,3,4},{ 1,2,3,4},{ 1,2,3,4} } } };
            Console.WriteLine("Hello World!");
        }
    }
}

//Addition, Subtraction and Multiplication
using System;

namespace addition
{
    class Program
    {
        static void Main(string[] args)
        {
            //Addition, Subtraction and Multiplication
            Console.Write("Enter the number of rows in matrixA: ");
            int m = int.Parse(Console.ReadLine());
            Console.Write("Enter the number of columns in matrixA: ");
            int n = int.Parse(Console.ReadLine());
            int[,] matrixA = new int[m,n];

            Console.Write("Enter the number of rows in matrixB: ");
            int x = int.Parse(Console.ReadLine());
            Console.Write("Enter the number of columns in matrixB: ");
            int y = int.Parse(Console.ReadLine());
            int[,] matrixB =new int[x,y];

            Console.WriteLine("Enter the cells of the matrixA: ");
            for (int i = 0; i < m; i++)
            {
                for (int j = 0; j < y; j++)
                {
                    Console.Write("matrixA[{0},{1}] = ", i, j);
                    matrixA[i, j] = int.Parse(Console.ReadLine());
                }
            }

            Console.WriteLine("Enter the cells of the matrixB: ");
            for (int a = 0; a<m;  a++)
            {
                for (int b = 0; b < y; b++)
                {
                    Console.Write("matrixB[{0},{1}] = ", a, b);
                    matrixB[a, b] = int.Parse(Console.ReadLine());
                }
            }

            int[,] matrixC = new int[m, n];
            int[,] matrixD = new int[m, n];
            int[,] matrixE = new int[m, n];

            if (m == x && n == y)
            {



                for (int i = 0; i < m; i++)
                {
                    for (int j = 0; j < n; j++)
                    {
                        for (int a = 0; a < x; a++)
                        {
                            for (int b = 0; b < y; b++)
                            {
                             
                                    matrixC [i,j]= matrixA[i, j] + matrixB[a, b];
                                    Console.WriteLine(matrixC);
                                    matrixD[i, j] = matrixA[i, j] - matrixB[a, b];
                                    Console.WriteLine(matrixD);
                                    matrixE[i, j] = matrixA[i, j] * matrixB[a, b];
                                    Console.WriteLine(matrixE);


                            }
                        }


                    }
                }
                Console.WriteLine();
                Console.WriteLine("Hello World!");

            }
        }
    }
}

//determinant
using System;  
public class Exercise28 
{  
    public static void Main()
   {
            int i,j;
        	int[,] arr1 = new int[3,3];
            int det=0;
  
  
       Console.Write("\n\nCalculate the determinant of a 3 x 3 matrix :\n");
       Console.Write("-------------------------------------------------\n");  

	 Console.Write("Input elements in the matrix :\n");
       for(i=0;i<3;i++)
        {
            for(j=0;j<3;j++)
            {
	           Console.Write("element - [{0}],[{1}] : ",i,j);
             Console.Write("\n");
	          }

  for(i=0;i<3;i++)
      det = det + (arr1[0,i]*(arr1[1,(i+1)%3]*arr1[2,(i+2)%3] - arr1[1,(i+2)%3]*arr1[2,(i+1)%3]));

  Console.Write("\nThe Determinant of the matrix is: {0}\n\n",det);
       }
   }
