# ex3.17_C_how_to_program
#include <stdio.h>


/* Exercise 3.17 [C : How to Program, 7th Edition by Paul Deitel, Harvey Deitel]
 Solution provided by Chijioke Ahuchogu                                     */


int main()
{
    float begBal = 0, totalCharges = 0, totalCredits = 0 , credLimit = 0, newBalance  = 0;
    int accNo;
    
    printf("Enter account number (-1 to end) : ");
    scanf("%d", &accNo);
    
    while ( accNo != -1) {
    
            printf("Enter beginning balance : ");
            scanf("%f", &begBal);
    
            printf("Enter total charges: ");
            scanf("%f", &totalCharges);
    
            printf("Enter total credits : ");
            scanf("%f", &totalCredits);
    
            printf("Enter credit limit : ");
            scanf("%f", &credLimit);
        
            newBalance = begBal + totalCharges - totalCredits;
        
        
            printf("Account:\t\t %d\n" , accNo);
            printf("Credit Limit: %.2f\n" , credLimit);
            printf("Balance:\t\t %.2f\n", newBalance);
        
            if (newBalance > credLimit) {
                printf("Credit Limit Exceeded\n");
            }
        
            printf("Enter account number (-1 to end) : ");
            scanf("%d", &accNo);
    }
}
