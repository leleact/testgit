#二级指针
二级指针即是指向指针的指针

示例：
``` c
int movestr(char **s, int n) {
	*s = *s + n;
	return 0;
}
```


``` c
#include <stdio.h>
#include <string.h>
int main() {
	char s[20 + 1];
	memset(s, 0x00, sizeof(s));
	strcpy(s, "Hello World");
	char *ptr = s;
	movestr(&ptr, 4);
	printf("ptr = [%s]\n", ptr);
	return 0;
}
```