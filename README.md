# 오픈소스SW개론 과제 2

## 리눅스 명령어


### **1. top**

`$ top [option]`

<img src = "https://user-images.githubusercontent.com/103545438/172032520-88e4ac72-b9ea-4c28-bdaf-e4b6179f47e8.png" width = "1200" height = "300">

- 현재 OS의 상태를 나타내주는 CLI 애플리케이션
- 시스템 상태(메모리 사용량, CPU 사용량 등)를 전반적으로 빠르게 파악할 수 있다.
- 옵션 없이 입력한다면 일정한 간격(기본 3초)으로 화면을 갱신하면서 정보를 보여준다.
- 요약 영역은 상단에 위치하고 있으며, 전체 프로세스가 OS에 대해서 리소스를 어느정도 차지하고 있는지 알려준다.
- top 관련 주요 옵션

|옵션|설명|
|-------|-------|
|-b|순간의 정보를 알 수 있다.(batch 모드)|
|-n|top의 실행 주기를 설정한다.(반복 횟수)|


### **2. ps**

`$ ps [option]`
<img src = https://user-images.githubusercontent.com/103545438/172032836-6b86bd88-82b8-4dc7-a925-e240e475cfff.png width = "1200" height = "100">

- Prcess Status, 현재 실행 중인 프로세스 목록과 상태를 보여준다.
- top과의 차이점 : ps는 ps 한 시점에 proc에서 검색한 cpu 사용량, top은 proc에서 일정 주기로 합산해 cpu 사용률을 출력한다.
- ps 관련 주요 옵션

|옵션|설명|
|-------|-------|
|-e|실행 중인 모든 프로세스의 정보를 출력한다.|
|-f|프로세스의 정보를 풀포맷으로 출력한다.|
|-l|프로세스의 정보는 긴 포맷으로 출력한다.|


### **3. jobs**

`$ jobs [옵션[작업번호]`

<img src = https://user-images.githubusercontent.com/103545438/172033331-5cda0c86-8e68-4c9b-ae63-d298974587c5.png width = "1200" height = "80">

- 작업의 상태를 표시한다.
- 현재 쉘 세션에서 실행시킨 백그라운드 작업의 목록이 출력되며, 각 작업에 붙은 번호를 '%번호'로 kill 명령어 뒤에 사용할 수 있다.
- jobs로 출력되는 주요 상태값

|상태|설명|
|-------|-------|
|Running|작업이 계속 진행 중이다.|
|Done|작업이 완료되어 0을 반환했다.|
|Stopped|작업이 일시 중단됐다.|

- jobs 관련 주요 옵션

|옵션|설명|
|-------|-------|
|-l|프로세스 그룹 ID를 State 필드 앞에 출력한다.|
|-n|프로세스 그룹 중에 대표 프로세스 ID를 출력한다.|
|-p|각 프로세스 ID에 대해 한 행식 출력한다.|


### **4. kill**
`$ kill [option] <pid>`

<img src = https://user-images.githubusercontent.com/103545438/172033636-1f028dce-da92-477d-93c4-ba331ecd5349.png width = "1200" height = "80">

- 주로 프로세스를 죽일 때 사용한다.
- 내부적으로는 프로세스에 시그널을 보내 원하는 작업을 하게 하는 명령어 이다.
- kill 관련 주요 옵션

|옵션|설명|
|-------|-------|
|-l|signal 의 종류를 출력한다.|

-> 옵션으로 시그널의 번호나 이름을 넣어서 사용한다.


-----------------------

## VIM 에디터에서의 매크로 사용법

### **매크로**
- 특정한 움직임 또는 입력을 키에 저장함으로써 단순하고, 반복되는 동작을 쉽고 빠르게 해준다.

### **매크로 사용 순서**

1. **q + 원하는 문자** : 원하는 문자의 매크로 recording 시작
2. **반복하고 싶은 동작** 입력
3. **q** : recording 종료
4. **@ + 설정한 매크로 문자** : 설정한 매크로 동작을 수행한다.

- @@ : 방금 실행한 매크로를 실행한다.
- 10@(매크로 문자) : 매크로를 10회 실행한다.


