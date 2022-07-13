#C 

### gcd

```C
#include <stdio.h>
int main(){
int mod, i, j;

scanf("%d%d", &i, &j);
while ((i % j) != 0){
    mod = i%j;
    i = j;
    j = mod;
}
printf("%d", j);

}
```

### 找質數
```C
#include  <stdio.h>
#include <stdbool.h>
#define ARRAYSIZE 100
bool prim[ARRAYSIZE];
int main(){
for (int i = 0; i < ARRAYSIZE; i++){
    prim[i] = true;
}
prim[0] = false;
prim[1] = false;
for (int j = 2; j*j <= ARRAYSIZE; j++){
        int k = 2;
        while (j*k < ARRAYSIZE){
            //printf("%d\n", j*k);
            prim[j*k] = false;
            k++;
        }
}

for (int i = 0; i <= ARRAYSIZE; i++){
    if (prim[i]){
        printf("%d\n", i);
    }
}

}
```

### bobble sort
```C
#include  <stdio.h>
#include <stdbool.h>
#include<math.h>
#define ARRAYLEN 5

int main() {

    int arr[ARRAYLEN];
    for (int i = 0; i < ARRAYLEN; i++) {
        scanf("%d", &arr[i]);
    }

    for (int i = 0; i < ARRAYLEN - 1; i++) {
        for (int i = 0; i < ARRAYLEN - 1; i++) {
            int k = i + 1;
            if (arr[k] > arr[i]){
                int tmp = arr[i];
                arr[i] = arr[k];
                arr[k] = tmp;
            }
        }
    }

    for (int i = 0; i < ARRAYLEN; i++){
        printf("%d", arr[i]);
    }
}
```
