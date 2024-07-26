---
layout: post
title: "CertMan Update History"
tags: [X.509,Cert,Certificate,CRL,RSA,ECDSA,PKI,CSR,KeyPair]
category: Software
---
CertMan Version 1.8.4 업데이트 하였습니다.  
CertMan에 대한 파일 설명은 [CertMan ( X509 Cert, CRL Manager )](https://jykim74.tistory.com/37) 을 참조하세요.

[\[Download\] CertMan Version 1.8.4 ( Windows 64bits )](https://jykim74.github.io/msi/CertMan-enV184.msi)  
[\[Download\] CertMan Version 1.8.4 ( MacOS )](https://jykim74.github.io/dmg/CertManV184.dmg)  
[\[Download\] CertMan Version 1.8.4 ( Linux 64bits )](https://jykim74.github.io/zip/CertManV184.zip)

## Version 1.8.4 업데이트
- 안정화 및 오류 수정
- UI 인터페이스 상당 수 개선

## Version 1.8.2 업데이트

-   입력 길이에서 Hex 길이에 홀수 입력 '\_' 표시
-   인증서 체인 내보내기 지원
- 	입력값 인코딩 체크 및 오류 (한글 입력) 수정
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
-   UI 개선

## Version 1.6.0 업데이트

-   비라이선스 모드 안정화 및 타이틀 표시
-   메인 아이콘 변경

## Version 1.5.6 업데이트

-   리눅스 64비트 지원
-   Q&A 링크 Groogle Groups 변경
-   Tray 기능 제거
-   DN 생성 창 지원
-   가져오기에서 입력창 지원
-   오류 수정 및 안정화

## Version 1.5.4 업데이트

-   CSR 가져오기에서 가져오기 시간 설정 및 NotUsed 상태 처리
-   ChallengePassword 값 표시 오류 수정
-   CSR 에서 UnstrusturedName 필드 지원
-   DN 값 만들기 창 지원

## Version 1.5.2 업데이트

-   폰트 설정 적용 개선
-   로그 일시 정지 기능 추가
-   인증서 및 CRL 프로파일 상세 로그 개선
-   Change Password 기능 추가
-   데이타 있어도 Set Password 기능 지원
-   qmake 에서 cmake 개발 환경 변경

## Version 1.5.0 업데이트

-   인증서 프로파일 변경하면 오류로 버전 및 CSR용으로 선택 오류 수정
-   인증서 및 CRL 발긊 시 가져오기 인증서는 제외 시킴
-   인증서 및 CRL 확장자 프로파일 보기 상세화
-   요청서 보기에서 공개키 보기 추가
-   getLDAP 을 getURI 로 변경 (http URL 지원)
-   인증서 프로파일에서 이름제한에서 dirName 포맷지원
-   CRL 정보에서 LastUpdate 호칭을 ThisUpdate로 변경 (DB도 변경)
-   인증서 보기에서 공개키 값 보기 세분화
-   인증서 및 프로파일 중복값 방지
-   그외 다수의 UI 및 메세지 개선 및 오류 수정
-   ( 1.5.0 버전에서 DB 스키마 변경으로 이전 버전의 데이타를 사용하면 안됩니다 )

## Version 1.4.6 업데이트

-   인증서 보기에서 공개키 값 표시 지원
-   인증서 보기에서 속성 선택 콤보 지원
-   인증서 생성시 Authority Key Identifier 값 생성 오류 수정
-   CSR 파일 읽기 발급 오류 수정
-   인증서 및 CRL 마지막 발급자 및 프로파일 자동 선택 처리
-   그외 UI 및 메세지 개선

## Version 1.4.4 업데이트

-   윈도우 환경과 MacOS 환경 지원 UI 개선 ( MacOS 다수 환경 개선 )
-   윈도우 기본 폰트 Consolas 폰트 사용
-   오류로 인한 메모리 크래쉬 안정화 작업

## Version 1.4.2 업데이트

-   자동 업데이트 기능 지원
-   RSA 개인키 내보내기 오류 수정
-   License 정보 보기 및 추가 지원
    -   현재 2023-12-31 일 까지 라이선스가 포함 되어 있음
-   MacOS 기본 폰트를 Monaco 폰트 사용

## Version 1.4.0 업데이트

-   요청서(CSR) 정보 보기 기능 추가
-   CSR 생성 시 Extension 영역 지원
-   인증서 생성 시 CSR Extension 적용 지원
-   원경 DataBase 지원( MySQL, PosgreSQL 지원)
    -   현재 MySQL과 PostgreSQL 외부 라이브러리는 별도 넣어 줘야 함
    -   원경 DB 사용 할려면 DB 및 Table 생성은 개별 작업 필요함 ( 추후 메뉴얼 예정 )
-   개인키 패스워드 저장 방식 변경
    -   AES-CBC 암호화에서 PKCS#8 형식으로 암호화 변경
-   요청서(CSR) 정보 보기 기능 추가
-   DB생성 이후에도 개인키 암호화 설정 기능 추가
    -   저장된 개인키가 없을 때 사용 가능
-   연결 끊기 기능 추가
-   버그 및 이슈 메뉴와 Q&A 메뉴 추가
-   UI 개선 및 오류 수정
-   이전 버전(1.2.X 이전 버전)에서 생성한 DB 파일은 지원 안됨
    -   원경 DB 지원으로 스키마 변경 및 개인키 암호화 방식 변경으로 이전 버전 호환 안됨

## Version 1.2.4 업데이트

-   PKCS11 방식 CSR, 인증서, CRL 생성 오류 수정
-   PKCS11 저장에서 라벨 정보 설정 지원
-   개인키 가져오기 기능에서 상태를 Not Used 로 설정
-   PFX 가져오기 개인키는 Used 설정
-   그외 메세지 및 UI 개선

## Version 1.2.2 업데이트

-   폰트 패밀리 설정 기능 지원
-   PKCS#11 모듈 사용 오류 개선
-   DSA 및 EdDSA 가져오기/내보내기 기능 지원
-   공개키 내보내기 기능 추가
-   개인키 및 PFX 암호화 알고리즘 옵션 선택 기능 지원
-   개인키 정보창에서 키 쌍 체크 추가
-   개인키 정보창에서 PKCS#11 저장 기능 추가
-   인증서 AltName에서 otherName 형식 지원
-   인증서 기간 갱신 기능 추가
-   PKCS#11 PIN 설정 추가
-   인증서 폐기시 아이콘 표시 변경
-   SM2 키 인경우 인증서 생성시 프로파일 해쉬가 SM3 아니라도 SM3변경 지원
-   UI 및 메세지 개선
-   알고리즘 인식 오류로 인한 문제 수정

## Version 1.2.0 업데이트

-   EdDSA 알고리즘 Ed25519, Ed448 지원
-   DSA 알고리즘 키쌍, CSR, Certificate, CRL 생성 지원
-   EdDSA 알고리즘 키쌍, CSR, Certificate, CRL 생성 지원
-   Read Only UI 색지정
-   윈도우 기본 폰트 굴림체 지정
-   Read Only UI 색지정
-   개인키 정보 보기 기능 추가
-   그외 버그 수정 및 UI 개선

## Version 1.0.2 업데이트

-   요청서 만들기에서 Challenge 의 길이가 0 이하이면 NULL 처리
-   SM2 인증서의 공개키 값 OID 정보 오류 수정
-   요청서 생성시 SM2 파라미터 경우 자동 해쉬를 SM3 선택
-   인증서 발급시 일반 모드에서는 유저 정보 그룹 제거
-   키 목록 및 요청서 목록에서 선택키 NotUsed 인경우 선택한 키이름으로 요청서 및 인증서 생성창 보임
-   키쌍 삭제시 이미 사용하는 CSR 또는 인증서가 있으면 삭제 못함
-   인증서 경우 CA 인증서일 경우 발급한 인증서 또는 CRL 있을 시 삭제 못함
-   CA 이면서 Self 인증서 삭제시 왼쪽 트리 메뉴도 제거함
-   MakeCertDlg UI 및 MakeReqDlg UI 등 그외 UI개선

## Version 1.0.1 업데이트

-   명령어로 DB 파일 열기 지원
-   Cert Profile 과 CRL Profile 에서 Default 해쉬 설정 지원
-   CRL Profile 에서 SM3 해쉬 알고리즘 지원

## Version 1.0.0 업데이트

-   폴더명 한글 포함 경우 버그 수정
-   About에 OpenSSL 와 QT 버전 표시
-   인증서 또는 CRL 가져오기에서 PEM 과 DER 자동 구분
-   초기 해쉬 및 ECC 파라미터 설정 기능 추가
-   일부 UI 개선

[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fjykim74.github.io%2Fsoftware%2F2024%2F03%2F08%2FCertManUpdate.html&count_bg=%23C83DBB&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false)](https://hits.seeyoufarm.com)
