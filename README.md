# Ongil.cloud — 사이트 프로토타입

온길 인터내셔널(Ongil International) COEX 데모 준비를 위한 정적 사이트 구조입니다.
빌드 도구 없이 순수 HTML/CSS로 작성되어 Vercel 등 정적 호스팅에 그대로 배포할 수 있습니다.

## 구조

```
index.html              메인 랜딩 ("Here" 페이지) — 문제/해결/워크플로우/로드맵/파트너 로고월
onboarding.html          파트너 온보딩 4단계 템플릿 + 새움 실사례
brands/
  saeum.html             (주)새움·삼시먹거리 개별 브랜드 홈페이지 (실사례)
  [partner-slug].html    신규 파트너 추가 시 saeum.html을 복제해 데이터만 교체
docs/
  2026-08-analysis-report.html   자료 7종 종합 분석 + 8~9월 실행 타임라인 보고서
```

## 파트너 추가 방법 (현재는 수동, 추후 세움 AI로 자동화 예정)

1. `brands/saeum.html`을 복제해 `brands/{새 파트너 slug}.html` 생성
2. `card-top`/`brand-id` 영역의 로고 이니셜·브랜드명·주소·담당자 정보 교체
3. `product-grid`의 제품 카드 2~3개를 신규 파트너의 대표 제품으로 교체
4. `index.html`의 파트너 로고월(`#partners`)과 `onboarding.html`의 예시 카드에 신규 파트너 링크 추가

## 디자인 시스템

- 팔레트: 오렌지(`--accent`) · 네이비(`--navy`) · 골드(`--gold`) — 온길·새움 브랜드 아이덴티티 문서(Phase 1 컬러 팔레트 3종)에서 도출
- 폰트: 시스템 산세리프(Apple SD Gothic Neo/맑은 고딕 등) — 외부 웹폰트 의존 없이 한글 렌더링 안정성 확보
- 다크모드: 모든 페이지가 OS 다크모드(`prefers-color-scheme`)를 자동 지원

## 알려진 제한사항

- 17개 HACCP 제품 전체 목록이 아직 제공되지 않아, 대표 제품은 확인된 2종(프리미엄 떡볶이·어묵탕)만 반영했고 3번째 슬롯은 "확정 예정"으로 표시했습니다.
- COEX 시연 일정이 자료 간 상이합니다(9/30 vs 11/4–7) — 자세한 내용은 `docs/2026-08-analysis-report.html` §06 참고.
- 실제 로고 파일이 없어 로고는 텍스트 이니셜 칩으로 대체했습니다.
