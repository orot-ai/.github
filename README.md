# orot-ai 공통 이슈·PR 템플릿

이 저장소의 템플릿은 orot-ai의 모든 저장소에 기본으로 적용됩니다. 저장소 안에 `.github` 템플릿이 따로 없으면 이것이 쓰입니다.

- 이슈 3종: Bug(고장 신고), Story(새 기능이나 흐름), Task(작은 일 하나). 칸: 요청 원문, 완료 조건, 맡을 담당·모델·이유, 화면
- PR: 요청 사항(Closes #), 바꾼 것, 확인 결과(이슈 완료 조건마다), 화면 전후
- PR 본문 점검(`workflow-templates/pr-links-issue.yml`): PR 본문에 `Closes #N`·`Refs #N`(다른 저장소면 `orot-ai/<저장소>#N`)이 없으면 실패합니다. 이 파일이 정본이고, 각 저장소의 `.github/workflows/pr-links-issue.yml`은 베이온 `900_system/integrations/gh-issue/issue.py workflow --all`이 같게 맞춥니다.
- 시크릿 소비 확인(`workflow-templates/secret-consumers.yml`): PR이 시크릿 폴더(`900_system/secrets`·`.claude/secrets`)·`.env`·셸 시작 파일·토큰 로더를 건드리면, 본문에 건드린 이름마다 `소비 확인 <이름>: <그걸 쓰는 작업> exit=0`(또는 `HTTP 200`) 줄이 있어야 통과합니다. 값은 적지 않습니다. 설치·갱신은 위와 같습니다.
- 화면 전후 캡처 붙이는 법: 그 저장소의 `pr-assets` 브랜치에 `<이슈번호>/<파일>.png`로 올리고, PR 본문에 `<img src="https://github.com/orot-ai/<저장소>/blob/pr-assets/<이슈번호>/<파일>.png?raw=true" width="260">`을 넣습니다. 캡처에는 모의 데이터만 씁니다.

## 라벨

모든 저장소에 같은 라벨을 둡니다.

| 라벨 | 뜻 |
|---|---|
| `type:bug` · `type:story` · `type:task` | 이슈 종류. 제목 앞 `[Bug]`·`[Story]`·`[Task]`와 짝 |
| `status:todo` · `status:in-progress` · `status:review` | 시작 전 · 맡아서 하는 중 · PR 올림 |
| `owner:cloud` · `owner:local` | 클라우드 세션이 할 일 · 로컬 Mac이 있어야 하는 일 |
| `owner:miri` | 대표의 답변·결정이 필요한 일 |

정본은 이 저장소 하나입니다. 저장소마다 복사하지 않습니다.
