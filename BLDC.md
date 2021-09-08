# BLDC Motor

### link
https://www.youtube.com/watch?v=bCEiOnuODac

## BLDC 모터의 구조
DC 모터는 브러쉬를 통한 기계적인 접촉 구조이냐 아니냐에 따라 Brushed DC 모터와 Brushed less DC 모터로 구분합니다.
<br>
<img src="./img/DC_Motor.PNG" width = 20%><br>**DC_Motor**</img>
1. Brushed DC 모터는 2개의 전선으로만 구성되어 있다.
  - 장점 : ***전동기를 구동시키기 위한 드라이버의 설계 및 제어가 용이하다
  - 단점 : Brush의 접촉을 통해서 회전에 따라 전기자 전류의 극성이 바뀌게 되므로, ***기계적 소음과 전기적 잡음이 심하며 내구성이 떨어짐.
  -     : 긴 수명과 신뢰성을 요구하는 작업에서는 사용되어서는 안 된다.
<br>
<img src="./img/Brushed_DC_Motor.PNG" width = 60%><br>**Brushed_DC_Motor**</img>
2. BLDC 모터는 Brushr 가 제거된 형태입니다. 위 그림에서 보이듯 BLDC 모터는 가운데 영구자석으로 되어있는 회전자, 고정자의 이빨에 권선이 감겨있는 형태입니다.
   또한, BLDC 모터의 영구자석(회전자)을 회전 시키기 위해서는 영구자석의 위치 및 극성에 따라 회전자에서 정확한 시점과 정확한 방향으로 자속을 발생시켜야 합니다.
   [ 홀센서 - 3개  :  영구자석의 위치를 검출하기 위해 ]
   [ 전선 - 3개    :  3상을 스위칭하여 제어하기 때문에 ]
  - 장점 : 소음이 더 적다
        : 동일한 출력을 내는 Brushed 모터에 비해 가볍다.
        
## BLDC 모터 내부 구조
<img src="./img/BLDC_Motor_Rotor.PNG" width = 60%>**BLDC 모터 회전자(Rotor)**</img>
<br>
BLDC 모터의 Rotor(회전자)는 영구 자석입니다.

<br>
<img src="./img/BLDC_Motor_Stator.PNG" width = 60%>**BLDC 모터 고정자(Stator)**</img>
<img src="./img/BLDC_Motor_Stator2.PNG" width = 60%>**BLDC 모터 고정자(Stator)**</img>
<img src="./img/BLDC_Motor_Stator3.PNG" width = 60%>**BLDC 모터 고정자(Stator)**</img>

고정자(Stator)는 보이는 것과 같은 코일 배열을 갖습니다.

<br>
<img src="./img/BLDC_Motor_Coil.PNG" width = 60%>**BLDC 모터 코일(Coil)**</img>
<img src="./img/BLDC_Motor_Coil2.PNG" width = 60%>**BLDC 모터 코일(Coil)**</img>
<img src="./img/BLDC_Motor_Coil3.PNG" width = 60%>**BLDC 모터 코일(Coil)**</img>

코일에 전원이 들어가면서 전자석이 됩니다.

<br>
<img src="./img/BLDC_Motor_Movement.PNG" width = 60%>**BLDC**</img>
<img src="./img/BLDC_Motor_Movement2.PNG" width = 60%>**BLDC 모터 동작**</img>
<img src="./img/BLDC_Motor_Movement3.PNG" width = 60%>**BLDC 모터 동작**</img>
<img src="./img/BLDC_Motor_Movement4.PNG" width = 60%>**BLDC 모터 동작**</img>
<img src="./img/BLDC_Motor_Movement5.PNG" width = 60%>**BLDC 모터 동작**</img>
<img src="./img/BLDC_Motor_Movement6.PNG" width = 60%>**BLDC 모터 동작**</img>

<br>
1. 코일 A에 전류가 흐르면 반대쪽 극에서 회전자와 고정자가 서로를 끌어 당기고
2. 코일 A에서 코일 B로 가까워지면서 코일 B에 동력이 발생합니다
3. 마찬가지로, 회저자가 코일 B에서 코일 C로 갈 때, 동력이 발생합니다
4. 그 이후 코일에서는 반대의 극성의 전압이 발생합니다
5. 이 과정은 반복되며 회전자는 계속해서 반복합니다


<br>
<img src="./img/BLDC_Motor_Movement7.PNG" width = 60%>**BLDC 모터 동작**</img>
<img src="./img/BLDC_Motor_fault.PNG" width = 60%>**BLDC 작동 중, 단점**</img>
<img src="./img/BLDC_Motor_fault2.PNG" width = 60%>**BLDC 작동 중, 단점**</img>

BLDC 모터 단점
- 단 하나의 코일에만 전기가 흐르고 다른 두 개의 모터에는 전기가 흐르지 않기 때문에, 모터의 힘이 많이 줄어든다.

<img src="./img/BLDC_Motor_trick.PNG" width = 60%>**BLDC 모터 힘 출력 트릭**</img>
<img src="./img/BLDC_Motor_trick2.PNG" width = 60%>**BLDC 모터 힘 출력 트릭**</img>
<img src="./img/BLDC_Motor_tric3k.PNG" width = 60%>**BLDC 모터 힘 출력 트릭**</img>
<img src="./img/BLDC_Motor_trick4.PNG" width = 60%>**BLDC 모터 힘 출력 트릭**</img>

