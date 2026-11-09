# DHost

여러 서버에 안전하게 SSH로 접속하고 작업하는 macOS용 앱입니다.
이 저장소에는 **설치 파일만** 있습니다.

**[최신 버전 내려받기 →](https://github.com/dongh94/DHost-releases/releases/latest)**

## 지원 환경
- macOS 12 Monterey 이상
- Apple Silicon (M1 이상) Mac

## 설치
1. [최신 Release](https://github.com/dongh94/DHost-releases/releases/latest)에서 `DHost_<버전>_aarch64.dmg`를 내려받습니다.
2. `.dmg`를 열고 **DHost**를 **응용 프로그램** 폴더로 끌어 놓습니다.
3. 처음 열 때 **"손상되었기 때문에 열 수 없습니다"**가 나오면, 휴지통으로 옮기지 말고 **취소**를 누른 뒤 터미널에서 한 번 실행합니다.
   ```bash
   xattr -dr com.apple.quarantine /Applications/DHost.app
   ```
   파일이 망가진 것이 아니라, Apple 인증서로 서명하지 않은 앱에 macOS가 띄우는 경고입니다. 이 Release에서 받은 DHost에만 쓰세요.
4. 다시 DHost를 엽니다.

> 파일이 온전한지 확인하려면 같은 Release의 `SHA256SUMS.txt`와 비교하세요: `shasum -a 256 ~/Downloads/DHost_*_aarch64.dmg`

## 라이선스 등록
DHost는 관리자가 발급한 라이선스가 있어야 서버에 접속할 수 있습니다.
1. 관리자에게 라이선스 파일(`이름.dhost-license`)을 받습니다.
2. **설정 → 라이선스 → 라이선스 파일 등록**에서 파일을 고릅니다. 메신저로 내용을 받았다면 옆의 붙여넣기 버튼을 씁니다.
3. 만료 14일 전부터 상태 표시줄에 **라이선스 D-n**이 보입니다. 새 라이선스를 받아 같은 방법으로 등록하세요.

라이선스가 없거나 만료되면 새 접속만 막히고, 서버 목록·설정·백업 내보내기·앱 업데이트는 그대로 쓸 수 있습니다.

## 업데이트
새 버전이 나오면 앱 아래쪽 상태 표시줄에 **새 버전 업데이트** 버튼이 나타납니다. 누르면 서명을 확인한 뒤 설치하고 다시 시작합니다. 서버 목록·설정·저장한 비밀번호는 그대로 남습니다.

## 지우기
1. 응용 프로그램 폴더에서 DHost를 휴지통으로 옮깁니다.
2. 데이터까지 지우려면 `~/Library/Application Support/io.github.dongh94.dhost/` 폴더를 지웁니다. 저장한 비밀번호는 키체인 접근 앱에서 `io.github.dongh94.dhost` 항목을 지웁니다.

## 문의
설치·라이선스 문의는 관리자에게 연락하세요.
