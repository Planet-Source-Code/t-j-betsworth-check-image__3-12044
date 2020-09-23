<div align="center">

## Check Image


</div>

### Description

displays a 8x8 square check image
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[T J Betsworth](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/t-j-betsworth.md)
**Level**          |Advanced
**User Rating**    |4.0 (8 globes from 2 users)
**Compatibility**  |C\+\+ \(general\)
**Category**       |[Miscellaneous](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/miscellaneous__3-1.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/t-j-betsworth-check-image__3-12044/archive/master.zip)





### Source Code

```
#include <iostream>
#include <stdlib.h>
#include <windows.h>
using namespace std;
HANDLE hout = GetStdHandle(STD_OUTPUT_HANDLE);
int x=18; int y = 3;
void check()
 {
  for(int a = 0;a <12;a++){
  for(int b = 0;b <8;b++){
  COORD coord = {x+a,y+b};
  SetConsoleCursorPosition(hout,coord);
  if ((a==0||a==1||a==2||a==3||a==4||a==5)&&(b==0||b==1||b==2||b==3))
  {
    SetConsoleTextAttribute(hout,119);
    cout<<char(219);
  }
  if ((a==6||a==7||a==8||a==9||a==10||a==11)&&(b==4||b==5||b==6||b==7))
  {
    SetConsoleTextAttribute(hout,119);
    cout<<char(219);
  }
  else
  {
  SetConsoleTextAttribute(hout,85);
  cout<<char(219);
  }
 }
 }
  }
int main()
   {
COORD coord = {84,40};
SMALL_RECT rec = {0, 0, 0, 0};
SetConsoleScreenBufferSize(hout, coord);
rec.Right = coord.X -1;
rec.Bottom = coord.Y -1;
SetConsoleWindowInfo(hout,TRUE,&rec);
SetConsoleTitle("Check Image");
for (int i=0; i<16; i++){
check();
y+=8;
if(y > 27)
  {
  y = 3;
  x += 12;
 }
 }
COORD coord1 = {27,37};
SetConsoleCursorPosition(hout, coord1);
SetConsoleTextAttribute(hout,9);
system("PAUSE");
return 0;
}
```

