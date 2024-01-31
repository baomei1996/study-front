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
    -   node hello.js
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
-   create react app 폴더 구조 설명
-   component간 props전달
-   react hooks (useState, useEffect)
    - 실습1: Counter component
    - 실습2: Timer component
-   typescript / eslint / prettier config
    - React 프로젝트 포맷팅을 통한 자동 코드 스타일 포맷팅 & 코드 품질 관리
    - Prettier는 코드 포매팅 도구입니다. Prettier를 사용하면 코드를 일관된 스타일로 자동 정렬해주기 때문에, 개발자가 코드 스타일에 대해 신경 쓰지 않고 로직에 집중할 수 있습니다.
    - ESLint는 코드 품질을 체크하는 린팅 도구입니다. ESLint를 사용하면 문법 오류, 버그의 원인이 될 수 있는 코드 패턴, 코드 스타일 등을 체크할 수 있습니다.
    - prettier 설정 방법
      ```
      // prettier 설치
      yarn add -D prettier
      ```

      ```
      // prettier config
      // https://prettier.io/docs/en/options.html
      module.exports = {
            singleQuote: true, // 문자열을 작성할 때 작은따옴표('')를 사용합니다.
      semi: true, // 문장의 끝에 세미콜론(;)을 사용합니다.
      useTabs: false, // 들여쓰기에 탭 대신 공백을 사용합니다.
      tabWidth: 4, // 한 탭의 너비를 2개의 공백으로 설정합니다.
      trailingComma: "all", // 객체나 배열, 함수 파라미터 등에서 마지막 항목 뒤에 항상 콤마(,)를 붙입니다.
      printWidth: 80, // 한 줄의 최대 너비를 80자로 제한합니다.
      }
      ```

      ```
      // prettier 포맷팅 스크립트 추가
       "format": "prettier --write \"src/**/*.{ts,tsx}\""
      ```

      ```
      // eslint 설정 시 필요 라이브러리 설치
      eslint eslint-config-prettier eslint-plugin-prettier eslint-plugin-react @typescript-eslint/eslint-plugin @typescript-eslint/parser

        // eslint: JavaScript 코드를 분석해 문제점을 찾고 고치는 린팅(linting) 도구입니다.
        // prettier: 코드 포매팅을 자동으로 해주는 도구입니다.
        // typescript: JavaScript에 타입을 추가한 언어로, 적절한 타입 체크를 통해 버그를 사전에 방지할 수 있습니다.
        // eslint-config-prettier: Prettier와 ESLint가 충돌하지 않도록 ESLint 규칙을 재정의하는 패키지입니다.
        // eslint-plugin-prettier: Prettier를 ESLint에서 실행할 수 있게 해주는 플러그인입니다.
        // eslint-plugin-react: React에 특화된 ESLint 규칙을 제공하는 플러그인입니다.
        // @typescript-eslint/eslint-plugin: TypeScript에 특화된 ESLint 규칙을 제공하는 플러그인입니다.
        // @typescript-eslint/parser: ESLint가 TypeScript 코드를 파싱할 수 있게 해주는 파서입니다.
     ```

      ```
      module.exports = {
          parser: '@typescript-eslint/parser', // ESLint가 TypeScript 코드를 파싱하기 위해 사용하는 파서를 설정합니다.
          extends: [
            'plugin:react/recommended', // React에 대한 추천 ESLint 규칙을 적용합니다.
            'plugin:@typescript-eslint/recommended', // TypeScript에 대한 추천 ESLint 규칙을 적용합니다.
            'prettier/@typescript-eslint', // Prettier와 TypeScript ESLint 규칙이 충돌하지 않도록 설정합니다.
            'plugin:prettier/recommended', // Prettier 규칙을 적용하고, Prettier를 ESLint의 플러그인으로 설정합니다.
          ],
          rules: {
            // 여기에 추가적인 ESLint 규칙을 설정할 수 있습니다.
            // https://eslint.org/docs/latest/rules/
          },
        };
      ```

## Chepter3: 추천해요!
-   typescript: https://typescript-exercises.github.io/#exercise=1&file=%2Fnode_modules%2Ftype-assertions%2Findex.ts
-   css: https://cssbattle.dev/
-   can i use: https://caniuse.com/
-   flexboxfroggy.com
