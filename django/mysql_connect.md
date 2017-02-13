django 에서 mysql 을 연동했습니다.

진행순서.
0. django 설치
 - 연동 전 이미 설치되었음
1. mysql 설치
 - localhost 로 테스트하기로함
2. mysql database 생성 
 - 이부분이 다른 글에는 안나와서 당황함. 당연한 부분이라 따로 표시하지 않은걸로 추정. 생성하지 않으면 밑의 makemigration 명령어 실행시  없는 데이터베이스 라고 엑세스 거부가 뜸.
3. django library 설치 - PyMySQL, mysql-connector-python 
 - 한개씩 설치하고 테스트한 부분이 아니라 둘중 하나만 있어도 되는지는 미확인
4. polls/models.py 에 클래서 선언으로 테이블 설정
 - 장고는 클래스로 테이블을 설정해서 migrate 로 생성할 수 있다
5. misite/settings.py 의 DATABASES 설정 수정
 - 원래부분 주석처리하고 MySQL 용으로 수정
	'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'django_test',
        'USER': 'admin',
        'PASSWORD': 'admin',
        'HOST': 'localhost',
        'PORT': '3306',
        #'ENGINE': 'django.db.backends.sqlite3',
        #'NAME': os.path.join(BASE_DIR, 'db.sqlite3'),
    }
6. 명령 manage.py makemigration
7. 명령 manage.py migrate
8. 실제 db에 테이블이 생긴걸 확인