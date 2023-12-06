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
```
## 2023-12-01 진행
## 문자열 4번
```c++
#include <iostream>
#include <string>
using namespace std;

int main()
{
    char str;
    std::cin >> str;
    int number = static_cast<int>(str);
    std::cout << number;
 
    return 0;
}
```
## 문자열 5번
```c++
#include <iostream>
#include <string>
using namespace std;
/*
첫째줄에는 입력한 숫자 count
둘째줄에는 숫자의 합
*/
int main() {

    int num1;
    std::cin >> num1;
    char num2;

    int sum = 0;

    for (int i = 0; i < num1; i++)
    {
        std::cin >> num2;
        sum += num2 - '0';
    }

    std::cout << sum << "\n";

    return 0;
}
```
## 2023-12-04 진행
## 문자열 6번
```c++
#include <iostream>
#include <string>
using namespace std;
int main() {
    string s;
    string alphabet = "abcdefghijklmnopqrstuvwxyz";
    cin >> s;
    for(int i = 0; i < alphabet.length(); i++)
        cout << (int)s.find(alphabet[i]) << " ";
    return 0;
}
```
## 2023-12-05 진행
## 문자열 7번
```c++
#include <iostream>
#include <string>

int main(){
	int i, j, selectNum, workNum;
	std :: string str, result;
	// 반복 문자열 개수 ex) 2번 사용
	std :: cin >> selectNum;
	while(selectNum>0){
		// 문자 반복 횟수 지정
		std :: cin >> workNum;
		std :: cin >> str;
		// 문자 반복 횟수 지정을 한다.
		for(i=0; i<str.length(); i++){
			for(j=0; j<workNum; j++){
				std :: cout <<str[i];
			}//for
		}//2for
		std :: cout << "\n";
		selectNum--;
	}//while
	return 0;
}
```
## 2023-12-06 진행
## 문자열 8번
```c++
#include <iostream>
#include <string>

int main() {

    int cnt = 0;

    std::string str;
    getline(std::cin, str);
    cnt = 1;
   
    for (int i = 0; i < str.length(); i++) {
        if (str[i] == ' ') {
            cnt++;
        }
    }

    if (str[0] == ' ') {
        cnt--;
    }
    
    if (str[str.length() - 1] == ' ') {
        cnt--;
    }

 
    std::cout << cnt << "\n";

    return 0;
}
```