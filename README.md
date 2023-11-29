#  algorithm_Study
 알고리즘 공부

## 2023-11-28 복습
## 문자열 1번 문제
```c++
#include <iostream>
#include <string>

int main(void) {
	std::string str;
	int select;
	std::cin >> str;
	std::cin >> select;
	std::cout<< str[select-1];
}

```
## 문자열 2번 문제
```c++
#include <iostream>
#include <string>

int main(void) {
	std::string str;
	std::cin >> str;
	std::cout << str.length();
}
```
## 문자열 3번 문제
```c++
#include <iostream>
#include <string>

int main(void) {
	std::string str;
	int i,selectNum;
	std::cin >> selectNum;
	
	for (i = 0; i < selectNum; i++) {
		std::cin >> str;
		std::cout << str[0] << str[str.size()-1] << '\n';
	}//for

}
## 2023-11-29 진행예정