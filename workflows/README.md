# workflows

자동화 본체를 도구별로 보관합니다. 한 업무에 여러 도구를 섞어 써도 되며, 이 경우 설계서에 연결 구조를 적습니다.

## 도구 선택 기준

| 상황 | 추천 |
| --- | --- |
| 여러 서비스(메일, 시트, 캘린더, Notion)를 연결 | n8n |
| Google 문서·시트·폼 안에서 끝나는 작업 | Google Apps Script |
| 저장소 이벤트(push, PR, 일정)에 반응 | GitHub Actions |
| 파일 가공, 데이터 처리, 복잡한 로직 | Python 등 스크립트 |

## 폴더

| 폴더 | 내용 |
| --- | --- |
| `n8n/` | n8n에서 Export한 워크플로 JSON |
| `github-actions/` | Actions 예시와 템플릿 (실제 동작 파일은 `.github/workflows/`) |
| `google-apps-script/` | Apps Script 코드 |
| `scripts/` | 독립 실행 스크립트 |
| `_template/` | 새 워크플로 설계서 양식 |

## 워크플로 목록

| 이름 | 영역 | 도구 | 트리거 | 담당자 | 상태 |
| --- | --- | --- | --- | --- | --- |
| (아직 없음) | | | | | |

상태: 계획 → 개발 중 → 운영 중 → 중단
