# 🐙 GitHub 저장소 링크 미리보기(썸네일) 설정 가이드

> **목표:** 카카오톡/페이스북/슬랙 등에 `https://github.com/qkrgudwhd/blog-steel/`
> 주소를 붙여넣었을 때, 위에 만든 골드 + 스테인레스 썸네일이 자동으로 펼쳐지게 만드는 방법.
>
> **소요 시간:** 약 2분

---

## 📌 작동 원리 (간단 설명)

GitHub 저장소 페이지(`github.com/...`)는 SNS에 공유될 때 두 가지 방법으로 미리보기 그림을 표시합니다:

1. **README.md 첫 부분의 이미지** — 자동으로 사용됨 (이미 적용 완료 ✅)
2. **저장소 Settings 의 "Social Preview" 이미지** — 더 깔끔하게 강제 지정 (아래 단계로 진행)

두 가지 모두 적용하면 어떤 채널에서도 안정적으로 썸네일이 표시됩니다.

---

## ✅ 1단계 — 파일을 GitHub에 푸시 (1분)

다음 4개 파일이 `blog-steel` 저장소에 업로드되어야 합니다:

| 파일 | 위치 | 역할 |
| :--- | :--- | :--- |
| `index.html` | 저장소 루트 | OG 메타 태그 포함된 메인 페이지 |
| `README.md` | 저장소 루트 | GitHub 페이지 첫 화면 + 자동 썸네일 |
| `assets/og-image.png` | assets 폴더 | 1200×630 — 카카오톡 링크 미리보기용 |
| `assets/github-social.png` | assets 폴더 | 1280×640 — GitHub Social Preview용 |
| `assets/kakao-thumbnail.png` | assets 폴더 | 640×640 — 정사각형 (선택) |

**업로드 방법** (GitHub 웹사이트에서 직접):
1. https://github.com/qkrgudwhd/blog-steel 접속
2. 파일 영역에서 **[Add file]** → **[Upload files]** 클릭
3. 위 파일들을 드래그&드롭 (assets 폴더는 빈 폴더가 아닌 파일이 들어있는 폴더로 끌어다 놓으면 자동으로 폴더가 생성됨)
4. 하단에 `Add og image and readme` 같은 메시지 입력 후 **[Commit changes]** 클릭

---

## 🖼 2단계 — Social Preview 이미지 등록 (1분, 가장 중요)

저장소 페이지에서:

1. 우측 상단 **[⚙ Settings]** 탭 클릭
2. 좌측 메뉴 맨 위 **[General]** (이미 선택되어 있음)
3. 화면을 아래로 스크롤하면 **"Social preview"** 섹션이 있습니다
4. **[Edit]** 또는 **[Upload an image...]** 버튼 클릭
5. `assets/github-social.png` 파일 선택 (1280×640)
6. 저장 → 완료!

> 📌 **권장 사이즈:** 1280×640 픽셀 (이미 그 사이즈로 만들어 두었습니다 ✅)

---

## 🧪 3단계 — 카카오톡에서 테스트

1. 카카오톡 아무 채팅방을 열기 (혼자만 있는 "나에게 보내기" 추천)
2. 다음 두 주소를 각각 붙여넣어 보세요:

   **① GitHub 저장소 주소:**
   ```
   https://github.com/qkrgudwhd/blog-steel/
   ```

   **② 라이브 사이트 주소:**
   ```
   https://qkrgudwhd.github.io/blog-steel/
   ```

3. 두 가지 모두 **큰 그림 미리보기**가 펼쳐져야 정상 ✅

---

## ⚠️ 미리보기가 안 뜬다면?

### 🔄 카카오톡 미리보기 캐시 강제 갱신

카카오톡은 한 번 본 링크의 미리보기를 **약 1주일 동안 캐시**합니다. 옛 화면이 그대로 뜨면:

- 주소 끝에 `?v=2` 처럼 임의 값을 붙여서 보내세요:
  ```
  https://qkrgudwhd.github.io/blog-steel/?v=2
  https://github.com/qkrgudwhd/blog-steel/?v=2
  ```
- `v=2`, `v=3`, `v=hello` 등 매번 다른 값으로 바꾸면 강제 새로고침됩니다.

### 🔍 OG 이미지 확인 도구 (선택)

페이스북 공식 디버거로 OG 메타 태그가 정상 인식되는지 확인:
- https://developers.facebook.com/tools/debug/
- 위 주소에 `https://qkrgudwhd.github.io/blog-steel/` 입력 → **[Debug]** 클릭

이 도구로 **Scrape Again** 을 한 번 누르면 페이스북 캐시도 초기화되어 카카오톡까지 빠르게 반영됩니다.

---

## 📞 추가 도움이 필요하시면

설정 중 막히는 부분이 있으면 카카오톡 오픈채팅으로 문의해 주세요.
🔗 https://open.kakao.com/o/gwcemGqi

📞 010-4554-9110 (평일 09~18시)
