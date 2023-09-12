#include <stdio.h>

int main() {
    int b, Start, End;

    
    printf("Enter the base number: ");
    scanf("%d", &b);
    printf("Enter the range start: ");
    scanf("%d", &Start);
    printf("Enter the range end: ");
    scanf("%d", &End);

    printf("Multiples of %d within the range %d to %d that share common factors:\n", b, Start, End);

  
    for (int i = Start; i <= End; i++) {
        if (i % b== 0) {
            int a = i;
            int c= b;
            while (c != 0) {
                int temp = c;
                c= a % b;
                a = temp;
            }
            if (a > 1) {
                printf("%d = %d)\n", i, a);
            }
        }
    }

    return 0;
}
