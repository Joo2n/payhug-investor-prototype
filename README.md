# PayHug 투자자 어드민 — 시연용 프로토타입

투자자용 어드민 화면 설계(안)를 조작 가능한 형태로 보여 주는 시연 전용 배포본. 사이드바 메뉴 7종·화면 13개·상태 18개를 `index.html` 한 파일에서 전환하며, 엑셀 4종·투자자산 증명서 PDF·재양도합의서 묶음은 실물 파일이 그대로 내려온다. 표기 금액·요율·상호는 전부 예시이고 요율·산식은 미확정 사안이다. 이 저장소에는 프로토타입과 화면이 실제로 부르는 자산만 있다.

- 투자자 공유 정리(이 배포본에만): 탭 제목은 「PayHug 투자자 어드민」이고, 투자 자산 요약 카드 아래 「비중 … · 보관 ㈜…」 줄, 투자 자산 현황 표의 「비중」「보관」 두 열, 「투자자산 현황」 엑셀의 같은 두 열이 없다. 통합본(`app.html`)에는 그대로 있다. 변환은 `scripts/sync_prototype.py` `investor_share()` · 엑셀은 `patch_assets_status_xlsx()`.
- 배포: https://payhug-investor-prototype.vercel.app/
- 딥링크: `#<화면>/<상태>` — 예 `#invest-assets/cert-confirm`, `#acquisition-list/signing`

`index.html`은 직접 고치지 않는다. 원본은 `Joo2n/payhug-investor-admin`의 `app.html`이고, 그 저장소의 GitHub Actions(`sync-prototype.yml`)가 `scripts/sync_prototype.py`로 변환해 이 저장소에 반영한다. 여기서 고친 내용은 다음 동기화에서 사라진다.

## 갱신

| 날짜 | 내용 |
|---|---|
| 2026-09-09 | 투자자 공유 정리 — 탭 제목 · 카드 아래 비중·보관 줄 · 현황 표 비중·보관 열 · 엑셀 같은 두 열 제거 (원본 app.html `d7ce377` 기준, 통합본 무변경) |
