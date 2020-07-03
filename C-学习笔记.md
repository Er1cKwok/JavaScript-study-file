### include
```
#include <studio.h>

#include "1.txt"

双引号：  // 先找当前目录，再去编译器目录找。
尖括号：  // 直接去编译器目录找
```

### 数组长度
```
int arr[] = {1, 2, 3};
int len = sizeof(arr) / sizeof (arr[0]);
```