# 교통 약자를 위한 지능형 교통 시스템

## 기술 스택
<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=Python&logoColor=white"> <img src="https://img.shields.io/badge/raspberrypi-A22846?style=for-the-badge&logo=raspberrypi&logoColor=white">

## 개요
교통 약자들의 보행 시간을 고려하여 최대 10초를 추가적으로 부여하여 유동적으로 신호등이 변화할 수 있도록 설계하고  
해당 정보를 차량에서도 수신될 수 있도록 V2I 통신 개념을 이용한 지능형 교통 체계를 구축

* 2024-1 MIDAS 종합설계
* 개발 기간 : 2024.03.04 ~ 06.07
* 프로젝트 인원 : 2명

## 프로젝트 핵심기능
`Beacon`
* EddyStone URL Beacon을 통해 WiFi 정보를 담아 신호등과 차량이 같은 네트워크에 접속될 수 있도록 함.

`Car`
* 신호등의 정보가 필요할 때 신호를 송신하게 되면 신호등의 남은 시간과 추가 시간을 수신함으로써 향후 자율주행에서 필요한 양방향 통신을 구축.

`TrafficLight`  

[영상처리]
* YOLOv8을 이용하여 객체를 인식하고 DeepSORT 알고리즘을 이용하여 객체를 추적하여 각각의 객체들이 안전하게 횡단보도를 건널 수 있는 시간을 계산함.
* 실제 신호등의 남은 시간이 5초일 때, 몇 초의 시간이 더 필요할지 계산하여 최대 10초의 시간을 유동적으로 부여함.
  
[통신]
* 차량으로 부터 특정 신호가 송신되면 현재 신호등의 남은 시간과 추가 시간을 송신함.

## Functional Block Diagram
<img width="1112" height="639" alt="Image" src="https://github.com/user-attachments/assets/87c2d37e-b554-424c-aefb-57399ca156aa" />

## Sequence Diagram
<img width="904" height="461" alt="Image" src="https://github.com/user-attachments/assets/0340e05b-f37c-4854-a6d7-b5d03fdb1bc8" />
