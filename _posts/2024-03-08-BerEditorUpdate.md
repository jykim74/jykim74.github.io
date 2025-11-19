---
layout: post
title: "BerEditor Update History"
tags: [ASN.1,ASN.1 viewer, BER, DER, PQC, RSA, ECDSA, DSA, PQC, ML-KEM, ML-DSA, SLH-DSA]
category: Software
---
BerEditor 버전 2.6.4 업데이트 하였습니다.  
BerEditor에 대한 설명은 [BerEditor ( ASN.1 DER BER Viewer and Editor )](https://jykim74.tistory.com/36) 을 참조 하세요.

[\[Download\] BerEditor Version 2.6.4 (Winows 64bits)](https://jykim74.github.io/msi/BerEditor-enV264.msi)  

[\[Download\] BerEditor Version 2.6.2 (MacOS)](https://jykim74.github.io/dmg/BerEditorV262.dmg) 

[\[Download\] BerEditor Version 2.6.4 (Linux 64bits)](https://jykim74.github.io/zip/BerEditorV264.zip)

## Version 2.6.4 업데이트
- SSS 오류 수정 및 GF(256) 지원
- PKCS8 PKCS12 암호화 방식 설정 지원
- 내부 관리 효율 개선

## Version 2.6.2 업데이트
- ChaCha20 ChaCha20_Poly1305 암복호화 지원

## Version 2.6.0 업데이트
- DER 보기에서 BITSTRING OCTETSTRING 자동 확장 설정 지원
- Init/Update/Final 상태 정보 표시 개선
- CSR DN 표시 동일 RDN 지원

## Version 2.5.8 업데이트
- 오류 수정 및 UI 개선

## Version 2.5.6 업데이트
- 오류 수정 및 UI 개선

## Version 2.5.4 업데이트
- 다수 기능 창들 Drag and Drop 지원
- 일부 오류 수정 및 UI 개선

## Version 2.5.2 업데이트
- 인증서 정보 서명값 표시 비트스트링 BER 헤더 제거
- UI 개선


## Version 2.5.0 업데이트
- PQC 알고리즘 ML-KEM, ML-DSA, SLH 지원( 키생성, CSR, 전자서명, 인증서)
- 해시 지원 알고리즘 추가 : SHAKE128, SHAKE256, SHA3 모두
- 인증서, 개인키보기, CSR 보기에서 KID 표시
- 키 관리(Key Manage) 에서 KEM 기능 추가
- BER 주요 포맷 체크 기능 추가
- MAC 검증 기능 추가
- OpenSSL 3.5.3 라이브러리 적용
- UI 개선 및 다수 오류 수정

## Version 2.4.4 업데이트
- Doc Signer 기능 추가
- PKCS7 CMS 분리 및 기능 개선
- UI 개선 및 오류 수정

## Version 2.4.2 업데이트
- 인증서 관리 오류 수정 및 개선
- 인증서 경로 검증 신뢰 목록 지원 오류 수정
- 내부 코드 개선

## Version 2.4.0 업데이트
- CMS 보기에서 TSP 메세지 보기 지원
- 종료시 파일 저장 유무는 경로 존재시만 묻기
- TSP 클라이언트에서 사용자 인증 요청 지원
- 오류 수정 및 UI 개선

## Version 2.3.8 업데이트
- CertMan, KeyPairMan, KeyList 마우스 우클릭 메뉴 지원
- X509 비교에서 CRL 보기 오류 수정
- 서명/검증 공개키 암복호화에서 KeyPairMan 지원
- 데이타 변환기에서 바이너리 파일 쓰기 지원
- 개인키 PEM 형식시 헤더 오류 수정
- 다수 오류 수정 및 UI 개선

## Version 2.3.6 업데이트
- ACME 클라이언트 기능 추가
- 2038년 이후 시간처리 오류 수정
- 안정화 및 오류 수정

## Version 2.3.4 업데이트
- 인증서 CRL 에서 2038년 이후 시간처리 오류 수정

## Version 2.3.2 업데이트
- 키 동의(KeyAgree)에서 DH 파라미터 가져오기 내보내기 지원
- X509 ( Certificate, CRL, CSR ) 비교 기능
- 빅넘 계산이에서 타이머 표시 지원
- 폰트 설정 모노스페이스 폰트로 제한
- SSL 정보 트리 및 로그 창 DockWidget 처리
- 인증서 정보 창에서 OCSPClient, CA CRL BER 가져오기 기능 추가
- OCSP Client 에서 Nonce 입력 지원 및 응답 CertID 보기 지원
- KMIP Encoder UI 전체 개선
- 다수 UI 개선 및 오류 수정

## Version 2.3.0 업데이트
- 파일 선택시 최근 경로 읽기
- CMS UI 개선

## Version 2.2.8 업데이트
- Shamir Secret Sharing 오류 수정 및 안정화
- 테이블 헤더 UI 활성화 처리 제거
- UI 개선

## Version 2.2.6 업데이트
- 숫자 변환기 UI 개선
- UI 설명 메세지 일부 추가
- 오류 수정 및 안정화

## Version 2.2.4 업데이트
- 빅넘 계산이 1자리 수 오류 수정
- UI 상 메세지 개선
- 일부 오류 수정

## Version 2.2.2 업데이트
- 키 관리에서 SCrypt 지원
- SSL 체크에서 신뢰인증서 게시 오류 수정
- 일부 UI 개선

## Version 2.2.0 업데이트
- SM2 알고리즘 지원
- 오류 수정 및 안정화

## Version 2.1.8 업데이트
- 설정에서 기본값 복원 지원
- 툴바 및 메뉴등 영문 메세지 변경
- 오류 및 UI 개선

## Version 2.1.6 업데이트
- 일부 라이선스 인식 오류 수정
- UI 및 오류 수정

## Version 2.1.4 업데이트
- 키 목록 관리 기능 지원
- XML, JSON, Text 보기 라인 표시 및 개선
- 정보 보기 라인 표시
- 안정화 및 UI 개선
- 오류 수정 (중요 버그 수정 되었으니 꼭 업데이트 하세요)

## Version 2.1.2 업데이트
- BER TTLV 찾기 기능 지원
- UI 개선

## Version 2.1.0 업데이트
-   툴바 아이콘 선택 지원
-   JSON 보기 지원
-   PKI 표준 문서 링크 지원
-   내보내기 UI 개선

## Version 2.0.8 업데이트
- CMS (PKCS7) 메세지 보기 지원
- CMS 기능 개선
- 키쌍 관리 키 편집 설정 지원
- UI 개선 및 오류 수정

## Version 2.0.6 업데이트
- ACVP 기본 알고리즘 부분 지원(기본 옵션 위주만 동작)
- 인증서 관리 및 키 쌍 관리에서 서명/검증 및 공개키 암/복호화 연계 지원
- Hash MCT alternate 지원
- GMAC 에서 IV 입력 지원
- DRBG 에서 Nonce 없는 경우 지원
- CCM 암/복호화 오류 수정(AAD 없는 경우 오류 발생)
- Seed MCT 오류 수정

## Version 2.0.4 업데이트
- Key Manage HKDF, ANSX963 KDF 지원
- CMP, OCSP, TSP, SCEP 클라이언트 오류 수정
- CAVP MCT 테스트 오류 수정
- CertMan 오류 수정
- 안정화 및 UI 개선

## Version 2.0.2 업데이트
- BN 계산기 UI 개선
- JSON, Text 보기 전체 및 부분보기 지원
	* BER TTLV 둘다 지원
	* 전체 보기에서 선택 영역 표시
	* SyntaxHilighter 제거(딜레이 없애기 위해)
- EdDSA 서명/검증 오류 수정
- 기타 성능 개선 및 안정화

## Version 2.0.0 업데이트
- 안정화 및 오류 수정
- UI 인터페이스 상당 수 개선
- 중요한 오류를 많이 수정 했으니 꼭 업데이트 하세요.

## Version 1.9.6 업데이트
- 개인키 공개키 보기 지원
- 입력값 인코딩 체크 및 오류 (한글 입력) 수정
- UI 개선 및 안정화

## Version 1.9.4 업데이트

-   KMIP 프로토콜 TTLV 포맷 인코딩/디코딩 지원
    -   디코딩, 인코더, 클라이언트, 복사등 메뉴 지원
-   입력 길이에서 Hex 길이에 홀수 입력 '\_' 표시
-   UI 개선 수정 및 안정화

## Version 1.9.2 업데이트
-   인증서 관리에서 다른 인증서 관리 기능 지원
-   SSS 입력값 짧은 길이 제한
-   Hash, Mac, Sign/Verify, Enc/Dec 파일 처리에서 쓰레딩 기능 지원
-   UI 개선 및 오류 수정

## Version 1.9.0 업데이트
-   키쌍 관리 기능
    *   키쌍 생성, 암/복호화, CSR 생성
-   인증서 관리 기능
    *   개인키와 인증서 쌍관리 CA, CRL 그리고 신뢰 RootCA 관리 기능
    *   PFX 가져오기/내보내기 및 인증서 선택 기능 지원
    *   암호화 메뉴내에서 인증서 선택시 인증서 선택 지원
-   OCSP, TSP, CMP, SCEP 클라이언트 기능 지원
    *   자제 개발된 서버(OCSP, TSP, CMP, SCEP) 연계용
- 큰숫자(BigNum) 계산기 오류 수정 및 UI 개선
-   그외 UI 개선 및 오류 수정
  
## Version 1.8.4 업데이트
- SSS 연산 OpenSSL 사용 및 Prime 값 입력 지원
- Big Num 계산기 기능 추가
- UI 개선 및 안정화

## Version 1.8.2 업데이트
- SSL Verify 신뢰 처리 오류 수정
- SSL Verify 신뢰 목록 추가에 대한 문의 처리
- 숫자 변환 시 마이너스 10진수 처리 지원
- 비트스트링 길이 표시 오류 수정
- BER 추가에서 (BitString, Integer, OID 텍스트 값을 Hex 값 변환 지원)
- 그외 UI 개선

## Version 1.8.0 업데이트
- 주요 메뉴 단축키 지원
- SSL Verify 오류 수정
- 헥사 정보 고정 넓이 설정 지원
- 데이타 인코딩 파일 읽기 지원
- 라이선스 체크 변경 및 온라인 발급 지원
  * [라이선스 신청 페이지](https://jykim74.mycafe24.com/user_reg.php)
  * [무료 라이선스 발급 방법](https://jykim74.tistory.com/notice/273)
- UI 개선 및 오타 수정
  
## Version 1.7.2 업데이트
- VID 생성 및 검증 기능 지원

## Version 1.7.0 업데이트

-   저작권 표시 및 사용 오픈소스에 대한 저작권 정보 표시
-   OpenSSL 3.0.8 변경 없이 지원
-   영문 메세지 개선
-   에러 코드 구체화
-   SSS 기능 오픈소스 변경
-   암/복호화 CCM 모드 오류 수정

## Version 1.6.2 업데이트

-   인증서, CRL 및 CSR 보기 포맷 체크 후 확인 기능
-   SSL 검증 UI 개선
-   SSL 검증에서 호스트명 체크 오류 수정

## Version 1.6.0 업데이트

-   비라이선스 모드 안정화 및 타이틀 표시
-   SSL 검증 기능 추가
-   인증서, CRL 및 CSR 열기 기능 추가
-   암/복호화에서 DES 알고리즘 제거
-   종료시 PEM 으로 열경우 변경 물음에 대해 묻지 않게 개선 함

## Version 1.5.6 업데이트

-   리눅스 64bit 지원
-   Q&A 링크 Google Groups 로 변경
-   BitString 표시에서서 Hex 값 표현 및 BitLength 정보 추가
-   오류 수정 및 안정화

## Version 1.5.4 업데이트

-   BER 입력 및 변경 버그 수정 및 UI 개선
-   폰트 설정 적용 개선
-   로그 일시 정지 기능 추가
-   qmake 에서 cmake 개발 환경 변경

## Version 1.5.2 업데이트

-   CAVP DRBG 에서 Hash-DRBG 와 HMAC-DRBG 모드 지원
-   이름제한(NameConstraints) 에서 dirName 포맷 지원
-   KeyWrap 에서 String, Base64 포맷 지원
-   CRL 정보에서 LastUpdate를 ThisUpdate 로 이름 변경
-   인증서 보기에서 공개키 정보 세분화
-   OID 정보에서 OID값 전체 보기 및 Nid 값 지원
-   그외 메세지 및 UI 다수 개선

## Version 1.5.0 업데이트

-   인증서 보기에서 죽는 문제 수정
-   인증서 보기에서 속성 선택 콤보 지원
-   CAVP RSA, ECC 기능 다수 오류 수정
-   CAVP RSA, ECC 에서 Hash 선택 콤보 지원
-   CAVP Rsp 파일 지정 개선
-   그외 UI 및 메세지 개선

## Version 1.4.8 업데이트

-   윈도우 환경과 MacOS 환경 지원 UI 개선 ( MacOS 다수 환경 개선 )
-   윈도우 기본 폰트 Consolas 폰트 사용
-   오류로 인한 메모리 크래쉬 안정화 작업

## Version 1.4.6 업데이트

-   자동 업데이트 기능 지원
-   버그 및 이슈 알림과 Q&A 링크 지원
-   License 정보 보기 및 추가 지원
    -   현재 2023-12-31 일 까지 라이선스가 포함 되어 있음
-   MacOS 기본 폰트를 Monaco 폰트 사용

## Version 1.4.4 업데이트

-   공개키 암호화 ECIES 알고리즘 추가
-   Get URI 창에서 저장 URI 지우기 추가 및 URI 주소 인식 개선
-   Get URI 에서 HTTP 가져오기 오류 수정
-   그외 메세지 및 UI 개선

## Version 1.4.2 업데이트

-   폰트 패밀리 설정 기능 지원
-   오른쪽 테이블 데이타 마우스 우클릭 선택 복사 기능 추가
-   서명/검증에서 암호화 개인키 지원
-   공개키 암/복호화에서 암호화 개인키 지원
-   CMS에서 암호화 개인키 지원
-   인증서 AltName 에서 otherName 형식 지원
-   공개키 암복호화 SM2 오류 수정
-   서명 및 검증에서 DSA 및 EdDSA 오류 수정
-   UI 및 메세지 개선
-   알고리즘 인식 오류로 인한 문제 수정

## Version 1.4.0 업데이트

-   MAC 용 ToolBar 아이콘 사이즈 24x24 로 변경함
-   Hash 에서 파일 입력 지원
-   MAC 에서 파일 입력 지원
-   CMS 에서 입력 값 파일 일기 지원
-   서명/검증에서 파일 입력 지원
-   암호화/복호화에서 파일 입력 지원
-   File 읽기에서 한번에 읽기 사이즈 설정 기능 추가
-   전자 서명/검증에서 DSA 와 EdDSA(Ed25519, Ed448) 지원
-   Read Only UI 색지정
-   SignRecover, VerifyRecover 기능 추가
-   윈도우 기본 폰트 굴림체 지정
-   그외 버그 수정 및 UI 개선

## Version 1.2.3 업데이트

-   CMS API 함수명 변경 및 로그 추가
-   키 동의 메뉴에서 전체 데이타 지우기 버튼 추가
-   MAC 에서 로그 메세지에 MAC 값이 아닌 Key 값 로그 표시 오류 수정
-   명령어로 BER 파일 열기 지원
-   서명/검증에서 검증 실행 시 인증서 공개키 자동 체크시 공개키를 잘못 처리 버그 수정
-   공개키 암/복호화에서 암호화 실행 시 인증서 공개키 자동 체크시 공개키 잘못 처리 버그 수정
-   공개키 암/복호화 SM2 인증서 및 개인키에 대한 알고리즘 자동 체크 오류 수정
-   전자서명, 공개키 암/복호화 그리고 CMS 에서 인증서와 개인키 타입 체크 기능 추가
-   Insert BER 와 Edit BER UI 개선 및 String 과 Base64 타입 지원

## Version 1.2.2 업데이트

-   SSS 길이 제한 및 키 분할 시 중복 값 나오는 버그 수정
-   초기 해쉬 알고리즘 설정 기능
-   전자서명, 공개키 암복호화에서 인증서 공개키 자동 체크 지원
-   CAVP 기능 Cryptogram 으로 이동
-   Cryptogram 메뉴 내의 모든 기능 모달레스 지원 (로그 보기와 동시 사용 하기 위해 )
-   한글 폴더명이 있을 시 읽기 문제 수정
-   OTP 생성 기능 버그 수정 및 UI 개선
-   DH 비밀키 일부 오류 경우 수정
-   MAC기능에서 GMAC 기능 지원 및 CMAC 경우 CBC 모드 고정
-   서명/검증 공개키 암/복호화, CMS에서 PEM 또는 DER 자동 인식
-   인증서 보기 및 디코딩 개인키 디코딩 기능 지원
-   CMS 에서 라이오 선택 그룹화 버그 수정
-   암호 메뉴 내에 기능들 전체 데이타 지우기 기능 추가
-   About에 OpenSSL 와 QT 버전 표시

## Version 1.2.1 업데이트

-   인증서 검증창에서 정책 검증 기능 추가
-   대칭키 암호화/복호화 다시 시도시 잘못 된 값 나오는 오류 수정
-   암/복호화 창 AE 기능에서 ReqTagLen 옵션 지원
-   SSS 기능 오픈소스 변경
-   UI 개선
-   기타 오류 및 메세지 수정
-   전체 창 사이즈 변경 가능

[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fjykim74.github.io%2Fsoftware%2F2024%2F03%2F08%2FBerEditorUpdate.html&count_bg=%233DC8C4&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false)](https://hits.seeyoufarm.com)
