# orot-ai 공통 이슈·PR 템플릿

이 저장소의 템플릿은 orot-ai의 모든 저장소에 기본으로 적용됩니다. 저장소 안에 `.github` 템플릿이 따로 없으면 이것이 쓰입니다.

- 이슈 3종: Bug(고장 신고), Story(새 기능이나 흐름), Task(작은 일 하나)
- PR: 요청 사항(Closes #), 바꾼 것, 확인한 방법, 화면 전후
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
