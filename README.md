# wim-mail-protocol

대표(william@wimcorp.co.kr) 받은편지함을 매일 아침 한 번 훑어서, **중요한 것만 남기고 브리핑**하고, 정해진 유형에는 **회신 초안을 만들거나 자동 발송**하는 규칙 저장소.

- 규칙 정본: [`PROTOCOL.md`](PROTOCOL.md) — 남길 것 5유형, 거를 것, 회신 3단계, 브리핑 형식
- 회신 템플릿: [`templates/replies.md`](templates/replies.md)
- 실행 프롬프트: [`ROUTINE_PROMPT.md`](ROUTINE_PROMPT.md) — claude.ai 클라우드 루틴이 매일 08:00 KST에 실행

## 동작

1. 클라우드 루틴이 이 저장소를 받아 `PROTOCOL.md`를 읽는다
2. Gmail 커넥터로 최근 26시간 수신 메일을 조회한다
3. KEEP 5유형만 남기고 나머지는 건수만 센다
4. Tier 1은 초안(기본) 또는 자동 발송(`send_mode: auto`), Tier 2는 초안, Tier 3은 회신 안 함
5. 브리핑 메일을 대표 본인에게 보낸다 (제목 `[메일 브리핑] YYYY-MM-DD`)
6. 처리한 스레드에 `Claude/…` 라벨을 붙여 다음 날 중복 처리를 막는다

## 규칙 바꾸기

`PROTOCOL.md`를 고치고 커밋한다. 다음 실행부터 반영된다. 루틴 자체(시간·모델)는 https://claude.ai/code/routines 에서 바꾼다.

## 주의

- 웹훅 URL·토큰 같은 비밀은 이 저장소에 넣지 않는다 (루틴 프롬프트에만 둔다)
- 브리핑에는 임원 민감 정보가 섞일 수 있으므로 수신자는 대표 본인뿐이다
