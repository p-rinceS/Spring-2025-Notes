

execve(v\[0], v, 0); 

```C
int main (int argc, char *argv[]){
	char *v[3];
	if (argc < 2) {
		printf("Please type a file name");
		return 1;
	}

		v[0] = "bin\cat"; v[1] = argv[1]; v[2] = 0;

	execve(v[0], v, 0); // This is safe because code and data are clearly separated; there is no way for user data to become the code.
	
	return 0;
}
```