*이 문제를 해결하는 트릭이 있다.
1. 회전자가 회전자를 당기는 첫 번쨰 코일과 함께 있을 때, 그 뒤에 있는 코일을 이용하여 이러한 방법으로 로터를 미는 방향으로 코일에 전압을 가할 수 있다.
2. 동일한 극성의 전류가 두 번째 코일을 통과하면, 결합된 효과로 인해 모터에서 더 많은 힘이 출력된다.
3. 결합된 힘은 BLDC가 이 구성으로 일정한 특성을 갖도록 합니다.
4. 이 구성에서는 2개의 코일을 개별적으로 에너자이징 해야합니다.

<br>
<img src="./img/BLDC_Motor_connection.PNG" width = 60%>**BLDC 모터 연결 단순화**</img>
<img src="./img/BLDC_Motor_connection2.PNG" width = 60%>**BLDC 모터 연결 단순화**</img>
<img src="./img/BLDC_Motor_connection3.PNG" width = 60%>**BLDC 모터 연결 단순화**</img>
<img src="./img/BLDC_Motor_connection4.PNG" width = 60%>**BLDC 모터 연결 단순화**</img>


*고정자 코일 수정하여 모터의 작동 과정을 단순화 할 수 있다.
1. 코일의 한쪽 끝을 연결하는 것으로 과정을 단순화 할 수 있다.
2. 코일 A와 B사이에 전원을 넣었을 때, 코일을 통해 흐르는 전류는


<img src="./img/BLDC_Motor_connection5.PNG" width = 60%>**BLDC 모터 연결 단순화**</img>
3. BLDC 동작에서 어떦게 회전자가 지속적으로 회전하는 동안 고정자에서 동력이 발생하는 의구심을 가지게 된다.

<img src="./img/BLDC_Motor_connection6.PNG" width = 60%>**BLDC 모터 연결 단순화**</img>
4. 제어기는 회전자의 위치와 기본적인 센서의 정보가 코일의 동력을 발생하는데 결정한다.

<img src="./img/BLDC_Motor_connection7.PNG" width = 60%>**BLDC 모터 연결 단순화**</img>
5. 그리고 홀 효과 센서를 사용한다.



<br>
## BLDC 모터의 구동 원리
BLDC 전동기를 구동시키기 위해서는 회전자(영구자석)가 회전하도록 영구자석의 위치에 따라 고정자의 권선에 전류를 흘려서 자속을 발생시킬 권선을 순시적으로 바꾸어 주어야 합니다.
<img src="./img/BLDC_Cycle_Sequence.PNG" width = 60%> **BLDC 전동기의 회전 순서**</img>

윗 그림과 같이 3상 2극의 BLDC 전동기를 예로 들어 보겠습니다.
가운데 영구자석이 회전하고 고정자에는 3개의 고정자 상이 존재합니다. 
이 때, 각각의 상을 U, V, W 상이라고 합니다. 그리고 3개의 홀센서는 HA, HB, HC 혹은 HU, HV, HW 라고 합니다.

가정 1 : 고정자의 권선에 + 방향으로 전류를 흘리면 N극이 되고, +방향으로 전류를 흘리면 S극이 된다고 가정.
가정 2 : 홀센서가 자석의 S극이 다가올 때는 LOW(0), N극이 다가올 때는 HIGH(1)라고 가정.

첫 번째 step 부터 살펴보면 회전자가 반시계 방향으로 회전하기 위해서 고정자 U, V, W 상은 각각 어떤 자속을 발생시켜야 할지 보겠습니다.
U 상은 회전자의 S극을 당겨야 하므로 N극이 될 수 있게 전류를 흘려야 하고,
W 상은 회전자의 S극을 밀어야 하므로 S극이 될 수 있게 전류를 흘려야 합니다.
V 상은 애매한 위치에 있으므로 float 싱태로 전류를 흘려보내지 않으면 됩니다.

이때의 홀센서 신호를 살펴보겠습니다. 홀센서가 자석의 S극이 다가올 때는 LOW(0), N극이 다가올 때는 HIGH(1)라고 가정하면 HA는 S극이 가까이에 있으므로 0, HB와 HC는 N극이 가까이에 있으므로 1이 됩니다.
따라서, HC/HB/HA의 신호 조합은 110이라 할 수 있겠습니다.

다시 말해, 홀센서의 조합이 110이 나오면 U는 N극이 될 수 있게, W상은 S극이 될 수 있게 전류를 흘려주면 회전자가 회전하게 됩니다.

두 번째 step 역시 마찬가지입니다. Step2를 살펴보면 이번에는 회전자의 N극을 밀어내기 위해서는 V상이 N극, 회전자의 N극 당겨주기 위해서는 W상이 S극이 되면 됩니다.
이 때, U상의 위치는 애매하므로 float 상태로 둡니다. Step2의 홀센서 신호를 조합하면 HC/HB/HA: 100이 됩니다.
같은 방식으로 6 step을 들고 나면 제자리로 오게 됩니다.

<img src="./img/BLDC_Motor_Chart.PNG" width = 60%> **BLDC 전동기의 순서 차트**</img>

