//Heap data structure in C++
//Heap is used to to store value using array where node data is greater
//Than its both child or its less than its both child
//While deleting data always top value is deleted from heap
#include<iostream.h>
#include<conio.h>
class Heap
{
private:
  int cap;
  int top;
  int *arr;
public:
  Heap(int cap)
  {
    top=0;
    arr=new int[cap];
    this->cap=cap;
  }
  void insert(int data);  //Done
  void deleteData();      //Done
  void display();         //Done
  //int isReplacementRequired(int data,int i);
  /*                                       |
  int returnGreater(int data1,int data2)   |    FUNCTION FOR SIMPLE VERSION
  {                                        |    OF DELETION IN HEAP
    if(data1>data2)                        |
      return(data1);                       |    *return geater value
    else                                   |
      return(data2);                       |
  }  */
  ~Heap()
  {
    delete []arr;
  }
};
/*                                                   |   FUNCTION FOR
int Heap::isReplacementRequired(int data,int i)      |   SIMPLE VERSION FOR
{                                                    |   DELETION IN HEAP
int largeValue;                                      |
  if(2*i+2<top)                                      |
  {                                                  |   *state whether
    largeValue=returnGreater(arr[2*i+1],arr[2*i+2]); |   replacement will be
    if(largeValue>data)                              |   done with first
    {                                                |   child, second child
      if(largeValue==arr[2*i+1])                     |   or no requirement of
	return(1);                                   |   replacement
      else                                           |
	return(2);                                   |
    }                                                |
    else                                             |
      return(0);                                     |
  }                                                  |
  else if(2*i+1<top)                                 |
  {                                                  |
    if(arr[2*i+1]>data)                              |
      return(1);                                     |
    else                                             |
      return(0);                                     |
  }                                                  |
  else                                               |
    return(0);                                       |
} */
void Heap::deleteData()//Delete first data inside heap
{
int data;
  data=arr[top-1];
  arr[0]=data;
  int i=0;
/*                                         |
  int value;                               |
  repeat:                                  |
  value=isReplacementRequired(data,i);     |
  if(value==1)                             |     SIMPLE VERSION FOR
  {                                        |
    arr[i]=arr[2*i+1];                     |       DELETION IN HEAP
    i=2*i+1;                               |
    goto repeat;                           |
  }                                        |
  else if(value==2)                        |
  {                                        |
    arr[i]=arr[2*i+2];                     |
    i=2*i+2;                               |
    goto repeat;                           |
  }                                        |
  else                                     |
  {                                        |
    arr[i]=data;                           |
  }*/
  repeat:
  if(top>(2*i)+2)
  {
    if(arr[(2*i)+1]>arr[(2*i)+2])
    {
      if(arr[(2*i)+1]>data)
      {
	arr[i]=arr[(2*i)+1];
	i=(2*i)+1;
	goto repeat;
      }
      else
	goto end;
    }
    else
    {
      if(arr[(2*i)+2]>data)
      {
	arr[i]=arr[(2*i)+2];
	i=(2*i)+2;
	goto repeat;
      }
      else
	goto end;
    }
  }
  else if(top>(2*i)+1)
  {
     if(arr[(2*i)+1]>data)
      {
	arr[i]=arr[(2*i)+1];
	i=(2*i)+1;
	goto repeat;
      }
      else
	goto end;
  }
  else
  {
    end:
    arr[i]=data;
  }
  top--;
}
void Heap::display()  //Display data in heap
{
int i;
  cout<<"\n";
  for(i=0;i<top;i++)
    cout<<" "<<arr[i];
}
void Heap::insert(int data)    //Insert new data in Heap
{
int i;
if(top<cap)
{
  arr[top]=data;
  i=top;
  while(i!=0&&arr[(i-1)/2]<arr[i])
  {
    arr[i]=arr[(i-1)/2];
    arr[(i-1)/2]=data;
    i=(i-1)/2;
  }
  top++;
}
else
  cout<<"\nNot enough space for data";
}
void main()
{
  clrscr();
  Heap a(10);
  a.insert(15);
  a.insert(5);
  a.insert(16);
  a.insert(10);
  a.insert(20);
  a.deleteData();
  a.display();
  getch();
}












