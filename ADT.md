# include<stdio.h>
# include<stdlib.h>

struct myArray
{
    int total_size;
    int used_size;
    int *ptr; //* means first elemnt of array
};

void createArray(struct myArray * a, int tSize, int uSize)       // void for function 
{                       
    // (*a).total_size = tSize;
    // (*a).used_size = tSize;
    // (*a).ptr = (int *) malloc(tSize*sizeof(int)); 
    
     a->total_size = tSize;
     a->used_size = tSize;
     a->ptr = (int *) malloc(tSize*sizeof(int));// * means value of operator =
}

void show(struct myArrey *a){
    for (int i = 0; i < a->used_size; i++)
    {
        printf("%d\n", (a->ptr)[i]);
    }
    
}

int main(){
struct myArray marks;
createArray(&marks, 10, 2);
show(&marks);

return 0;
}

