---
title:  "[1일차] 여러 기술들과 라이브러리, 프레임워크"
excerpt: "현재 회사에서 쓰이고 있는 기술들의 개념과 용어 정리"

categories:
  - Blog
tags:
  - [Blog, jekyll, Github, Git, AI, DeepLearning]

toc: true
toc_sticky: true
 
date: 2022-09-01
last_modified_at: 2022-09-01
---
- Jetson이란?
<br>NVIDIA가 만드는 자사의 Tegra CPU 기반 개발자 보드, 저전력 특성, 임베디드 AI나 영상처리용 보드로 쓰임.

- Jetson Nano란?
<br>젯슨 TX1 모듈을 그대로 쓰면서 전체적인 크기를 대폭 줄이고 원가 절감을 한 모델.

- Jetson Xavier란?
<br>이전 장치에 대비 20배의 가속과 전력효율 10배 개선

- Tegra란?
<br>NVIDIA에서 설계한 SoC 브랜드.

- SoC란?
<br>완전 구동이 가능한 제품과 시스템이 한 개의 칩에 들어있는 것, 하나의 칩 내에서 CPU, GPU, NPU, RAM, ROM 등 다양한 역할을 함, 모바일 기기나 아두이노와 같이 저전력 소비에 이용됨. ex) M1

- PLM이란? 
<br>제품 수명 주기 관리 = 제품의 전 생명 주기를 통해 제품의 관련된 정보와 프로세스 관리

- NX란?
<br>지멘스에서 개발한 그래픽 툴. 한 파일 내에서 모델링, 어셈블리, 드로잉이 가능.

- Pytorch란?
<br>딥러닝을 구현하기 위한 파이썬 기반의 오픈소스 머신러닝 라이브러리, numpy를 대체하면서 GPU를 이용하여 쉽게 인공 신경망 모델을 만들고 학습시킴, 최대한의 유연성과 속도를 제공함.

- ONNX란?
<br>Tensorflow, PyTorch와 같이 서로 다른 DNN(심층신경망) 프레임워크 환경에서 만들어진 모델들을 서로 호환해서 사용할 수 있게 도와주는 공유 플랫폼. 이것 또한 DNN 프레임워크

- TensorRT란?
<br>NVIDA사에서 개발한 딥러닝 연산 최적화 엔진, 학습된 딥러닝 모델을 최적화하여 NVIDIA GPU 상에서 속도를 수배~수십배까지 향상시킴.

- Pose estimation & tracking이란?
<br>의미있는 key points들을 검출(오른쪽 어깨와 같은), 관련성을 찾고, 지속적으로 추적
<br>\- Bottom-up 방식: 사람의 관절을 모두 추정, 그리고 특정한 포즈 or 하나의 사람 객체의 포즈로 그룹지어주는 방식.
<br>\- Top-down 방식: 사람을 먼저 뽑아내서 관절을 추정

- Object Detection(객체 탐지)이란?
<br>컴퓨터 비전의 하위 분야 중 하나, 이미지 및 비디오 내에서 유의미한 특정 객체를 감지하는 작업
<br>물체의 위치와 그 종류를 찾아내는 것, classification과 localization을 동시에 수행, 여러개의 object를 찾을 수 있어야 함. 
