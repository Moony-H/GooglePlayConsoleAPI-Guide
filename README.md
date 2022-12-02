# Google Play Console API Guide



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

![스크린샷 2022-11-28 시간: 18 50 54](https://user-images.githubusercontent.com/53536205/204414214-afe99c77-9ad8-4c07-ac1e-efc4d9967ff0.png)



### 서비스 계정 생셩 및 연결.


[Google Cloud](https://cloud.google.com/)에 접속하여 프로젝트에 들어갑니다.

<br/>

IAM 및 관리자 버튼을 눌러 페이지에 들어갑니다.

![스크린샷 2022-11-28 시간: 19 08 27](https://user-images.githubusercontent.com/53536205/204251164-09c26858-be63-47e3-be34-371a05e69907.png)

왼쪽 탭의 서비스 계정을 클릭합니다.


![스크린샷 2022-11-28 시간: 19 10 49](https://user-images.githubusercontent.com/53536205/204251711-5ce66361-fd61-4967-90fd-3d9b1430e5e2.png)

<br/>

그 다음 상단의 **+ 서비스 계정 만들기**를 클릭합니다.

<br/>

![스크린샷 2022-11-28 시간: 19 15 27](https://user-images.githubusercontent.com/53536205/204252549-6f94e619-e063-4299-8fb2-1a970b00a1d3.png)

<br/>

서비수 계정 이름과 서비스 계정 ID를 수정한 후에 **만들고 계속하기**를 클릭합니다. 

(완료를 누르면 추후에 권한을 수정해야 합니다.)

![스크린샷 2022-11-28 시간: 19 20 21](https://user-images.githubusercontent.com/53536205/204414650-2e8c6a7e-cf72-4bcf-b8ea-c751e199b21b.png)

<br/>

프로젝트에 대한 엑세스 권한 부여를 합니다.

엑세스 권한을 기본의 편집자로 선택한 후 계속, 완료를 누릅니다.

![스크린샷 2022-11-29 시간: 10 20 30](https://user-images.githubusercontent.com/53536205/204415184-fec45b4d-da50-4da2-9a7f-da56a3b83e39.png)

서비스 계정이 생성된 것을 확인한 후, 다시 Google Play Console로 돌아가 API 엑세스 탭으로 들어갑니다.



오른쪽의 새로 고침을 누릅니다.


![스크린샷 2022-11-29 시간: 10 24 47](https://user-images.githubusercontent.com/53536205/204415870-60c06e35-f30b-43ad-9c11-06ddc1bfdb5f.png)


방금 만든 서비스 계정이 표시되면 오른쪽의 Play Console 권한 관리를 클릭합니다.


![스크린샷 2022-11-29 시간: 10 29 35](https://user-images.githubusercontent.com/53536205/204416205-74642e5f-3ac3-4bc2-878d-370c7a24c329.png)

앱 권한 탭에서 애플리케이션 추가를 눌러 API를 사용할 앱을 추가합니다.

![스크린샷 2022-11-29 시간: 10 35 02](https://user-images.githubusercontent.com/53536205/204416999-446a5e36-0fa6-4d0c-9ae5-db0103a2208a.png)

아래와 같은 창이 뜨면 적용을 누릅니다.

![스크린샷 2022-11-29 시간: 10 37 46](https://user-images.githubusercontent.com/53536205/204417192-d0c82f7d-f7e7-43b1-8f06-dc9c68bdfbb7.png)

오른쪽 하단의 사용자 초대를 눌러 사용자를 초대합니다.

![스크린샷 2022-11-29 시간: 11 56 04](https://user-images.githubusercontent.com/53536205/204427632-0ad82ecf-b4ff-4c8c-9627-f89f0914dea1.png)


### 키 생성 및 저장

이번에는 키를 생성하고 저장하는 방법을 설명합니다.


먼저 [Google Cloud](https://cloud.google.com/)에 접속합니다.

그 다음 **IAM 및 관리자**를 클릭합니다.

![스크린샷 2022-11-28 시간: 19 08 27](https://user-images.githubusercontent.com/53536205/204251164-09c26858-be63-47e3-be34-371a05e69907.png)

왼쪽 탭의 **서비스 계정**을 클릭합니다.

![스크린샷 2022-11-28 시간: 19 10 49](https://user-images.githubusercontent.com/53536205/204251711-5ce66361-fd61-4967-90fd-3d9b1430e5e2.png)

전 단계에서 생성한 서비스 계정을 클릭합니다.

![스크린샷 2022-11-29 시간: 10 50 47](https://user-images.githubusercontent.com/53536205/204418834-e685f78d-bdc7-461e-ae85-172c5bce0056.png)


키 탭에 들어가 키 추기 -> 새 키 만들기를 눌러 키를 Json 형식으로 생성합니다.

![스크린샷 2022-11-29 시간: 10 53 54](https://user-images.githubusercontent.com/53536205/204419400-5d483011-263b-49cc-9561-60b0e064cbee.png)

![스크린샷 2022-11-29 시간: 10 57 27](https://user-images.githubusercontent.com/53536205/204419881-ee1d4ef1-8f65-47a2-8508-71e77567e957.png)

다운로드 된 키를 안전하게 보관합니다.


### Access token 생성


앞서 말한 바와 같이 Java, Kotlin을 사용하여 엑세스 토큰을 생성합니다.

예제에서는 Intellij CE와 Kotlin, Gradle을 사용합니다.

Intellij Community Edition은 [이곳](https://www.jetbrains.com/ko-kr/idea/)에서 다운 받으실 수 있습니다.

먼저 새로운 프로젝트를 생성합니다.

Kotlin, Gradle을 선택한 후, Create를 합니다.

![스크린샷 2022-11-29 시간: 11 23 53](https://user-images.githubusercontent.com/53536205/204423562-3af742da-27a7-475e-9406-05e04beac5b1.png)


build.gradle 파일을 연 후, 아래와 같은 코드를 dependencies 블록 안에 넣습니다.


![스크린샷 2022-11-29 시간: 11 26 17](https://user-images.githubusercontent.com/53536205/204423711-04120562-97ca-45da-8f55-0b3eecc59378.png)


```gradle
dependencies {
    ...
    
    implementation 'com.google.auth:google-auth-library-oauth2-http:1.12.1'
    implementation 'com.google.apis:google-api-services-androidpublisher:v3-rev20221108-2.0.0'
    
    ...

}
```

그 다음 오른쪽 상단의 sync를 눌러 적용합니다.

![스크린샷 2022-11-29 시간: 11 21 32](https://user-images.githubusercontent.com/53536205/204424081-ed92485a-f153-4660-b4ea-7ccdeaf2ca46.png)

그 다음 Main.kt 파일로 돌아가 아래와 같은 코드를 복사해서 붙여 넣습니다.

{다운 받은 Json 파일 경로}에는 앞서 Json 파일로 다운 받은 서비스 계정 키의 파일 경로를 넣습니다.

```kotlin
import com.google.auth.oauth2.ServiceAccountCredentials
import java.io.FileInputStream

fun main(args: Array<String>) {
    val credentials= ServiceAccountCredentials.fromStream(FileInputStream("{다운 받은 Json 파일 경로}"))
        .createScoped(setOf(AndroidPublisherScopes.ANDROIDPUBLISHER,"https://www.googleapis.com/auth/playdeveloperreporting"))
    credentials.refreshIfExpired()


    println(credentials.accessToken.tokenValue)
}
```

그 다음 오른쪽 상단의 Run 버튼을 눌러 코드를 실행합니다.

![스크린샷 2022-11-29 시간: 11 36 47](https://user-images.githubusercontent.com/53536205/204425108-21c03be7-a154-4c2e-9769-793790b0b218.png)

하단의 표시된 키 갚을 사용하여 api에 접근할 수 있게 되었습니다.















