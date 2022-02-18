# matrx
using System;

namespace exersise
{
    class Sumofdiagnols
    {
        static void Main(string[] args)
        {
            int maxRow=0, maxcol, sum = 0;
            int[,] matrix;
            Console.WriteLine("\nSUM OFdiagnol of matrx........\n");
            Console.Write(" enter the number of rows:\n");
            maxRow= Convert.ToInt32(Console.ReadLine());
            Console.Write("\n enter the number of columns:\n");
            maxcol = Convert.ToInt32(Console.ReadLine());
            if ( maxRow!=maxcol)
            {
                Console.WriteLine("/n The dimensions entered are not of sqare matrix");
                Console.Write("\n exiting the program");
                return;
            }
            matrix = new int[maxRow,maxcol];
            for(int i=0;i<maxRow;i++)
            {
                for (int j = 0; j< maxcol; j++)
                {
                    Console.Write("\n enter the ({0},{1})th element of the matrix:", (i+1) , (j + 1));
                    matrix[i, j] = Convert.ToInt32(Console.ReadLine());
                }
            }
            Console.WriteLine("\n the enter the Matrix is:");
            for (int i = 0; i < maxRow; i++)
            {
                for (int j = 0; j < maxcol; j++)
                {
                    Console.Write("  " + matrix[i,j]);
                    if(i==j)
                    {
                        sum += matrix[i, j];
                    }
                }
                Console.WriteLine();
            }
            Console.WriteLine("\n The sum of Diagonal is :" + sum);
        }
    }

}

OUTPUT
![Screenshot 2022-02-18 121424](https://user-images.githubusercontent.com/98301023/154631770-e49e531f-b85f-471d-b013-cb0184f4d4f2.png)



