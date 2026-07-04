# classup-kiosk-barrier-free-releases

클래스업 배리어프리 윈도우 키오스크(`classup-kiosk-barrier-free-client`)의 **GitHub Release 자동업데이트 배포 저장소**입니다.

- 소스코드는 없습니다. **설치 파일 + `latest.yml`만 GitHub Releases로 배포**합니다. (소스: private repo `classup-kiosk-barrier-free-client`)
- electron-updater가 `UPDATE_URL` 설정(빌드 시 주입, `.../releases/latest/download`)으로 이 레포의 최신 릴리즈를 조회해 자동업데이트합니다.
- S3(`classup-kiosk-barrier-free-update` 버킷)에서 이 레포로 전환(2026-07). 전환 시점의 첫 릴리즈는 과도기 빌드로 **S3와 이 레포에 모두 배포**했습니다 — 기존 S3 채널로 설치돼 있던 PC가 이 전환 빌드로 자동업데이트되면, 그 이후부터는 앱 자체에 내장된 설정에 따라 이 레포(GitHub)를 보고 업데이트합니다.
