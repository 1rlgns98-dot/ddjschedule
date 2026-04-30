# 행동활성화 프로그램

정적 HTML로 만든 행동활성화 프로그램입니다. 별도 빌드 과정 없이 GitHub 저장소를 Vercel에 연결해서 배포할 수 있습니다.

## 파일 구성

- `behavioral-activation.html`: 실제 프로그램 화면
- `index.html`: 루트 접속 시 프로그램으로 이동하는 진입 파일
- `vercel.json`: Vercel에서 `/` 접속을 프로그램 파일로 연결하는 설정

## GitHub에 올리기

이 PC에서 `git` 명령이 아직 잡히지 않는다면 먼저 Git for Windows를 설치하고 PowerShell을 새로 열어 주세요.

```powershell
git init
git add .
git commit -m "Deploy behavioral activation program"
git branch -M main
git remote add origin https://github.com/내아이디/저장소이름.git
git push -u origin main
```

GitHub 웹사이트에서 새 저장소를 만든 뒤, 위 명령의 `내아이디/저장소이름`만 본인 저장소 주소로 바꾸면 됩니다.

## Vercel 배포

1. https://vercel.com 에 로그인합니다.
2. `Add New...` -> `Project`를 선택합니다.
3. GitHub 저장소를 Import합니다.
4. Framework Preset은 `Other` 또는 자동 감지 그대로 둡니다.
5. Build Command는 비워둡니다.
6. Output Directory도 비워둡니다.
7. Deploy를 누릅니다.

배포 후 Vercel이 제공하는 주소로 접속하면 행동활성화 프로그램이 열립니다.

## 업데이트 배포

파일을 수정한 뒤 아래처럼 다시 커밋하고 푸시하면 Vercel이 자동으로 재배포합니다.

```powershell
git add .
git commit -m "Update program"
git push
```
