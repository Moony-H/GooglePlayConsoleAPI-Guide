#
Dpectrum Google Play Console API Guide



<br/>

## 개요

<br/>

**이 문서는 Java, 혹은 Kotlin을 사용하여 구글 플레이 콘솔 API 사용법을 기록하기 위한 Repository 입니다.**

따라서 이 API를 사용하려면 세 가지가 준비되어야 합니다.

<br/>

1. Java, 혹은 Kotlin Compiler

2. Google Play Console 개발자 계정.

3. Google Cloud Platform

<br/>

이 셋을 통하여 Google Play Console API를 사용할 수 있습니다.

## 사용법

<br/>

<br/>

API를 사용하려면 먼저 Google Cloud Platform 프로젝트가 있어야 합니다.

Google Cloud Platform에 새로운 프로젝트를 만들거나 기존 프로젝트를 준비하여 연결합니다.



### 기존 프로젝트를 연결.

먼저 [Google Cloud](https://cloud.google.com/)에 접속합니다.

google play console과 조직이 같은지 확인 후 기존 프로젝트로 이동하여 **API 및 서비스**를 클릭합니다.

![스크린샷 2022-11-28 시간: 17 36 36](https://user-images.githubusercontent.com/53536205/204231604-e2b3704d-2c66-48e1-aa20-a2ccdd3a8bc4.png)

상단의 **+ API 및 서비스 사용 설정**을 클릭합니다.

![스크린샷 2022-11-28 시간: 17 30 05](https://user-images.githubusercontent.com/53536205/204232170-3f6ed487-d800-4589-ad80-0e6b0c20d8e8.png)

google play android developer api를 검색하여 추가합니다.


![스크린샷 2022-11-28 시간: 17 43 32](https://user-images.githubusercontent.com/53536205/204232816-6e071249-4812-4842-a7a4-23f051935dce.png)

<br/>

![스크린샷 2022-11-28 시간: 17 46 48](https://user-images.githubusercontent.com/53536205/204233613-0416b780-f301-4054-bf71-b59a107efe96.png)




그 다음 [여기](https://play.google.com/console/about/)에 접속하여 Google Play Console을 엽니다.

**앱의 화면이 아닌 모든 앱 화면에서** 왼쪽 탭의 **API 엑세스**를 눌러 이동합니다.

<br/>

<br/>

![스크린샷 2022-11-28 오후 4 58 51](https://user-images.githubusercontent.com/53536205/204225331-a11c077f-428c-4429-9c9e-7bb5f719fbd8.png)

<br/>

**기존 Google Cloud 프로젝트 연결**을 누른 후 Google Cloud Platform에서 API를 추가한 Project를 선택합니다

![스크린샷 2022-11-28 시간: 18 05 13](https://user-images.githubusercontent.com/53536205/204237261-e601883a-1f6f-46ee-9e36-c3c757256abe.png)


<br/>

오른쪽 하단의 저장 버튼을 눌러 변경사항을 저장합니다.

<br/>

아래와 같은 화면이 나오면 성공입니다.

<br/>

![스크린샷 2022-11-28 시간: 18 50 54](https://user-images.githubusercontent.com/53536205/204247346-f8f9137f-c91f-4253-851c-48b7cc1896ad.png)

### 새 프로젝트로 연결

**새 Google Cloud 프로젝트 만들기**를 누르고 오른쪽 하단의 저장 버튼을 눌러 변경사항을 저장합니다.

![스크린샷 2022-11-28 시간: 18 52 53](https://user-images.githubusercontent.com/53536205/204247697-783e4c60-30be-4453-8534-1c0b4b53d694.png)

이렇게 하면 Google Cloud에 "Google Play Console Developer"프로젝트가 생성되고 연결 됩니다.

아래와 같은 화면이 나오면 성공입니다.

![스크린샷 2022-11-28 시간: 18 52 53](https://user-images.githubusercontent.com/53536205/204249477-f683e386-ff33-4b1c-8c4f-10d39ae0ecb6.png)


### 서비스 계정 생셩 및 연결.














