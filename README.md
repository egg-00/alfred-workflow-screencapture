# alfred-workflow-screencapture

## Keyword : screen capture


### 설명
Command + Shift + 4 를 자꾸 잊어먹어서 알프레드 키워드로 만들었습니다. 


### 사용방법
키워드 후 마우스 선택영역이 데스크톱에 png로 저장이 됩니다. 


## Source
    #!/usr/bin/python

    import time
    import os

    now = time.localtime()

    datetime = "%04d%02d%02d%02d%02d%02d" % (now.tm_year, now.tm_mon, now.tm_mday, now.tm_hour, now.tm_min, now.tm_sec)

    os.system('screencapture -is ~/Desktop/%s.png' % datetime)
