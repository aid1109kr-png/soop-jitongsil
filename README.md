# 🖥️ SOOP 4인 지통실

한아련 · 목츄리 · 싱유 · 이투의 방송을 한 화면에서 볼 수 있는 **4인 지통실 웹사이트**입니다.

검은색 지통실 스타일의 2×2 화면으로 구성되어 있으며, 각 방송 화면을 누르면 해당 SOOP 방송으로 이동합니다.

---

# 🚀 가장 쉬운 GitHub 배포 방법

## 1. GitHub 회원가입 / 로그인

아래 사이트에 접속합니다.

https://github.com/

계정이 없다면 **Sign up**, 있다면 **Sign in**을 누릅니다.

---

## 2. 새 저장소 만들기

GitHub에 로그인한 뒤 오른쪽 위의 **+** 버튼 → **New repository**를 누릅니다.

다음처럼 입력합니다.

- Repository name: `soop-jitongsil`
- Description: `SOOP 4인 지통실`
- Public 선택
- 나머지는 기본값 그대로

그리고 **Create repository**를 누릅니다.

> ⚠️ `Add a README file`은 체크하지 않아도 됩니다.
> 이 ZIP 안에 이미 README가 들어 있습니다.

---

## 3. 파일 올리기

새로 만든 저장소 화면에서

**Add file → Upload files**

를 누릅니다.

이 ZIP 파일을 먼저 압축 해제한 뒤, 안에 있는 **파일과 폴더 전체**를 업로드합니다.

업로드해야 하는 구조는 정확히 다음과 같습니다.

```text
soop-jitongsil/
├── index.html
├── 404.html
├── .nojekyll
├── README.md
└── .github/
    └── workflows/
        └── pages.yml
```

### ⚠️ 중요한 점

`index.html`이 저장소의 가장 바깥쪽에 있어야 합니다.

잘못된 예:

```text
soop-jitongsil/
└── soop-jitongsil-site/
    └── index.html
```

올바른 예:

```text
soop-jitongsil/
├── index.html
└── .github/
```

---

## 4. 저장하기

파일을 올린 뒤 아래쪽의

**Commit changes**

버튼을 누릅니다.

메시지는 기본값 그대로 둬도 됩니다.

---

# 🌐 5. 웹사이트 배포

파일을 올리면 GitHub Actions가 자동으로 사이트를 배포합니다.

저장소에서:

**Settings → Pages**

로 들어갑니다.

`Build and deployment` 부분에서 GitHub Actions를 사용하도록 설정합니다.

이 프로젝트에는 이미 다음 파일이 들어 있습니다.

```text
.github/workflows/pages.yml
```

따라서 `main` 브랜치에 변경사항이 올라가면 자동으로 배포됩니다.

---

# 🔗 6. 내 사이트 주소 확인

배포가 끝나면 보통 다음 형태의 주소가 만들어집니다.

```text
https://내GitHub아이디.github.io/soop-jitongsil/
```

예를 들어 GitHub 아이디가 `abc123`이라면:

```text
https://abc123.github.io/soop-jitongsil/
```

GitHub 저장소의

**Settings → Pages**

에서도 실제 주소를 확인할 수 있습니다.

---

# 🔴 지통실에 등록된 방송

현재 4명은 다음과 같이 연결되어 있습니다.

| 이름 | SOOP ID |
|---|---|
| 싱유 | `singu64` |
| 목츄리 | `xex3` |
| 이투 | `etwo22` |
| 한아련 | `rkdmsdl782` |

방송 화면을 클릭하면 각각의 SOOP 방송 페이지로 이동합니다.

---

# 🔄 방송 정보를 수정하고 싶을 때

`index.html`을 열면 아래 부분에 방송 정보가 있습니다.

```javascript
const streams=[
 {name:"싱유",id:"singu64",url:"방송주소",embed:"임베드주소"},
 {name:"목츄리",id:"xex3",url:"방송주소",embed:"임베드주소"},
 {name:"이투",id:"etwo22",url:"방송주소",embed:"임베드주소"},
 {name:"한아련",id:"rkdmsdl782",url:"방송주소",embed:"임베드주소"}
];
```

여기서 이름이나 방송 주소를 변경할 수 있습니다.

---

# 🛠️ 방송 화면이 검게 나오는 경우

SOOP에서 외부 사이트의 방송 임베드를 제한하는 경우가 있습니다.

이 경우에도 **방송 입장 버튼/화면 클릭으로 해당 SOOP 방송 페이지에 들어가는 기능은 사용할 수 있습니다.**

즉, 웹사이트 자체가 고장난 것이 아니라 SOOP의 외부 임베드 정책 때문일 수 있습니다.

---

# 📱 휴대폰에서도 사용 가능

반응형으로 만들어져 있기 때문에 휴대폰으로 접속하면

```text
[ 방송 1 ]
[ 방송 2 ]
[ 방송 3 ]
[ 방송 4 ]
```

형태로 자동 변경됩니다.

PC에서는

```text
[ 방송 1 ][ 방송 2 ]
[ 방송 3 ][ 방송 4 ]
```

형태로 표시됩니다.

---

# ✨ 다음에 추가할 수 있는 기능

원하면 이후에 다음 기능도 추가할 수 있습니다.

- 실제 방송 제목 표시
- 실제 시청자 수 표시
- 방송 중 / OFF 상태 자동 표시
- 방송 시작 알림
- 즐겨찾기
- 닉네임 검색
- 방송 순서 변경
- 다크/라이트 모드
- 모바일 전용 UI
- 관리자 페이지
- BJ 추가/삭제 기능
- 여러 명의 방송을 한 화면에 추가
- 내 도메인 연결

---

## 📌 핵심

**GitHub에 `index.html`이 가장 바깥에 있도록 업로드 → Settings → Pages → 배포 확인**

이것만 기억하면 됩니다.

무료 GitHub Pages로 운영할 수 있으며, 별도의 서버 프로그램이나 데이터베이스는 필요하지 않습니다.
