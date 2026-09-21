# chat_demo

치지직(CHZZK)·숲(SOOP) 라이브 채팅을 분석해 자체 스트리밍/후원 서비스용으로 재구성한 **라이브 채팅 프로토타입 & 기능 명세** 모음입니다.

## 구성

| 파일 | 설명 |
|------|------|
| [`chat-ui-prototype.html`](chat-ui-prototype.html) | **인터랙티브 채팅 UI 프로토타입.** 클린봇·후원·저속모드·모더레이션·공지 등록·채널 전환·채팅 팝업이 실제로 동작 |
| [`chzzk-chat-spec.html`](chzzk-chat-spec.html) | 치지직 라이브 채팅 기능 상세 요건 명세서 (SRS) |
| [`sooplive-chat-spec.html`](sooplive-chat-spec.html) | 숲(SOOP) 라이브 채팅 기능 상세 요건 명세서 (실측 기반) |
| [`chat-service-roadmap.html`](chat-service-roadmap.html) | 자체 채팅 서비스 기능 로드맵 (MVP → 확장) |

## 실행

별도 빌드 없이 각 HTML 파일을 브라우저에서 바로 열면 됩니다.

```bash
# 예: 로컬 서버로 열기
python -m http.server 8000
# http://localhost:8000/chat-ui-prototype.html
```

## 프로토타입 주요 기능

- **채널 전환** — 투네이션 · 치지직 · 유튜브 (플랫폼별 독립 채팅·공지·후원 재화)
- **클린봇** — 한국어 정규화(NFKC·자모 분해) + 사전 매칭 + 스팸/도배/광고 탐지 → 블라인드(개인 보기 토글)
- **후원** — 금액대별 4단계 색상 카드 (별풍선/치즈/슈퍼챗)
- **모더레이션** — 공지 등록·고정, 메시지 삭제/타임아웃, 채팅 얼리기, 등급 게이트
- **저속모드** — 전송 간격 카운트다운 (매니저 예외)
- **스크롤업 미리보기** — 위로 스크롤 시 최신 채팅을 하단 바로 실시간 표시
- **채팅 팝업** — 채팅창을 드래그 가능한 분리형 창으로 팝업

> 프로토타입의 비속어는 무해한 **데모 토큰**이며, 실서비스에서는 전역·스트리머별 사전으로 교체합니다.

---
🤖 Generated with [Claude Code](https://claude.com/claude-code)
