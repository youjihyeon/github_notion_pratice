## labnote 만들기

[기본적인 Markdown 노트작성 메뉴얼](https://quarto.org/docs/authoring/markdown-basics.html)

### Step 1. Visual Studio Code(VSCode) 다운로드

[Visual Studio Code의 공식 웹사이트](https://code.visualstudio.com/)

-   위 링크로 들어가서 현재 운영 체제에 해당하는 '다운로드'버튼을 클릭합니다.
-   다운로드가 완료되면 설치 파일을 실행합니다.
-    설치 마법사가 시작되면, 기본적으로 제안되는 옵션을 사용하여 설치를 진행합니다. 필요한 경우 사용자 지정 설치 옵션을 선택할 수 있습니다.

### Step 2. 

## Git의 버전 관리 과정 및 협업

### Git 저장소의 구조 및 기본 작업 흐름

![참조: velog.io/\@lillynextdoor/GIt의_기본-동작-원리](images/git%20construct.png)

```         
-   위 그림은 기본적으로 github가 어떻게 저장 및 공유를 하는지를 표현한 것입니다. 'Working Directory'는 우리가 작업하는 공간(예를 들어 .md file)을 말합니다. 그리고 'Staging Area'는 Git으로 올라가기전 파일들의 저장공간입니다. 우리는 'git add .' 명령어를 통해 파일들을 commit할 준비합니다.
-   'staging area'에서 'local repository'로 'commit'함으로 변경내용이 기록됩니다. 이는 '버전관리 및 파일 추적'을 가능케 합니다. 모든 변경내용들은 'history'에서 확인할 수 있습니다.
-   원격저장소(remote repository)는 github에 저장되어 있는 온라인 저장소 개념이며, 반대로 로컬저장소(local repository)는 본인 컴퓨터의 저장소를 말합니다.
-   원격저장소(remote repository)는 팀원 모두가 공유하고 있습니다. 팀원 누군가 함부로 저장소의 내용을 변경할 수도 있기에 이를 방지할 수 있어야 합니다. 그래서 로컬저장소(local repository)가 도입되었습니다.
-   저장소(repository)는 'branch'로 구성되어 있습니다. main branch는 remote repository에 저장되어 있고, 팀원들은 'main repository'의 내용(파일)을 자신의 컴퓨터 local repository로 'git clone'으로 불러옵니다. 개인이 local repository에서 수정 작업을 하면 '개인의 branch' 형태로 저장이 됩니다. 이 과정이 'git add'와 'git commit'입니다.
-   local repository에서 remote repository로 변경내용을 upload하는 작업이 필요할 것입니다. 'git push'를 이용하여 '개인의 branch'를 remote repository로 옮긴다. 그럼 github에서 remote repository에 원래 있었던 main branch와 push된 '개인의 branch'를 확인할 수 있습니다.
-   두 branch를 합치는 과정이 merge입니다. merge를 하면, local에서 생성했던 branch는 사라지고 main branch만 변경된 내용을 포함해서 남게됩니다.
```

