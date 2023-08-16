# LegoGBC & Yolov7 & Deepsort
# 💡프로젝트 소개
* 경기대학교 산업경영공학과 4학년 1학기 교과목인 '산업경영공학종합설계'에서 진행한 프로젝트입니다.
* 레고를 활용하여 색상 분류, 불량 검출 공정을 만드는 주제입니다.
  
# 💻작동 구동 환경
* 레고 Ev3dev는 기계학습 및 Deep-Learning에 적합하지 않습니다.(Micro-Python, 단방형으로 상호 통신 불가, 연식이 있음)
* 앞서 말한 제약 조건들을 해결하기 위해 프로토콜 통신으로 프로젝트를 진행했습니다.
* 결과적으로, Python 환경에서 실시간 통신을 이용해 기계학습 및 Deep-Learning이 가능해졌습니다.
<img width="992" alt="스크린샷 2023-08-16 155022" src="https://github.com/Kimeuing/Image_Classification_GUI_PyQt5/assets/109636260/b835eca2-18d1-4862-8859-c2780336c2cd">

# 🎤분류 모델 소개
* 사용한 모델 [yolov7-deepsort](https://github.com/RizwanMunawar/yolov7-object-tracking/tree/main)
* Roboflow를 활용하여 데이터 셋 생성했습니다. [데이터 셋](https://app.roboflow.com/project-2i85d/ball-crack-detection-1d8gp/overview)
* 클래스는 ball, crack 두 가지로 설정했습니다. <img width="254" alt="사본 -스크린샷 2023-08-16 162159" src="https://github.com/Kimeuing/Image_Classification_GUI_PyQt5/assets/109636260/58e4782b-2a84-44fc-baf3-fec77e023cf8">

# 🕹모델 작동 방식
![image](https://github.com/Kimeuing/Image_Classification_GUI_PyQt5/assets/109636260/94a93d38-a2d6-4b6d-a016-51c1c1351a0f)
* Ball 이란 Class안에 Crack Class의 바운더리 박스 중점이 포함되면 그 Ball의 인스턴스의 Class를 Defect로 변경시킵니다.
* 왼쪽의 초록색 선에 인스턴스가 도착했을 때 그 인스턴스의 Class가 Ball인지 Defect인지 판단하여 레고 GBC 모터를 제어합니다.
  
https://github.com/Kimeuing/legoGBC/assets/109636260/5d9eef60-c315-46d9-a5a1-0ac6892ccc20

# 🖥GUI 소개
![image](https://github.com/Kimeuing/legoGBC/assets/109636260/c8763911-2305-4ae8-895c-df0c5ba339f2)

* 결과저장
    * 검사 결과를 엑셀로 저장 가능합니다
   ![image](https://github.com/Kimeuing/legoGBC/assets/109636260/14295612-8993-4ef7-83fb-b980ea2f6589)
* 불량_일련번호
    * 불량 검출 공정에서 분류되는 제품의 일련 번호를 순차적으로 출력합니다.
* 판정
    * 불량 과정에서 양품/불량품을 표기합니다.
* 공정 분류 결과
    * 각 공정에서 발생한 수량들을 표기합니다.
* 공정 제어 버튼
    * 각 모듈에 맞는 공정 모터를 제어할 수 있으며, 전체 공정도 제어가 가능합니다.
 
https://github.com/Kimeuing/legoGBC/assets/109636260/4db4a060-0094-4783-9ac7-30ae2e8fe4ed




