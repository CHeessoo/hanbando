# 🗺 한반도 투어
### 전국 방방곡곡 내 맘 가는 대로! 내 발 가는 대로!

<p>'한반도 투어'는 여행사 사이트로, 국내여행에 관련된 패키지여행 상품과 호텔 예약 서비스를 제공하는 웹 프로젝트입니다.</p>

---

<br/>

## 🕰️ 개발 기간
- 2023년 11월 20일 ~ 2023년 12월 19일


<br/>

## 👥 참여자 및 담당역할
- 남궁수민 : 메인배너, 호텔 상품 페이지
- 김세연 : 패키지여행 페이지, 찜목록
- 김태준 : 고객센터
- 나예솜, 심희수 : 로그인, 회원가입, 마이페이지
- 심희수 : 관리자 페이지, DB관리
- 이종혁 : 예약 페이지

<br/>

## ⚙️ 기술 스택

- Front-End
  - Thymeleaf
  - HTML
  - CSS
  - JavaScript
  - JQuery

- Back-End
  - JAVA
  - Spring Boot
  - Mybatis

- DB
  - Oracle DB

- Tools
  - STS4(Spring Tools Suite 4)
  - Git
  - Github
 
<br/>


## 📌 기능 요약
1. 회원은 국내 패키지여행에 대한 정보를 목록으로 조회하여 보다 편한 조회가 가능합니다. 상세페이지를 통해 선택한 패키지 이용자의 리뷰를 확인하거나 원하는 날짜를 선택하여 예약할 수 있습니다. 각각의 여행상품에 찜하기 기능 활용이 가능하며 찜목록에서 확인할 수 있습니다.
2. 회원은 국내 호텔 예약에 대한 정보를 목록으로 조회하여 편리한 이용을 할 수 있고, 상세페이지를 통해 원하는 날짜와 객실을 선택해서 예약할 수 있습니다. 
3. 고객센터는 공지사항, 자주 묻는 질문, 1:1 문의하기로 구성되어 있으며 관리자와 회원 간의 원활한 소통이 가능합니다.
4. 회원가입 또는 비밀번호 찾기 시 SMS 문자 인증 절차 과정이 진행됩니다. 최소한의 정보를 수집하면서도 회원에 대한 검증이 가능한 카카오, 네이버 간편 로그인을 선택하여 이용할 수도 있습니다.
5. 회원은 마이페이지에서 개인정보, 예약 목록, 찜목록 조회 및 수정, 삭제 또는 탈퇴 기능을 사용할 수 있습니다.
6. 관리자는 관리자 페이지에서 전체 회원(일반회원, 휴면 회원, 탈퇴 회원) 정보에 접근하여 조회, 정보 변경, 회원 탈퇴 기능을 이용한 회원관리가 가능하며, 상품(패키지여행, 호텔 예약) 관리 및 전체 리뷰를 조회하거나 삭제할 수 있습니다.
7. 예약 시 사용자가 정보를 입력하고 예약하면 대기 상태로 변환 진행되며 상세페이지를 통해 수정, 취소, 결제 중 선택하여 이용할 수 있습니다. 이후, 예약 목록을 통해 패키지여행 및 호텔 예약과 관련된 전반적인 내용을 확인할 수 있습니다.

<br/><br/>

## 구현 서비스

### 간략 개요
<img width="847" alt="기획문서(서비스개요)-이미지" src="https://github.com/CHeessoo/hanbando/assets/131851529/a622cbbf-c7c7-429c-a492-165f3e1f8eb0">


<br/><br/>


### 메인 페이지
>- 메인 페이지에서 캐러셀을 이용하여 최대 3개의 배너를 보여준다. 
>- 배너를 클릭하면 링크이동을 할 수 있다.
>- 관리자 페이지에서 배너 사진을 등록하고 링크 주소를 변경 할 수 있다. 
>- 패키지 상품을 예약이 많은 순서대로 4개 베스트 패키지 기획전으로 보여준다.
>- 테마 별 패키지를 무작위로 골라서 보여준다.
>><img width="815" alt="한반도메인-최종" src="https://github.com/CHeessoo/hanbando/assets/131851529/415707fb-95aa-4c47-809c-0cf1c7a17bfc">

