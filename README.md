# admin-automation

행정 업무 자동화를 위한 저장소입니다. n8n 워크플로와 업무 매뉴얼을 버전 관리합니다.

## 구성

| 폴더 | 내용 |
| --- | --- |
| `workflows/` | n8n 워크플로 JSON (n8n에서 Export한 파일) |
| `docs/` | 행정 업무 매뉴얼, 사용 가이드 |

## 사용 규칙

1. `main`에 직접 수정하지 않고 브랜치를 만들어 작업합니다.
2. 변경은 Pull Request로 검토 후 병합합니다.
3. 비밀번호, API 키, 개인정보는 절대 올리지 않습니다. (`.gitignore` 참고)
4. n8n 워크플로를 Export할 때 Credentials 값이 포함되지 않았는지 확인합니다.

## 작업 시작 전

```bash
git pull
git switch -c feature/작업이름
```
