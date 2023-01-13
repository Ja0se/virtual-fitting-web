# 2022 Donga-A University Computer Engeneering  Graduation work

## 가상 피팅 서비스와 추천 시스템을  활용한 옷장 관리 앱 

Project nickname : Hand Closet

Team name : 옷사조

Period : 2022/03~2022/11

Member : 

 - 장세진(팀장)

 - 박무진

 - 최가인

 - 이예림

 ---

### 소개

Hand closet은 가상 피팅 서비스와 색상에 따른 추천 시스템을 활용하여 출근시간에 옷 준비로 발생하는 시간을 줄이고 최근 착용 날짜를 활용하여 사용되지 않는 옷을 파악하고 관리할 수 있도록 서비스를 제공한다.

해당 코드는 가상 피팅 및 추천 시스템 구현을 테스트하기 위한 용도로 web에 구현

### 기능

#### 가상 피팅

Unet Segemtation을 활용하여 사람 이미지 누끼 제거 및 옷 누끼 제거

Openpose를 활용하여 사람의 관절을 매핑

로직에 따라 옷의 비율 변경-> 목/골반의 위치에 맞게 피팅 서비스 제공

### 추천 시스템

기존 상,하의가 구분되지 않던 Unet구조에서 업그레이드된 U2net Segmentation을 활용하여 이미지에서 상,하의 추출

Clustering을 활용하여 상,하의 이미지의 평균 색상을 판단(무신사 snapshot이미지 활용)

콘텐츠 기반 필터링으로 함께 많이 사용되는 3가지 색상중 임의로 한가지의 옷을 추천하여 제공

### 기술 Stack

React Native, Nodejs

Javascript, Python

Tensorflow, Pytorch, sklearn, OpenPose, pandas, OpenCV, Pillow

SQL - MySQL

### 기술 선택 이유

학습된 딥러닝 모델을 활용하기 위해 Python 오픈소스 활용 하여 모듈 작성후 TDD방식의 개발론 사용

### Usage

decompress zip file in trained_checkpoint folder and openpose_trained

main : app.js
-> npm start

### Git clone

[u2net cloth-segmentation](https://github.com/levindabhi/cloth-segmentation.git) 

We change infer.py

---

[unet cloths_segmentation](https://github.com/ternaus/cloths_segmentation)

[unet people_segmentation](https://github.com/ternaus/people_segmentation)

Make_Image.py

---

[OpenPose](https://github.com/CMU-Perceptual-Computing-Lab/openpose)

[OpenPose Python Code](https://m.blog.naver.com/rhrkdfus/221531159811)

