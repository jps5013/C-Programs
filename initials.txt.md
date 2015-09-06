# CS50

#include <stdio.h>
#include <cs50.h>
#include <string.h>
#include <ctype.h>

int main(void)
{
    // Get name and store in name
    string name = GetString();
    
    // taking care of corner cases 
    if (name != NULL)  
    { 
    
    // converting the first character in the string array to upper case
        name[0] = toupper(name[0]);
        printf("%c", name[0]);
        
        
        // initialize a loop that measure the entire string, and then iterates actions in the body over the entire string length           
        for(int i = 0, n =strlen(name); i < n; i++)
        {
            // looking at the ith char of the string and determining if it is a space
            // if the ith char of the string is not a space, then we do nothing.
            if (name[i] == ' ')
            /** how would I say if(name[i] == ASCII 32? ex if(name[i] == %d32)
             *  is there a reason isspace() is better than this method?
             */
            {
                printf("%c", toupper(name[i + 1])); 
                /** 
                 * how does c know what 1 is? 
                 * I declared name as a string, and i as an int
                 * so how does c know that + 1 moves to the next char in the
                 *string (char array) that is name?
                 **/
            } 
            /** should i have a return somewhere in here? 
             *  main is a function that returns an int and takes no inputs (void)
             *  the paramaters of the main function is the entire body
             *  so shouldnt I have to specify return = 0 at the end of my body
             *  for main to work?
             */
        }  
        
    }
    printf("\n");
}