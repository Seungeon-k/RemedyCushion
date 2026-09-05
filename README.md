# RemedyCushion

> 블루투스 기반 자세 감지 시스템

RemedyCushion은 Arduino 센서 데이터를 블루투스로 Android 앱에 전송하고, 수신한 상태에 따라 사용자에게 자세 교정이 필요한지 시각적으로 알려주는 프로젝트입니다.

## 주요 기능

- 블루투스 기기 검색 및 연결
- Arduino 센서 데이터 수신
- 자세 상태를 문구와 색상으로 표시
  - 파란색: 정상 자세
  - 빨간색: 자세 교정 필요
  - 회색: 측정 종료 또는 연결 전

## 기술 스택

- Android (Java)
- Arduino
- Bluetooth SPP
- MLX90614 적외선 온도 센서

## 동작 구조

```text
MLX90614 센서 → Arduino → Bluetooth → Android 앱 → 자세 상태 표시
```

## 프로젝트 구조

```text
RemedyCushion/
├── app/                    # Android 애플리케이션
└── arduino_thermometer/    # Arduino 센서 및 블루투스 통신 코드
```

## 실행 환경

- Android Studio
- Android SDK 29
- Arduino IDE
- Bluetooth 시리얼 통신 모듈

Android 앱은 `RemedyCushion` 디렉터리를 Android Studio에서 열어 실행할 수 있습니다. Arduino에는 `arduino_thermometer.ino`를 업로드한 뒤 블루투스 모듈을 연결합니다.

