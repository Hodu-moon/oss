# oss
2022-01


# ***컴퓨터공학과_20194536_2학년_문영호***
# __oss_03분반_전찬준교수님__
# 과제#2

## 리눅스 명령어
---------------------

* top

<img width="600" alt="Screen Shot 2022-06-04 at 6 59 50 PM" src="https://user-images.githubusercontent.com/82320750/171994516-05f92148-e096-40c1-af85-d8e9292305cc.png">

top 명령어를 알아보기 전에 터미널에서 top 를 쳐보니 1초마다 갱신되는 화면들을 볼 수 있었습니다.
iterm2에서 top명령어를 치니 iterm2프로그램은 sleep 상태가 되었고 top 프로그램은 running 상태가 되었습니다.
나머지는 정확한 의미를 모르겠어서 구글링을 해보았습니다

_top 는 table of process의 약자로 cpu와 메모리 이용에 관한 정보를 표시하는 수많은 유닉스 계열 운영체제에서 볼 수 있는 작업관리자 프로그램이다._

소문자'o'를 입력시 __primary key[-pid]:__라는 문자열이 나오는데 이곳에 mem,pid,command,time등 문자열의 사용량을 기준으로 소팅이 된다.
예를들어 primary key[-pid]: 에 mem 을 입력하였다면 메모리 사용량으로 소팅을 한다
//<span style="color:red">CPU</span>디폴트값은 cpu이다.

|PID| COMMAND|<span style="color:red">CPU</span>| TIME|#TH| #WQ|#PORT|MEM|PURG|CMPRS|PGRP|PPID|STATE|
|:---|:-------|:---|:---- |:---|:---|:-----|:---|:----|:-----|:----|:----|:-----|
|153| WindowServer|28.9|11:21:58|24|6|2685|743M+|185M|246M|153|1|sleeping|

