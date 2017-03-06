장고걸즈 튜토리얼을 하면서 알게된 점을 정리하겠습니다.

1. __ 더블언더스코어는 줄여서 "던더" 라고도 합니다.
2. www.pythonanywhere.com 에서 블로그를 만들고 gitgub를 끌어오면 배포가 쉬워집니다.
3. setting.py 의 ALLOWED_HOSTS 옵션에 호스트를 넣어주어야 웹앱 구동이 가능합니다(장고걸즈엔 없음)
4. 당연한거지만.. 윈도우 기반 코드를 리눅스에 올리면 돌아가지 않습니다(venv 등). 때문에 venv 같은 코드는 git에서 제외하고 순수 파이썬 코드만 커밋하는게 좋습니다.
5. 객체를 정렬할때 Post.objects.filter(dated_date__lte=timezone.now()).order_by('-dated_date') 의 방식으로 정렬 가능하며 -dated_date 는 desc 방식으로 정렬합니다. dated_date 는 asc 이며, 기본값 입니다.
6. 배포는 www.pythonanywhere.com 에서 연습합니다. 
	git clone https://github.com/DrakeYang/DateFood.git
	
	$ cd DateFood
	$ virtualenv --python=python3.4 venv
	$ source myvenv/bin/activate
	(mvenv) $  pip install django whitenoise
	(mvenv) $ python manage.py collectstatic
	이후 yes 입력
	(mvenv) $ python manage.py migrate
	(mvenv) $ python manage.py createsuperuser
	
	웹 카테고리에 Add a new web app 클릭
	수동설정(manual configuration)클릭
	Python 3.4을 선택하고 다음(Next)를 클릭
	가상환경 섹션의 Enter the path to a virtualenv 에 입력 : 
	/home/YangTheProgrammer/DateFood/venv/
	
	WSGI configuration file 에 입력 : 
import os
import sys

path = '/home/YangTheProgrammer/DateFood' 
if path not in sys.path:
    sys.path.append(path)

os.environ['DJANGO_SETTINGS_MODULE'] = 'mysite.settings'

from django.core.wsgi import get_wsgi_application
from whitenoise.django import DjangoWhiteNoise
application = DjangoWhiteNoise(get_wsgi_application())

	settings 파일에 yangtheprogrammer.pythonanywhere.com 도메인 추가
	
	Reload 버튼 클릭
	생성되는 링크 클릭하면 배포 확인 가능