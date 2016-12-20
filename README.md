# myfirst
school work
#include<stdio.h>
#include<stdlib.h>
#include<time.h>
int Prod();
int Guessn(guess);
void Judge(magic,guess);
main()
{ 
  int magic,guess,m;
  char p;
  do{  magic=Prod(); 
    m=1;  
  do{
    m++;
    guess=Guessn();
    Judge(magic,guess);
    }while(m<=10&&guess!=magic);
    printf("if you want to again plase input 'y''Y'(continue) or'n''N'(end):");
    scanf("%s",&p);
    }while(p=='y'||p=='Y');
 }
    int Prod()
    { 
    int i;
    srand(time(NULL));
    i=rand()%100+1;
    return i;
    }
    int Guessn()
    { 
    int ret,guess;
    printf("plase enter the guess number:");
    ret=scanf("%d",&guess);
    while(ret!=1) {  while(getchar()!='\n');
    printf("plase enter the guess number:");
    ret=scanf("%d",&guess);
    } 
    return guess;
    }
    void Judge(magic,guess)
    {
    if(magic>guess)
    printf("too small!\n");
    else if(magic<guess)
    printf("too big!\n");
    else 
    printf("right!\n");
    }
