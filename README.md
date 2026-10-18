# 이희승 백엔드 개발자 포트폴리오

백엔드 개발자 이희승의 기술 포트폴리오입니다. 동시성 제어, 데이터 정합성, 장애 격리, 재실행 가능한 작업 흐름을 프로젝트 사례와 구조도로 정리했습니다.

## 공개 주소

- Portfolio: https://boclair98.github.io/heeseung-backend-portfolio/
- Resume: https://boclair98.github.io/heeseung-backend-portfolio/resume.html

## 구성

- 핵심 역량과 기술 스택
- 실무 경험
- 대표 프로젝트 3개와 추가 프로젝트 4개
- 프로젝트별 아키텍처 및 트러블슈팅
- 해수 담수화 수상 프로젝트
- 자격증과 교육 이력

## 배포

`main` 브랜치에 변경 사항이 반영되면 GitHub Actions가 정적 파일을 GitHub Pages에 배포합니다.

## 홈페이지 디자인과 로컬 확인

OpenUI 계획은 `design.md`에 있습니다. 첫 화면은 프로젝트와 이력서를 바로 읽을 수 있는
타이포그래피 중심 구성으로 정리했습니다. 기존 프로젝트 상세, 기술 필터와 이력서는 유지합니다.

별도 빌드나 환경 변수 없이 Python 3로 실행합니다.

```bash
python -m http.server 4173 --bind 127.0.0.1
```

브라우저에서 `http://127.0.0.1:4173`을 엽니다. 1440×900, 768×1024,
390×844, 360×800에서 화면과 가로 넘침을 확인했습니다. 키보드로 프로젝트 이동,
기술 필터, 상세 열기·Escape 닫기·포커스 복귀와 이력서 링크를 확인했습니다.

UI 작업은 `AGENTS.md`의 공통 지침과 `.agents/skills/openui/SKILL.md`를 따릅니다.

## 개인정보

공개 웹 버전에는 이메일과 GitHub 프로필만 표시하며 전화번호와 이력서 PDF는 포함하지 않습니다.
