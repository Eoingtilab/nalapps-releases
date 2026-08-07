# NallaReview 1.1.0

## 주요 변경
- NalaApps WPF 디자인 시스템 적용
- 첨부 NALLA APPS 이미지를 활용한 5초 인트로(1초 fade-in, 3초 유지, 1초 fade-out)
- 첫 실행 시 임시 시리얼 입력 및 로컬 저장. 현재는 비어 있지 않은 모든 시리얼 허용
- 향후 app.nal.la EDD 라이선스 연동용 설정 필드 예약
- NVIDIA 무료 API 추가: `https://integrate.api.nvidia.com/v1`, 모델 `openai/gpt-oss-20b`
- 기존 Ollama `gpt-oss:20b`, DeepSeek API 유지
- `nalapps-releases` latest.json 기반 업데이트 감지/다운로드/SHA-256 검증/앱 교체 구조 추가
- 기존 no-ai-tell, 무한스크롤, fingerprint 중복방지, 민감 리뷰 보류, 등록 확인 fail-closed 유지

## 배포 상태
Windows Release build와 Self-Test를 통과한 바이너리 ZIP이 생성되기 전까지 `latest.json`의 `downloadUrl` 및 `sha256`은 비워둡니다. 이 상태에서는 기존 설치본이 업데이트 파일을 다운로드하지 않습니다.
