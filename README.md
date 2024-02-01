# SocialLoginEx
소셜 로그인 테스트용 코드

# 소셜 로그인 관련 애플 문서
https://developer.apple.com/app-store/review/guidelines/#login-services

# 현재 원문(20240201)
4.8 Login Services
Apps that use a third-party or social login service (such as Facebook Login, Google Sign-In, Sign in with Twitter, Sign In with LinkedIn, Login with Amazon, or WeChat Login) to set up or authenticate the user’s primary account with the app must also offer as an equivalent option another login service with the following features:

- the login service limits data collection to the user’s name and email address
- the login service allows users to keep their email address private as part of setting up their account
- the login service does not track users as they interact with your app

A user’s primary account is the account they establish with your app for the purposes of identifying themselves, signing in, and accessing your features and associated services.

Another login service is not required if:

- Your app exclusively uses your company’s own account setup and sign-in systems.
- Your app is an education, enterprise, or business app that requires the user to sign in with an existing education or enterprise account.
- Your app uses a government or industry-backed citizen identification system or electronic ID to authenticate users.
- Your app is a client for a specific third-party service and users are required to sign in to their mail, social media, or other third-party account directly to access their content.

# 한글






# 이전 정책 한글
4.8 Apple로 로그인
앱에서 사용자의 기본 계정을 설정 또는 인증하기 위해 타사 또는 소셜 로그인 서비스(Facebook 로그인, Google 로그인, Twitter로 로그인, LinkedIn으로 로그인, Amazon으로 로그인 또는 WeChat 로그인 등)를 사용하는 앱은 Apple로 로그인 역시 동등한 옵션으로 제공해야 합니다. 사용자의 기본 계정은 사용자 식별, 로그인, 앱의 기능 및 연결된 서비스에 접근하기 위한 목적으로 앱에 설정한 계정을 의미합니다.

Apple로 로그인은 다음 경우에 필요하지 않습니다.

- 회사의 자체 계정 설정 및 로그인 시스템을 전용으로 사용하는 앱인 경우.
- 사용자가 기존의 교육 또는 기업 계정을 사용해 로그인해야 하는 교육, 기업 또는 비즈니스 앱인 경우.
- 정부 또는 업계 지원 주민 확인 시스템이나 전자 ID를 사용하여 사용자를 인증하는 앱인 경우.
- 특정 타사 서비스의 클라이언트인 앱으로 사용자가 콘텐츠에 접근하려면 메일, 소셜 미디어 또는 기타 타사 계정에 직접 로그인해야 하는 경우.


# 카카오 로그인
## 구현 방식 
### 카카오톡으로 로그인(카카오가 권장하는 방법)
- 카카오톡에 연결된 카카오 계정 및 인증 정보를 사용
- 사용자가 카카오계정 정보를 직접 입력하지 않아도 간편하게 로그인 가능
- launchMethod 파라미터를 사용해 커스텀 스킴 또는 유니버설 링크 중 하나로 앱 전환 방식 설정 가능
### 카카오 계정으로 로그인
- 기본 웹 브라우저를 통해 카카오 계정 정보를 입력하고 로그인
- 사용자가 카카오 계정 정보를 직접 입력하는 단계를 거침
- 사용자가 여러 개의 카카오 계정을 사용하는 서비스, 카카오톡 미설치 또는 미지원 디바이스에서 사용

## 카카오 개발자 센터 설정
1. https://developers.kakao.com/ 
- 카카오 계정을 활용한 로그인
2. '내 애플리케이션' 생성
- 앱을 구별할 수 있게 이름 설정
3. 내 애플리케이션 -> 앱 설정 -> 요약 정보 -> 번들 등록
- 개발중인 앱과 동일한 번들 사용
4. 제품 설정 -> 카카오 로그인 -> 활성화 설정 
- 활성화 설정 상태를 On으로 변경
5. 제품 설정 -> 카카오 로그인 -> 동의항목
- 필요한 데이터를 선택 
- 카카오 정책에 따라서 권한이 필요한 동의항목에 대한 심사를 진행

## SDK 다운로드
- Cocoapods과 Swift Package Manager를 지원
