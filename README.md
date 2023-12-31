
![header](https://capsule-render.vercel.app/api?type=waving&color=gradient&height=250&section=header&text=Operating%20System&fontSize=60&animation=fadeIn&fontAlign=32&fontAlignY=40)


---
## 목차

- [운영체제 개요](#운영체제-개요)
- [컴퓨터 시스템의 구조](#컴퓨터-시스템의-구조)
- [프로세스 관리](#프로세스-관리)
- [CPU 스케쥴링](#cpu-스케쥴링)
- [병행제어](#병행제어)


<br/>

---

## 운영체제 개요

<br/>

### 01. 운영체제란 무엇인가요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="Untitled.png" width="400" height="200"><br/>

- 운영체제란 컴퓨터 하드웨어 바로 위에 설치되어 사용자 및 다른 소프트웨어와 하드웨어를 연결하는 소프트웨어 계층입니다<br/><br/>

#

### 02. 운영체제의 목적은 무엇인가요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="Untitled 1.png" width="400" height="200">

&nbsp;&nbsp;&nbsp;&nbsp;<img src="Untitled 2.png" width="400" height="200"><br/>

- 컴퓨터 하드웨어를 직접적으로 다루면 매우 어렵고 복잡하기 때문에 운영체제라는 중간다리를 만듦으로서 컴퓨터 시스템을 편리하게 사용할 수 있는 환경을 제공합니다
- 또한 운영체제는 실행중인 프로그램을 메모리 공간에 적절히 분배함으로서 컴퓨터 시스템의 자원을 효율적으로 관리합니다<br/><br/>

#

### 03. CPU 스케줄링이란 무엇인가요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="Untitled 3.png" width="400" height="200"><br/>

- CPU 스케쥴링이란 어떤 프로그램에게 CPU 사용권을 줄지에 대한 과정입니다
- CPU는 하드웨어라 생각을 못합니다 그냥 코드를 읽어와서 계산만 수행합니다
- 어떤 프로그램을 얼마나 CPU를 할당해서 수행할 것인지 정하는 것은 메모리 영역 가장 밑단에 있는 운영체제가 결정합니다
- 즉 CPU스케쥴링은 운영체제의 주요 기능중 하나입니다<br/><br/>

#

### 04. 디스크 스케줄링이란 무엇인가요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="Untitled 4.png" width="400" height="200"><br/>

- 디스크는 CPU에 비해 백만배정도 느립니다
- 메모리는 CPU에 비해 백배정도 느립니다
- 디스크는 워낙 느리다보니 프로그램 A로부터도 오고 프로그램 B로부터도 오고 요청이 밀리게 됩니다.
- 이때 요청이 온 순서대로 처리하면 자원이 굉장히 비효율적입니다
- 따라서 순서를 뒤바꿔서라도 자원을 최적화하여 활용하기 위해 운영체제는 디스크 스케쥴링을 합니다
- 예를 들어 엘리베이터가 1층에서 100층으로 가고 있는데 중간에 30층이 눌리면 비록 30층 요청이 늦게 들어왔지만 30층에서 문이 열리는 것과 같습니다<br/><br/>

#

### 05.  CPU 스케쥴링이란 무엇인가요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="Untitled 5.png" width="400" height="200"><br/>

- CPU 스케쥴링이란 운영체제의 중요한 역할 중 하나로 어떤 프로그램에게 CPU 사용권을 줄건지 순서를 매기는 것과 같습니다<br/><br/>

#

### 06. SJF(Shortest-Job-First)란 무엇인가요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="Untitled 6.png" width="400" height="200"><br/><br/>

- 순서를 매기는데 있어서 p1이 24초, p2, p3이 3초씩 쓴다면 p1이 먼저오더라도 p2,p3에게 CPU를 먼저 내주는 것이 효율적입니다.
- 이처럼 CPU 사용시간이 가장 짧은 프로세스를 먼저 스케쥴링하는 것을 SJF라고 합니다
- 하지만 CPU를 길게써야하는 프로그램이 무한정 기다릴 수도 있는 Starvation(기아 현상)이 발생가능합니다<br/><br/>

#

### 07. Round Robin(RR) 에 대해 설명해주세요

&nbsp;&nbsp;&nbsp;&nbsp;<img src="Untitled 7.png" width="400" height="200"><br/>

- Round Robin은 CPU 스케쥴링의 방법들 중 하나로 CPU할당시간을 딱 정해서 각 프로세스들이 할당시간만큼만 돌아가면서 사용하고 작업을 완료했으면 I/o로 보내는 방법입니다
- 이 방법의 장점은 CPU를 효율적으로 사용하면서 starvation을 방지할 수 있다는 것입니다<br/><br/>

#

### 08. 가상메모리란 무엇인가요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="Untitled 8.png" width="400" height="200">

&nbsp;&nbsp;&nbsp;&nbsp;<img src="Untitled 9.png" width="400" height="200"><br/>

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

&nbsp;&nbsp;&nbsp;&nbsp;<img src="Untitled 10.png" width="400" height="200"><br/>

- 미래에 재사용될 가능성이 높은 작업은 후순위로 재사용 가능성이 낮은 작업을 먼저 메모리에서 지웁니다
- 이때 재사용 가능성에 대한 판단은 LRU와 LFU 방식을 사용합니다
- LRU는 가장 오래전에 참조한 페이지를 삭제합니다
- LFU는 참조횟수가 가장 적은 페이지를 삭제합니다<br/><br/>

#

### 11.  디스크 스케쥴링은 어떻게 동작하나요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="Untitled 11.png" width="400" height="200"><br/>

- CPU를 쓰고나서 디스크로부터 파일을 읽어야하거나 저장을 해야하면 작업들이 디스크 큐에 쌓이게 됩니다.
- 디스크 접근시간 중 가장 많은 부분을 차지하는 것이 디스크 헤드 이동시간(seek time)입니다. 따라서 디스크 헤드 이동을 얼마나 최소화하느냐가 중요합니다
- 그래서 큐에 들어온 시간 순서대로 처리하는 것이 아니라 순서를 뒤바꿔서라도 헤드이동을 최소화하게 스케쥴링을 하게 됩니다<br/><br/>

#

### 12. 디스크 접근 시간 구성에 대해 좀 더 자세히 설명해주세요

&nbsp;&nbsp;&nbsp;&nbsp;<img src="Untitled 12.png" width="400" height="200"><br/>

- 디스크 접근시간 (Access time)은 탐색시간(Seek time), 회전지연(Rotational latency), 전송 시간(Transfer time)으로 구성되어 있습니다
- 이러한 3가지요소중 Seektime(헤드 이동)시간이 가장 오래걸리기 때문이 이를 최소화 시키는 것이 목표입니다<br/><br/>

#

### 13. Seektime 최소화를 목표에 둘 경우 어떤 문제점이 발생하나요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="Untitled 13.png" width="400" height="200"><br/>

- 앞서 봤던 CPU 스케쥴링에서처럼 Starvation문제가 발생할 수 있습니다
- 즉 탐색시간이 긴 작업의 경우 지나치게 뒤늦게 처리될 수 있습니다<br/><br/>

#

### 14. 디스크 스케줄링에서 SCAN에 대해 설명해주세요

&nbsp;&nbsp;&nbsp;&nbsp;<img src="Untitled 14.png" width="400" height="200"><br/>

- 이전의 탐색시간 최소화를 최우선했을 경우의 starvation의 문제를 보완하기 위해 SCAN이라는 디스크 스케쥴링 방법이 현재 가장 근본적으로 사용되고 있습니다
- 헤드가 순차적으로 한쪽 끝에서 다른쪽 끝으로 이동하며 가는 길목에 있는 요청들을 처리하는 방식으로 형평성과 효율성을 모두 잡을 수 있는 방법입니다<br/><br/>

#

### 15. 빠른 CPU와 느린 I/O 장치들의 속도를 어떻게 완충시키나요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="Untitled 15.png" width="400" height="200"><br/>

- CPU(최상단)와 I/O(최하단) 사이에는 다음과 같은 계층 구조가 있습니다
- 저장장치 계층구조의 특징은 최상단일 수록 빠르지만 값이 비싸서 적은 양의 작업만 처리하는 반면 하단일 수록 느리지만 많은 양의 작업을 가질 수 있습니다
- 휘발성(Volatility)에 있어서도 Secondary영역은 전원이 꺼져도 메모리가 유지되지만 Primary는 메모리가 날라갑니다. 이때 Primary는 CPU가 직접 메모리를 실행시키는 영역입니다
- 즉 Primary는 컴퓨터내부, Secondary는 I/O 장치라고 볼 수 있습니다 (Primary는 excutable한 메모리, Secondary는 I/O 작업을 거쳐야하는 메모리)
- 작업을 처리해야하면 위로 위로 올리고 저장을 해야겠다 싶으면 아래로 내리는 작업을 반복합니다
- 이때 아래로 내리고 위로 올리는 과정에서 시간이 소요되기 때문에 **Caching** 이라는 복사본을 만들어서 위에서 CPU에서 처리할 작업을 그냥 바로 던져버리자라는 개념입니다.<br/><br/>

#

### 16. 플래시 메모리란 무엇인가요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="Untitled 16.png" width="400" height="200"><br/>

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

&nbsp;&nbsp;&nbsp;&nbsp;<img src="17.png" width="400" height="200"><br/>

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

### 03. 컴퓨터 시스템에서 mode bit이 하는 역할은 무엇인가요? 

&nbsp;&nbsp;&nbsp;&nbsp;<img src="18.png" width="400" height="200">
&nbsp;&nbsp;&nbsp;&nbsp;<img src="19.png" width="400" height="200"><br/>



- OS가 할당을해서 특정 사용자 프로그램이 CPU의 제어권을 손에쥐면 이후부터는 OS가 제어할 수 없습니다
- CPU가 실행하는 기계어가 특정 사용자 프로그램인지 운영체제가 실행하는 것인지 구분하는 역할을 **mode bit**이 수행합니다 
- 운영체제가 CPU를 실행시킬 때는 mode bit이 0(모니터모드), CPU를 사용자 프로그램에게 넘길 때는 Mode bit이 1(사용자 모드)이 됩니다.
- CPU가 실행하고 있는 기계어가 OS인지 사용자 프로그램인지 구분함으로서 보안과 같은 중요한 명령어(**특권명령**)는 OS에서만 실행되도록 제한합니다 ()

#

### 04. 컴퓨터 시스템에서 intterupt line 이 하는 일은 무엇인가요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="20.png" width="400" height="200"><br/>

- CPU 에서 기계어를 실행시키기에 앞서 interrupt 유무를 확인하는 역할을 합니다
- interrupt line 에서 interrupt 이 확인되면 자동적으로 CPU 권한은 운영체제에게 넘어갑니다 (= mode bit이 0이 됩니다)
- OS kernel은 이러한 interrupt 를 받아 다음작업을 CPU에게 할당합니다

#

### 05. PC(Program Counter) Register 의 역할은 무엇인가요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="21.png" width="400" height="200"><br/>

- PC Register는 다음번에 CPU에서 실행할 프로그램의 메모리 주소를 가리키고 있는 역할을 합니다.

#

### 06. timer 의 역할은 무엇인가요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="18.png" width="400" height="200"><br/>

- 다른 프로그램이 실행 중일 때 운영체제는 함부로 CPU 권한을 가져올 수 없습니다
- 만약 프로그램이 무한루프를 돌면서 CPU를 돌려주지 않는다면 매우 골치아파집니다. 이를 방지하기 위해 timer가 있습니다
- timer를 통해 운영체제는 프로그램마다 일정시간을 할당하고 CPU를 넘깁니다
- 무한루프가 돌더라도 일정시간이 지나면 OS가 다시 CPU 주도권을 가져와 다른 프로그램에게 CPU 권한을 줄 수 있습니다

#

### 07. System Call 이란 무엇인가요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="22.png" width="400" height="200"><br/>

- I/O 장치에 대한 명령어는 모두 특권명령으로 묶여있습니다. 따라서 사용자 프로그램이 특권명령으로 묶인 명령을 실행할 수 없습니다.
- 따라서 I/O장치에 명령을 내릴려면 운영체제의 도움을 받아야합니다. 이를 위해 CPU를 점유하고 있던 사용자 프로그램이 스스로 interrupt를 겁니다. 이것을 바로 system call이라고 부릅니다
- System call은 다시말해 사용자 프로그램이 운영체제의 서비스를 받기 위해 커널을 호출하는 것입니다.

#

### 08. Trap 이란 무엇인가요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="23.png" width="400" height="200"><br/>

- 인터럽트에는 하드웨어에서 발생시키는 인터럽트(일반적 - Timer, Disk controller ...)와 소프트웨어에서 발생시키는 인터럽트가 있습니다. 이때 후자의 경우를 따로 **trap**이라 부르기도 합니다
- Trap의 예로는 개별 프로그램이 kernel의 도움을 받기위해 스스로 interrupt 시키는 system call 이 있습니다.(interrupt의 출발지가 소프트웨어)

#

### 09. I/O 이 동작하는 순서를 알려주세요

&nbsp;&nbsp;&nbsp;&nbsp;<img src="18.png" width="400" height="200"><br/>

- 먼저 OS가 I/O 작업이 들어가있는 사용자 프로그램에게 CPU를 줍니다
- 사용자 프로그램은 I/O 작업이 수행될 때 스스로 interrupt를 걸어 커널에게 시스템 콜을 날립니다
- 운영체제는 CPU를 받아 Controller 에게 I/O를 요청합니다
- 컨트롤러는 이 요청을 받아서 수행합니다 하지만 이 작업은 굉장히 느리기 때문에 다른 사용자프로그램에게 CPU를 넘김니다
- 만약 I/O controlelr가 작업을 완료해서 CPU에게 interrupt를 걸면 다시 CPU는 운영체제에게 넘어가고 운영체제는 이전에 I/O 작업이 있던 사용자 프로그램에게 다시 CPU를 넘겨줍니다.

#

### 10. device driver 와 firmware의 차이는 무엇인가요?

- device driver 는 CPU가 device controller 에게 작업을 부탁하는 용도로 사용되는 소프트웨어입니다, 즉 컴퓨터 내부에서 CPU가 수행하는 코드입니다.
- firmware는 디바이스에서 실행되는 자체적으로 내장된 코드로 Disk나 I/O 디바이스에 read/write하는 코드입니다

#

### 11. 동기식 입출력 (synschronous I/O)과 비동기식 입출력 (asynschronous I/O) 에 대해서 설명해주세요

&nbsp;&nbsp;&nbsp;&nbsp;<img src="24.png" width="400" height="200"><br/>

- 동기식: I/O 입출력시 시스템 콜을 한 후 입출력 작업이 완료된 이후에야 커널이 사용자 프로그램에게 CPU를 넘기는 방법입니다
- I/O 가 완료될 때 가지 OS가 CPU를 점유하게 됩니다
- 비동기식: I/O 입출력시 시트템 콜을 하고 입출력이 I/O 디바이스에서 실행되면 작업이 끝나기 전에 OS가 다른 사용자 프로그램에게 CPU를 바로 넘깁니다.
- 디바이스로부터 결과값을 가져와서 먼가 해야할 때는 동기식으로 처리해야하지만 쓰기 작업 같은 경우는 결과값을 기다리지 않아도 되기때문에 비동기식으로 할 수 있습니다
- 두경우 모두 I/O 작업이 끝나면 interrupt를 CPU에 보냅니다

#

### 12. DMA(direct memory access) Controller 란 무엇인가요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="25.png" width="400" height="200">
&nbsp;&nbsp;&nbsp;&nbsp;<img src="26.png" width="400" height="200"><br/>

- Interrupt도 일종의 오버헤드입니다. 특히 고속 I/O 장치의 경우 인터럽트가 너무 자주 발생해 성능저하 문제를 일으킬 수 있습니다
- 이를 방지하기 위해 DMA가 디바이스 버퍼에 저장되어 있던 I/O 값을 직접 메모리에 블록단위로 복사해서 저장합니다.  
- 따라서 바이트 단위가 아닌 블록 단위로 인터럽트가 발생합니다.

#

### 13. I/O를 수행하는 기계어 2가지에 대해 설명해주세요

&nbsp;&nbsp;&nbsp;&nbsp;<img src="27.png" width="400" height="200"><br/>

- CPU에서 I/O 작업을 요청하는 기계어를 실행할 때 메모리 주소와 디바이스 주소를 따로 나누어 접근하는 방식이 있고 아예 디바이스를 메모리 주소로 넣어 메모리 주소로만 접근하는 방식이 있습니다
- 후자의 경우를 Memory Mapped I/O 라고 합니다 

#

### 14. Caching 이란 무엇인가요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="28.png" width="400" height="200"><br/>

- 저장장치 계층 구조에서 원본 데이터는 항상 하위 계층에 있고 상위 계층에서는 필요한 정보만 뽑아쓰는 방식입니다.
- 하지만 언제나 정보를 아래에서 위까지 계속 끌어다 쓰면 오버헤드 문제가 있기 때문에 자주 사용할 정보는 상위 계층에 공간을 따로 만들어 저장해서 재사용할 경우 하위 계층까지 내려가지 않고 바로 가져다 씁니다. 
- 이러한 정보를 복사해서 상위 계층에 저장해놓는 시스템을 Caching 이라고 부릅니다
- 물론 용량에 제한이 있기 때문에 최대한 재사용성이 높은 정보를 저장해야 합니다
- (Primary는 excutable한 메모리, Secondary는 I/O 작업을 거쳐야하는 메모리)

<br/>

 ---

## 프로세스 관리

<br/>

### 1. 커널과 Virtual 메모리 주소 공간은 어떻게 구성되어 있나요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="pic/29.png" width="400" height="200"><br/>

- virtual memory 또한  code / data / stack 공간을 보유하고 있습니다
- 커널은 일종의 프로세스로서 code / data / stack 공간을 보유하고 있습니다
- 커널의 코드영역에는 시스템콜과 인터럽트 처리 코드 그리고 자원 관리와 기타 서비스를 위한 코드가 내재되어 있습니다
- 커널의 데이터 영역에는 모든 하드웨어들을 관리하기 위한 자료구조, 모든 프로세스들을 관리하기 위한 자료구조를 가지고 있습니다
- 이때 프로세스를 관리하기 위한 자료구조를 PCB라고 부릅니다

#

### 2. 사용자 프로그램이 사용하는 함수는 어떤 종류로 나뉘나요?

- 사용자 프로그램이 사용하는 함수는 사용자 정의 함수, 라이브러리 함수, 커널 함수 3가지 입니다.
- 사용자 정의 함수는 자신의 프로그램에서 정의한 함수(ex. 개발자가 정의한 함수)입니다.
- 라이브러리 함수는 외부에서 가져다 쓴 함수로 자신의 프로그램 실행파일에 포함되어 있습니다
- 커널함수는 운영체제 프로그램의 함수로 시스템 콜이 동작하는 함수입니다.

#

### 3. 한 프로그램의 실행 과정을 설명해주세요

&nbsp;&nbsp;&nbsp;&nbsp;<img src="pic/30.png" width="400" height="200"><br/>

- 함수의 종류에 따라 거쳐가는 주소공간이 다릅니다.
- 사용자 정의 함수와 라이브러리 함수는 사용자 프로그램 주소공간의 코드가 user mode에서 실행됩니다
- 반면에 시스템 콜이 불리면 운영체제에게 넘어가 kernel 주소공간의 커널함수가 실행됩니다.
- 즉 프로그램이 실행된다는 것은 사용자 프로그램 주소공간의 사용자저정의/라이브러리 함수 -> 시스템콜 -> 커널공간의 커널함수 -> ,,, 반복하다 프로그램이 끝나는 것입니다.

#

### 4. 프로세스의 문맥(Context)란 무엇인가요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="pic/31.png" width="400" height="200"><br/>

- 프로세스란 실행중인 프로그램을 말합니다 "Process is a program in execution"
- 프로세스가 진행되면서 현재 어떤 상태에 있느냐가 바로 프로세스의 문맥(Context)입니다. 따라서 Context는 시간에 따라 바뀌는 개념입니다.
- 현재를 놓고 봤을 때 이 프로세스는 CPU를 얼마나 쓰고있느냐, 메모리를 얼마나 가지고 있느냐, 어디함수를 실행하고 있는가 이런 종합된 정보가 프로세스의 Context 입니다.
- CPU에서 현재 상테에 PC는 어딜 가리키고 레지스터에는 어떤 값을 넣고 있었느냐와 같은 정보를 하드웨어 문맥이라고 부릅니다

#

### 5. Running, Ready, Blocked(wait, sleep) 상태에 있다는 말은 어떤 뜻인가요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="pic/32.png" width="400" height="200"><br/>

- CPU가 작업하고 있는 프로세스를 일컬어 Running상태에 있다고 부릅니다 (CPU를 잡고있는 프로세스)
- CPU를 쓰고싶지만 기다리고 있는 프로세스들을 Ready 상태에 있다고 부릅니다
- CPU를 줘봤자 실행하지 못하는, 오래걸리는 작업(I/O 작업등) 때문에 CPU를 얻어봤자 무의미한 프로세스를 Blocked 상태에 있다고 부릅니다.
- 프로세스는 언제나 위 3가지 상태중 하나에 놓이게 됩니다.

#

### 6. 프로세스 상태(state)에 대해 설명해주세요

&nbsp;&nbsp;&nbsp;&nbsp;<img src="pic/33.png" width="400" height="200"><br/>

- 프로세스의 상태는 Ready, Running, Waiting 3가지가 있습니다.
- ready상태에 있는 프로세스는 CPU만 준다면 바로 실행됩니다.(프로세스가 이미 메모리에 올라와있는등 다른 조건 만족한 상태)
- 앞선 프로세스가 CPU를 내주는 경우는 3가지입니다 -> timer interrupt, I/O 작업등으로 인한 Blocked 진입, exit(종료될 때) 
- 이때 주의할 점은 프로세스가 종료되면 더이상 프로세스가 아닙니다. terminated는 프로세스 종료전 무언가 뒷처리가 남은 상태입니다
- Running은 CPU를 점유하고 명령어들을 수행중인 상태입니다
- Blocked(Wait, Sleep)상태는 I/O등의 이벤트를 (스스로)기다리는 상태입니다

# 

### 7. Process Control Block(PCB)에 대해 설명해주세요

&nbsp;&nbsp;&nbsp;&nbsp;<img src="pic/34.png" width="400" height="200"><br/>

- 운영체제가 각 프로세스를 관리하기 위해 프로세스당 유지하는 정보를 말합니다.
- CPU를 프로세스들이 일정시간 점유하고 빠질 때 상태정보를 PCB에다 저장함으로써 나중에 다시 CPU를 점유할 때 PCB에 저장된 상태부터 계산을 시작합니다

#

### 7. 문맥교환(Context SwitCh)이란 무엇인가요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="pic/35.png" width="400" height="200"><br/>


- 프로세스 A에서 프로세스 B로 넘어가는 과정을 말합니다
- 즉 CPU를 한 프로세스에서 다른 프로세스로 넘겨주는 과정입니다.
- 운영체제는 이러한 문맥교환 과정에서 기존 프로세스 상태를 PCB에 저장하고, 새롭게 불러들이는 프로세스의 상태를 PCB로부터 읽어옵니다

#

### 8. system call이나 interrupt 발생시 항상 Context Switch가 일어나나요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="pic/36.png" width="400" height="200"><br/>

- 항상 문맥교환이 일어나는 것은 아닙니다. 사용자 프로세스가 바뀌지 않는다면 문맥교환없이 User mode로 복귀하게 됩니다.
- 문맥교환이 없는 경우에도 context의 일부를 PCB에 저장하지만 문맥교환 하는 경우의 부담보다 훨씬 적다고 볼 수 있습니다.

#

### 9. 스케줄러(Scheduler)에 대해서 설명해주세요

- 스케쥴러에는 3가지 종류가 있습니다 (장기 스케쥴러 / 단기 스케쥴러 / 중기 스케쥴러)
- 장기 스케쥴러는 프로세스 중 어떤 것들을 ready queue로 보낼지 결정합니다. 즉 프로세스에 memory를 주는 문제를 관리합니다. 하지만 time sharing system(요즘 쓰이는 리눅스 윈도우 등등)들은 장기 스케쥴러가 없이 이미 프로세스가 메모리에 올라온채로 시작합니다.
- 단기 스케쥴러는 timer interrupt가 걸릴 때마다 호출되는 스케쥴러로 어떤 프로세스를 다음번에 running시킬지 결정합니다. 즉 프로세스에 CPU를 주는 문제를 관리합니다
- time sharing systme은 장기 스케쥴러를 안쓰는 대신 중기스케쥴러를 사용하게 됩니다. Swapper라고도 불리는 이 녀석은 여유 공간 마련을 위해 프로세스를 통째로 메모리에서 디스크로 쫒아냅니다. 즉 프로세스에게서 메모리를 뺏는 역할을 합니다.
- 정리하자면 장기 스케쥴러는 프로세스에게 메모리를 주는 문제, 중기 스케쥴러는 프로세스로부터 메모리를 뺏는 문제를 담당합니다

#

### 10. 프로세스의 상태중 Blocked 와 Suspended 의 차이를 알려주세요

- 둘 모두 CPU를 얻을 수 없는 프로세스 상태입니다.
- 하지만 Blocked는 내부적인 이유(I/O등의 이벤트 기다림)로, Suspended의 경우 외부적인 이유(메모리 공간 부족으로 프로세스를 디스크로 쫒아냄)로 프로세스 수행이 정지된 상태입니다.

#

### 11. 디스크 I/O의 interrupt는 하드웨어 interrupt입니까? 소프트웨어 interrupt입니까?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="pic/37.png" width="400" height="200"><br/>

- 둘 모두 해당합니다.
- 프로세스가 CPU에서 Running 도중에 디스크 I/O 작업이 생긴다면 운영체제에게 요청합니다
- 운영체제는 디스크 컨트롤러에게 I/O작업을 요청합니다. -> 여기까지 system call -> 소프트웨어 interrupt
- I/O 작업이 다 끝나면 디스크 컨트롤러가 I/O작업이 다 끝났다고 interrupt를 겁니다 -> 하드웨어 interrupt

  #

### 12. Thread 란 무엇인가요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="pic/38.png" width="400" height="200"><br/>

- 프로세스 단위로 작업할 경우 프로세스의 주소공간(Code/Data/Stack)이 작업마다 만들어지고 동일한 프로세스의 프로그램(웹브라우저를 여러개 실행시킨다던지)을 실행시키면 앞선 주소공간을 중복해서 사용하는 문제점이 발생합니다. 또한 Context Switch도 오버헤드가 크기 때문에 최대한 줄여야합니다.
- 이를 효율적으로 처리하기 위해 하나의 프로세스 작업 안에서 CPU 작업 수행 단위인 Thread를 이용하게 되었습니다
- 스택 공간에서 스레드를 구분해서 사용하고 코드, 데이터, 힙 공간을 공유함으로서 효율적으로 하나의 프로세스 작업을 수행합니다. 이를 통해 Context Switch 횟수도 최소화할 수 있습니다.

#

### 13. Task란 무엇인가요?

- Task란 Thread가 동료 Thread와 공유하는 부분을  말합니다
- 이러한 Task에는 코드, 데이터, 힙, OS resource가 있습니다.

#

### 14. Thread 의 장점을 설명해주세요

- 다중스레드로 구성된 경우 하나의 서버스레드가 blocked 상태더라도 동일한 task내의 다른 스레드가 running되어 빠른 처리가 가능해집니다
- 동일한 일을 수행하는 다중스레드가 협력하여 높은 처리율(throughput)을 달성합니다
- 스레드를 사용하면 병렬성을 높일 수 있습니다.
- (프로세스를 하나 만드는 것보다 스레드 하나를 만드는 것보다 30배의 시간이 걸립니다)
- (프로세스의 문맥전환과 스레드 전환의 시간차이는 5배가 납니다)

#

### 15. Kernel thread 에 대해 설명해주세요

&nbsp;&nbsp;&nbsp;&nbsp;<img src="pic/39.png" width="400" height="200"><br/>

- thread는 프로세스 내에서의 작업단위이지만 이러한 프로세스를 운영체제에서 알고 있는 경우가 있습니다. 이를 Kernel Thread라고 부릅니다. 
- 운영체제가 thread를 모르는 경우에는 User thread라고 부릅니다. 이러한 User thread는 프로세스 포장지에 잘 포장되어 운영체제가 직접 접근할 수 없습니다.
- kernel thread는 운영체제가 직접 전환을 명령할 수 있습니다

#

### 16. 프로세스는 어떻게 만들어지나요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="pic/40.png" width="400" height="200"><br/>

- 부모 프로세스(Parent process)가 자식 프로세스(children process) 생성하는 방법으로 만들어집니다.
- 이때 부모 프로세스는 직접 만들지 못하고 System call을 통해 운영체제에게 부탁합니다. 이때 시스템콜 이름을 `fork()`라고 부릅니다
- 다시말해 `fork()`는 자식프로세스를 만들어달라는 커널의 함수입니다. 이 `fork()`에 의해 프로세스가 만들어집니다 -> 독자적인 코드,데이터,스택 공간이 만들어집니다.
- 이때 자식프로세스는 별개의 프로세스로 취급하지만 경우에 따라 부모프로세스와 자원을 공유하기도합니다.

#

### 17. 프로세스가 만들어진 이후에 실행과정은 어떻게 되나요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="pic/41.png" width="400" height="200"><br/>

- 부모 프로세스를 `fork()`에 의해 자식프로세스를 만듦에 있어 부모를 그대로 복사하다보니 전역변수/함수들이나 각종 데이터들이 그대로 넘어오게됩니다.
- 그래서 `fork()` 이후에 `exec()`이라는 시스템 콜을 실행시켜 새로운 프로세스 메모리를 덮어 씌웁니다.

#

### 18. 프로세스 종료(process termination) 과정은 어떻게 되나요?

- 프로세스가 종료될 때는 운양체제에게 `exit()` 시스템 콜을 통해 종료되었음을 알려줍니다.
- 자식 프로세스가 종료될 때는 `wait()`을 통해부모 프로세스에게 종료되었음을 알립니다.
- 경우에 따라 부모 프로세스가 자식 프로세스의 수행을 종료시키는 경우 `abort()`를 실행시킵니다
- 이러한 경우의 예로는 자식이 할당 자원의 한계치를 넘어서거나, 자식에게 할당된 태스크가 더이상 필요하지않은 경우 등이 있습니다.
- 부모 프로세스가 자식프로세스가 먼저 끝나는 경우 운영체제는 자식프로세스 부터 종료시키게 됩니다 -> 단계적인 종료

#

### 19. 부모프로세스와 자식프로세스는 어떻게 구분되나요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://www.it.uu.se/education/course/homepage/os/vt18/images/module-2/fork-details.png" width="400" height="200"><br/>

- `fork()` 시스템 콜이 실행되면 `exec`이 실행되지 전까지 부모 프로세스가 그대로 복제되어 자식프로세스를 만들기 때문에 구분이 어렵습니다.
- 이때 pid 값을 자식 프로세스에게는 0을 할당하여 pid number을 통해 구분할 수 있습니다.

#

### 20. 프로세스와 관련된 시스템 콜을 정리해주세요

- 프로세스와 관련된 시스템 콜은 4가지가 있습니다
- `fork()`: 자식 프로세스를 만들 때 사용합니다
- `exec()`: 자식 프로세스에 데이터를 덮어씌울 때 사용합니다
- `wait()`: 자식 프로세스를 종료시킬 때 사용합니다
- `exit()`: 부모 프로세스를, 전체적인 프로세스를 종료시킬 때 사용합니다

#

### 21. 프로세스 종료에서 자발적 종료와 비자발적 종료에 대해 설명해주세요

- 프로세스 종료에는 두가지 종류, 자발적 종료와 비자발적 종료가 있습니다.
- 자발적 종료는 말그대로 작업을 다 마치고 자연스럽게 종료되는 종료입니다.
- 자발적 종료는 마지막 statement 수행후 exit() 시스템 콜이 실행됩니다. 이때 개발자가 굳이 적지 않더라도 컴파일러가 자동적으로 `main()`함수가 리턴되는 위치에 넣어줍니다.
- 비자발적 종료는 키보드로 kill, break등을 쳐서 부모 프로세스나 자식프로세스를 강제종료시키는 경우입니다.
- 이러한 경우의 특징은 자식프로세스가 메모리 한계치를 넘어서거나 자식 프로세스 할 일이 더이상 필요하지 않는 경우가 있으며 부모 프로세스를 강제종료 시킬경우 자식 프로세스를 먼저 죽이고 부모 프로세스를 죽이는 단계적인 종료절차가 진행됩니다.

<br/>

 ---

## CPU 스케쥴링

<br/>

### 01. 프로세스 간 협력은 어떻게 이루어지나요?

- 평소에는 프로세스는 CPU와 메모리를 두고 경쟁을 하게 됩니다.
- 또한 프로세스는 메모리 공간이 독립적이라 다른 프로세스의 메모리를 들여다볼 수 없습니다.
- 하지만 경우에 따라 프로세스끼리 협력해야하는 상황이 있습니다. 이러한 협력 방법은 크게 두 가지 종류가 있습니다 - 메세지 전달 방법 / 주소 공간 공유 방법

#

### 02. 메세지 전달 방법에 대해 설명해주세요

&nbsp;&nbsp;&nbsp;&nbsp;<img src="pic/42.png" width="400" height="200">
&nbsp;&nbsp;&nbsp;&nbsp;<img src="pic/43.png" width="400" height="200"><br/>

- P라는 프로세스와 Q라는 프로세스는 메세지를 매개로 협력하게 됩니다
- 하지만 서로다른 프로세스끼리 메세지를 직접 보낼 수 없기 때문에 kernel(운영체제)를 중간에 한 번 거쳐서 보내게됩니다.(시스템 콜)
- 메세지 패싱 방법은 목적지를 명시하는 Direct Communication과 누구한테 전달하지는 모르지만 메일박스or포트m에다 메세지를 넣고 먼저 메일박스를 열게되는 프로세스와 공유하는 방법인 Indirect Communication이 있습니다.

#

### 03. 주소 공간을 공유하는 방법에 대해 설명해주세요

&nbsp;&nbsp;&nbsp;&nbsp;<img src="pic/43.png" width="400" height="200"><br/>

- 원칙적으로는 프로세스는 각자의 데이터공간을 가지고 있어 분리되어 있습니다
- 하지만 이렇게 메모리 공간을 공유하는 경우 운영체제에게 시스템 콜을 요청해서 공통된 메모리 공간을 공유합니다
#

### 04.CPU burst 와 I/O burst에 대해 설명해주세요

&nbsp;&nbsp;&nbsp;&nbsp;<img src="pic/44.png" width="400" height="200"><br/>

- CPU burst는 CPU가 기계어를 해석하고 있는 단계, I/O하는 단계를 I/O burst라고 부릅니다
- 프로그램별로 burst의 간격은 다릅니다. 주로 사람과 ineract하는 프로그램이 사진처럼 버스트가 번갈아 등장하게 됩니다. 연산량을 많이 필요로하는 작업은 CPU Burst의 간격이 넓어지게 됩니다.
- 이러한 I/O를 길게 쓰는 프로그램을 I/O bound job(process), CPU를 길게 쓰는 프로그램을 CPU bound job(process)이라고 부릅니다.
- 

#

### 05. Burst time에 따라 CPU 우선권은 어떻게 달라지나요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="pic/45.png" width="400" height="200"><br/>

- I/O bound job 과 CPU bound job 중 운영체제는 I/O bound job에게 먼저 CPU 사용 우선권을 주게됩니다.
- I/O bound job 에게 CPU를 먼저 할당해야 오래걸리는 I/O 작업을 하러 떠남으로서 더 효율적으로 프로세스 관리가 이루어지게 되기 때문입니다.
- 또한 I/O bound job은 사람과 interaction 하는 작업이기 때문에 최대한 먼저 결과물을 전달해주어야 합니다.

#

### 06. CPU scheduler 와 Dispathcer는 무엇인가요?

- 운영체제의 코드중 일부코드입니다.
- CPU 스케쥴러 코드는 Reay상태 프로세스 중에 CPU를 할당해줄 프로세스를 고릅니다.
- Dispatcher 코드는 CPU의 제어권을 CPU 스케쥴러에 의해 선택된 프로세스에게 넘깁니다. 이러한 과정을 문맥 교환이라고도 부릅니다.

#

### 07. Process의 상태변화에 대해서 설명해주세요

- CPU 스케줄링이 필요한 경우는 다음과 같은 상태변화가 있습니다.
1. Running -> Blocked (예: I/O 요청하는 시스템 콜)
2. Running -> Ready (예: 할당시간 만료로 timer inerrupt)
3. Blocked -> Ready (예: I/O 완료후 인터럽트)
4. Terminated
- 1~4 스케쥴링은 강제로 빼앗지 않고 자진 CPU 제어권을 반납하는 **nonpreemptive** scheduling
- 1~4 에 해당하지 않는 모든 스케쥴링은 강제로 빼았는 **preemptive** scheduling

# 

### 08. CPU 성능 척도(performance index)에 있어 기준이 무엇인지 설명해주세요

- CPU 성능 척도의 기준은 5가지입니다. 1,2은 시스템의 입장, 3,4,5는 클라이언트의 입장이라 볼 수 있습니다.
1. CPU 이용률 (CPU utilization)
2. 처리량 (Throughput)
3. 소요시간, 반환시간 (Turnaround time)
4. 대기시간 (Waiting time)
5. 응답시간 (Repsonse time)

#

### 09. 스케쥴링 알고리즘 중 FCFS(Fisrt-Come Fisrt-Served) 에 대해 설명해주세요

&nbsp;&nbsp;&nbsp;&nbsp;<img src="pic/46.png" width="400" height="200"><br/>

- FCFS는 먼저 도착한 프로세스에게 가장 먼저 CPU 제어권을 줍니다.
- 이러한 선착순대로 처리하는 방법(FCFS)는 non-preemptive한 스케쥴링입니다.
- 하지만 만약 앞선 프로세스의 작업량이 많고 뒤이은 프로세스의 작업량이 적은 경우 매우 비효율적인 스케쥴링이 될 수 있습니다
- 이러한 FCFS처럼 순서에 따라 성능차이가 나는 것을 **Convoy effect**라고 부릅니다

#

### 10. 스케쥴링 알고리즘 중 SJF(Shortest-Job-Fisrt)에 대해 설명해주세요

&nbsp;&nbsp;&nbsp;&nbsp;<img src="pic/47.png" width="400" height="200"><br/>

- SJF는 짧은 작업량을 먼저 처리할 수 있도록 CPU 제어권을 넘기는 알고리즘으로 Convoy effect를 고려한 방법이라고 할 수 있습니다
- SJG는 대기시간의 관점에서 보았을 때 가장 최적화된 방법이라고 볼 수 있습니다
- 만약 한 프로세스에게 CPU 제어권을 넘겼는데 더 짧은 작업량의 프로세스가 온다면 일단 제어권을 가지고 있는 프로세스의 작업 마무리는 기다려 줍니다 -> non-preemptive
- 만약 대기큐에서 더 짧은 프로세스가 온다면 이 프로세스를 우선순위를 앞에다 둡니다 -> preemptive
- 가장 최적화된 방법은 preemptive 입니다.

#

### 11. SJF(Shortest-Job-Fisrt)의 단점에 대해서 설명해주세요

&nbsp;&nbsp;&nbsp;&nbsp;<img src="pic/48.png" width="400" height="200"><br/>

- SJF는 사실상 최적화된 방법임에도 치명적인 두 가지 약점이 있습니다.
- 가장 먼저 **Starvation** 문제가 있다는 것입니다. 계속해서 작업량이 적은 프로세스가 새치기를 할경우 뒤에있던 프로세스가 영원히 처리되지 않을 수도 있습니다
- 두번째는 CPU burst time에 대한 파악이 정확하지 않다는 문제입니다. 운영체제는 각 프로세스의 CPU 작업량을 인풋 데이터나 브런치, 과거의 CPU burst(exponential reveraging)등을 종합하여 **추정**할 뿐입니다. 따라서 만약 짧다고 생각해서 CPU 제어권을 넘겼는데 알고보니 CPU작업량을 많이 차지하는 녀석이라면 문제가 될 수 있습니다.

#

### 12. 스케쥴링 알고리즘 중 Priority Scheduling에 대해 설명해주세요

- 우선순위가 높은 프로세스에게 CPU 제어권을 넘깁니다. SJF도 일종의 Priority Scheduling이라고 볼 수 있습니다.
- 이때 SJF는 Priority를 CPU burst time 예측으로 매깁니다.
- 따라서 Priority Scheduling 도 **Starvation** 이라는 문제점을 가지고 있습니다
- Priority Scheduling에서는 Starvation의 문제 해결방안으로 **Aging**을 사용하고 있습니다.
- **Aging**이란 큐에 머물러있는 시간에 따라 프로세스의 우선순위를 높여주는 방법입니다.

#

### 13. 스케쥴링 알고리즘 중 Round Robin(RR)에 대해 설명해주세요

&nbsp;&nbsp;&nbsp;&nbsp;<img src="pic/48.png" width="400" height="200"><br/>

- 프로세스에게 CPU를 넘길 때 timer을 사용해서 점유시간을 미리 설정해놓는 방식입니다
- 일정시간이 지나면 인터럽트가 걸려 운영체제에게 다시 CPU가 넘어갑니다. 이때 할당시간을 **time quantum** 이라 부릅니다
- 현대 운영체제 프로그램에서 가장 많이 쓰이는 알고리즘입니다.
- 한 가지 단점은 일반적으로 SJF보다 프로세스당 평균적으로 작업 끝내는 시간이 길어진다는 것입니다.
- 따라서 RR은 비슷한 동일한 작업들이 있을 때보다 짧은 작업, 긴 작업 섞여있있을 때 써야 효율적입니다.




<br/>

 ---

## 병행제어

<br/>

### 01. Multilevel Queue란 무엇인가요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="pic/49.png" width="400" height="200"><br/>

- 이전까지의 큐가 한 라인의 큐였다면 Ready queue를 여러개로 분할하는 것을 말합니다
- Multi level Queue에서는 큐의 종류를 두가지로 나눕니다. -> **foreground** / **background**
- 이러한 큐를 나누는 기준은 사용자와 ineteract를 하는경우에 foreground 큐에 그렇지 않은 경우에 background 큐에 둡니다
- forground는 사용자와 interactive하기 때문에 더 많은 CPU time 을 줍니다
- 보통 Time slice로 RR알고리즘을 사용하여 80%는 foreground, 20%는 FCFS 알고리즘으로 background에 할당하여 starvation을 방지합니다

#

### 02. Hard Real time system 과 Soft real time system 의 차이를 알려주세요

- Hard real time system 의 task는 정해진 시간안에 반드시 끝내도록 스케쥴링 해야합니다
- Hard real time system 은 데드라인을 지키는 것이 매우 중요하기 때문에 offline 스케쥴링이 많습니다 (offline: 미리 프로세스들이 언제 도착할지 알고있음)
- Soft real time system 은 정해진 시간에 완수하지 못하더라도 높은 priority의 작업으로 할당해야합니다(동영상 스트리밍 etc)
- Soft real time system 은 online 스케쥴링으로 됩니다 (프로세스 도착 시간 미리 생각안하고 그때그때 처리)

#

### 03. Thread 를 구현하는 2가지 방법에 대해서 설명해주세요

- Thread scheduling에는 Local Scheduling과 Global scheduling 두 가지 방법이 있습니다.
- 운영체제가 스레드의 존재 유무를 알고 있다면 커널에 의해 스케쥴링 되는 global scheduling, 운영체제가 해당 스레드의 존재유무를 모른다면 (user level thread) 라면 프로세스 내부에서 스케줄링이 결정되는 local scheduling이 있습니다.

# 

### 04. 어떤 CPU 스케쥴링이 좋은 알고리즘인지 어떻게 평가할까요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="pic/50.png" width="400" height="200"><br/>

- 크게 3가지 방법이 있습니다 (**Queueing models**, **Implementation(구현)&Measurement(성능측정)**, **Simulation(모의 실험)**)
- Queueing models: Arrival rate(도착율-얼마나 빠른 빈도로 CPU를 쓰겠다고 도착하느냐)와 Service rate(처리율-단위시간당 얼마나 많은 작업을 처리하느냐) 두 가지를 이용해서 평가합니다.
- Implementation(구현)&Measurement(성능측정): 실제로 구현해서 작업 비교를 통해 성능을 측정하는 방법입니다.
- Simulation(모의 실험): 실제로 구현하는 것이 아닌 가상적으로 돌려보는 방법입니다. trace(주어진 작업)를 모의프로그램으로 돌려보는 방법이라고 할 수 있습니다.

#

### 05. 컴퓨터가 데이터를 접근하는 순서가 어떻게 되나요

&nbsp;&nbsp;&nbsp;&nbsp;<img src="pic/51.png" width="400" height="200"><br/>

1. 먼저 데이터가 저장되어 있어야합니다
2. 저장된 데이터 중 연산할 데이터를 읽어옵니다.
3. 데이터를 연산합니다
4. 연산결과를 다시 데이터에 저장합니다
   
#

### 06. Race condition(경쟁 상황)이란 어떤 상황을 이야기하나요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="pic/52.png" width="400" height="200"><br/>

- 만약 읽어가는 연산이 2개 이상 있을 경우 Race Condition의 가능성이 있습니다
- 이때 Race condition이란 한쪽이 1을 더하는 연산, 한쪽이 1을 빼는 연산을 할 때 둘의 순서에 따라 저장값에 차이가 납니다.
- 이러한 S-box(memory address space)를 두고 여러 E-Box(CPU process)가 경쟁하는 상황을 Race Condition이라 부릅니다

#

### 07. 경쟁상황은 CPU가 2개 이상이여만 생기나요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="pic/53.png" width="400" height="200"><br/>

- 그렇지 않습니다. CPU가 1개일 때도 경쟁상황이 나타날 수 있습니다.
- 한 프로세스가 CPU를 가지고 일을 하다 운영체제에게 시스템 콜을 합니다. 이렇게 운영체제 안의 데이터값을 바꾸고 있을 때 자신의 CPU할당시간이 끝나버려 다음 프로세스에게 넘어갑니다.
- 이 때 다음 프로세스도 시스템 콜을 하게되면서 그전의 프로세스가 날린 시스템 콜이 건드리는 커널의 데이터와 겹치게 되면 경쟁상황이 발생합니다.
- 즉 프로세스에 의해서도 경쟁상황이 발생합니다

#

### 08. 어떻게 Race condition(경쟁상황)을 해소할 수 있을까요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="pic/54.png" width="400" height="200"><br/>

- 시스템 콜을 하여 커널모드에서 수행 중일 때는 CPU를 사용하지 않는 것입니다.
- 즉 커널 모드에서는 CPU를 preempt(점유)하지 않고 커널 모드에서 사용자모드로 돌아갈 때 다시 preempt 합니다.

#

### 09. Process Synchronization 문제란 무엇인가요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="pic/55.png" width="400" height="200"><br/>

- 공유 데이터(shared data)의 동시접근(concurrent access)할 때 생기는 문제로 데이터 불일치 문제(inconsistency)입니다.
- 이를 방지하기 위해, 다시말해 일관성(consistency) 유지를 ㅜ이해 협력 프로세스(Cooperating process)간의 실행 순서(orderly execution)를 정해주는 매커니즘이 필요합니다.
- 이러한 겹쳐서 이용되는 구간(Critical section)에 하나의 프로세스가 있을 때 모든 프로세스를 막는 방법(lock)으로 문제를 보완할 수 있습니다.


### 10. 프로세스 간의 경쟁상황을 해결하는 충족 조건을 말해주세요

- 프로세스 간 경쟁상황을 해결하는 조건은 3가지가 있습니다 -> Mutual Exclusion, Progress, Bounded Waiting
- Mutual Exclusion(상호배제): 한 프로세스가 Critical Section을 이용중이면 다른 프로세스는 이용불가 -> **Mutex**
- Progress(진행): Critical Section 이용 대기자가 없으면 이용하고자 하는 프로세스에게 내준다
- Bounded Waiting(유한대기): 프로세스 대기열이 길 경우 각 프로세스 대기 시간이 유효해야 한다 (starvation이 생기지 않도록)

#

### 11. 하드웨어 측면에서 경쟁상황을 어떻게 해결할 수 있을까요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="pic/56.png" width="400" height="200"><br/>

- 하드웨어에서 데이터를 atomic하게 작업할 수 있도록 해준다면 문제를 해결할 수 있습니다
- 즉 접근과 수정을 하나의 단위로 묶는 작업(Test and set) 으로 하드웨어에서 보완하는 것입니다. 이
- 이렇게 되면 단순히 작업할 때와 하지 않을 때 락을 걸거나 풀기만 하면 됩니다.

#

### 12. Semaphores 란 무엇인가요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="pic/57.png" width="400" height="200"><br/>

- 세마포란 일종의 추상 자료형으로 앞선 경쟁상황을 처리하기 위한 일종의 방법입니다.
- 세마포 변수값은 정수로 정의됩니다.(자원을 쓰는 개수), 만약 Smeaphore mutex(세마포 변수) 가 1이면 1개가 Critical Secstion에 들어갈 수 있다.
- 세마포 자료형의 연산은 p연산과 v연산 두가지로 이루어집니다, P연산은 자원을 획득하는 과정, V연산은 자원을 반납하는 과정입니다
- 예를 들어 세마포어 변수값이 1이면 P연산을 할경우 lock을 획득하는 과정이라 볼 수 있습니다.
- 자원을 다쓰고 나올때 v연산을 하게되면 lock이 풀리는 과정이라고 볼 수 있습니다.
- 이러한 p연산과 v연산 사이에 공유자원을 쓰는 작업이 수행됩니다. 세마포는 이러한 P연산 - CS작업 - V연산을 atomic하게 처리합니다
  
#

### 13. busy wait 문제란 무엇인가요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="pic/58.png" width="400" height="200"><br/>

- 만약 누군가 CS에 들어가 있어서 뮤텍스 값이 0일 때 P연산을 하면 P연산의 While문에서 무한루프가 돌아가 아무도 CS에 접근하지 못하는 문제를 busy-wait문제라 합니다.
- 앞선 CS작업을 하는 녀석이 빠져나와야 불필요한 P연산의 while 반복문을 끝낼 수 있습니다

#

### 14. Block / Wake up 방식이란 무엇인가요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="pic/59.png" width="400" height="200"><br/>

- 앞선 busy-wait문제를 방지할 수 있는 세마포 구현방식입니다.
- 이전에 세마포 변수에 정수를 설정하여 0이면 잠그고 1이상이면 열었던 단순한 방식과 다르게 이 방식에서는 세마포 구조체를 만들어 관리합니다.
- 세마포 변수L에 의해서 프로세스들을 줄세워 기다리게 하는 방법입니다.
- Block / Wake up 방식을 사용하면 이전에 CPU를 계속 쓰면서(p연산 while문에서 대기하면서) 대기 했던 것과 다르게 CPU 밖 큐라는 대기열에서 프로세스들이 대기하게 됩니다. (blokced 되면서 큐에서 sleep하게 합니다, 쓰게할 때는 wake up)

#

### 15. Busy-Wait 와 Block/WakeUp 중 어떤 세마포 구현 방법이 더좋은지 알려주세요

- 일반적으로 Block/WakeUp이 더 효율적입니다. Busy-Wait 방식은 대기를 하는 프로세스가 CPU에서 계속 동작하고 있기 때문입니다.
- 하지만 Critical Section의 길이가 매우 짧은 경우 WakeUp도 일종의 오버헤드이기 때문에 busy-wait가 좀더 효율적일 수 있습니다.

#

### 16. Mutex(Binary semaphore)와 Counting semaphore의 차이를 알려주세요

- 전자는 세마포 변수값이 0 또는 1만 가지고 후자는 세마포 변수값이 0이상의 임의의 정수값을 가집니다.
- 전자의 경우 mutual exclusion(락걸고 풀기)에 사용되고 후자의 경우 resource counting에 사용됩니다.

#

### 17. Bounded Buffer Problem(Producer-Consumer Problem) 이란 무엇인가요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="pic/60.png" width="400" height="200"><br/>

- 공유데이터를 쓰는 Buffer에서 경쟁상황이 생기는 문제입니다.
- 공유데이터 버퍼에는 두가지 프로세스가 있습니다 (Producer-생산자 프로세스 와 Consumer-소비자 프로세스)
- 만약 Producer가 버퍼를 채우고 있을 때 다른 Producer에게 CPU를 빼앗기면 똑같은 빈 버퍼에 데이터가 중복되어 저장되어 유실되는 문제가 있습니다. 이러한 비슷한 상황이 Consumer에서도 발생합니다.
- 이러한 Bounded Buffer Problem을 방지하기 위해 lock을 거는 방법이 있습니다.

#

### 18. Readers-Writer Problem 이란 무엇인가요?

- 주로 DB에서 발생하는 문제로 한 프로세스가 Write 중일 때 다른 프로세스가 접근하는 경우 생기는 문제입니다. (read는 동시에 여럿이 해도 문제 x)
- 이를 해결하기 위해서는 Writer가 진입할 때는 대기 중인 Reader가 없을 때만 허용하고 Writer가 빠져나가야만 Reader의 접근을 허용합니다
- 이때 Writer가 일찍 도착했음에도 Reader가 계속와서 틈을 주지 않으면 Starvation 문제가 발생할 수 있습니다.
- 이러한 Starvation은 일정시간 단위로 reader의 접근을 허용하고 짤라 Writer를 들어오게 함으로써 문제를 보완할 수 있습니다.

#

### 19. Dining-Philosophers Problem 이 무엇인지  설명해주세요 

&nbsp;&nbsp;&nbsp;&nbsp;<img src="pic/61.png" width="400" height="200"><br/>

- 탁자에 둘러앉아 식사를 하는데 한 사람이 오른쪽 젓가락을 쓰고있고 왼쪽 젓가락을 기다리고 또 옆에 사람은 왼쪽 젓가락을 기다리고 오른쪽 젓가락을 쓰고있는.. 자기 젓가락을 안내려놓고 서로의 젓가락을 기다리기만 기다리는 상황을 Dining-Philosophers Problem 이라고 합니다. 이때 젓가락은 공유데이터이고 세마포의 경우 1로 설정되었다고 볼 수 있습니다.
- 일종의 데드락 상황이라고 볼 수 있습니다.
- 이를 해결하기 위해서는 젓가락 두개 모두 집을 수 있을 때만 젓가락을 집을 수 있게하는 방법이 있습니다
- 또다른 방법으로는 데드락을 해결하는 대표적인 방법인 짝수(홀수) 철학자는 왼쪽(오른쪽) 젓가락부터 잡도록 설계하는 방법이 있습니다.

#

### 20. 

