# oss
![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=Hodu-moon&show_icons=true&theme=gruvbox)



# ***컴퓨터공학과_20194536_2학년_문영호***
# __oss_03분반_전찬준교수님__
# 과제#2

## 리눅스 명령어
---------------------

##  top

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
## ps

Process Status의 약자입니다.

`ps [option]`

|옵션|내용|
|:---:|:---:|
|-A| 모든 프로세스를 출력합니다.|
|-a|터미널과 연관된 프로세스를 출력합니다.(-A의 반대)터미널이랑 연관 없으면 스킵합|
|-e|Identical to -A.|
|-f|uid, pid, parent pid, recent CPU usage, process start time, controlling tty, elapsed CPU usage, and the associated command(이 옵션은 강력한 옵션인 것 같다)|
|-p|특정 PID를 지정할 때 사용합니다.|
|-u|특정 사용자의 프로세스 정보를 확인할 때 사용한다. 사용자를 지정하지 않으면 현재 사용자를 기준으로 정보를 출력한다.|
|-x|로그인 상태에 있는 동안 아직 완료되지 않은 포로세스들을 보여준다. 유닉스 시스템은 사용자가 로그아웃 한 후에도 임의의 프로세서가 계속 동작하게 할 수 있다. 그러면 그 프로세스는 자신을 실행시킨 셸이 없이도 계속 자신의 일을 수행하는데 이러한 프로세스는 일반적인 ps 명령으로 확인할 수 없다. 이때 -x옵션을 사용하면 자신의 터미널이 없는 프로세스들을 확인 할 수 있다. |


### 자주 쓰는 조합

* ps -ef | grep '프로세스명'
* ps aux | grep '프로세스명'<br>
시스템에 동작중인 모든 프로세스를 소유자 정보와 함께 다양한 정보를 출력합니다.

<img width="1028" alt="Screen Shot 2022-06-04 at 11 09 18 PM" src="https://user-images.githubusercontent.com/82320750/172005071-9dfdb13d-1b77-44bc-8853-d6793263ccc1.png">
알아보기 편하게 나온다!

ex) `ps aux | grep apache`<br>
특정 프로세스 보고싶으면 이렇게 한다.
* `ps -ef | more `<br> 한줄씩 보고싶으면
ex) ps -fp [PID]
PID를 키워드로 프로세스 정보를 확인하는 방법입니다.
* `ps -t pts/18`<br>
특정 TTY에서 실행되는 프로세스 또한 뽑아서 확인할 수 있습니다.

--------------------
## jobs

`jobs [옵션][작업번호]`<br>
|옵션|번호|
|:---:|:---:|
|-l|프로세스 그룹ID를 state 필드 앞에 출력|
|-n|프로세스 그룹 중에 대표 프로세스 ID를 출력|
|-p|각 프로세스 ID에 대해 한 행씩 출력|
|command|지정한 명령어를 실행|



<br>
|상태|설명|
|:---:|:---:|
|Running|작업이 일시 중단되지 않았고 종료하지 않고 계속 진행 중임을 뜻한다.|
|Done|작업이 완료되어 0을 반환하고 종료했음을 뜻한다.|
|Done(code)|작업이 정상적으로 완료했으며, 0이 아닌 코드를 반환했음을 뜻한다.|
|Stopped|작업이 일시 중단됨을 뜻한다.|
|Stopped(SIGTSTP)|SIGSTP 신호가 작업을 일시 중단했음을 뜻한다.|
|Stopped(SIGSTOP)|SIGSTOP 신호가 일시 중단했음을 뜻한다.|
|Stopped(SIGTTIN)|SIGTTIN 신호가 작업을 일시 중단했음을 뜻한다.|
|Stopped(SIGTTOUT)|SIGTTOUT 신호가 작업을 일시 중단했음을 뜻한다.|



----------------
## kill


kill 명령어는 프로세스에 **시그널(signal)** 을 보내는 명령어입니다.

     1       HUP (hang up)
     2       INT (interrupt)
     3       QUIT (quit)
     6       ABRT (abort)
     9       KILL (non-catchable, non-ignorable kill)
     14      ALRM (alarm clock)
     15      TERM (software termination signal)
     
 kill 명령어의 default 시그널은 TERM(15)입니다. 
  
`kill -s[signal][pid]`


     
     

top 명령어를 통해 한 프로세스가 너무 많은 메모리나 CPU 자원을 사용하고있으면 


`kill <PID Number>`

명령어를 통해 프로세스를 없앨 수 있다.


----------------------------------

## vim 에디터 매크로 사용방법(q, @)

|기능|일반모드|예제|
|:---:|:---:|:---:|
|녹화|q+(매크로key)| qa|
|녹화종료|q|q|
|재생|@ + (매크로key)|@ a|
|마지막매크로실행|@@|@@|
|횟수실행|(횟수)@(매크로key)|10@a|

`let @(매크로key) = (CTRL + r CTRL+r (매크로KEY))`