<br/>

### 로그인(아이디 찾기, 비밀번호 찾기) / 회원가입 / 마이페이지
>- 사이트 자체 로그인, 네이버와 카카오 API를 사용한 간편 로그인을 구현하였다.
>- cool SMS API를 사용한 문자 인증 서비스를 구현하였다. (회원가입과 비밀번호 찾기에 적용)
>- Daum 우편번호 서비스(Kakao 주소) API를 이용하여 상세 주소 입력 기능을 구현하였다.
>- 회원가입 및 비밀번호 변경 시 정규식을 이용하여 조건을 충족하지 못한 경우 입력된 비밀번호의 사용을 제한한다.
>><img width="942" alt="로그인1" src="https://github.com/CHeessoo/hanbando/assets/131851529/61d12b7a-3f54-4a1b-b8e9-3e6b0292cbc8">
>><img width="929" alt="회원가입1" src="https://github.com/CHeessoo/hanbando/assets/131851529/7c8cf68a-c5b2-4820-9a7c-89af09d4db8b">
>><img width="944" alt="아이디찾기1" src="https://github.com/CHeessoo/hanbando/assets/131851529/c4e62a43-c283-4354-8548-0e4df1328cae">
>><img width="931" alt="비밀번호변경1" src="https://github.com/CHeessoo/hanbando/assets/131851529/52b059f5-3a1c-49b0-8a9b-5bc4f810b10c">
>><img width="908" alt="마이페이지1" src="https://github.com/CHeessoo/hanbando/assets/131851529/1222507d-ad0b-4723-8cc4-5196909bbf0f">


<br/>
  
### 패키지 여행 상품
>- 패키지 목록
>- 상세페이지
>><img width="931" alt="패키지목록" src="https://github.com/CHeessoo/hanbando/assets/131851529/dd202382-8dd1-452e-9c19-1b51734600b9">
>><img width="947" alt="패키지상세" src="https://github.com/CHeessoo/hanbando/assets/131851529/7508cb92-356f-4065-9516-49477a4a2632">

<br/>

### 호텔 예약 상품
>- 호텔 목록
>- 상세페이지
>><img width="752" alt="호텔메인" src="https://github.com/CHeessoo/hanbando/assets/131851529/647c646a-3847-47d9-961e-873bedcefe34">
>><img width="883" alt="호텔상세" src="https://github.com/CHeessoo/hanbando/assets/131851529/6ebfb1f1-4be3-4cc1-af1a-cdb7936321b6">

<br/>

### 예약하기 기능
><img width="923" alt="패키지예약1" src="https://github.com/CHeessoo/hanbando/assets/131851529/c66f5283-cdda-446f-83c1-b69fca91c016">
><img width="951" alt="패키지예약2" src="https://github.com/CHeessoo/hanbando/assets/131851529/389b993b-86da-4f30-bb9d-5e66ace38cc6">

<br/>

### 관리자
#### 일반 회원 관리
>- 관리자는 일반 회원의 상세정보 조회가 가능하며, 수정, 탈퇴가 가능하다.
>- 관리자 권한으로 비밀번호 변경 시 제한 없이 수정이 가능하다.
>- 관리자 보기 전용 회원 찜목록 게시판 조회가 가능하다.
>- Daum 우편번호 서비스(Kakao 주소) API를 이용하여 상세 주소 기능을 구현하였다.
>><img width="855" alt="일반회원관리목록" src="https://github.com/CHeessoo/hanbando/assets/131851529/0d29533f-da59-4edc-a22d-50f5fad0360a">
>><img width="680" alt="일반회원관리상세" src="https://github.com/CHeessoo/hanbando/assets/131851529/b859ebec-dca6-40f9-a1b2-ea577feead04">

