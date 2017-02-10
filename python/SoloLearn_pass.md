Solo Learn - python 앱을 통해서 배운것들.

1. 코드 시작부분에 """ 를 이용해서 코드의 내용을 정리해줍니다. 이 부분은 주석으로 처리되며 엔터를 쳐도 인식합니다.
2. 수식부분
	// 는 나누기의 몫(quotient), % 는 나머지.
	! (exlamation)
	
3. input 입력을 받을때 사용합니다.
4. type conversion 이 가능합니다.
5. del var 로 var 삭제가 가능합니다. 실제 값이 사라지는것은 아니며 가리키는 링크를 삭제합니다. 아무도 가리키지 않는 값은 가비지 컬렉터가 삭제합니다.
6. Ture False 첫글자가 대문자 입니다.
7. elif (다른 언어의 else if )
8. ** (exponentiation) 제곱표시입니다. 2**3 은 2의 3승이라는 뜻입니다.
9. while e=2; 의 형식으로 사용디며 break 로 종료 가능합니다. 종료 없이 다음 whlie 문을 돌리려면 continue를 사용합니다.
10. none 이 null을 뜻합니다.
11. yield 값을 리턴하지만 break 처럼 종료시키지 않습니다.

List 관련
1. [] (square brakets)
2. {} (curly braces)
3. in 을 사용하면 list 안에 해당 값이 존재하는지 확인합니다.
4. .append 로 값을 리스트 마지막에 추가합니다.
5. len()으로 길이를 확인합니다.
6. 사용할 때 .이름 은 메소드, 이름() 은 펑션입니다.
7. insert(num,thing) 으로 원하는 위치에 삽입합니다.
8. max(), min() 이 있습니다.
9. .count	.remove	.reverse
10. range(start,end,interval) 로 조건에 맞는 값을 표현합니다. 
 - range(0,10,2) 는 0부터 9까지 2 간격으로 표현합니다.
 11. "str {0}{1}".format(nums[0],nums[1]) 사용가능합니다.
 
 
 Function 관련
 1. def func(x,y,z="spam") 으로 함수를 생성 및 초기화 합니다.
 2. return 은 값을 내놓고 함수를 종료합니다.
 3. # 한줄 주석입니다.
 4. from math import pi as py 로 모듈을 불러옵니다.
 5. try :  except  sth,sth2 로 트라이 익셉션 사용합니다.
 6. finally 로 에러와 상관없이 출력합니다.
 7. raise errortype("str") 로 에러타입을 출력합니다.
 8. assert 로 에러를 조건절로 생성합니다.
 9. cont = file.read() 나 file=readlines() 로 파일을 읽습니다.
 10. file.close() 로 연 파일은 닫아주어야 합니다.
 11. def mfunc(x,**kwargs): mfunc(7,a=5,b=7) 이방법으로 여러변수를 한번에 선언합니다.
 
 dictionary
 1.age={"a":22} 같은 형태로 선언합니다.
 2. in 이나 not in 가능합니다.
 3. age.get(key) 로 키값에 연결된 값 출력합니다.
 
 tuple
 1. 리스트보다 빠릅니다.
 2. 값 제거가 안됩니다.
 
 class
 1. constructor __init__ 
 2. class son(dad) 로 상속가능합니다(inheritance)
 3. 추상화의 개념으로 __var , _func__var 가 있습니다. __var 로 외부에서 접속하기 못하게 설정한 후 _func__var 로 값을 얻는 방식입니다.
 
 Regular Expression 
 정규식으로 다양한 문자열을 검색합니다.
 
pep8
권장되는 규칙으로 강제력은 없습니다.
1. 모듈 이름은 짧게, 모두 소문자로
2. 클래스 이름은 CapStyleWord 
3. func,var 는 lowcases_with_underscores
4. constants 는 CAP_WITH_UNDERSCORES
5. 한 라인은 80글자를 넘지 않도록.
6. from module import * 는 지양하자.
7. 한 줄에 한 문장만.