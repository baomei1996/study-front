# study-front

## 사전 준비

1. node 설치
2. yarn 설치
3. nvm 설치 (Optional)
4. VSC Extensions
    - [ ] ESLint
    - [ ] Prettier
    - [ ] ES7+ React/Redux/React-Native snippets
    - [ ] Multiple cursor case preserve (Optional)
    - [ ] Code Spell Checker (Optional)
    - [ ] Auto Rename Tag (Optional)
    - [ ] TODO Highlight (Optional)
    - [ ] Material Icon Theme (Optional)
    - [ ] Dracula Official (Optional)

## Chepter1:

-   https://joshua1988.github.io/webpack-guide/
-   Node란?
    -   Node.js는 브라우저 밖에서도 자바스크립트를 실행할 수 있는 환경을 의미합니다. Node.js가 나오기 전까지는 자바스크립트가 브라우저의 동작을 제어하는데 사용되었고 브라우저에서만 실행할 수 있었지만 이제는 Node.js로 자바스크립트를 브라우저 밖에서도 실행할 수 있게 되었습니다.
    -   node 실행
-   Npm / yarn (feat: nvm)
    -   NPM(Node Package Manager)는 명령어로 자바스크립트 라이브러리를 설치하고 관리할 수 있는 패키지 매니저입니다. NPM 공식 사이트에서도 안내가 되어 있지만 전 세계 자바스크립트 개발자들이 모두 자바스크립트 라이브러리를 공개된 저장소에 올려놓고 npm 명령어로 편하게 다운로드 받을 수 있습니다.
    -   전역 설치, 지역 설치 (개발용, 배포용) 옵션

```
1. **성능**: yarn은 npm보다 설치 속도가 빠른 것으로 알려져 있습니다. 이는 yarn이 병렬로 패키지를 설치하기 때문입니다. 반면 npm은 패키지를 순차적으로 설치합니다.

2. **보안**: yarn은 설치 시 자동으로 패키지의 checksum을 생성하여 패키지의 무결성을 보장합니다. npm도 이제 checksum을 제공하지만, yarn이 처음 도입한 기능입니다.

3. **lock 파일**: 두 패키지 매니저 모두 lock 파일을 사용하여 의존성을 정확히 관리합니다. 하지만 yarn은 yarn.lock 파일을, npm은 package-lock.json 파일을 사용합니다.

4. **작업 모드**: yarn은 'workspaces'라는 기능을 통해 모노레포를 쉽게 관리할 수 있습니다. 이는 여러 개의 패키지가 하나의 저장소 안에 있는 프로젝트를 관리하는데 유용합니다. npm도 'workspaces' 기능을 제공하지만, yarn이 먼저 도입한 기능입니다.

5. **CLI 명령어**: 두 도구의 CLI 명령어에는 약간의 차이가 있습니다. 예를 들어, 패키지를 제거할 때 npm은 'npm uninstall [패키지명]', yarn은 'yarn remove [패키지명]'을 사용합니다.
```

-   package.json
    -   NPM 패키지 관리 파일
-   실습 1: npm init
-   실습 2: npm install package with option
-   실습 3: 스크립트 작성

## Chepter2: React

-   무엇이고, 왜 쓰는가?
-   실습1: CRA로 리액트 프로제트 시작하기
-   폴더 구조 설명 / 구동 원리
-   hooks
-   component간 props전달
-   실습2: counter 만들기
-   전역 상태관리 Feat: MobX - 회사 비지니스 로직
-   실습3: userList api를 요청하여 받아와서 화면에 리스트 형식으로 표시하자
-   typescript / eslint / prettier config

## Chepter3: 추천해요!

-   typescript: https://typescript-exercises.github.io/#exercise=1&file=%2Fnode_modules%2Ftype-assertions%2Findex.ts
-   css: https://cssbattle.dev/
-   can i use: https://caniuse.com/
-   flexboxfroggy.com
