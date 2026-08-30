# 회신 템플릿 (templates/replies.md)

`{이름}` `{직함}` `{기관}` `{제목}` 은 원문에서 확인된 값만 채운다. 확인 안 되면 "담당자님"으로 쓴다.
줄표, 이모지, 느낌표 금지. 마침표·쉼표·콜론만 쓴다.

## T1-확인 (자료·일정 안내 수신 확인)

```
{이름} {직함}님, 안녕하세요.
주식회사 윔 전우진입니다.

보내주신 "{제목}" 내용 잘 받았습니다. 확인했습니다.
추가로 필요한 사항이 있으면 회신 부탁드립니다.

감사합니다.
주식회사 윔 대표 전우진 드림
```

## T1-견적접수 (인바운드 견적·문의 접수)

```
{이름} {직함}님, 안녕하세요.
주식회사 윔 전우진입니다.

"{제목}" 관련 문의 잘 받았습니다.
내용을 검토한 뒤 담당자가 2영업일 안에 연락드리겠습니다.
그 사이 필요한 사양이나 일정이 있으면 이 메일로 알려주시면 함께 검토하겠습니다.

감사합니다.
주식회사 윔 대표 전우진 드림
```
참조(CC): `quote_owner_cc` 값 1명만.

## T1-inquiry-en (영문 인바운드 문의)

```
Dear {Name},

Thank you for reaching out regarding "{subject}".
We have received your inquiry and our team will get back to you within two business days.
If there are specific requirements or timelines we should be aware of, please reply to this email.

Best regards,
Woojin Jun
CEO, WIM Inc.
```

## T2 초안 작성 지침 (Tier 2는 템플릿이 아니라 지침)

- 첫 줄: 상대 이름과 인사. 둘째 줄: 무엇에 대한 답인지 한 문장.
- 상대가 물은 것에만 답한다. 모르는 사실은 `[대표 확인: ...]` 로 괄호 표시하고 빈칸으로 둔다.
- 일정 제안이 온 경우: 상대 제안을 그대로 되짚고 `[대표 확인: 가능 여부]` 표시. 대신 정하지 않는다.
- 금액·조건은 절대 쓰지 않는다. `[대표 확인: 금액]` 으로 둔다.
- 마지막 줄 서명 동일.
