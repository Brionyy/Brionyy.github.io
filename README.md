# Dongui Lee · CV 사이트

명함 QR에 연결할 개인 CV 사이트입니다. 서버 없이 파일만으로 돌아가는 정적 사이트이며, GitHub Pages에 무료로 올릴 수 있습니다.

## 폴더 구성

| 파일 | 역할 |
|---|---|
| `index.html` | 사이트 본문. 내용을 고칠 때는 이 파일만 수정하면 됩니다. |
| `assets/favicon.svg` | 브라우저 탭 아이콘 (DL 모노그램) |
| `.nojekyll` | GitHub Pages가 파일을 변환하지 않고 그대로 올리게 하는 빈 파일. 지우지 마세요. |
| `README.md` | 이 안내서. 사이트에는 보이지 않습니다. |

## 1. 게시 전 확인할 항목 (TBC)

사이트에서 주황색 `TBC` 표시가 붙은 곳입니다. `index.html`에서 `TBC`로 검색하면 모두 찾을 수 있습니다. 내용을 확정한 뒤 `<span class="tbc" ...>...</span>` 부분을 통째로 지우면 표시가 사라집니다.

| 위치 | 확인할 내용 |
|---|---|
| Education · 석사 논문 | 제목의 "Use on"이 맞는지, "Use of"인지 |
| Education · 학사 | 학위 종류 (예: Bachelor of Science / Bachelor of Arts) |
| Experience · 펠로우십 | 공식 직함이 "Program Coordinator"가 맞는지 |
| Experience · 교수님 RA | 시작 시기 ("Fall 2026" 대신 정확한 연월) |
| Experience · KOFIH 연구 | 과제의 공식 영문명 |
| Publications | 저자 순서 |

## 2. GitHub Pages에 올리기

GitHub 공식 안내(docs.github.com/en/pages/quickstart)를 따른 절차입니다.

1. github.com에서 계정을 만들고 로그인합니다. 사용자 이름이 곧 주소가 되니 신중히 정하세요. 예를 들어 사용자 이름이 `donguilee`이면 주소는 `https://donguilee.github.io`가 됩니다.
2. 오른쪽 위 **+** 메뉴 → **New repository**를 누릅니다.
3. Repository name에 `사용자이름.github.io`를 정확히 입력합니다. 예: `donguilee.github.io`.
4. **Public**을 선택합니다. 무료 계정은 공개 저장소에서만 Pages를 쓸 수 있습니다.
5. **Create repository**를 누릅니다.
6. 저장소 화면에서 **uploading an existing file** 링크(또는 **Add file → Upload files**)를 누르고, 이 폴더의 파일을 끌어다 놓습니다. `index.html`, `assets` 폴더, `.nojekyll`이 저장소 맨 위에 있어야 합니다. 맥 Finder에서는 `.nojekyll`이 숨김 파일이라 보이지 않을 수 있습니다. 이때는 Finder에서 `Cmd + Shift + .`을 눌러 숨김 파일을 표시하세요.
7. 아래 **Commit changes**를 누릅니다.
8. **Settings → Pages**로 가서 **Source**가 **Deploy from a branch**, **Branch**가 `main` / `/(root)`인지 확인하고 **Save**를 누릅니다.
9. 몇 분 기다린 뒤 `https://사용자이름.github.io`에 접속합니다. 반영에는 최대 10분 정도 걸릴 수 있습니다.

## 3. 명함 QR 만들기

사이트가 열리는 것을 확인한 뒤, 그 주소로 QR 코드를 만드세요. 이 주소는 저장소 이름을 바꾸지 않는 한 그대로 유지되므로 명함을 다시 찍을 필요가 없습니다.

QR 생성 사이트 중에는 중간에 자기 주소를 거치게 하거나(동적 QR), 일정 기간 뒤 유료로 전환되는 곳이 있습니다. 반드시 사이트 주소가 그대로 들어가는 **정적 QR**로 만드세요. 만든 QR은 휴대폰 카메라로 찍어서 주소가 `https://사용자이름.github.io`로 바로 뜨는지 확인한 뒤 인쇄소에 넘기세요.

## 4. 나중에 내용 고치기

1. 저장소에서 `index.html`을 누르고 연필 아이콘(**Edit this file**)을 누릅니다.
2. 고친 뒤 **Commit changes**를 누르면 몇 분 안에 사이트에 반영됩니다.
3. 맨 아래 `Last updated October 2026`도 함께 고쳐 주세요.

새 논문이나 경력을 추가할 때는 같은 구역의 `<li class="entry"> ... </li>` 한 덩어리를 복사해서 바로 위에 붙이고 내용만 바꾸면 됩니다. Claude에게 수정한 `index.html`을 받아서 다시 업로드해도 됩니다.

## 5. 사진 넣기 (선택)

1. 세로 4:5 비율 사진을 `portrait.jpg`라는 이름으로 `assets` 폴더에 올립니다.
2. `index.html`에서 `<div class="mono" aria-hidden="true"><div>DL</div></div>`를 찾아 아래처럼 바꿉니다.

```html
<div class="mono"><div><img src="assets/portrait.jpg" alt="Dongui Lee"></div></div>
```

## 참고

- 휴대폰이 다크 모드이면 사이트도 자동으로 어두운 배색으로 바뀝니다.
- 서울대 공식 로고·시그니처는 넣지 않았습니다. 개인 페이지에 학교 로고를 쓰면 학교 공식 페이지처럼 보일 수 있어서입니다. 넣고 싶으시면 서울대 UI 규정(identity.snu.ac.kr)을 확인한 뒤 추가하세요.
- 전화번호, 주소, 생년월일, 만료된 어학 점수는 공개 CV에 넣지 않았습니다.
