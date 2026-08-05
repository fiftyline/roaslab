# ROAS LAB — 매체별 성과 대시보드 (데모)

CRM 기준 실제 ROAS를 매체·캠페인·상품 단위로 분석하는 멀티채널 광고 성과 대시보드 프로토타입.
모든 수치는 **데모용 가짜 데이터**이며, 실제 서비스에서는 데이터 파이프라인 산출값으로 대체됩니다.

## 구성

| 파일 | 설명 |
|---|---|
| `index.html` | 진입점 → 대시보드로 리다이렉트 |
| `roas-lab-overview.html` | 대시보드 홈 (KPI · 도넛 · 콤보 · 매체별 성과표 · 드릴다운) |
| `analysis.html` | 광고 상세 분석 (KPI · 일/주/월 콤보 · 사용자 피벗 테이블 · CSV 다운로드) |
| `roas-data.json` | 대시보드용 집계 데이터(캠페인·일자 단위) |
| `roas-facts.json` | 상세 분석용 팩트 데이터(날짜×매체×캠페인×상품) |

## 실행

정적 파일이지만 `fetch`로 JSON을 읽으므로 **HTTP로 서빙**해야 합니다.

```bash
python -m http.server 8000
# → http://localhost:8000/
```

GitHub Pages로 배포 시 루트 URL이 자동으로 대시보드로 이동합니다.
