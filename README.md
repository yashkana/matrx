# matrx
using System;<br>

namespace exersise<br>
{<br>
    class Sumofdiagnols<br>
    {<br>
        static void Main(string[] args)<br>
        {<br>
            int maxRow=0, maxcol, sum = 0;<br>
            int[,] matrix;<br>
            Console.WriteLine("\nSUM OFdiagnol of matrx........\n");<br>
            Console.Write(" enter the number of rows:\n");<br>
            maxRow= Convert.ToInt32(Console.ReadLine());<br>
            Console.Write("\n enter the number of columns:\n");<br>
            maxcol = Convert.ToInt32(Console.ReadLine());<br>
            if ( maxRow!=maxcol)<br>
            {<br>
                Console.WriteLine("/n The dimensions entered are not of sqare matrix");<br>
                Console.Write("\n exiting the program");<br>
                return;<br>
            }<br>
            matrix = new int[maxRow,maxcol];<br>
            for(int i=0;i<maxRow;i++)<br>
            {<br>
                for (int j = 0; j< maxcol; j++)<br>
                {<br>
                    Console.Write("\n enter the ({0},{1})th element of the matrix:", (i+1) , (j + 1));<br>
                    matrix[i, j] = Convert.ToInt32(Console.ReadLine());<br>
                }<br>
            }
            Console.WriteLine("\n the enter the Matrix is:");<br>
            for (int i = 0; i < maxRow; i++)<br>
            {<br>
                for (int j = 0; j < maxcol; j++)<br>
                {<br>
                    Console.Write("  " + matrix[i,j]);<br>
                    if(i==j)<br>
                    {<br>
                        sum += matrix[i, j];<br>
                    }<br>
                }<br>
                Console.WriteLine();<br>
            }<br>
            Console.WriteLine("\n The sum of Diagonal is :" + sum);<br>
        }<br>
    }<br>

}<br>

OUTPUT
![Screenshot 2022-02-18 121424](https://user-images.githubusercontent.com/98301023/154631770-e49e531f-b85f-471d-b013-cb0184f4d4f2.png)



