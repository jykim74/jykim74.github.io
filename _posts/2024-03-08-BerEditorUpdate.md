---
layout: post
title: "BerEditor Update History"
tags: [ASN.1,ASN.1 viewer, BER, DER, PQC, RSA, ECDSA, DSA, PQC, ML-KEM, ML-DSA, SLH-DSA]
category: Software
---
BerEditor 버전 2.8.0 업데이트 하였습니다.  
BerEditor에 대한 설명은 [BerEditor ( ASN.1 DER BER Viewer and Editor )](https://jykim74.tistory.com/36) 을 참조 하세요.

[\[Download\] BerEditor Version 2.8.0 (Winows 64bits)](https://jykim74.github.io/msi/BerEditor-enV280.msi)  

[\[Download\] BerEditor Version 2.8.0 (MacOS)](https://jykim74.github.io/dmg/BerEditorV280.dmg) 

[\[Download\] BerEditor Version 2.8.0 (Linux 64bits)](https://jykim74.github.io/zip/BerEditorV280.zip)

## Version 2.8.0 업데이트
- PDF 서명 보기 오류 수정
- PKCS7 오류 수정

## Version 2.7.8 업데이트
- 라이선스창에서 무료 라이선스 발급 지원 (이메일 입력 필요함)

## Version 2.7.6 업데이트
- BER 노드 보기 지원
- 다른이름 저장 오류 수정
- PDF 서명 오류 수정
- PKCS7 CMS DETACHED 에서 데이타 입력 지원


## Version 2.7.4 업데이트
- CMS PKCS7 오류 수정
- PDF 서명 기능

## Version 2.7.2 업데이트
- 인증서 CRL 만료에 따른 아이콘 표시
- 각각의 기능창에 대한 아이콘 표시

## Version 2.7.0 업데니트
- BER 트리 마우스 우클릭 죽는 오류 수정
	- 그동안 테스트 부족으로 못한 안정화 작업이 되었습니다.
	- 가능한 이전 버전 사용자는  업데이트 해주세요

## Version 2.6.8 업데이트
- BER 이전 다음 이동 기능 추가
- BER 검색 기능 오류 수정 및 검색어 포함 유무 검색 지원
- BER BITSTREAM 확장시 오류 수정
- TTLV 이전 다음 이동 기능 추가
- TTLV 검색 기능 오류 수정 및 검색어 포함 유무 검색 지원
- BER과 TTLV 선택 영역 표시 설정 각각 처리로 설정 분리
- 인증서 경로 검증에서 CertMan CA 및 CRL 읽어오기 옵션 지원

## Version 2.6.6 업데이트
- BER 편집(추가/삭제/변경) 오류 수정 및 UI 개선
- BER 편집시 길이 0x80 (Indefinite 모드) 지원
- TTLV 편집(추가/삭제/변경) 오류 수정 및 UI 개선

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
