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
## 2023-12-07 진행
## 문자열 9번
```c++
#include <iostream>
#include <algorithm>
#include <string>

int reverse(int n) {
    std::string s = std::to_string(n);
    reverse(s.begin(), s.end());
    return atoi(s.c_str());
}

int max(int a, int b) {
    int final;
    if (a > b) {
        final = a;
    }
    else if (a < b)
    {
        final = b;
    }
    return final;
}

int main() {

    int num1, num2, result;
    std::cin >> num1;
    std::cin >> num2;
    
    num1 = reverse(num1);
    num2 = reverse(num2);
    
    result = max(num1, num2);

    std::cout << result;

    return 0;
}
```
## 2023-12-08 진행
## 문자열 10번 - 실패.. 한번 더 도전예정
```c++
#include <iostream>
#include <string>
using namespace std;
int main() {

	/* 다이얼 번호 돌리기
	   숫자 1 클릭 시 2초가 소요된다.
	   숫자 1에서 한칸 옆으로 가면 1초가 더 소요된다.
	   숫자별로 영단어가 적혀있다.
	   ex) UNUCIC -> 868242 -> 시간 초를 구하는 형태의 프로그램 구현

	  입력 : 첫째 줄 알파벳 대문자로 이루어진 단어가 주어진다. 단어의 길이는 2보다 크거나같고 15보다 작거나 같다.
	*/
	string phone; 
	int result = 0, time, i;
	cin >> phone;
	int alphabatCnt[26] = {};
	
	for (char c: phone) {
		alphabatCnt[c - 'A']++;
	}
	for (i = 0; i <= 'Z' - 'A'; i++) {
		if (i == 'S' - 'A' || i == 'V' - 'A') {
			result += (i / 3 + 2) * alphabatCnt[i];
			continue;
		}
		if (alphabatCnt[i]) {
			time = i / 3 + 3;
			result += (time > 9) ? 10 * alphabatCnt[i] : time * alphabatCnt[i];
		}
	}
	cout << result;
	return 0;
}
```
## 2023-12-11 진행
## 문자열 11번
```c++
#include <iostream>
#include <string>
#include <algorithm>

int main() {
	/*
		그대로 출력하기
		입력 받은 대로 출력하는 프로그램을 작성하시오
		알파벳 소문자, 대문자, 공백, 숫자로만 이루어있다. 각줄은 100 페이지글자만 안넘으며, 빈 줄은 주이지않는다.
		또 각 줄은 공백으로 시작하지 않고 공백으로 끝나지 않는다.
	*/
	int test = 1;
	std::string inputStr;
	while (true) {
		
		std::getline(std::cin, inputStr);
			if (inputStr == "")
				break;
		std::cout << inputStr << "\n";
		
		test++;
	}
	return 0;
}
```
## 2023-12-12 진행
## 심화1-1
```c++
#include <iostream>
#include <string>

using namespace std;

int main(int argc, char const* argv[]) {

	string s = "         ,r'\"7\n";   // \", \n 이 제어문자다.
	s += "r`-_   ,'  ,/\n";    // \n 이 제어문자다.
	s += " \\. \". L_r'\n";    // \\, \", \n 이 제어문자다.
	s += "   `~\\/\n";         // \\, \n 이 제어문자다.
	s += "      |\n";           // \n 이 제어문자다.
	s += "      |";
	cout << s;
	return 0;
}
```