# 2026년 하반기 EZCOM 인턴쉽

> 곽민서, 김지혜

## 1. 조직 개요

| 항목 | 내용 |
|---|---|
| 목적 | 인턴 2인 프로젝트 협업 |
| 구성원 | 2명 (둘 다 Owner) |
| 프로젝트 수 | 2개 |
| 플랜 | Free |


## 2. 멤버

| 이름 | 계정 | 역할 | 비고 |
|---|---|---|---|
| 곽민서 | [mkms0222-ez](https://github.com/mkms0222-ez) | 프론트엔드 | |
| 김지혜 | [zeehyee00](https://github.com/zeehyee00) | 백엔드 | |

## 3. 브랜치 네이밍 규칙

### 3.1 기본 브랜치

| 브랜치 | 용도 |
|---|---|
| `main` | 항상 동작하는 안정 버전. 직접 푸시하지 않고 PR로만 반영 |

### 3.2 작업 브랜치

형식: `{타입}/{간단한-설명}`

| 타입 | 용도 | 예시 |
|---|---|---|
| `feature` | 새 기능 개발 | `feature/login-page` |
| `fix` | 버그 수정 | `fix/null-error` |
| `docs` | 문서 수정 | `docs/update-readme` |
| `refactor` | 코드 구조 개선 (기능 변화 없음) | `refactor/user-service` |
| `chore` | 설정, 빌드, 패키지 등 기타 작업 | `chore/add-eslint` |
| `hotfix` | 긴급 수정 | `hotfix/payment-crash` |

규칙:

- 영문 소문자와 하이픈(`-`)만 사용하고, 한글·공백·대문자는 쓰지 않습니다.
- 설명은 2~4단어 이내로 짧게 씁니다.
- 브랜치 하나에는 작업 하나만 담습니다.
- PR이 머지되면 브랜치를 삭제합니다. (레포 설정 **Automatically delete head branches**를 켜면 자동으로 삭제됩니다.)

## 4. 커밋 메시지 규칙

형식: `{타입}: {변경 내용}`

```
feat: 로그인 페이지 추가
fix: 회원가입 시 null 에러 수정
docs: README 실행 방법 보완
```

| 타입 | 의미 |
|---|---|
| `feat` | 기능 추가 |
| `fix` | 버그 수정 |
| `docs` | 문서 변경 |
| `refactor` | 리팩터링 |
| `style` | 포맷팅 등 코드 의미에 영향 없는 변경 |
| `chore` | 빌드, 설정, 패키지 관리 |

- 제목은 한 줄로, 무엇을 했는지 알 수 있게 씁니다.
- 한 커밋에는 한 가지 변경만 담습니다.

## 5. 작업 흐름

```
 [main]  최신 상태
    │
    ▼
 ① 작업 브랜치 생성
    git switch -c feature/login-page
    │
    ▼
 ② 작업 & 커밋
    git commit -m "feat: 로그인 페이지 추가"
    │
    ▼
 ③ 푸시 & Pull Request 생성
    git push -u origin feature/login-page
    │
    ▼
 ④ 상대방 리뷰
    │
    ├── 수정 요청 ──▶ ②로 돌아가 추가 커밋 후 푸시
    │
    ▼ 승인 (Approve)
 ⑤ 상대방이 main에 머지
    │
    ▼
 ⑥ 브랜치 삭제 & 로컬 main 최신화
    git switch main
    git pull
    │
    ▼
 [main]  다음 작업 시작
```

원칙:

- 본인이 올린 PR은 본인이 머지하지 않고, 상대방이 확인한 뒤 머지합니다.
- `main`에는 직접 푸시하지 않습니다.
- 충돌이 나면 PR을 올린 사람이 해결합니다.
