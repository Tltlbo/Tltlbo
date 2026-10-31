# 안녕하세요, 박진성입니다 👋

**센서 데이터 수집부터 펌웨어 제어, Linux 서버 연동까지 개발하는 임베디드·IoT 개발자입니다.**

STM32와 Linux를 중심으로 하드웨어와 소프트웨어를 연결하는 시스템을 만들고 있습니다.통신 병목과 신호 처리 문제를 데이터시트와 측정값으로 분석하고, 해결 과정은 코드와 문서로 남깁니다.iOS 앱을 개발하며 쌓은 오디오 처리와 비동기 프로그래밍 경험도 시스템 개발에 활용하고 있습니다.

[기술 블로그](https://velog.io/@js1436kt/posts) · [포트폴리오](https://aware-warlock-c88.notion.site/0798e65e1b628348975c81101840214c) · [Email](mailto:js1436kt@gmail.com)

## 🛠️ Tech Stack

### Embedded



### System & Network



### Edge AI & Data



### iOS



### Tools



## 🚀 Selected Projects

### [건물 지진 관제 및 능동 제어 시스템](https://github.com/Tltlbo/Earthquake-Monitoring-System-for-Buildings)

센서와 비전 AI의 관측 결과를 결합해 위험도를 판단하고, 8축 서보를 제어하는 IoT 시스템입니다.

* **관제 서버:** `pthread` 기반 TCP 중계 서버와 MariaDB 연동 중앙 제어 클라이언트 구현
* **진동 감지:** 10ms 주기 수집과 20샘플 슬라이딩 윈도우의 P2P·RMS 분석으로 순간값 기반 감지의 미탐 문제 개선
* **검증:** 하드웨어 없이 실행하는 C 단위 테스트로 수집 공백, 정수 극값, 타이머 오버플로 경계 조건 검증

`C` `STM32` `Linux` `TCP/IP` `Python` `Jetson` `MariaDB`

### [스마트 주차 관리 시스템](https://github.com/Tltlbo/ParkingLotSystem)

3대의 STM32 보드로 주차 감지, 차단기 제어, 양방향 비상 인터폰을 통합한 시스템입니다.

* **팀장 / 펌웨어:** 10채널 ADC DMA 주차 감지와 I2S 수음·PWM 오디오 출력 구현
* **통신 병목 개선:** PCM 오디오 전송에 필요한 대역폭을 계산하고 UART를 921600bps로 확장
* **프로토콜 설계:** DMA 더블 버퍼와 FSM 파서로 단일 UART에서 오디오·주차 데이터 전송 처리

`C` `STM32` `UART` `DMA` `I2S` `PWM`

### [Linux 디바이스 드라이버 기반 음료 디스펜서](https://github.com/Tltlbo/college-projects)

Raspberry Pi에서 음료 3종의 혼합량을 선택하고, 펌프와 교반 모터로 혼합·배출하는 시스템입니다.

* **커널 드라이버:** 원료 펌프 3개·배출 펌프 1개·교반 모터의 캐릭터 디바이스 드라이버와 `ioremap()` 기반 GPIO 레지스터 제어 구현
* **사용자 공간 연동:** `open`·`write`·`close`로 디바이스에 제어 명령을 전달하고, `fork()`·`execl()`을 활용한 펌프·모터 제어 프로그램 작성
* **GUI 연동:** Python Tkinter에서 음료별 용량을 30mL 단위로 선택하고 총 300mL로 제한하며, `subprocess`로 C 제어 프로그램을 호출하는 흐름 구현

`C` `Linux` `Kernel Module` `Raspberry Pi` `Python` `Tkinter`

### [Linux 파일 시그니처 기반 파일 타입 판별기](https://github.com/Tltlbo/college-projects)

* **파일 분석:** 확장자 대신 바이너리 헤더의 매직 넘버를 분석해 실제 파일 포맷을 판별하는 CLI 도구 개발
* **파일 시스템 탐색:** `lstat`·`opendir`·`readdir`를 활용한 하위 디렉토리 재귀 탐색 구현

`C` `Linux` `File I/O` `Make`

### [알쏭달쏭 — 실시간 허밍 퀴즈 앱](https://github.com/boostcampwm-2024/iOS07-alsongDalsong)

* **오디오 모듈:** 녹음·재생·분석을 담당하는 `ASAudioKit` 설계 및 XCTest 단위 테스트 작성
* **신호 처리 / 동시성:** PCM 전력 분석 기반 파형 시각화와 Swift `actor` 기반 오디오 세션 접근 제어 구현

`Swift` `AVFoundation` `Swift Concurrency` `SwiftUI` `UIKit`

### [PinForYou — 위치 기반 카드 혜택 추천 앱](https://github.com/Tltlbo/PinforYou)

* **팀장 / iOS:** 지도 기반 주변 가맹점 탐색과 카드 혜택 추천 기능 개발
* **앱 구조:** Combine 기반 REST API 서비스 계층 설계, KakaoMap SDK 및 소셜 로그인 연동

`Swift` `SwiftUI` `Combine` `CoreLocation` `KakaoMap`

## 🎓 Education

* **서울기술교육센터 온디바이스 AI SW 개발 과정** · 2026.07 ~ 2027.02 예정, 이수 중
* **NAVER Boostcamp 웹·모바일 9기 iOS** · 2024.08 ~ 2024.12 수료
* **영남대학교 컴퓨터공학과** · 2019.03 ~ 2025.02 졸업
