---
layout: post
title: "CryptokiMan Update History"
tags: [Cryptoki, CryptokiMan, ECDSA, HSM, PKCS#11, PKI, RSA]
category: Software
---
CryptokiMan Version 1.9.6 업데이트 하였습니다.  
이프로그램은 PKCS#11 Version 2.4 표준 문서를 기준으로 만들어 졌습니다.  
CryptokiMan에 대한 파일 설명은 [CryptokiMan ( PKCS#11 Cryptoki Manager )](https://jykim74.tistory.com/38) 을 참조하세요.

[\[Download\] CryptokiMan Version 1.9.6 (Windows 64bits)](https://jykim74.github.io/msi/CryptokiMan-enV196.msi)  
[\[Download\] CryptokiMan Version 1.9.6 (MacOS)](https://jykim74.github.io/dmg/CryptokiManV196.dmg)
[\[Download\] CryptokiMan Version 1.9.6 (Linux 64bits)](https://jykim74.github.io/zip/CryptokiManV196.zip)

## Version 1.9.6 업데이트

- HSM 관리 메뉴 추가
- 개인키 공개키 비밀키 선택 창 지원
- UI 및 오류 개선

## Version 1.9.4 업데이트

-   UI 개선
-   오류 수정 및 안정화

## Version 1.9.2 업데이트

-   라인선스에 따른 기능 제한 정책 변경
-   CSR 만들기 기능 지원
-   안정화 및 UI 개선

## Version 1.9.0 업데이트

-   툴바 아이콘 선택 지원
-   비대칭키 보기 및 내보내기 지원
-   오류 및 안정화


## Version 1.8.8 업데이트
- EdDSA 키 메카니즘 지원
- CK 타입 이름 찾기 지원
- 내부 UI 개선
- 다수 오류 수정 및 안정화

## Version 1.8.6 업데이트
- OpenSession Login 처리 슬롯 아이콘 표시 함
- PKCS#11 정의값 Hex 표시
- 안정화 및 오류 수정

## Version 1.8.4 업데이트
- 안정화 및 오류 수정
- UI 인터페이스 상당 수 개선

## Version 1.8.2 업데이트

-   파일 해시,서명/검증, 암/복호화 쓰레드 실행 지원
- 	입력값 인코딩 체크 및 오류 (한글 입력) 수정
-   입력 길이에서 Hex 길이에 홀수 입력 '\_' 표시
-   UI 개선 수정 및 안정화

## Version 1.8.0 업데이트
- 주요 메뉴 단축키 지원
- 헥사 정보 고정 넓이 설정 지원
- 라이선스 체크 변경 및 온라인 발급 지원
  * [라이선스 신청 페이지](https://jykim74.mycafe24.com/user_reg.php)
  * [무료 라이선스 발급 방법](https://jykim74.tistory.com/notice/273)
- UI 개선 및 오타 수정
  
## Version 1.7.0 업데이트

-   저작권 표시 및 사용 오픈소스에 대한 저작권 정보 표시
-   OpenSSL 3.0.8 변경 없이 지원
-   영문 메세지 개선
-   에러 코드 구체화
-   Edit Attribute 목록 기능 지원
-   UI 및 다수 오류 수정

## Version 1.6.4 업데이트

-   Session 에서 State 오류 수정
-   객체 관련 Boolean 초기 선택 모두 해제
-   Boolean 초기 값을 false 에서 true 로 변경

## Version 1.6.2 업데이트

-   CreateKey 생성 오류 수정
-   인증서 및 공개키에서 Sensitive 속성 기능 제거
-   UI 개선

## Version 1.6.0 업데이트

-   비라이선스 모드 안정화 및 타이틀 표시
-   객체 검색 기능 추가

## Version 1.5.2 업데이트

-   리눅스 64비트 지원
-   Q&A 링크 Goolge Groups로 변경
-   PIN 번호 변경시 입력 확인 기능 추가
-   Derive 기능에서 ECDH 기능 지원
-   RSA 키 쌍 생성 시 키길이 값(3072, 4096) 오류 수정
-   키 쌍생성에서 DSA 알고리즘 및 RSA\_PKCS\_OAEP 암호화 지원
-   UI 수정 및 안정화

## Version 1.5.0 업데이트

-   전체 폰트 설정 UI 개선
-   Derive 기능에서 CKA\_DERIVE 가 TRUE 값 키 만 불러 오기
-   하단 정보 UI 개선
-   FindMaxObjectCounts 설정 지원

## Version 1.4.8 업데이트

-   서명 및 검증에서 DSA 관련 메커니즘 지원
-   서명에서 메커니즘 선택 안되는 오류 수정
-   서명 검증에서 설정 장치 메커니즘 사용 기능 지원

## Version 1.4.6 업데이트

-   인증서와 개인키에서 SPKI 자동 입력 지원
-   CKA\_COPYABLE CKA\_DESTROYABLE 속성 선택 기능 지원
-   CopyObject 창 및 기능 지원
-   객체 (인증서, 공개키, 개인키, 비밀키 및 데이타) 상세 보기 메세지 개선
-   OpenSession 및 Login 처리에 따른 왼쪽 트리 폰트 강조 및 언더라인 처리
-   개발 환경을 qmake 에서 cmake 로 변경
-   그외 버그 및 UI 개선

## Version 1.4.2 업데이트

-   비대칭키 Subject 값에서 Text 와 DER 값 형식 지원
-   GenKeyPair 에서 Subject 값 선택 시 오류 수정
-   인증서 보기에서 이름제한 (NameConstraints) 필드에서 dirName 형식 지원
-   인증서 보기에서 공개키 값 세분화
-   그외 UI 및 메세지 수정

## Version 1.4.0 업데이트

-   개인키, 인증서, PFX 가져오기에서 Use SKI 옵션 지원
-   개인키, 공개키 생성 기능에서 Use SKI 옵션 지원
-   대칭키 생성 기능에서 CKA\_ID 를 랜덤 값 설정 지원
-   CKA\_TRUSTED, CKA\_SIGN\_RECOVER, CKA\_VERIFY\_RECOVER 옵션 지원
-   인증서 정보 보기에서 속성 선택 콤보 지원
-   UI 개선 및 다수 오류 수정

## Version 1.2.8 업데이트

-   윈도우 환경과 MacOS 환경 지원 UI 개선 ( MacOS 다수 환경 개선 )
-   윈도우 기본 폰트 Consolas 폰트 사용
-   오류로 인한 메모리 크래쉬 안정화 작업

## Version 1.2.6 업데이트

-   자동 업데이트 기능 지원
-   버그 및 이슈 알림과 Q&A 링크 지원
-   License 정보 보기 및 추가 지원
    -   현재 2023-12-31 일 까지 라이선스가 포함 되어 있음
-   MacOS 기본 폰트를 Monaco 폰트 사용

## Version 1.2.4 업데이트

-   ECC 공개키 저장시 잘못 된값 저장 오류 수정
-   CreateKey 에서 설정 메키니즘 사용 시 적용 오류 수정
-   그외 메세지 및 UI 개선

## Version 1.2.2 업데이트

-   폰트 패밀리 설정 기능 지원
-   Use Device 메커니즘 설정 시 자동 지원
-   DSA 키 쌍 생성 기능 추가
-   모든 날짜 초기 값을 현재 날짜로 변경
-   PFX 와 개인키 가져오기에서 DSA 알고리즘 지원
-   개인키 가져오기에서 암호화된 개인키 지원
-   인증서 보기에서 AltName에서 otherName 형식 지원
-   UI 및 메세지 개선
-   알고리즘 인식 오류로 인한 문제 수정

## Version 1.2.0 업데이트

-   Digest 에서 파일 모드 지원
-   서명에서 파일 서명 지원
-   Verify 에서 파일 Verify 기능 지원
-   Encrypt, Decrypt 파일 입력 지원
-   File 읽기에서 한번에 읽기 사이즈 설정 기능 추가
-   Read Only UI 색지정
-   AES GCM Encrypt/Decrypt 지원
-   장치 메커니즘 사용 옵션 지원 (설정 기능 추가)
-   윈도우 기본 폰트 굴림체 지정
-   그외 버그 수정 및 UI 개선

## Version 1.0.0 업데이트

-   Digest 에서 DigestKey 기능 추가
-   서명에서 SignRecoverInit, SignRecover 기능 추가 및 UI 수정
-   검증에서 VerifyRecoverInit, VerifyRecover 기능 추가 및 UI 수정
-   WaitForSlotEvent 체크 추가
-   EditAttribute 에서 Value 값 String 및 Base64 인코딩 지원
-   명령어로 cryptoki library 파일 열기 지원

[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fjykim74.github.io%2Fsoftware%2F2024%2F03%2F08%2FCryptokiUpdate.html&count_bg=%23C8883D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false)](https://hits.seeyoufarm.com)

