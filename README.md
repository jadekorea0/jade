# 🍶 심리학부 주점 POS

고려대 심리학부 주점 카운터용 포스기. 프레임워크 없는 단일 `index.html` 파일이라 GitHub Pages에 그대로 올리면 바로 실행됩니다.

**데모(배포 후 주소)**: `https://jadekorea0.github.io/jade/index.html`

## 기능
- 1~20번 테이블 4열 배치, 테이블별 주문/합산
- 총 매출 · 쿠폰 할인 · 순수익 실시간 대시보드
- 할인쿠폰(1,000원), 체류시간 타이머
- 리셋(주문취소) / 자리치움 버튼
- 엑셀(.xlsx) 내보내기
- 데이터는 브라우저(localStorage) 자동 저장

## 메뉴 / 가격
냉면 8,000 · 닭강정 10,000 · 육회(소) 16,000 · 육회(중) 24,000 · 음료수 2,000 · 짜계치 8,000 · 콘치즈 6,000

---

## GitHub Pages 배포 방법

### 방법 A — 웹사이트에서 (터미널 불필요, 추천)
1. GitHub 로그인 → 오른쪽 위 **＋** → **New repository**.
2. 저장소 이름에 `jade` 입력 → **Public** 선택 → **Create repository**.
3. 생성된 페이지에서 **uploading an existing file** 클릭.
4. `POS.html`(과 원하면 `README.md`)을 드래그해서 올리고 **Commit changes**.
5. 상단 **Settings → Pages** 이동.
6. **Build and deployment → Source**를 **Deploy from a branch**로, Branch를 **main / (root)**로 두고 **Save**.
7. 1~2분 후 `https://jadekorea0.github.io/jade/index.html` 주소로 접속.

### 방법 B — 터미널(git)에서
```bash
# 이 폴더에서 실행
git init
git add index.html README.md
git commit -m "주점 POS"
git branch -M main
git remote add origin https://github.com/jadekorea0/jade.git
git push -u origin main
```
이후 **Settings → Pages**에서 위 6~7번과 동일하게 설정.

---

## 참고
- 인터넷이 되는 환경이면 엑셀(.xlsx)로, 안 되면 자동으로 CSV로 저장됩니다.
- 데이터는 **접속한 그 브라우저에만** 저장됩니다. 카운터를 한 기기에서 운영하세요. 여러 기기 공유가 필요하면 별도 백엔드(Firebase 등)가 필요합니다.
