
![header](https://capsule-render.vercel.app/api?type=waving&color=gradient&height=250&section=header&text=Operating%20System&fontSize=60&animation=fadeIn&fontAlign=32&fontAlignY=40)


---
## 목차

- [운영체제 개요](#운영체제-개요)
- [컴퓨터 시스템의 구조](#컴퓨터-시스템의-구조)
- [프로세스 관리](#프로세스-관리)
- [운영체제 개요](#운영체제-개요)
- [운영체제 개요](#운영체제-개요)



<br/>

---

## 운영체제 개요

<br/>

### 01. 운영체제란 무엇인가요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="Untitled.png" width="400" height="200"><br/><br/>

- 운영체제란 컴퓨터 하드웨어 바로 위에 설치되어 사용자 및 다른 소프트웨어와 하드웨어를 연결하는 소프트웨어 계층입니다<br/><br/>

#

### 02. 운영체제의 목적은 무엇인가요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="Untitled 1.png" width="400" height="200">

&nbsp;&nbsp;&nbsp;&nbsp;<img src="Untitled 2.png" width="400" height="200"><br/><br/>

- 컴퓨터 하드웨어를 직접적으로 다루면 매우 어렵고 복잡하기 때문에 운영체제라는 중간다리를 만듦으로서 컴퓨터 시스템을 편리하게 사용할 수 있는 환경을 제공합니다
- 또한 운영체제는 실행중인 프로그램을 메모리 공간에 적절히 분배함으로서 컴퓨터 시스템의 자원을 효율적으로 관리합니다<br/><br/>

#

### 03. CPU 스케줄링이란 무엇인가요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="Untitled 3.png" width="400" height="200"><br/><br/>

- CPU 스케쥴링이란 어떤 프로그램에게 CPU 사용권을 줄지에 대한 과정입니다
- CPU는 하드웨어라 생각을 못합니다 그냥 코드를 읽어와서 계산만 수행합니다
- 어떤 프로그램을 얼마나 CPU를 할당해서 수행할 것인지 정하는 것은 메모리 영역 가장 밑단에 있는 운영체제가 결정합니다
- 즉 CPU스케쥴링은 운영체제의 주요 기능중 하나입니다<br/><br/>

#

### 04. 디스크 스케줄링이란 무엇인가요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="Untitled 4.png" width="400" height="200"><br/><br/>

- 디스크는 CPU에 비해 백만배정도 느립니다
- 메모리는 CPU에 비해 백배정도 느립니다
- 디스크는 워낙 느리다보니 프로그램 A로부터도 오고 프로그램 B로부터도 오고 요청이 밀리게 됩니다.
- 이때 요청이 온 순서대로 처리하면 자원이 굉장히 비효율적입니다
- 따라서 순서를 뒤바꿔서라도 자원을 최적화하여 활용하기 위해 운영체제는 디스크 스케쥴링을 합니다
- 예를 들어 엘리베이터가 1층에서 100층으로 가고 있는데 중간에 30층이 눌리면 비록 30층 요청이 늦게 들어왔지만 30층에서 문이 열리는 것과 같습니다<br/><br/>

#

### 05.  CPU 스케쥴링이란 무엇인가요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="Untitled 5.png" width="400" height="200"><br/><br/>

- CPU 스케쥴링이란 운영체제의 중요한 역할 중 하나로 어떤 프로그램에게 CPU 사용권을 줄건지 순서를 매기는 것과 같습니다<br/><br/>

#

### 06. SJF(Shortest-Job-First)란 무엇인가요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="Untitled 6.png" width="400" height="200"><br/><br/>

- 순서를 매기는데 있어서 p1이 24초, p2, p3이 3초씩 쓴다면 p1이 먼저오더라도 p2,p3에게 CPU를 먼저 내주는 것이 효율적입니다.
- 이처럼 CPU 사용시간이 가장 짧은 프로세스를 먼저 스케쥴링하는 것을 SJF라고 합니다
- 하지만 CPU를 길게써야하는 프로그램이 무한정 기다릴 수도 있는 Starvation(기아 현상)이 발생가능합니다<br/><br/>

#

### 07. Round Robin(RR) 에 대해 설명해주세요

&nbsp;&nbsp;&nbsp;&nbsp;<img src="Untitled 7.png" width="400" height="200"><br/><br/>

- Round Robin은 CPU 스케쥴링의 방법들 중 하나로 CPU할당시간을 딱 정해서 각 프로세스들이 할당시간만큼만 돌아가면서 사용하고 작업을 완료했으면 I/o로 보내는 방법입니다
- 이 방법의 장점은 CPU를 효율적으로 사용하면서 starvation을 방지할 수 있다는 것입니다<br/><br/>

#

### 08. 가상메모리란 무엇인가요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="Untitled 8.png" width="400" height="200">

&nbsp;&nbsp;&nbsp;&nbsp;<img src="Untitled 9.png" width="400" height="200"><br/><br/>

- 프로그램을 실행하게 되면 디스크의 실행파일들이 메모리(휘발성)로 이동한뒤 프로세스가 되어 실행됩니다
- 하지만 좀 더 세부적으로 따지면 바로 메모리에 올라가는 것이 아닌 중간에 가상메모리라는 단계를 거치게 됩니다.
- 가상메모리에 먼저 메모리 공간이 만들어진 후 물리적인 메모리에는 가상 메모리 중 당장 필요한 부분만 올라가게 됩니다<br/><br/>

#

### 09.  디스크에서 파일 시스템과 스왑영역에 대해 설명해주세요

- 파일시스템은 전원이 나가더라도 실행 파일이 사라지지 않도록 저장하는 공간입니다
- 가상 메모리가 물리적인 메모리로 올라갈 때 당장 필요한 영역들이 올라가게 됩니다. 이때 나머지 가상메모리들을 스왑영역 디스크에 저장하게 됩니다. 즉 스왑영역은 메모리의 연장공간입니다.
- 컴퓨터가 꺼지면 파일시스템도 남고 스왑영역도 남지만 스왑영역의 메모리는 전원이 꺼질경우 의미가 없기 때문에 전원이 나가기전에 지우는 것이 바람직합니다<br/><br/>

#

### 10. 메모리가 꽉찼을 경우 또다른 작업을 요청받았을 때 OS는 어떻게 동작하나요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="Untitled 10.png" width="400" height="200"><br/><br/>

- 미래에 재사용될 가능성이 높은 작업은 후순위로 재사용 가능성이 낮은 작업을 먼저 메모리에서 지웁니다
- 이때 재사용 가능성에 대한 판단은 LRU와 LFU 방식을 사용합니다
- LRU는 가장 오래전에 참조한 페이지를 삭제합니다
- LFU는 참조횟수가 가장 적은 페이지를 삭제합니다<br/><br/>

#

### 11.  디스크 스케쥴링은 어떻게 동작하나요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="Untitled 11.png" width="400" height="200"><br/><br/>

- CPU를 쓰고나서 디스크로부터 파일을 읽어야하거나 저장을 해야하면 작업들이 디스크 큐에 쌓이게 됩니다.
- 디스크 접근시간 중 가장 많은 부분을 차지하는 것이 디스크 헤드 이동시간(seek time)입니다. 따라서 디스크 헤드 이동을 얼마나 최소화하느냐가 중요합니다
- 그래서 큐에 들어온 시간 순서대로 처리하는 것이 아니라 순서를 뒤바꿔서라도 헤드이동을 최소화하게 스케쥴링을 하게 됩니다<br/><br/>

#

### 12. 디스크 접근 시간 구성에 대해 좀 더 자세히 설명해주세요

&nbsp;&nbsp;&nbsp;&nbsp;<img src="Untitled 12.png" width="400" height="200"><br/><br/>

- 디스크 접근시간 (Access time)은 탐색시간(Seek time), 회전지연(Rotational latency), 전송 시간(Transfer time)으로 구성되어 있습니다
- 이러한 3가지요소중 Seektime(헤드 이동)시간이 가장 오래걸리기 때문이 이를 최소화 시키는 것이 목표입니다<br/><br/>

#

### 13. Seektime 최소화를 목표에 둘 경우 어떤 문제점이 발생하나요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="Untitled 13.png" width="400" height="200"><br/><br/>

- 앞서 봤던 CPU 스케쥴링에서처럼 Starvation문제가 발생할 수 있습니다
- 즉 탐색시간이 긴 작업의 경우 지나치게 뒤늦게 처리될 수 있습니다<br/><br/>

#

### 14. 디스크 스케줄링에서 SCAN에 대해 설명해주세요

&nbsp;&nbsp;&nbsp;&nbsp;<img src="Untitled 14.png" width="400" height="200"><br/><br/>

- 이전의 탐색시간 최소화를 최우선했을 경우의 starvation의 문제를 보완하기 위해 SCAN이라는 디스크 스케쥴링 방법이 현재 가장 근본적으로 사용되고 있습니다
- 헤드가 순차적으로 한쪽 끝에서 다른쪽 끝으로 이동하며 가는 길목에 있는 요청들을 처리하는 방식으로 형평성과 효율성을 모두 잡을 수 있는 방법입니다<br/><br/>

#

### 15. 빠른 CPU와 느린 I/O 장치들의 속도를 어떻게 완충시키나요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="Untitled 15.png" width="400" height="200"><br/><br/>

- CPU(최상단)와 I/O(최하단) 사이에는 다음과 같은 계층 구조가 있습니다
- 저장장치 계층구조의 특징은 최상단일 수록 빠르지만 값이 비싸서 적은 양의 작업만 처리하는 반면 하단일 수록 느리지만 많은 양의 작업을 가질 수 있습니다
- 휘발성(Volatility)에 있어서도 Secondary영역은 전원이 꺼져도 메모리가 유지되지만 Primary는 메모리가 날라갑니다. 이때 Primary는 CPU가 직접 메모리를 실행시키는 영역입니다
- 즉 Primary는 컴퓨터내부, Secondary는 I/O 장치라고 볼 수 있습니다
- 작업을 처리해야하면 위로 위로 올리고 저장을 해야겠다 싶으면 아래로 내리는 작업을 반복합니다
- 이때 아래로 내리고 위로 올리는 과정에서 시간이 소요되기 때문에 **Caching** 이라는 복사본을 만들어서 위에서 CPU에서 처리할 작업을 그냥 바로 던져버리자라는 개념입니다.<br/><br/>

#

### 16. 플래시 메모리란 무엇인가요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="Untitled 16.png" width="400" height="200"><br/><br/>

- 플래시 메모리는 반도체 장치로 하드디스크의 역할을 수행합니다
- 하지만 하드디스크에 비해 크기가 작고, 전력소모가 적으며, 물리적인 충격에 더 강합니다. 이러한 특징은 모바일 장치에 매우 적합합니다
- 플래시메모리는 모바일 용으로 출발했다가 현재에는 컴퓨터 등 전반적인 곳에서 널리 사용되고 있습니다
- 플래시메모리는 read/write 횟수에 제약이 있다는 점, 전하가 조금씩 빠져나가서 같은 공간의 메모리에 변형이 오는등에서 하드디스크에 비해 단점이 있습니다
- 이러한 하드웨어적인 플래시메모리의 단점을 소프트웨어 개발자들이 보완해야합니다. (read/write 횟수를 최소화하거나 전하누수 방지를 위해 저장 공간을 어쩌다 한 번씩 바꿔주는 등등)<br/><br/>

<br/>

 ---

## 컴퓨터 시스템의 구조

<br/>

#### 01. 운영체제에 대해서 범위에 따라 설명해주세요

&nbsp;&nbsp;&nbsp;&nbsp;<img src="17.png" width="400" height="200"><br/><br/>

- 협의(좁은의미)의 운영체제는 커널을 뜻합니다. 커널은 운영체제의 핵심부분으로 메모리에 상주하고 있습니다
- 광의(넓은의미)의 운영체제는 커널(메모리 상주 o) 뿐 아니라 각종 주변 시스템 유틸리티(메모리 상주 x)를 포함한 개념입니다

#

#### 02. 운영체제들은 어떻게 분류할 수 있을까요?

- 운영체제는 **동시작업 가능 여부, 사용자의 수, 처리방법** 3가지 기준으로 분류할 수 있습니다
- 먼저 **동시작업 가능여부**에 있어서는 단일작업(한번에 하나 작업만 처리)과 다중작업(동시에 두 개 이상 작업처리)이 있습니다
- 현대 운영체제는 다중작업으로 OS의 스케쥴링도 이러한 여러 작업을 어떻게 효율적으로 처리하는가에 대한 고민입니다
- **사용자 수에**에 있어서는 단일 사용자인가와 다중 사용자인가로 나눌 수 있습니다
- **처리방법**에 있어서는 일괄처리(batch processing), 시분할 처리방식(time sharing), 실시간 처리방식(Realtime OS)로 나눌 수 있습니다
- 일괄처리방식은 작업 요청의 일정량을 모아서 한꺼번에 처리합니다. 
- 일반적인 OS(리눅스, 윈도우즈)는 시분할 방식으로 여러작업을 수행할 때 컴퓨터 처리능력을 일정한 시간 단위로 분할하여 사용합니다.
- 실시간 방식은 정해진 시간 안에 어떠한 일이 반드시 종료됨을 보장될 때 사용하는 OS입니다. 예를들어 원자로/공장제어, 미사일 제어, 반도체 장비, 로보트 제어가 있습니다 즉 데드라인이 중요할 때 사용하는 OS입니다

#

#### 03. 컴퓨터 시스템에서 mode bit이 하는 역할은 무엇인가요? 

&nbsp;&nbsp;&nbsp;&nbsp;<img src="18.png" width="400" height="200">
&nbsp;&nbsp;&nbsp;&nbsp;<img src="19.png" width="400" height="200"><br/><br/>



- OS가 할당을해서 특정 사용자 프로그램이 CPU의 제어권을 손에쥐면 이후부터는 OS가 제어할 수 없습니다
- CPU가 실행하는 기계어가 특정 사용자 프로그램인지 운영체제가 실행하는 것인지 구분하는 역할을 **mode bit**이 수행합니다 
- 운영체제가 CPU를 실행시킬 때는 mode bit이 0(모니터모드), CPU를 사용자 프로그램에게 넘길 때는 Mode bit이 1(사용자 모드)이 됩니다.
- CPU가 실행하고 있는 기계어가 OS인지 사용자 프로그램인지 구분함으로서 보안과 같은 중요한 명령어(**특권명령**)는 OS에서만 실행되도록 제한합니다 ()

#

#### 04. 컴퓨터 시스템에서 intterupt line 이 하는 일은 무엇인가요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="20.png" width="400" height="200"><br/><br/>

- CPU 에서 기계어를 실행시키기에 앞서 interrupt 유무를 확인하는 역할을 합니다
- interrupt line 에서 interrupt 이 확인되면 자동적으로 CPU 권한은 운영체제에게 넘어갑니다 (= mode bit이 0이 됩니다)
- OS kernel은 이러한 interrupt 를 받아 다음작업을 CPU에게 할당합니다

#

#### 05. PC(Program Counter) Register 의 역할은 무엇인가요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="21.png" width="400" height="200"><br/><br/>

- PC Register는 다음번에 CPU에서 실행할 프로그램의 메모리 주소를 가리키고 있는 역할을 합니다.

#

#### 06. timer 의 역할은 무엇인가요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="18.png" width="400" height="200"><br/><br/>

- 다른 프로그램이 실행 중일 때 운영체제는 함부로 CPU 권한을 가져올 수 없습니다
- 만약 프로그램이 무한루프를 돌면서 CPU를 돌려주지 않는다면 매우 골치아파집니다. 이를 방지하기 위해 timer가 있습니다
- timer를 통해 운영체제는 프로그램마다 일정시간을 할당하고 CPU를 넘깁니다
- 무한루프가 돌더라도 일정시간이 지나면 OS가 다시 CPU 주도권을 가져와 다른 프로그램에게 CPU 권한을 줄 수 있습니다

#

#### 07. System Call 이란 무엇인가요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="22.png" width="400" height="200"><br/><br/>

- I/O 장치에 대한 명령어는 모두 특권명령으로 묶여있습니다. 따라서 사용자 프로그램이 특권명령으로 묶인 명령을 실행할 수 없습니다.
- 따라서 I/O장치에 명령을 내릴려면 운영체제의 도움을 받아야합니다. 이를 위해 CPU를 점유하고 있던 사용자 프로그램이 스스로 interrupt를 겁니다. 이것을 바로 system call이라고 부릅니다
- System call은 다시말해 사용자 프로그램이 운영체제의 서비스를 받기 위해 커널을 호출하는 것입니다.

#

#### 08. Trap 이란 무엇인가요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="23.png" width="400" height="200"><br/><br/>

- 인터럽트에는 하드웨어에서 발생시키는 인터럽트(일반적 - Timer, Disk controller ...)와 소프트웨어에서 발생시키는 인터럽트가 있습니다. 이때 후자의 경우를 따로 **trap**이라 부르기도 합니다
- Trap의 예로는 개별 프로그램이 kernel의 도움을 받기위해 스스로 interrupt 시키는 system call 이 있습니다.(interrupt의 출발지가 소프트웨어)

#

#### 09. I/O 이 동작하는 순서를 알려주세요

&nbsp;&nbsp;&nbsp;&nbsp;<img src="18.png" width="400" height="200"><br/><br/>

- 먼저 OS가 I/O 작업이 들어가있는 사용자 프로그램에게 CPU를 줍니다
- 사용자 프로그램은 I/O 작업이 수행될 때 스스로 interrupt를 걸어 커널에게 시스템 콜을 날립니다
- 운영체제는 CPU를 받아 Controller 에게 I/O를 요청합니다
- 컨트롤러는 이 요청을 받아서 수행합니다 하지만 이 작업은 굉장히 느리기 때문에 다른 사용자프로그램에게 CPU를 넘김니다
- 만약 I/O controlelr가 작업을 완료해서 CPU에게 interrupt를 걸면 다시 CPU는 운영체제에게 넘어가고 운영체제는 이전에 I/O 작업이 있던 사용자 프로그램에게 다시 CPU를 넘겨줍니다.

#

#### 10. device driver 와 firmware의 차이는 무엇인가요?

- device driver 는 CPU가 device controller 에게 작업을 부탁하는 용도로 사용되는 소프트웨어입니다, 즉 컴퓨터 내부에서 CPU가 수행하는 코드입니다.
- firmware는 디바이스에서 실행되는 자체적으로 내장된 코드로 Disk나 I/O 디바이스에 read/write하는 코드입니다

#









