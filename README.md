# codes1
t1
#include<iostream>
using namespace std;
char sq[10]={'0','1','2','3','4','5','6','7','8','9'};
int winorlose()
{
    if(sq[1]==sq[2] && sq[2]==sq[3])
    {
        return 1;
    }
    else if(sq[4]==sq[5] && sq[5]==sq[6])
    {
        return 1;
    }
    else if(sq[7]==sq[8] && sq[8]==sq[9])
    {
        return 1;
    }
    else if(sq[1]==sq[4] && sq[4]==sq[7])
    {
        return 1;
    }
    else if(sq[2]==sq[5] && sq[5]==sq[8])
    {
        return 1;
    }
    else if(sq[3]==sq[6] && sq[6]==sq[9])
    {
        return 1;
    }
    else if(sq[1]==sq[5] && sq[5]==sq[9])
    {
        return 1;
    }
    else if(sq[3]==sq[5] && sq[5]==sq[7])
    {
        return 1;
    }
     else if(sq[1]!='1' && sq[2]!='2' && sq[3]!='3' && sq[4]!='4' && sq[5]!='5' && sq[6]!='6'
      && sq[7]!='7' && sq[8]!=8 && sq[9]!='9')
    {
        return 0;
    }
    else
    {
        return -1;
    }

}
void xoboard()
{
   system("cls");
   cout<<"\n\nTIC TAC TOE GAME\n\n";
   cout<<"Player1(X) - Player2(O)"<<endl<<endl;
   cout<<endl;
   //code to draw xoboard
   cout << "     |     |     " << endl;
   cout << " " << sq[1] << "   |   " << sq[2] << " |   " << sq[3] << endl;
   cout << "_____|_____|_____" << endl;
   cout << "     |     |     " << endl;
   cout << " " << sq[4] << "   |   " << sq[5] << " |   " << sq[6] << endl;
   cout << "_____|_____|_____" << endl;
   cout << "     |     |     " << endl;
   cout << " " << sq[7] << "   |   " << sq[8] << " |   " << sq[9] << endl;
   cout << "     |     |     " << endl<<endl;
}
int main()
{
    int player=1,i,ch;
    char mark;
    do{

        xoboard();
        player=(player%2)?1:2;
        cout<<"Player"<<player<<", enter the number:";
        cin>>ch;
        mark=(player ==1)?'X' :'O';
        if(ch==1 && sq[1]=='1')
        {
            sq[1]=mark;
        }
        else if(ch==2 && sq[2]=='2')
        {
            sq[2]=mark;
        }
        else if(ch==3 && sq[3]=='3')
        {
            sq[3]=mark;
            }
        else if(ch==4 && sq[4]=='4')
        {
            sq[4]=mark;
        }
        else if(ch==5 && sq[5]=='5')
        {
            sq[5]=mark;
        }
        else if(ch==6 && sq[6]=='6')
        {
            sq[6]=mark;
        }
        else if(ch==7 && sq[7]=='7')
        {
            sq[7]=mark;
        }
        else if(ch==8 && sq[8]=='8')
        {
            sq[8]=mark;
        }else if(ch==9 && sq[9]=='9')
        {
            sq[9]=mark;
        }
        else{
            cout<<"INVALID MOVE!";
            player--;
            cin.ignore();
            cin.get();
        }
        i=winorlose();
        player++;
    }
    while(i==-1);
    xoboard();
    if(i==1){
        cout<<"\nCONGRATULATIONS!! PLAYER "<< --player<<" WINS!!";
    }
    else{
        cout<<"\nDRAW";
    }
    cin.ignore();
    cin.get();
    return 0;
}
