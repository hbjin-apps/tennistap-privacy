# TennisTap 개인정보처리방침 사이트

`index.html` 하나로 이루어진 정적 페이지입니다. 외부 리소스(폰트·스크립트·이미지)를 전혀
불러오지 않으므로 파일만 있으면 어디서든 그대로 열립니다.

**공개 URL**: https://hbjin-apps.github.io/tennistap-privacy/

## 구조

- 7개 언어(en, ko, ja, zh-Hans, es, fr, de) 섹션이 **모두 HTML에 그대로 들어 있습니다.**
- 인라인 스크립트는 브라우저 언어에 맞는 섹션만 남기는 *향상* 기능일 뿐입니다.
  스크립트가 실행되지 않아도 7개 언어 전문이 그대로 노출됩니다 — 심사자 환경에서
  빈 페이지가 뜨는 사고를 막기 위한 의도적인 설계이므로, 섹션을 `display:none`으로
  숨기는 방식으로 바꾸지 마세요.
- `#ko`, `#ja` 처럼 언어 코드를 해시로 붙이면 해당 언어로 바로 열립니다.

## 내용을 수정할 때

1. `index.html`에서 **7개 언어 섹션을 모두** 수정합니다.
2. 각 섹션의 `Last updated / 최종 수정일` 날짜를 갱신합니다.
3. 커밋 후 push 하면 1~2분 내에 GitHub Pages에 반영됩니다.

```bash
git add index.html && git commit -m "Update privacy policy" && git push
```

## 최초 배포 (1회)

이 디렉터리는 SVN 작업본 안에 있으면서 동시에 독립된 git 리포입니다.

1. GitHub에서 `hbjin-apps/tennistap-privacy` **public** 리포를 생성합니다
   (README·.gitignore·라이선스 체크박스는 모두 해제).
2. ```bash
   git remote add origin https://github.com/hbjin-apps/tennistap-privacy.git
   git push -u origin main
   ```
3. 리포 **Settings → Pages** → Source `Deploy from a branch`, Branch `main` / `/ (root)` → Save.
4. 1~2분 뒤 **시크릿 창**에서 공개 URL이 로그인 없이 열리는지 확인합니다.

## URL을 바꾸게 되면

같은 URL이 세 곳에 박혀 있습니다. 도메인을 옮기면 전부 갱신해야 합니다.

| 위치 | 경로 |
| --- | --- |
| 앱 내 문자열 (iOS) | `iOS/TennisTap Watch App/Views/PrivacyView.swift` |
| 앱 내 문자열 (Android) | `aOS/app/src/main/res/values/strings.xml` 의 `privacy_url` |
| 스토어 콘솔 | App Store Connect · Google Play Console (`docs/store-privacy-checklist.md` 참고) |
