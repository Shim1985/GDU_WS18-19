# GDU_WS18-19

## arduino code for Stepper Motor


```

\#include \<AFMotor.h\>

// M 1 에 DC 모터 연결된 경우.

// M 2 에 DC 모터 연결된 경우.

// M 3 에 DC 모터 연결된 경우.

// M 4에 DC 모터 연결된 경우.

AF\_DCMotor motor1(1); // 

AF\_DCMotor motor2(2); //

AF\_DCMotor motor3(3); //

AF\_DCMotor motor4(4); //

void setup() {

 Serial.begin(9600); // set up Serial library at 9600 bps

 Serial.println("DC Motor 4 pcs test");

 motor1.setSpeed(255); // 최대 255

 motor2.setSpeed(255); // 최대 255

 motor3.setSpeed(255); // 최대 255

 motor4.setSpeed(255); // 최대 255

 motor1.run(RELEASE); // 정지와 같습니다. DC 모터 정지

 motor2.run(RELEASE); // 정지와 같습니다. DC 모터 정지

 motor3.run(RELEASE); // 정지와 같습니다. DC 모터 정지

 motor4.run(RELEASE); // 정지와 같습니다. DC 모터 정지 

 delay(2000);

}

// 1초다마 1개씩 순차적으로 회전해봅니다.

void loop()

{

Serial.println("1");

 Serial.println("2");

 Serial.println("3");

 Serial.println("4");

 //작은 푄

 motor1.run(FORWARD);

 motor2.run(FORWARD); 

 //큰 푄

 motor3.run(FORWARD);

 motor4.run(FORWARD);

 delay(10000); 

 motor1.run(RELEASE);

 motor2.run(RELEASE);

 // 큰 푄은 정지 없이 계속 돌아가기

 //motor3.run(RELEASE);

 //motor4.run(RELEASE);

 delay(7000);

}

```
