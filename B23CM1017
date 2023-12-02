#include <stdio.h>
#include <math.h>




float AreaofCircle(float radius);
float AreaofTriangle(float s1, float s2, float s3);
float AreaofRectangle(float length, float width);
float AreaofParallelogram(float base, float height);
float AreaofRhombus(float diagonal1, float diagonal2);
float AreaofTrapezium(float side1, float side2, float height);
float AreaofPentagon2(float side);
float AreaofPentagon1(float side, float apothemlength);
float AreaofHexagon(float side);

void printHollowRectangle(int length, int width);
void printHollowTriangle(int height);
void printHollowParallelogram(int rows,int columns);
void printHollowTrapezium(int size);
void printHollowRhombus(int diagonal1,int diagonal2 );
void printHollowHexagon(int height);
void printHollowPentagon(int n);
void space(int size);
void print_symbol(int size);

int main() {
    printf("******************************************************************\n");
    printf("    ********** *********** ************ ************ *********\n");
    printf("       *******   ********     ********     ********    *******\n");
    printf("        ******    ******       ******       ******      ****\n");
    printf("         ***       ***          ***          ***         ***\n");
    printf("          *         *            *            *           *\n");
    printf("                    _ _ _   _ _ _   _ _ _   _ _ _\n") ;
    printf("                      |       |       |       |  \n");
    printf("                      |       |       |       |  \n");
    printf("                    _ _ _   _ _ _   _ _ _   |_|\n") ;
    printf("                  Welcome to the ICS project.\n");
    printf("                Our project is an Areas calculator.\n");

    int sides;
    printf("Enter the number of sides (0 [circle],3-6 [others]): ");
    scanf("%d", &sides);

    switch (sides) {
        case 0:
            float radius;
            printf("Enter the radius of the circle: ");
            scanf("%f", &radius);
            float area = AreaofCircle(radius);
            printf("Area of the Circle: %.2f square units\n", area);

           
            printHollowCircle((int)radius);
            break;
        
        case 3: {
            float s1, s2, s3;
            printf("Enter the sides of the triangle: ");
            scanf("%f %f %f", &s1, &s2, &s3);
            float area = AreaofTriangle(s1, s2, s3);
            printf("Area of the equilateral triangle: %.2f square units\n", area);

           
            printHollowTriangle((int)s1);
            break;
        }
        case 4: {
            float length, width, base, height, diagonal1, diagonal2;
            int choice;
            printf("Available choices are: 1)rectangle 2)parallelogram 3)rhombus 4)trapezium\n");
            printf("Enter the option of quadrilateral that you require: ");
            scanf("%d", &choice);

            switch (choice) {
                case 1:
                    printf("Enter the length and width of the rectangle: ");
                    scanf("%f %f", &length, &width);
                    float areaRect = AreaofRectangle(length, width);
                    printf("Area of the rectangle: %.2f square units\n", areaRect);

                   
                    printHollowRectangle((int)length, (int)width);
                    break;
                case 2:
                    printf("Enter the base and height of the parallelogram: ");
                    scanf("%f %f", &base, &height);
                    float areaPara = AreaofParallelogram(base, height);
                    printf("Area of the parallelogram: %.2f square units\n", areaPara);

                    
                  void HollowParallelogram(height, base);
                    printHollowParallelogram(height, base); 
                    break;
                case 3:
                    printf("Enter the diagonals of the rhombus: ");
                    scanf("%f %f", &diagonal1, &diagonal2);
                    float areaRhom = AreaofRhombus(diagonal1, diagonal2);
                    printf("Area of the rhombus: %.2f square units\n", areaRhom);

          
                    printHollowParallelogram(diagonal1, diagonal2); 
                    break;
                case 4:
                    float side1, side2, trapHeight;
                    printf("Enter the sides and height of the trapezium: ");
                    scanf("%f %f %f", &side1, &side2, &trapHeight);
                    float areaTrap = AreaofTrapezium(side1, side2, trapHeight);
                    printf("Area of the trapezium: %.2f square units\n", areaTrap);

    
                    printHollowTrapezium((int)trapHeight);
                    break;
                default:
                    printf("Invalid choice for quadrilateral!\n");
            }
            break;
        }
        case 5: {
            float side, apothemlength;
            int choice;
            printf("Available choices are: 1)knowing side and apothem length 2)knowing only length\n");
            printf("Enter the option of pentagon that you require: ");
            scanf("%d", &choice);

            switch (choice) {
                case 1:
                    printf("Enter the side and apothem length of pentagon1: ");
                    scanf("%f %f", &side, &apothemlength);
                    float areaPent = AreaofPentagon1(side, apothemlength);
                    printf("Area of the regular pentagon: %.2f square units\n", areaPent);

                 
                    printHollowPentagon((int)side);
                    break;
                case 2:
                    printf("Enter the side length of the regular pentagon2: ");
                    scanf("%f", &side);
                    printf("Area of the regular pentagon: %.2f square units\n", AreaofPentagon2(side));

                    printHollowPentagon((int)side);
                    break;
                default:
                    printf("Invalid choice for pentagon!\n");
            }
            break;
        }
        case 6: {
            float side;
            printf("Enter the side length of the regular hexagon: ");
            scanf("%f", &side);
            float areaHex = AreaofHexagon(side);
            printf("Area of the regular hexagon: %.2f square units\n", areaHex);
             
            printHollowHexagon((int)side);
            break;
        }
        default:
            printf("Invalid number of sides entered!\n");
    }

    return 0;
}


