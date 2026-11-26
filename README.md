# site-seo-geo-audit

웹사이트의 SEO·GEO·E-E-A-T를 점검하고, 클라이언트가 직접 수정할 수 있는 작업 가이드를 만드는 Claude 스킬입니다.

## 하는 일

**A. 점검 (읽기 전용)**
1. 사이트 직접 분석: 메타·canonical·hreflang·구조화 데이터·사이트맵·옛 주소 리디렉션·분석 코드
2. PageSpeed Insights (모바일)
3. 구글 서치콘솔: 실적, 색인 미생성 사유
4. 빙 웹마스터 도구: 권장 사항, AI(코파일럿) 인용
5. GA4: 유입 경로, 주요 이벤트, 동의 설정, 서치콘솔 클릭과 교차 검증
6. 구글 비즈니스 프로필: 조회수 대비 웹사이트 클릭, 빈 항목
7. 사실 일치 점검 (이름·주소·전화·개업 연도 등)
8. 점검 보고서 작성

**B. 작업 가이드**
- 플랫폼별 수정 경로 (카페24 / 워드프레스 / Cloudflare + GitHub 등)
- 매 대화 첫 메시지로 쓰는 공통 시작 프롬프트, 코드 작업용 시작 프롬프트
- 단계별 프롬프트 (읽기 → 변경 → 확인 → 통과 기준)
- 최종 확인 체크리스트, 문제가 생겼을 때 대처법, 작업 일지 양식

## 필요한 것

- Claude (claude.ai) + 크롬 확장 프로그램 Claude in Chrome
- 같은 크롬에서 로그인된 계정: 구글(서치콘솔·GA4·비즈니스 프로필), 빙 웹마스터 도구
- 보고서·가이드를 문서로 만들 수 있는 환경 (Claude Docs 등)

## 사용 예

```
https://example.com
이 사이트를 SEO, GEO 관점에서 점검하고 E-E-A-T 방해 요소도 찾아줘.
크롬에 서치콘솔, 빙 웹마스터, GA4, 비즈니스 프로필, PageSpeed를 열어 두었어.
```

점검 보고서의 '확인이 필요한 사항'에 답한 뒤:

```
클라이언트가 클로드 웹으로 직접 수정할 수 있게 작업 가이드를 만들어줘.
```

## 설치

1. [site-seo-geo-audit.zip](https://github.com/seon-biz/site-seo-geo-audit/raw/main/site-seo-geo-audit.zip)을 내려받습니다. 압축은 풀지 않습니다.
2. Claude(claude.ai)에서 **Customize > Skills** → **+** → **Create skill** → **Upload a skill**을 누르고 ZIP을 올립니다.
3. 무료·Pro·Max 요금제는 먼저 **Settings > Capabilities**에서 **Code execution and file creation**(새 화면에서는 Create and edit files)을 켜 둡니다.

저장소의 "Download ZIP"은 폴더 이름이 바뀌어 스킬로 인식되지 않을 수 있으니, 위 ZIP을 사용하세요.
