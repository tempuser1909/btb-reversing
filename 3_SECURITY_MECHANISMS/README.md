# 3. SECURITY MECHANISMS

#### DEP/NX
- GCC compiled by default
- to disable use ```-fno-stack-protector```
- to prevent CPU from executing assembly code on stack --> prevents attacker to write code on stack (aka send with payload)

#### ASLR
- to randomise the head of the starting location --> to prevent attackers from using static memory addresses
- is machine-to-machine basis
- it is a setting on your machine at ```/proc/sys/kernel/randomize_va_space```
	- 0 --> disable
	- 1 --> conservative randomization
	- 2 --> full randomization

#### Canary/Stack Cookie
Pseudoecode of canary:
```c
int cookie_value = randomized_each_run();

int func1(){
	int cookie = cookie_value;
	
	...
	normal function stuff
	...

	if(cookie != cookie_value){
		printf("Error, exploitation detected!!!");
	}
	return 0;
}
```
- usually can see from assembly --> call stack_chk_fail

#### Reference links
- https://askubuntu.com/questions/318315/how-can-i-temporarily-disable-aslr-address-space-layout-randomization