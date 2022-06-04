# oss
2022-01
![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=깃허브아이디&show_icons=true&theme=gruvbox)



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



|PID|COMMAND|CPU|TIME|#TH|#WQ|#PORT|MEM|PURG|CMPRS|PGRP|PPID|STATE|
|:---|:-------|:---|:---- |:---|:---|:-----|:---|:----|:-----|:----|:----|:-----|
|153| WindowServer|28.9|11:21:58|24|6|2685|743M+|185M|246M|153|1|sleeping|

* PID - 해당 프로스세의 유일한 프로세스번호(Process ID, 키값)
* COMMAND - 프로세스의 이름이다. (user process or system process)
* CPU - 프로세스가 사용하는 cpu의 사용율
* TIME - 프로세스가 사용한 토탈 CPU시간
* #TH - the number of threads in the process.
* #WQ - 
* #PORT -  포트 번호이다.
* MEM - 프로세스가 사용중인 RAM의 사용율
* PURG - Purgeable memory size. //맥 os에서 사용되는 Sierra의 최적화 된 저장소와 관련되어있는것
* CMPRS - mac의 메모리 관리 기술
* PGRP - Process group ID.
* PPID - Parent process ID. maleware 같은 프로세스를 확인할 수 있는 방법중 하나라 중요하다. 
* STATE - 프로세스의 현재 상태를 나타냅니다



* load average : 작업의 대기시간을 말합니다. 값이 1이 나왔다면 1분동안 평균 1개 정도의 프로세서가 대기상태에 있다는 것입니다. 싱글 코어 기준 loadaverage 가 0.7이면 초과하기전에 장비를 추가하던지 최적하를햐아하고, 1.0이면 즉시 문제를 찾아 수정하고 5.0이면 이미 망한거라고 본다고 한다. 멀티 cpu에서는 코어의개수가 1이면 1 2이면 2 이런식으로 따진다고 한다 내 cpu는 8개이므로 1.7이면 무리없이 잘 돌아가고있다.

소문자'o'를 입력시 __primary key[-pid]:__라는 문자열이 나오는데 이곳에 mem,pid,command,time등 문자열의 사용량을 기준으로 소팅이 된다.
예를들어 primary key[-pid]: 에 mem 을 입력하였다면 메모리 사용량으로 소팅을 한다
디폴트값은 cpu이다.


__top [옵션]__
|옵션|설명|
|:---------:|:------:|
|-b|배치모드로 정보를 출력합니다.|
|-d delay||
|-i idle|토글값이 off일 때, idle프로세스나 좀비 프로세스 정보를 출력하지 않습니다|
|-n num|지정한 시간(num)만큼 업데이트 정보를 출력합니다.|
|-p pid|지정한 프로세스 ID(pid)의 정보만을 출력합니다.|
|-q|시간의 간격 없이 계속하여 업데이트 정보를 출력합니다.|
|-s| 몇 개의 대화식 명령을 비활성화 합니다.|
|-S|누적된 정보를 출력합니다.|


---------------------------------------------





----------------
* kill

top 명령어를 통해 한 프로세스가 너무 많은 메모리나 CPU 자원을 사용하고있으면 


`kill <PID Number>`

명령어를 통해 프로세스를 없앨 수 있다.



