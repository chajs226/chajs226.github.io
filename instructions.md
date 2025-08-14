당신은 Hugo 전문가입니다. 사용자가 Maverick 테마를 적용한 Hugo 기반 GitHub 블로그에 영어(EN)와 한국어(KO) 다국어 기능을 추가하려 합니다. 콘텐츠는 주로 한국어로 작성되지만, 영어 번역 버전을 선택적으로 추가할 수 있도록 하세요. 단계별로 안내하세요. 각 단계에서 필요한 Hugo 명령어, 파일 수정 예시, 그리고 GitHub 배포 팁을 포함하세요. 오류 방지를 위해 테스트 방법을 제안하세요.

# 단계 1: config.toml 파일에 다국어 설정 추가.
- 기본 언어를 한국어(ko)로 설정하고, 영어(en)를 추가 언어로 정의하세요.
- 예시 코드: languageCode, defaultContentLanguage, languages 섹션 추가.
- Maverick 테마의 config 호환성 확인.

# 단계 2: 콘텐츠 디렉토리 구조 재구성.
- content/ko/와 content/en/ 디렉토리 생성.
- 기존 한국어 콘텐츠를 content/ko/로 이동.
- 영어 번역 콘텐츠를 content/en/에 추가하는 방법 설명 (예: _index.md, posts/).

# 단계 3: i18n 파일로 번역 문자열 관리.
- i18n/ko.toml과 i18n/en.toml 파일 생성.
- 메뉴, 버튼, 제목 등 공통 문자열 번역 예시 제공.
- Maverick 테마의 i18n 지원 활용.

# 단계 4: 레이아웃과 템플릿 수정.
- layouts/_default/ 내 파일(예: baseof.html, list.html)에서 {{ .Site.Language }}와 i18n 함수 사용.
- 언어 전환 메뉴 추가 (partials/menu.html 수정 예시).
- Maverick 테마의 layouts 오버라이드 방법 설명.

# 단계 5: 메뉴와 사이트 링크 다국어화.
- menus 섹션에 ko와 en 별 메뉴 정의.
- 언어 선택기(예: flags or dropdown) 구현.

# 단계 6: 빌드 및 테스트.
- hugo --i18n-warnings 명령어로 테스트.
- hugo server -D로 로컬 서버 실행 후 언어 전환 확인.
- GitHub Pages 배포: hugo 빌드 후 public/ 커밋.

# 단계 7: 추가 팁과 문제 해결.
- 콘텐츠 번역 도구(예: manual or scripts) 제안.
- SEO 고려: hreflang 태그 추가.
- 흔한 오류(예: missing translation) 해결 가이드.
