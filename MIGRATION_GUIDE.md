# HIDY STUDIO 단일 저장소 이전 가이드

## 중요한 원칙

**HidyGames와 MOYJI 저장소를 먼저 삭제하지 마세요.**

현재 두 저장소의 GitHub Pages 서비스가 활성화되어 있다면, 사용자 사이트의 같은 경로와 충돌하거나 종전 콘텐츠가 계속 표시될 수 있습니다. 먼저 새 파일을 올린 후 기존 저장소의 GitHub Pages만 비활성화하고 모든 URL을 검증하세요.

이전 후 사이트 URL은 기존과 동일하게 유지됩니다.

| 페이지 | 주소 |
|---|---|
| 메인 | https://hidystudio.github.io/ |
| 게임 | https://hidystudio.github.io/HidyGames/ |
| 가챠 | https://hidystudio.github.io/HidyGames/gacha.html |
| GRAVTILE | https://hidystudio.github.io/HidyGames/gravtile.html |
| GRAVTILE 개인정보처리방침 | https://hidystudio.github.io/HidyGames/gravtile-privacy.html |
| MOYJI | https://hidystudio.github.io/MOYJI/ |
| Memth | https://hidystudio.github.io/MOYJI/memth.html |

## 1단계 — 업로드

1. `https://github.com/HIDYSTUDIO/hidystudio.github.io` 저장소를 열어 주세요.
2. 이 ZIP을 **압축 해제**한 뒤, `index.html`, `HidyGames`, `MOYJI`, `README.md`, `.nojekyll`, `404.html`을 저장소 최상위에 업로드하세요. `.nojekyll`은 숨김 파일이므로 함께 업로드되는지 확인하세요.
3. 기존 `index.html` 또는 `README.md`가 있다면 ZIP 안에 있는 것으로 **교체**하세요. 기존 파일을 지우지 않고 `index(1).html` 형태로 업로드하면 안 됩니다.
4. GitHub Pages 설정은 `Settings → Pages → Deploy from a branch → main → /(root)`를 유지합니다.
5. 대량 파일 업로드가 불편하면 PC에서 GitHub Desktop 또는 `git`으로 동기화하세요. GitHub 웹 인터페이스에서 폴더 드래그 업로드를 지원하는 경우 전체 폴더를 올릴 수 있습니다.

## 2단계 — 기존 Pages 게시 중단

1. `HIDYSTUDIO/HidyGames` 저장소의 `Settings → Pages`에서 기존 Pages 게시를 비활성화하세요.
2. `HIDYSTUDIO/MOYJI` 저장소도 똑같이 처리하세요.
3. 이 단계에서 **저장소 자체는 아직 삭제하지 마세요.**

## 3단계 — 검증

1. 브라우저 강력 새로고침(Ctrl+F5) 또는 시크릿 창으로 위 URL 7개를 각각 열어 주세요.
2. 메인에서 두 카드가 Games/MOYJI로 이동하는지 확인하세요.
3. Games에서 GRAVTILE / Gacha 이미지, 상세 페이지, 개인정보처리방침 링크를 확인하세요.
4. MOYJI에서 Memth 상세 페이지 이미지 4개가 표시되는지 확인하세요.
5. Games/MOYJI에서 `HIDY STUDIO ↗` 또는 `STUDIO ↗` 버튼으로 메인으로 돌아오는지 확인하세요.
6. PC와 모바일에서 메뉴가 겹치거나 깨지는지 점검하세요.
7. Play Store 또는 기타 서비스에 등록된 개인정보처리방침 링크가 유지되는지 확인하세요.

## 4단계 — 삭제 (선택)

모든 테스트가 통과한 후에만 옛 `HidyGames` 및 `MOYJI` 저장소를 삭제하세요.

- `Settings → General → Danger Zone → Delete this repository`
- GitHub 삭제는 이력, 이슈, 설정 등의 손실 위험이 있으니 원본 ZIP과 필요하다면 git 전체 백업을 보관하세요.
- 지금 구조에서는 **기존 웹 URL은 같지만** `github.com/HIDYSTUDIO/HidyGames` 또는 `github.com/HIDYSTUDIO/MOYJI`로 연결되던 **GitHub 저장소 링크**는 삭제 후 사용할 수 없습니다. 통합본 HTML은 기존 HidyGames 링크를 통합 저장소로 수정했습니다.

## 기타

- 통합본의 `HidyGames/404.html`은 원본을 보존한 것으로, GitHub Pages는 사이트 수준 `404.html`을 사용할 수 있습니다.
- `.nojekyll`은 GitHub Pages가 파일을 가공하지 않고 정적으로 배포하도록 돕습니다.
