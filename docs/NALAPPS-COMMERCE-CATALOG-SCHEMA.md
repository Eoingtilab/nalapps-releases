# NalApps Commerce Catalog v1

`nalapps-commerce-catalog.json`은 고객 사이트의 Core와 `app.nal.la` EDD Bridge가 함께 사용하는 공개 배포 카탈로그입니다.

## 신뢰 경계

- 원본 소스 저장소는 Private입니다.
- 고객 배포 자산은 `Eoingtilab/nalapps-releases`의 GitHub Release에만 둡니다.
- 카탈로그에는 공개 가능한 제품 메타데이터만 포함합니다.
- 라이선스 키, 고객정보, 주문정보, GitHub 토큰과 EDD 비밀값은 포함하지 않습니다.

## 필수 필드

각 `products[]` 항목은 다음 필드를 사용합니다.

- `product_id`: 변경하지 않는 제품 식별자
- `version`: 배포 버전
- `plugin_file`: `폴더/메인파일.php`
- `package_url`: HTTPS GitHub Release ZIP 주소
- `sha256`: 검증된 ZIP의 SHA-256
- `available`: 설치 허용 여부
- `free`: 무료/유료 구분
- `requires_core`, `requires_woocommerce`
- `requires_wp`, `requires_php`
- `license_policy`
- `item_id`: app.nal.la EDD Download ID. Core Free는 277 고정

## 활성화 규칙

`available=true`는 다음 조건을 모두 만족한 경우에만 허용합니다.

1. Release 자산이 실제 존재합니다.
2. ZIP 최상위 폴더와 `plugin_file`이 일치합니다.
3. PHP 구문검사와 제품 계약 테스트가 통과합니다.
4. `sha256`이 Release 자산과 일치합니다.
5. WordPress 스테이징 설치·활성화 테스트가 통과합니다.

검증 전 제품은 URL이 예약되어 있어도 `available=false`로 유지합니다.

## 버전 정책

- RC: `x.y.z-rc.n`
- Stable: `x.y.z`
- Stable Release 자산과 태그는 덮어쓰지 않습니다.
- Core와 각 애드온은 독립 버전을 사용합니다.
