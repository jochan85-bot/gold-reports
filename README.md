# 🪙 Gold Signal Reports

국제금(XAU/USD) 시그널 리포트를 매일 자동 갱신합니다.

- **라이브 사이트**: https://jochan85-bot.github.io/gold-reports/
- **시그널 엔진**: `gold_signal_v2` (rGold + RSI 다이버전스, COT/ETF 제거)

## 신호 체계 (v3)

| 신호 | 조건 | 액션 |
|---|---|---|
| 🟢 강력매수 | 강세 다이버전스 & rGold ≤ -7% | 사이징↑ |
| 🟩 분할매수 | 강세 다이버전스 & rGold ≤ -3% | 3회 분할 진입 |
| 👀 눌림 관찰 | rGold ≤ -3% (다이버전스 대기) | 관망 |
| 🟠 froth 경보 | rGold ≥ +30% 또는 (약세div & +18%) | 신규 투입 중단 |
| 🔴 BLOWOFF | rGold ≥ +35% | 전량 청산 검토 |

## 데이터

- `data/history.json` — 최근 라이브 스냅샷 (매일 자동 append)
- `data/v3_signal.json` — 전체 백테스트 히스토리 (2010~)

## 참고

- 가격 기준: XAU/USD (yfinance `GC=F`)
- MA 기준선: 200일 (50/90/120 테스트 후 200 최적 확인)
- 다이버전스 창: 40일
