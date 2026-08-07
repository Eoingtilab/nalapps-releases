# NallaReview 1.0.0

## 배포 상태

소스 정식본은 `Eoingtilab/nalapps-palce-autocomment`의 commit `68f2c94dec67a34123e963ea88a79ef8ed541524`에 반영되었습니다.

Windows x64 고객 배포 자산은 실제 Windows Release build와 내장 Self-Test가 PASS된 뒤 이 공개 배포 저장소의 GitHub Release 자산으로 올려야 합니다. 현재 공개 저장소에는 전체 소스 ZIP을 게시하지 않습니다.

## 주요 기능

- WebView2 내장 스마트플레이스 리뷰 관리 화면
- 무한스크롤/가상스크롤 리뷰 탐색
- 리뷰 fingerprint 중복 처리 방지
- Ollama `gpt-oss:20b` 및 DeepSeek API 선택
- no-ai-tell 자연어 후처리
- 민감/저별점 리뷰 자동 보류
- 최근 답글 유사도 차단
- 등록 성공 미확인 시 fail-closed 중단
- 로그인 만료/CAPTCHA/DOM 이상 시 중단
- 로컬 처리 이력, 로그, DOM 진단

## 배포 예정 자산

- `NallaReview-1.0.0-win-x64.zip`
- SHA-256 검증값

## 롤백

정식 배포 자산이 아직 공개되지 않았으므로 현재 롤백 대상 바이너리는 없습니다.
