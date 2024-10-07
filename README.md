# Ex-6-Pseudorandom-Number-Generation

## Aim:
To implement Pseudorandom Number Generation using the standard library functions in C.

## Algorithm:
1.Seed the random number generator using srand() to initialize it with a starting value.
2.Generate pseudorandom numbers using rand().
3.To ensure different results on each execution, seed srand() with a dynamic value like the current time (time(NULL)).
4.Use modulo operation to limit the range of generated numbers.

## Program:
```

#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() 
{
    int count, min, max;
    printf("Enter the number of random numbers to generate: ");
    scanf("%d", &count);
    printf("Enter the minimum value: ");
    
    scanf("%d", &min);
    printf("Enter the maximum value: ");
    scanf("%d", &max);
    srand(time(NULL));
    printf("Pseudorandom numbers:\n");   
    for (int i = 0; i < count; i++) 
    {
        int random_number = (rand() % (max - min + 1)) + min;
        printf("%d\n", random_number);
    }
    return 0;
}

```

## Output:
![image](https://github.com/user-attachments/assets/df53d99b-1dec-4189-89c2-6bf64148e7e0)



## Result:
Thus, the pseudorandom number generation was successfully implemented using the standard library functions srand() and rand().
