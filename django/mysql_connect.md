django ���� mysql �� �����߽��ϴ�.

�������.
0. django ��ġ
 - ���� �� �̹� ��ġ�Ǿ���
1. mysql ��ġ
 - localhost �� �׽�Ʈ�ϱ����
2. mysql database ���� 
 - �̺κ��� �ٸ� �ۿ��� �ȳ��ͼ� ��Ȳ��. �翬�� �κ��̶� ���� ǥ������ �����ɷ� ����. �������� ������ ���� makemigration ��ɾ� �����  ���� �����ͺ��̽� ��� ������ �źΰ� ��.
3. django library ��ġ - PyMySQL, mysql-connector-python 
 - �Ѱ��� ��ġ�ϰ� �׽�Ʈ�� �κ��� �ƴ϶� ���� �ϳ��� �־ �Ǵ����� ��Ȯ��
4. polls/models.py �� Ŭ���� �������� ���̺� ����
 - ���� Ŭ������ ���̺��� �����ؼ� migrate �� ������ �� �ִ�
5. misite/settings.py �� DATABASES ���� ����
 - �����κ� �ּ�ó���ϰ� MySQL ������ ����
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
6. ��� manage.py makemigration
7. ��� manage.py migrate
8. ���� db�� ���̺��� ����� Ȯ��