#### 휴면 회원 관리
>- 관리자는 휴면 회원 조회가 가능하며 상세정보 확인이 가능하다.
>><img width="740" alt="휴면회원관리목록" src="https://github.com/CHeessoo/hanbando/assets/131851529/d90ffea9-1127-4064-80b5-a1738160ba9a">
>><img width="658" alt="휴면회원관리상세" src="https://github.com/CHeessoo/hanbando/assets/131851529/ea0c6fbd-69b0-4ac9-b165-c5e48c79348a">


#### 탈퇴 회원 관리
>- 관리자는 탈퇴회원 조회가 가능하다.
>><img width="752" alt="탈퇴회원관리목록" src="https://github.com/CHeessoo/hanbando/assets/131851529/6ba49384-16e5-4195-a29c-9ef2457ad244">


#### 상품 관리(패키지, 호텔)
>- 관리자는 패키지 여행 상품과 호텔 예약 상품을 상품별로 조회가 가능하며 상세 확인 및 수정이 가능하다.
>><img width="702" alt="패키지상품관리목록" src="https://github.com/CHeessoo/hanbando/assets/131851529/3b0c91fa-e64e-4557-8313-a51c6621b4b7">
>><img width="652" alt="호텔상품관리목록" src="https://github.com/CHeessoo/hanbando/assets/131851529/3b5cacc8-82cc-462f-8851-c10026972868">
>><img width="668" alt="호텔상품관리-가격상세" src="https://github.com/CHeessoo/hanbando/assets/131851529/8d712b33-b1ad-471c-9f12-bb6dc25f5087">


#### 예약 관리
>- 관리자는 전체 예약 내역을 조회할 수 있으며 각 예약내역의 상세 확인이 가능하다.
>><img width="855" alt="예약관리목록" src="https://github.com/CHeessoo/hanbando/assets/131851529/ecb8ec0e-7158-462d-8452-191703e0147a">
>><img width="694" alt="패키지예약상세" src="https://github.com/CHeessoo/hanbando/assets/131851529/c74d408f-5144-4061-818f-01d8f9620150">
>><img width="723" alt="호텔예약상세" src="https://github.com/CHeessoo/hanbando/assets/131851529/5e4d35b0-8b8c-4e7f-8f05-980e49d41998">



#### 리뷰 관리
>- 관리자는 리뷰를 목록 구성으로 확인이 가능하며 검색, 삭제가 가능하다.
>><img width="692" alt="리뷰관리목록" src="https://github.com/CHeessoo/hanbando/assets/131851529/c7cf4c7d-df94-4a68-923c-b2a7936511b4">
>><img width="720" alt="리뷰관리상세" src="https://github.com/CHeessoo/hanbando/assets/131851529/9b8260d7-561c-4fe0-8f63-218cc12264ed">




<br/>

### 고객센터
>- 공지사항 (파일 첨부 가능)
>- 자주 묻는 질문
>- 1:1문의
>><img width="916" alt="공지사항1" src="https://github.com/CHeessoo/hanbando/assets/131851529/7304d2f0-56eb-4a9f-99f9-4e9dfe2edb10">
>><img width="913" alt="공지사항2" src="https://github.com/CHeessoo/hanbando/assets/131851529/23751a9d-4303-4171-8375-118671eca02e">
>><img width="914" alt="공지사항3" src="https://github.com/CHeessoo/hanbando/assets/131851529/79974588-6d72-45e0-805d-cbb0232f93b5">
>><img width="894" alt="공지사항4" src="https://github.com/CHeessoo/hanbando/assets/131851529/1e4587d2-3bb6-429f-a3e5-a5b73b4b49ca">



<br/>

### ERD

![erd](https://github.com/CHeessoo/hanbando/assets/131851529/3c1d7f20-b3de-44ac-ae87-cb98eb731db9)


### 사이트 맵
![사이트맵](https://github.com/CHeessoo/hanbando/assets/131851529/1d8c1951-ba54-4ee2-89ff-dadb87d8bad6)


