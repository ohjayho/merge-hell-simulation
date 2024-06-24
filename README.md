# Merge 지옥 시뮬레이션 Merge Hell Simulation

이 연습은 3명이 한 팀이 되어 하나의 깃헙 리포에서 작업합니다.
우리의 목표는 모든 lorem ipsum ( 더미 텍스트 )를 source.txt의 내용으로 바꾸는 것입니다.
아래 안내사항에 따라 수정을 하고, Merge 지옥을 직접 경험해 봅시다!

### 시작하기

1. 한 명의 멤버가 이 리포를 포크 합니다.
1. 나머지 두 멤버는 이 프로젝트의 collaborator로 등록 요청합니다.

### 파트 1: 팀원 간 Merge 지옥

- 파트 1에서는 directory_1 경로 안에서만 작업합니다.
- 각 파일의 각 문단에 있는 모든 더미 문장을 source.txt에서 명언으로 무작위로 대체합니다. 순서 또한 무작위로 바꾸고 **각 문단을 수정할 때 마다** 커밋합니다.
- 모든 문단을 수정할 때까지 계속합니다.
- file2.txt에서 같은 작업을 반복합니다.
- file3.txt 또한 같은 작업을 합니다.
- 마지막으로 git push
- push를 먼저 한 사람이 이깁니다!
- 나머지 멤버들은 `git pull --rebase` 커맨드를 통해 merge 충돌을 해결하고, `git add`와 `git rebase --continue`를 통해 마무리합니다.

### Part 2: 브랜치 간 Merge 지옥

1. 파트 2에서는 directory_2 경로 안에서만 작업합니다.
1. 시작하기 위해, 로컬 브랜치를 생성합니다. `git checkout -b feature/<your-name>`
1. 각 파일의 각 문단에 있는 모든 더미 문장을 source.txt에서 명언을 무작위로 골라 대체합니다. 순서 또한 무작위로 바꾸고 **각 문단을 수정할 때 마다** 커밋합니다.
1. feature 브랜치에서 모든 커밋을 한 다음에, master 브랜치로 이동합니다. `git checkout master`
1. `git merge feature/<your-name>` 커맨드를 통해 feature 브랜치를 로컬 master 브랜치에 머지합니다.
1. remote 마스터 브랜치에 푸시합니다. `git push`.

만약 누군가가 이미 remote 마스터 브랜치에 푸시 했다면, git push 오류가 발생합니다. 이 경우에는:

1. pull을 하고, `git pull`.
1. merge 충돌을 해결한 후 git add 합니다. `git add .`
1. `git commit`으로 merge commit을 생성하고, merge를 마칩니다.
1. 변경사항을 remote 마스터 브랜치에 푸시 합니다. `git push`

### 파트3

- 마스터 브랜치에서 긴급 기능 추가를 해야 하는 상황입니다. 우리는 프로그래밍 명언에서 동기부여 명언으로 주제를 바꾸려 합니다. 
- 우리가 해야할 것:
  - master 브랜치로 이동 `git checkout master`
  - file_1을 다음과 같이 업데이트:

```
<directory_2/file_1.txt title>

The best revenge is massive success. –Frank Sinatra

People often say that motivation doesn’t last. Well, neither does bathing.  That’s why we recommend it daily. –Zig Ziglar

Life shrinks or expands in proportion to one's courage. –Anais Nin
```

- git add와 git commit을 합니다.
- `git push`
- 휴, 가까스로 제시간에 긴급 수정을 완료했습니다.
