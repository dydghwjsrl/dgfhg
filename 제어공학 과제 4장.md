# 기말고사 이론시험을 대비하고자 노트로 풀이한 부분도 많습니다!

# P4.8  
-----
전자회로 주변에서 온도가 극단적으로 변하면 다양한 고장이 발생한다.  
온도제어 궤환시스템은 실외저온을 극복하기 위해 히터를 사용하여 온도변화를 감소시킨다.  
한 시스템의 블록선도가 그림 4.8에 있다. 주변온도 하락은 Td(s)에서 계단감소로 표현된다.  

<img src = "https://drive.google.com/uc?id=14DCxoODhUrNNzV_NeYeeqrzwMmGUOmMe">  
전자회로의 실제 온도는 Y(s)이다. 전자회로의 온도변화의 동역학은 다음과 같은 전달함수로 표현된다.

$$  
G(s) = \frac{100}{s^2+25s+100} 
$$  


----


## (a) K에 대한 시스템의 감도를 구하여라   
일단 먼저 $T(S)$를 구해야한다.  
매트랩을 사용해서 구해보자  

<img src = "https://drive.google.com/uc?id=1V2ToeBxMDE88CNV7T_nDBqA5yfTbI5wV">


$$  
T(s) = \frac{100k}{100k+(0.2s+1)(s^2+25s+100)}
$$  


간단하게 정리하면 위 공식과 같이 나타낼 수 있다.  

이제 시스템에 대한 감도의 대한 식을 보면  


$$S_kt = \frac{dT(s)} {dk}*\frac{K} {T(s)}$$


임을 알 수 있다.  
매트랩을 사용해서 확인하면  
$T(s)$를 k에 대해서 미분한 값은  

<img src = "https://drive.google.com/uc?id=1c7zmpquLJ2x7mLSt6M2XTFikUyiUpx4Q">  
임을 알 수 있고  

시스템에 대한 감도는  

<img src = "https://drive.google.com/uc?id=1rwFyOZMRkS9JhOVnZn4qdXqpNBJCeWrD">    
임을 알 수 있다.    


## (b) 외란 Td(s)가 출력 Y(s)에 미치는 영향을 구하여라  


$$\frac{Y(s)} {T_d(s)} = \frac{G(s)} {1+G_1(s)G(S)}$$


이다 결국 Disturbance가 $Y(s)$에 미치는 영향은 아래 매트랩으로 구한 식에  
T_d(s)를 곱하면 된다.  

<img src = "https://drive.google.com/uc?id=1aEqeBs0U3x9GLeS2yDzfCkZzrO2kd49t">  

## P4.12  
그림 4.12(a)와 (b)에 두개의 궤환시스템이 주어졌다.   
<img src = "https://drive.google.com/uc?id=1iVSN7M4mzfEiZZ2-r7IrY2Am42a0ndVx">  
  
### (a) 각 시스템의 폐루프 전달함수 T_1과 T_2를 계산하라  

T_1계산  
<img src = "https://drive.google.com/uc?id=1uYWFmc1bqyRkpEzSNX5eaxNNRNqqMqlH">  

T_2계산  
<img src = "https://drive.google.com/uc?id=1F6kCAuCYLVjYiFLHEHeljVrdUbo8pMDv">  


### (b) 공칭값이 K_1 = K_2 =1 일 때 매개변수 K_1에 대한 두 시스템의 감도를 구하여라  

<img src = "https://drive.google.com/uc?id=1O0gI2Q2WVAjf685r9SPlEnaLKmK3AApV">  

(a)그림에 대한 감도를 먼저 알아보자.  

시스템에 대한 감도는 아래와 같이 구할 수 있다.
$$S_k1 = \frac{dT_1(s)} {dK_1}*\frac{K_1} {T_1(s)}$$

Ts1_diff는 T_1값을 K_1값에 대해서 미분한 것을 의미한다.  

Ts1_diff_result는 미분한 값에 $\frac{K_1} {T_1(s)}$값을 곱해준 것을 의미한다.

