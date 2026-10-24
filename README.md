# 아카라이브 스포일러 가림 해제

유니콘 Pro 사용자 필터입니다. `arca.live` 본문의 흐림·흑백 효과를 제거하며, 스포일러 경고 배너의 유지 여부에 따라 두 버전 중 하나를 선택할 수 있습니다.

## 구독 URL

유니콘 Pro의 사용자 필터 추가 화면에 원하는 버전의 주소를 입력하세요.

**배너와 본문 가림 모두 제거 — 기존 버전**

```text
https://raw.githubusercontent.com/parking-place/unicorn-pro-archive-spoiler-filter/main/arcalive-no-spoiler.txt
```

**배너 유지, 본문 가림만 제거 — 추가 버전**

```text
https://raw.githubusercontent.com/parking-place/unicorn-pro-archive-spoiler-filter/main/arcalive-no-blur.txt
```

**두 필터 중 하나만 활성화하세요.** 배너 유지 버전으로 바꿀 때는 기존 `arcalive-no-spoiler.txt` 필터를 꺼야 합니다. 두 버전을 함께 켜면 기존 필터가 배너를 계속 숨깁니다.

## 갤럭시 / Chrome 설정

1. 유니콘 Pro의 필터 관리에서 사용자 필터 추가를 엽니다.
2. 위 Raw URL을 입력하고 추가한 필터를 활성화합니다.
3. 유니콘 Pro의 인증서 설치를 완료하고, 앱 관리에서 Chrome의 네트워크 필터링·HTTPS 필터링·광고 차단을 켭니다. DNS 보호만으로는 이 필터가 적용되지 않습니다.
4. 아카라이브가 화이트리스트에 있으면 해제한 뒤, 열려 있던 게시글을 새로고침합니다.

메뉴 이름은 앱 버전에 따라 다를 수 있습니다. 원래 표시로 되돌리려면 이 사용자 필터를 끄고 새로고침하세요.

## 확인한 내용

- 2026-10-24에 아카라이브의 실제 HTML, CSS, JavaScript를 확인했습니다.
- Chromium에서 해당 HTML/CSS를 사용해 390px 및 1280px 너비로 검증했습니다. 필터 적용 후 경고 배너는 숨겨지고 본문 `filter`는 `none`이 되며, 본문 높이는 유지됩니다.
- 배너 유지 버전은 기존의 본문 스타일 규칙을 그대로 사용하고, 배너를 숨기는 규칙만 제외했습니다.
- 실제 갤럭시 기기의 유니콘 Pro 앱 내 동작은 아직 검증하지 않았습니다.
- 사이트가 HTML 클래스나 CSS를 변경하면 규칙 수정이 필요할 수 있습니다.

## 참고

- [아카라이브 CSS](https://arca.live/static/assets/dist/common.css)
- [유니콘 공식 답변: 지원하는 스타일 규칙](https://support.getunicorn.app/hc/ko/community/posts/28994016818585)
- [유니콘 공식 안내: 브라우저별 필터링 설정](https://support.getunicorn.app/hc/ko/articles/39543101145625)
