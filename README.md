# 처음시작!!
1. 
npx create-next-app --typescript 이름

2. 
yarn add -D eslint 
               prettier 
               eslint-plugin-prettier 
               eslint-config-prettier 
               eslint-plugin-import 
               eslint-plugin-react 
               eslint-plugin-react-hooks 
               @typescript-eslint/parser 
               @typescript-eslint/eslint-plugin

3. eslintrc 

    {
      "extends": ["react-app", "prettier/prettier"],
      "plugins": ["react-hooks", "simple-import-sort", "prettier"],
      "rules": {
        "prettier/prettier": "error",
        "react-hooks/rules-of-hooks": "error",
        "simple-import-sort/imports": "error",
        "simple-import-sort/exports": "error",
        "no-multiple-empty-lines": ["error", { "max": 1, "maxEOF": 0 }],
        "comma-dangle": ["error", "always-multiline"],
        "object-curly-spacing": ["error", "always"],
        "space-in-parens": ["error", "never"],
        "computed-property-spacing": ["error", "never"],
        "comma-spacing": ["error", { "before": false, "after": true }],
        "eol-last": ["error", "always"],
        "quotes": ["error", "single"],
        "no-tabs": "error",
        "semi": ["error", "never"],
        "import/no-anonymous-default-export": 0,
        "object-shorthand": "error",
        "padding-line-between-statements": [
          "error",
          { "blankLine": "always", "prev": "*", "next": "return" }
        ],
        "@typescript-eslint/no-redeclare": 0
      }
    }


4. prettierrc.json

{
      "printWidth": 80,
      "semi": true,
      "singleQuote": true,
      "trailingComma": "all",
      "tabWidth": 2,
      "bracketSpacing": true,
      "endOfLine": "auto",
      "useTabs": false
    }


5. 스타일드 컴터넌트 적용

// 기본 styled-components
yarn add styled-components @types/styled-components

// 문자열 안에 스타일 들어가는 것 처리를 위한 설치
yarn add -dev babel-plugin-styled-components

//전역 스타일링에서 이용하기 위함 
yarn add styled-reset 



1. .babelrc 파일을 package.json과 같은 위치에 만들기
npm i babel-plugin-styled-components

{
  "presets": ["next/babel"],
  "plugins": [
    [
      "babel-plugin-styled-components", {
        "ssr":true,
        "displayName": true // 개발모드일때 브라우저에서 styled components의 클래스 이름을 쉽게 확인 할 수 있게 함
      }
    ]
  ]
}

2. _document 에 추가 설정하기

3. global-styles.ts 추가 !! 
