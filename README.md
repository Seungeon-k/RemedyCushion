# RemedyCushion

> 블루투스 기반 자세 감지 시스템

RemedyCushion은 방석에 설치한 압력센서로 사용자의 착석 상태를 감지하고, 측정 데이터를 블루투스로 Android 앱에 전송하는 자세 교정 프로젝트입니다. 앱은 수신한 데이터에 따라 현재 자세 상태를 문구와 색상으로 표시하여 사용자가 자세 교정 필요 여부를 직관적으로 확인할 수 있도록 합니다.

## 주요 기능

- 블루투스 기기 검색 및 연결
- 압력센서를 활용한 착석 상태 감지
- Arduino 센서 데이터 처리 및 전송
- 자세 상태를 문구와 색상으로 표시
  - 파란색: 정상 자세
  - 빨간색: 자세 교정 필요
  - 회색: 측정 종료 또는 연결 전

## 기술 스택

- Android (Java)
- Arduino
- Bluetooth SPP
- 압력센서

## 동작 구조

```text
압력센서 → Arduino → Bluetooth → Android 앱 → 자세 상태 표시
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
