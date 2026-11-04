# admin-automation

행정 업무, AI 교육, 자동화 개발에 쓰는 **워크플로·스크립트·문서**를 한곳에서 관리하는 저장소입니다.
특정 도구에 묶이지 않고, 업무에 맞는 방식(n8n, GitHub Actions, Apps Script, Python 등)을 골라 씁니다.

## 이 저장소로 하는 일

| 영역 | 예시 | 주로 쓰는 방식 |
| --- | --- | --- |
| 행정 자동화 | 메일 분류·회신 초안, 일정 정리, 시트 취합, 보고서 생성 | n8n, Apps Script |
| AI 교육 | 강의 자료, 실습 예제, 프롬프트 모음, 수강생 안내 | 문서, 스크립트 |
| 개발 자동화 | 배포·점검·알림, 데이터 처리 | GitHub Actions, Python |

## 폴더 구성

```
admin-automation/
├── workflows/                 자동화 본체
│   ├── README.md              워크플로 목록(카탈로그)
│   ├── _template/             새 워크플로 설계서 양식
│   ├── n8n/                   n8n 워크플로 JSON
│   ├── github-actions/        GitHub Actions 예시·템플릿
│   ├── google-apps-script/    Google Workspace용 스크립트
│   └── scripts/               Python 등 독립 실행 스크립트
├── docs/
│   ├── manuals/               행정 업무 매뉴얼·절차서
│   ├── guides/                도구 사용 가이드(GitHub, n8n 등)
│   └── ai-education/          AI 교육 자료
└── .github/                   이슈·PR 양식, 실제 Actions 워크플로
```

## 새 자동화를 추가하는 순서

1. **이슈 등록**: `자동화 요청` 양식으로 무엇을, 왜 자동화하는지 적습니다.
2. **설계서 작성**: `workflows/_template/`를 복사해 목적·트리거·단계·담당자를 적습니다.
3. **구현**: 알맞은 도구 폴더에 파일을 추가합니다.
4. **카탈로그 갱신**: `workflows/README.md` 표에 한 줄 추가합니다.
5. **PR로 검토 후 병합**합니다.

## 규칙

- `main`에 직접 수정하지 않고 브랜치(`feature/작업이름`)에서 작업한 뒤 PR로 병합합니다.
- 비밀번호, API 키, 토큰, 개인정보는 올리지 않습니다. (`.gitignore` 참고)
- n8n 등에서 내보낸 파일에 Credentials 값이 포함됐는지 올리기 전에 확인합니다.
- 모든 자동화에는 담당자와 실패 시 대응 방법을 설계서에 적습니다.
- 파일명은 가급적 영문 소문자와 하이픈(`mail-triage.json`)을 씁니다. (Windows·Mac 공용 사용 대비)

## 시작하기

```bash
git clone https://github.com/ilumi76-dev/admin-automation.git
cd admin-automation
git switch -c feature/작업이름
```
