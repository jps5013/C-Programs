# CS50#include <stdio.h>
#include <cs50.h>
#include <string.h>
#include <ctype.h>
#include <stdlib.h>

int main(int argc, string argv[])
{
    int k = atoi(argv[1]);
    // int k = atoi( string argv[1]); 
    // why does using the reference50 notation cause the above to fail?
    // if( k != NULL)- why does this cause the program to fail?
    {
    
        if(k < 0)
        {
            return 1;
        }
        else
        {
            printf("%i\n", k);
            return 0;
        }
        return 0;
    }
}