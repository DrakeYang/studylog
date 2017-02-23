장고걸즈 튜토리얼을 하면서 알게된 점을 정리하겠습니다.

1. __ 더블언더스코어는 줄여서 "던더" 라고도 합니다.
2. www.pythonanywhere.com 에서 블로그를 만들고 gitgub를 끌어오면 배포가 쉬워집니다.
3. setting.py 의 ALLOWED_HOSTS 옵션에 호스트를 넣어주어야 웹앱 구동이 가능합니다(장고걸즈엔 없음)
4. 당연한거지만.. 윈도우 기반 코드를 리눅스에 올리면 돌아가지 않습니다(venv 등). 때문에 venv 같은 코드는 git에서 제외하고 순수 파이썬 코드만 커밋하는게 좋습니다.
5. 객체를 정렬할때 Post.objects.filter(dated_date__lte=timezone.now()).order_by('-dated_date') 의 방식으로 정렬 가능하며 -dated_date 는 desc 방식으로 정렬합니다. dated_date 는 asc 이며, 기본값 입니다.