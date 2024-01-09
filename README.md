#include<iostream>
#include<fstream>
using namespace std;
int main ()
{
    char input1[255];
    char input2[255];
    char input3[255];
    cout<<"Enter your name : "<<endl;
    cin.getline(input1,sizeof(input1));
    cout<<"Enter your phone number : "<<endl;
    cin.getline(input2,sizeof(input2));
    cout<<"Enter your address : "<<endl;
    cin.getline(input3,sizeof(input3));
    fstream outputFile("output.txt",ios::app);
    if (outputFile.is_open())
    {
        outputFile<<input1<<" "<<input2<<" "<<input3<<endl;
        outputFile.close();
        cout<<"Input appended to the file sucessfully!";
    }
    else
    {
        cout<<"Unable to to open file for appending ";
    }
}
