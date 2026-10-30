# 교내 개발 프로젝트

보안 프로젝트 외에 학교 수업과 졸업작품으로 진행한 개발 프로젝트입니다.

<br>

## Sign Play: 실시간 수어 학습 게임

> 졸업작품 · 2026.03 ~ 06 · 5명 · 통합 담당

- 팀원 4명이 각자 만든 Flutter 앱, 수어 인식 모델, 게임 서버, 영상 전처리 코드를 하나의 저장소로 통합했습니다.
- 총 4차례 다시 합치면서 Git 충돌을 정리했습니다.
- 사용 기술: Flutter, Python, FastAPI, PyTorch, MediaPipe, WebSocket, WebRTC, Firebase

<br>

## 게임형 스마트 분리수거 장치

> 임베디드시스템 수업 · 2025.11 ~ 12 · 개인 · [과정 기록 (GitHub Wiki)](https://github.com/carrotbyroot77/25-2-EmbededSystem/wiki)

- Raspberry Pi 4B에 로드셀(HX711), 버튼, USB 카메라를 연결해, 넣은 쓰레기를 TFLite 모델로 분류하고 미션과 맞으면 팀 점수가 오르는 장치를 만들었습니다.
- Node-RED에서 센서 스크립트를 직접 실행하면 HX711이 무한 대기에 빠져서, Python이 MQTT로 값을 보내고 Node-RED는 구독만 하는 구조로 바꿨습니다.
- 투입할 때마다 시간, 팀, 무게, 분류 결과, 정답 여부를 SQLite에 기록해 점수의 근거를 남겼습니다.
- 사용 기술: Raspberry Pi, Python, MQTT (Mosquitto), Node-RED, SQLite, TFLite Runtime

<br>

## 오-운-한: 학생용 헬스 PT 웹 서비스

> 클라우드컴퓨팅 수업 · 2025.10 ~ 12 · 5명 · 기획, 개발, 배포

- 오-운-한: "오늘 운동한 한세인들"이라는 이름입니다.
- 기존 코드가 동작하지 않아 Flask로 다시 작성하고 로그인, 비밀번호 찾기, 점수 랭킹을 구현했습니다.
- EC2 배포 후 외부 접속이 되지 않아, 마감 일정에 맞춰 PythonAnywhere로 옮겨 배포했습니다.
- 서버리스 버전에서는 DB 접속 정보를 코드에서 빼서 SSM Parameter Store에 두고, Lambda에는 필요한 권한만 줬습니다.
- 사용 기술: Python, Flask, SQLAlchemy, AWS (EC2, S3, CloudFront, API Gateway, Lambda, SSM, CloudWatch)
