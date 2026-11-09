<div align="center">

# 이준영 · Junyoung Lee

**문서·데이터에 근거해 답하는 AI 서비스를 만듭니다.**<br>
RAG 검색 · 권한 필터 · 검색 품질 평가 · 데이터 분석 에이전트

[![Email](https://img.shields.io/badge/Email-wljycjdi2001@naver.com-03C75A?style=flat-square&logo=naver&logoColor=white)](mailto:wljycjdi2001@naver.com)

</div>

---

## 🙋 소개

- 현대 부트캠프 **AI서비스개발과정** 교육 중 — 7인 팀 프로젝트에서 **검색 모듈**을 맡았습니다.
- "그럴듯한 답"보다 **근거가 있는 답**을 중요하게 생각합니다. 검색 결과는 권한을 DB로 다시 확인하고, 품질은 정답셋과 지표(Hit@k, MRR)로 측정합니다.
- 확인되지 않은 기능·수치는 README에 쓰지 않습니다. 아래 숫자는 모두 테스트 결과서 기준입니다.

## 📌 대표 프로젝트

### 1. 현답(Hyundap) — 다중 기업 AI 문서 검색 플랫폼 · `팀 7명` · 2026.10
> 회사 문서를 자연어로 묻고, 문서 근거와 함께 답·요약을 받는 사내 검색 서비스

**내 역할: 검색 모듈 `hyundap/search/`** — 질문한 사람이 볼 수 있는 문서만 골라 순위대로 반환
- **보안:** 허용 회사 범위로 먼저 거르고, 벡터 검색 결과를 DB 기준 8가지 조건(공개·삭제·현재 버전 등)으로 재검증 → 다른 회사 문서·옛 버전 노출 차단
- **문제 해결:** 문서 코드가 든 질문에서 정답이 6위로 밀리던 문제를, 코드로 검색 범위를 좁혀 해결 ([PR #224](https://github.com/paul8004-lee/Hyundap/pull/224))
- **품질 측정:** 정답셋 74건 + Hit@3·MRR·회사 간 누출 건수 평가 도구 ([PR #260](https://github.com/paul8004-lee/Hyundap/pull/260))
- **결과:** 팀 최종 테스트 검색 정확도 Hit@3 **8/10**, 권한 테스트 9개 중 8개 통과

`Python` `Gradio` `OpenAI Embedding` `Chroma` `MySQL` `LangChain`
→ [저장소](https://github.com/wljycjdi2001-ljy/Hyundap) · [포트폴리오 상세](https://github.com/wljycjdi2001-ljy/Hyundap/blob/develop/PORTFOLIO_이준영.md)

### 2. 탐나워치(TamnaWatch) — 제주 지역화폐 데이터 분석 AI 에이전트 · `팀 프로젝트` · 2026.11
> 「제주 AI·빅데이터 활용 AI Agent 개발 챌린지」 출품작

- 탐나는전·카드 결제 CSV를 올리면 현황 보고서·이상 급증 구역·예산 소진일을 계산하고 Word 보고서로 출력
- **AI 에이전트(Gemini):** 대표 질문 8개 도구 선택 8/8, 답변 속 숫자를 계산 결과와 자동 대조
- **반출 기준 자동 준수:** 10 미만 칸 가림, 외부 AI에는 비율·순위만 전송, 읽기 전용 SQL 잠금
- 자동 테스트 92개

`Python` `Streamlit` `DuckDB` `pandas` `Plotly` `Gemini`
→ 🔒 대회 심사 중 비공개 (종료 후 공개 예정)

### 3. 소득세법 RAG 챗봇 워크북 · `스터디 6명` · 2026.10
- 소득세법 PDF를 조문 단위로 분할해 RAG 베이스라인 → 계산봇/법령봇/상담봇 3종으로 확장
- 기능 브랜치 + PR 리뷰로 협업 (PR 15건)

`LangChain` `LangGraph` `FAISS` `OpenAI`
→ [저장소](https://github.com/wljycjdi2001-ljy/multi_rag_chabot_workbook)

## 🛠 기술 스택

| 분야 | 기술 |
| --- | --- |
| Language | Python |
| AI / RAG | OpenAI API, Gemini API, LangChain, LangGraph, Chroma, FAISS |
| Data | pandas, DuckDB, MySQL, Plotly, matplotlib |
| App | Gradio, Streamlit |
| Test / 협업 | pytest, unittest, Git, GitHub (Issue · PR · Code Review) |