float AreaofTriangle(float s1, float s2, float s3) {
    float s = (s1 + s2 + s3) / 2;
    float area = sqrt(s * (s - s1) * (s - s2) * (s - s3));
    return area; 
}

float AreaofRectangle(float length, float width) {
    return length * width; 
}

float AreaofParallelogram(float base, float height) {
    return base * height; 
}

float AreaofRhombus(float diagonal1, float diagonal2) {
    return (diagonal1 * diagonal2) / 2;
}

float AreaofTrapezium(float side1, float side2, float height) {
    return ((side1 + side2) * height) / 2;
}

float AreaofPentagon2(float side) {
    return (1.0 / 4.0) * sqrt(5 * (5 + 2 * sqrt(5))) * side * side; // Pentagon with side
}

float AreaofPentagon1(float side, float apothemlength) {
    return (5.0 / 2.0) * (side) * (apothemlength); // Pentagon with side and apothem length
}

float AreaofHexagon(float side) {
    return 1.5 * sqrt(3) * side * side; // For regular hexagon
}

void printHollowRectangle(int length, int width) {
    for (int i = 1; i <= length; i++) {
        for (int j = 1; j <= width; j++) {
            if (i == 1 || i == length || j == 1 || j == width) {
                printf("* ");
            } else {
                printf("  ");
            }
        }
        printf("\n");
    }
}

void printHollowTriangle(int height) {
    for (int i = 1; i <= height; i++) {
        for (int j = 1; j <= i; j++) {
            if (i == height || j == 1 || j == i) {
                printf("* ");
            } else {
                printf("  ");
            }
        }
        printf("\n");
    }
}

void printHollowParallelogram(int rows, int columns) {
    int i, j;
    for (i = 1; i <= rows; i++) {
        for (j = 1; j <= rows - i; j++) {
            printf(" ");
        }

        for (j = 1; j <= columns; j++) {
            if (i == 1 || i == rows || j == 1 || j == columns) {
                printf("*");
            } else {
                printf(" ");
            }
        }

        printf("\n");
    }
}

void printHollowTrapezium(int size) {
    printf("\n Size : %d \n\n", size);
    int i = 0;
    int j = 0;
    int first = 1;
    int second = (size * size) + 1;
    int back = size;

    for (i = 0; i < size; i++) {
        space(i + i);

        for (j = 0; j < (size - i); ++j) {
            printf("*");

            if (j != size - i - 1) {
                printf(" ");
            }
        }
        back--;

        for (j = size; j > i; --j) {
            printf("*");

            if (j - 1 != i) {
                printf(" ");
            }
        }

        printf("\n");
    }
}



void printHollowRhombus(int diagonal1,int diagonal2 ) {
   void printHollowParallelogram( diagonal1,diagonal2);
}
void print_symbol(int size)
{
	int counter = 0;
	for (counter = 0; counter < size; counter++)
	{
		printf("* ");
	}
}

  void printHollowHexagon(int size)
  {
	if (size < 2)
	{
		return;
	}
	
	int mid = size / 2;
	int i = 0;

	for (i = 0; i < size; ++i)
	{
		space(size - i);
		if (i == 0)
		{
			
			print_symbol(size);
		}
		else
		{
			printf("*");
			space(((size - 1) * 2) + i * 2 - 1);
			printf("*");
		}
		printf("\n");
	}

	for (i = 1; i < size; ++i)
	{
		space(i + 1);
		if (i + 1 == size)
		{
		
			print_symbol(size);
		}
		else
		{
			printf("*");
			space(((size - 1) * 4) - i * 2 - 1);
			printf("*");
		}
		printf("\n");
	}
  }

   void space(int size)
   {
  int counter = 0;
  for (counter = 0; counter < size; counter++)
  {

    printf(" ");
  }
}

void printHollowPentagon(int height)
{
  if (height < 0)
  {
    return;
  }
  int j = 2;
  for (int i = 0; i <= (height - 1) * 2; ++i)
  {
    if (i < height)
    {
      space(height * 2 - (i * 2));
      printf("*");
      space((i * 2) * 2 - 1);
      if (i > 0)
      {
        printf("*");
      }
    }
    else
    {
     
      space(j + 1);
      if (i == (height - 1) * 2)
      {
        print_symbol((height - 1) * 2 - (i - height));
      }
      else
      {
        printf("* ");
        space((height - 1) * 4 - j * 2);
        printf("*");
      }
      j++;
    }
    printf("\n");
  }
}
float AreaofCircle(float radius){
    return 3.14*(radius)*(radius);
}
void printHollowCircle(int radius ){
    const int TOL = 5;

for(int x = -radius; x <=radius ; x++)
  {
  for(int y = -radius; y <=radius ; y++)
  {

    int eq = x*x + y*y - radius*radius ;

    printf(abs(eq) < TOL ? "*" : " ");

  }

  printf("\r\n");

}
}
