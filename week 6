#include <stdio.h>
#include <stdlib.h>
#include <ctype.h>
#define MAX_SIZE 100
int stack[MAX_SIZE];
int top = -1;
void push(int item) {
if (top >= MAX_SIZE - 1) {
printf("Stack Overflow\n");
} else {
top++;
stack[top] = item;
}
}
int pop() {
if (top < 0) {
printf("Stack Underflow\n");
return -1;
} else {
return stack[top--];
}
}
int evaluateExpression(char* exp) {
int i, operand1, operand2, result;
for (i = 0; exp[i] != '\0'; i++) {
if (isdigit(exp[i])) {
push(exp[i] - '0');
} else {
operand2 = pop();
operand1 = pop();
switch (exp[i]) {
case '+':
push(operand1 + operand2);
break;
case '-':
push(operand1 - operand2);
break;
case '*':
push(operand1 * operand2);
break;
case '/':
push(operand1 / operand2);
break;
}
}
}
result = pop();
return result;
}
int main() {
char exp[MAX_SIZE];
printf("Enter the arithmetic expression: ");
scanf("%s", exp);
int result = evaluateExpression(exp);
printf("Result: %d\n", result);
return 0;
}
OUTPUT

Enter the arithmetic expression: 55
Result: 5
 
