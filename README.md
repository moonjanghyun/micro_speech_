< MicroTFLite를 활용한 마이크로컨트롤러 실시간 음성 인식 실습 >

본 실습에서는 Micro TFLite를 사용하여 마이크로컨트롤러(Arduino Nano 33 BLE Sense)에서 실시간으로 "yes"와 "no" 음성 명령을 인식하는 시스템을 구현합니다. 엔터키를 누르면 음성 인식 모드가 토글되며, 인식된 결과에 따라 LED가 다르게 반응합니다. 이 실습을 통해 제한된 자원을 가진 마이크로컨트롤러에서 머신러닝 모델을 실행하는 방법을 배울 수 있습니다.


- 필요 장비 및 환경

•	Arduino Nano 33 BLE Sense 보드 (내장 마이크 포함)
•	Arduino IDE (최신 버전 권장)
•	USB 케이블 (Arduino 연결용)
•	필요 라이브러리 : Arduino_MicroTFLite / PDM (Nano 33 BLE Sense에서 마이크 입력용)


- 파일 구조

micro_speech_
  ├── micro_speech.ino                                 <-- 메인 스케치 파일
  ├── model.h                                          <-- TFLite 모델의 C 배열
  ├── audio_provider.h / arduino_audio_provider.cpp    <-- 마이크 입력 처리
  ├── feature_provider.h / feature_provider.cpp        <-- 특징 추출 관리
  ├── micro_features_micro_features_generator.h /.cpp  <-- 특징 생성기
  └── micro_features_micro_model_settings.h /.cpp      <-- 모델 특징 세팅 관련 설정


  