actualvalue값은 K_1과 K_2값에 각각 1을 넣은 것을 의미한다.

-------------------


(b)그림에 대한 감도도 알아보자

<img src = "https://drive.google.com/uc?id=1Mwwa7B6j6NyEDBq35rwF_SaQIh1gyvlX">  
위와 같이 식으로 나타내었고  

<img src = "https://drive.google.com/uc?id=1flYw50W7KBGFVvN72R3kKvQvhZF0NvR_">  
아래와 같은 결과가 나왔다.  
  
# P4.17  
그림 P4.17(b)에 주어진 직류전동기 제어시스템을 이용하여 그림 P4.17(a)에 그련진 로봇집게의 각도가  $\Theta$가 되도록 닫혀지게 제어하고자 한다. 제어시스템의 모델은 그림 P.4.17(c)에 있으며, 이때 $K_m = 30$, $R_f = 1옴$, $K_f = K_i = 1$, $J = 0.1$, $b = 1$이다.  

<img src = "https://drive.google.com/uc?id=1jV8CHvg0gNa9IGX96J2rAecduJq4-ZHA">

### (a) K = 20일 때 θ_d(t)의 계단변화에 대한 시스템의 응답 θ_d(t)를 결정하라.  

<img src = "https://drive.google.com/uc?id=1jIuBiw8XtJluSKSCL3c3lcAYBJQj9Obr">  

위와 같이 매트랩 코딩을 진행하였다  


<img src = "https://drive.google.com/uc?id=1oBfV2Fj-cS3JlOXuGG4vvd9mgKAAHMo_">  


위와 같은 공식이 도출되었고,  


<img src = "https://drive.google.com/uc?id=1LG68u5tw9TPCKwXQz_0iZCg-bpln6lM4">  

계단 입력이기 때문에 $1/s$를 곱하면 된다. 위와 같이 계산하였다.  

일단 θ(s)값은 위와 같이 나타났다.  

이제 θ(t)값은 역라플라스 변환을 하면 알 수 있다.  

<img src = "https://drive.google.com/uc?id=1CA_wSz2OPBZ91A0TmZCP4kkzT2KPheFA">  

역라플라스 변환을 하였고 위와 같이 $\Theta$(t)값을 구할 수 있었다.  

### (b) θ_d(t) = 0으로 가정하여 부하외란 $T_d(s) = A/s$의 영향을 구하라  

입력이 0일 때 Loop Gain을 구하면 아래와 같이 나타난다.매트랩에서 사용한 코딩을 첨부하였다.  
매트랩으로 계산한 값을 정리한 다음 거기에 T_d(s)값을 곱한 다음에 steady state 
output을 알기 위한 final value Theorem을 계산한 값 역시 아래와 같이 나타난다   

<img src = "https://drive.google.com/uc?id=1vzu_gU31b283qfzTQ0XCb6EQFPG69N1U">  

 


### (c) 입력 r(t) = t, t>0 일 때 정상상태 오차 e_ss를 결정하라

($T_d(s) = 0$으로 가정한다)

시간도메인인 t에서 t를 입력했기 때문에 이것을 라플라스화 한 다음 그 값을 넣어주어야 한다.  
θ_d(t) = t 를 넣는 것은 θ_d(s) = $\frac{1} {s^2}$를 입력하는 것과 같다.  
에러시그널 공식에 θ_d(s)값과 θ_d(s)값을 넣은 것을 매트랩으로 계산하였고 steady state에러를 찾기 위해 s를 곱해주고 s값을 0으로 보내는 극한을 계산하였다.  

<img src = "https://drive.google.com/uc?id=11jNZQ5Im6DKy2GXAyg0QcV_g2AFBI1RF">  

<img src = "https://drive.google.com/uc?id=1THRASBDO9FH7CUcWU-LyZTDrGHwqaSup">  


그 결과 에러는 약 0.002가 나왔다.
