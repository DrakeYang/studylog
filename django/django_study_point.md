������ Ʃ�丮���� �ϸ鼭 �˰Ե� ���� �����ϰڽ��ϴ�.

1. __ ���������ھ�� �ٿ��� "����" ��� �մϴ�.
2. www.pythonanywhere.com ���� ��α׸� ����� gitgub�� ������� ������ �������ϴ�.
3. setting.py �� ALLOWED_HOSTS �ɼǿ� ȣ��Ʈ�� �־��־�� ���� ������ �����մϴ�(����� ����)
4. �翬�Ѱ�����.. ������ ��� �ڵ带 �������� �ø��� ���ư��� �ʽ��ϴ�(venv ��). ������ venv ���� �ڵ�� git���� �����ϰ� ���� ���̽� �ڵ常 Ŀ���ϴ°� �����ϴ�.
5. ��ü�� �����Ҷ� Post.objects.filter(dated_date__lte=timezone.now()).order_by('-dated_date') �� ������� ���� �����ϸ� -dated_date �� desc ������� �����մϴ�. dated_date �� asc �̸�, �⺻�� �Դϴ�.
6. ������ www.pythonanywhere.com ���� �����մϴ�. 
	git clone https://github.com/DrakeYang/DateFood.git
	
	$ cd DateFood
	$ virtualenv --python=python3.4 venv
	$ source myvenv/bin/activate
	(mvenv) $  pip install django whitenoise
	(mvenv) $ python manage.py collectstatic
	���� yes �Է�
	(mvenv) $ python manage.py migrate
	(mvenv) $ python manage.py createsuperuser
	
	�� ī�װ��� Add a new web app Ŭ��
	��������(manual configuration)Ŭ��
	Python 3.4�� �����ϰ� ����(Next)�� Ŭ��
	����ȯ�� ������ Enter the path to a virtualenv �� �Է� : 
	/home/YangTheProgrammer/DateFood/venv/
	
	WSGI configuration file �� �Է� : 
import os
import sys

path = '/home/YangTheProgrammer/DateFood' 
if path not in sys.path:
    sys.path.append(path)

os.environ['DJANGO_SETTINGS_MODULE'] = 'mysite.settings'

from django.core.wsgi import get_wsgi_application
from whitenoise.django import DjangoWhiteNoise
application = DjangoWhiteNoise(get_wsgi_application())

	settings ���Ͽ� yangtheprogrammer.pythonanywhere.com ������ �߰�
	
	Reload ��ư Ŭ��
	�����Ǵ� ��ũ Ŭ���ϸ� ���� Ȯ�� ����