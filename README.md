https://www.cnblogs.com/nikiss/p/14208341.html

void Crash1()
{
 char * p =(char*)100;
 *p=100;
}

void Crash2();
int main(int argc,char* argv[])
{
        Crash2();
        return 0;
}

void Crash2()
{
        char p[1];
        strcpy(p,"0123456789");
}



#include <iostream>
#include <fstream>
#include <math.h>
#define PI 3.1415927
using namespace std;

void write_wave(ostream *p, double wl, int amp, double hl, long length){
int height;
for (int i = 0; i < length; i ++){
height = (int)(sin(i * 2 * PI / wl) * amp * pow(2, -(i / hl)));
cout << (char *)height << endl; system("pause");
p->write((char *)height, sizeof(int));
}
return;
}

int main(){
int t;
ofstream outfile("C:\\Users\\Mark\\testwave.dat", ios::out|ios::binary);
write_wave(&outfile, 80.0, 20000, 80000.0, 200000);
outfile.close();
return 0;
}
  
void main()
{
char *a="xyz";
*a='1';
cout<<*a<<endl;
}
