# test
test
#include<iocc2530.h>
#define D3 P1_0
void delay(unsigned int i)
{
  unsigned int j,k;
  for(j = 0;j < i;j++)
  for(k = 0;k < 550;k++);
}
void main()
{
  P1SEL &= ~0X01;
  P1DIR |= 0X01;
  P1 = 0X00;
  while(1)
  {
    D3 = !D3;
    delay(1000);
  }
}
