# 🚀 GitLog (깃로그)
> **GitHub 코드를 보고도 복습 정리를 미루는 문제 해결**  
> 개발자가 커밋 URL만 입력하면 웹 대시보드(좌측 코드 뷰어 + 우측 AI 사이드바)에서 공부 복습 노트와 기술 블로그 글을 자동 생성하고 관리하는 Spring Boot + React 웹 서비스입니다.

---

## 📌 1. 프로젝트 개요 (Project Overview)
- **프로젝트명:** GitLog (깃로그)
- **주요 기술 스택:**
  - **Front-End:** React, Tailwind CSS, react-markdown
  - **Back-End:** Java 17, Spring Boot 3.x, Spring Data JPA, MySQL
  - **AI Integration:** Google Gemini API (Free Tier)
  - **External API:** GitHub REST API

---

## 💡 2. 해결하고자 하는 문제 (Problem & Solution)
* **Problem:** 개발자 및 대학생들이 GitHub에 코드를 올리고 커밋을 남기지만, 구현한 코드의 동작 원리나 학습 내용을 복습하고 기록(블로그/노트)하는 데 많은 시간과 번거로움이 발생합니다.
* **Solution:** GitLog 웹 서비스에서 복습하고 싶은 GitHub Commit/PR URL을 입력하면, 좌측 코드 뷰어로 변경점을 확인하는 동시에 우측 **AI 사이드바 에디터**에서 **'공부 복습 노트'** 또는 **'기술 블로그 마크다운'**을 원클릭으로 생성해 편집 및 저장할 수 있습니다.

---

## ✨ 3. 핵심 기능 (Key Features)
1. **GitHub URL 기반 코드 Diff & Context 파싱:** GitHub URL 입력만으로 백엔드에서 해당 커밋의 Diff 데이터를 수집하여 웹 화면 좌측에 코드 뷰어로 시각화합니다.
2. **AI 기반 양식 맞춤형 Markdown 생성:** Gemini API를 연동하여 `공부 복습 노트` 및 `기술 블로그` 형태의 구조화된 마크다운 본문을 실시간 생성합니다.
3. **우측 고정(Fixed) 사이드바 라이브 마크다운 에디터:** 좌측 코드를 참고하며 우측 사이드바에서 마크다운을 직접 수정하고 `.md` 파일로 다운로드할 수 있습니다.
4. **개인 복습 노트 이력 관리 (CRUD):** 작성 완료된 노트를 Spring Boot DB에 저장하고 마이페이지에서 조회, 수정, 삭제할 수 있습니다.

---

## 🗺️ 4. 로드맵 (Roadmap)
- [x] **Phase 1:** Standalone Web App 개발 (좌측 코드 뷰어 + 우측 AI 사이드바 대시보드)
- [ ] **Phase 2:** 동일한 Backend API를 활용한 Chrome Extension (Manifest v3 Side Panel API) 연동 및 확장
